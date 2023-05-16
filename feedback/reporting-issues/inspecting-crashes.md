# Inspecting Crashes

The [GNU Project Debugger \(gdb\)](https://www.gnu.org/software/gdb/) is a general purpose debugger, but we're mostly going to focus on getting useful information when an application crashes. To get started, open an application in gdb, for example AppCenter by running:

```bash
gdb io.elementary.appcenter
```

1. Now run this application by typing `run` and pressing enter.
2. If the application doesn't crash right away try reproducing the crash.
3. Get more information by typing `backtrace` and pressing enter.
4. Please share the lines after `(gdb) backtrace`, those should provide useful information.

For more information see the manpages by running: `man gdb`. Another tutorial: [Debugging with GDB](https://betterexplained.com/articles/debugging-with-gdb/)

## Investigating Spontaneous Crashes

Running the application under gdb slows down the application and is problematic to reproduce some crashes. In such cases, it is recommended to use the systemd-coredump service which will gather application information on crash.

Let's take our example above of AppCenter: if the application would have crashed without understanding what might have happened, the service would retain the backtrace which is then replayable with:

```bash
coredumpctl debug io.elementary.appcenter
```

If there are lines such as `0x00001234deadbeef in ?? ()` it means that we are missing some debugging symbols.

The debugging symbols of elementary OS are hidden by default (as they are taking some space). To be able to discover then, we need to add their corresponding debian source:

```bash
UPSTREAM_RELEASE=$(LSB_OS_RELEASE=/usr/lib/upstream-os-release lsb_release -cs)
echo "deb http://ddebs.ubuntu.com ${UPSTREAM_RELEASE} main restricted universe multiverse
deb http://ddebs.ubuntu.com ${UPSTREAM_RELEASE}-updates main restricted universe multiverse
deb http://ddebs.ubuntu.com ${UPSTREAM_RELEASE}-proposed main restricted universe multiverse" | \
sudo tee -a /etc/apt/sources.list.d/ddebs.list
echo "deb https://ppa.launchpadcontent.net/elementary-os/stable/ubuntu ${UPSTREAM_RELEASE} main/debug
deb https://ppa.launchpadcontent.net/elementary-os/os-patches/ubuntu ${UPSTREAM_RELEASE} main/debug" | \
sudo tee -a /etc/apt/sources.list.d/elementary-ddebs.list
sudo apt install ubuntu-dbgsym-keyring debian-goodies && sudo apt update
```

We can then install all the missing debugging symbols with:

```bash
find-dbgsym-packages --install $(which io.elementary.appcenter)
```

Rerunning `coredumpctl debug` should now show more useful traces.

For a flatpak application, we can use `flatpak-coredumpctl io.elementary.elementary.calculator` to see the latest traces of a crash inside flatpak.
