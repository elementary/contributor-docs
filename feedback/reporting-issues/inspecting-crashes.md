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

