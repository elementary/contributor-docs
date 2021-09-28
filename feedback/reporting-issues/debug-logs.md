# Debug Logs

## Adding Logs

One way to debug applications is logging information in the code. This enables seeing what code was run and what the value of variables where.

Example:

```text
debug("Something happened");
```

Example with arguments:

```text
string name = "Bob";
int age = 30;
debug("Person: %s %i", name, age);
```

`debug` is a convenience function that calls [log](https://valadoc.org/glib-2.0/GLib.log.html) with the "debug" log level, there are other less used convenience functions like: `info`, `message`, `warning`, `critical`.

The first argument is the message which is formatted like `printf`. This means that it can include "format specifiers" which can be replaced by the remaining arguments you pass to the function. The `%s` for example can be replaced by a string, the `%i` by an integer. [More info](http://www.cplusplus.com/reference/cstdio/printf/).

## Retrieving Logs

By default debug messages are not shown. To see them you need to set the `G_MESSAGES_DEBUG` environment variable to the log domain you're interested in. [More info on environmental variables](https://www.digitalocean.com/community/tutorials/how-to-read-and-set-environmental-and-shell-variables-on-a-linux-vps) Usually you'll set it to `all` to log everything. [More info on Running and debugging GLib Applications](https://developer.gnome.org/glib/stable/glib-running.html).

Run your application with debugging enabled:

```bash
G_MESSAGES_DEBUG=all com.github.myteam.myapp
```

Run the elementary OS calendar app with debugging enabled:

```bash
G_MESSAGES_DEBUG=all io.elementary.calendar
```

[More information on message logging](https://developer.gnome.org/glib/stable/glib-Message-Logging.html#g-log).

{% hint style="info" %}
To view logs from all your applications you can use [`journalctl`](https://www.digitalocean.com/community/tutorials/how-to-use-journalctl-to-view-and-manipulate-systemd-logs)\`\`
{% endhint %}

