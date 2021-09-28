# Contributor Guide

elementary OS is developed as an Open Source project. Want to contribute code to elementary OS itself? Here are some tips.

{% hint style="info" %}
Looking for documentation on creating your own apps? See [Developer Documentation](https://docs.elementary.io/develop/) instead.
{% endhint %}

## Restoring Original Packages

You can audit your system for files that have been changed from their originally installed packages:

```bash
sudo apt install debsums
sudo debsums_init
```

View changed files:

```bash
sudo debsums -cs
```

View which packages those files belong to:

```bash
sudo debsums -c | xargs -rd '\n' -- dpkg -S | cut -d : -f 1 | sort -u
```

Assuming that you've used `--prefix=/usr` when installing custom version you can restore them using:

```bash
sudo apt install appname --reinstall
```

## WingPanel

When developing the Panel \(codenamed WingPanel\) or panel-related packages like the Applications Menu and indicators, you want to start WingPanel from the command line to view logs. WingPanel is automatically started and restarted by `gnome-session`. If wingpanel is stopped/killed twice within a minute, it will stop automatically restarting, and you can gather logs:

1. In Terminal run `killall io.elementary.wingpanel` twice to stop the current WingPanel
2. Start wingpanel with debug logging by running `G_MESSAGES_DEBUG=all io.elementary.wingpanel`

To restore normal behavior simply logout and back in again to restart your session.

## Gala

Gala is the window manager of elementary OS. If it crashes or freezes during development, it can be nonobvious how to recover. Here's how to do it:

1. Go to one of the virtual consoles by pressing: Ctrl+Alt+F1
2. Log in
3. If Gala didn't crash but froze, you can kill it by running `killall gala`
4. Restart Gala by running `DISPLAY=:0 gala --replace &`
5. Switch back to the graphical session by pressing Ctrl+Alt+F7

If Gala doesn't start, you can reinstall the latest stable version by running `sudo apt install --reinstall gala`.

## 

