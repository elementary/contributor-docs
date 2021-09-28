# Retrieving Logs

Many apps will create logs for various types of errors with additional information that a developer can use to locate the source of the issue. Including those logs in your issue reports when you experience a problem can help solve the problem faster.

{% hint style="info" %}
To view existing logs from all your applications you can use [`journalctl`](https://www.digitalocean.com/community/tutorials/how-to-use-journalctl-to-view-and-manipulate-systemd-logs)\`\`
{% endhint %}

By default, debug messages are not shown since they can be quite noisy in normal usage. To see debug logs, start the app from Terminal using the [environmental variable](https://www.digitalocean.com/community/tutorials/how-to-read-and-set-environmental-and-shell-variables-on-a-linux-vps) `G_MESSAGES_DEBUG`

```bash
G_MESSAGES_DEBUG=all com.github.myteam.myapp
```

If the app in question is a Flatpak app, like the apps available from AppCenter, you'll need to start the app with `flatpak run` as well:

```bash
G_MESSAGES_DEBUG=all flatpak run com.github.myteam.myapp
```

Now that logs are being printed to Terminal, reproduce the issue you're experiencing then copy and paste the Terminal output to the bottom of your issue report.

{% hint style="info" %}
For information on creating logs in your app, see the [developer guide](https://docs.elementary.io/develop/writing-apps/creating-logs)
{% endhint %}

