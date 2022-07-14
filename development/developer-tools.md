# Developer Tools

## elementary SDK

The fastest way to get a collection of common app dependencies and developer tools is to install `elementary-sdk` from Terminal:

```bash
sudo apt install elementary-sdk
```

## Build Dependencies

You can quickly install all known dependencies for a project with `build-dep`:

```bash
sudo apt build-dep <packagename>
```

{% hint style="info" %}
This installs the dependencies for the currently-released version, so it may miss dependencies for unreleased updates. In those cases, refer to the project's README.
{% endhint %}

## Vala Linting

To make it easier to follow the [elementary Code-Style guidelines](https://elementary.io/docs/code/reference#code-style) you can use [vala-lint](https://github.com/elementary/vala-lint).

## GTK Inspector

The GTK [Inspector](https://wiki.gnome.org/Projects/GTK+/Inspector) is similar to a web browser's inspector, but for GTK apps. Using the Inspector can greatly speed up development, and allows you view and to test out changing properties without recompiling an app. You can also test out temporary in-app CSS.

First, make sure you have `elementary-sdk` installed. Then enable the Inspector keybinding:

```bash
gsettings set org.gtk.Settings.Debug enable-inspector-keybinding true
```

Focus an app, then launch the Inspector by pressing Ctrl+Shift+I to inspect the widget beneath your cursor, or Ctrl+Shift+D to open the inspector without a widget selected.

You can also run it temporarily together with an app by running:

```bash
GTK_DEBUG=interactive <appname>
```

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

## Gala

Gala is the window manager of elementary OS. If it crashes or freezes during development, it can be nonobvious how to recover. Here's how to do it:

1. Go to one of the virtual consoles by pressing: Ctrl+Alt+F1
2. Log in
3. If Gala didn't crash but froze, you can kill it by running `killall gala`
4. Restart Gala by running `DISPLAY=:0 gala --replace &`
5. Switch back to the graphical session by pressing Ctrl+Alt+F7

If Gala doesn't start, you can reinstall the latest stable version by running `sudo apt install --reinstall gala`.
