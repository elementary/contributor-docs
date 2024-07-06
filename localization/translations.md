# Translations

Localizing our website and apps is an important part of making elementary OS available to as many people as possible. Instead of relying solely on an internal translation team, we use crowdsourcing so that anyone can submit translations with little to no technical knowledge. In order to keep our voice consistent across the entire platform, and to help new translators get started, we’ve put together this translation guide.

## Using Weblate <a href="#steps-to-begin-translation" id="steps-to-begin-translation"></a>

Our apps and website are translated through Weblate: A libre web-based translation management system. In order to submit translations, you should:

1. Have a [Weblate account](https://l10n.elementary.io/accounts/register/)
2. Set your [language preferences](https://l10n.elementary.io/accounts/profile/)
3. Browse our [translatable projects](https://l10n.elementary.io/projects/)

Once you’ve selected a project, you can provide suggestions for strings that have not yet been translated, or suggest changes to strings that have already been translated. These suggestions will be evaluated by a translation team member and they will choose the most appropriate one. For more information about Weblate, you can refer to its [documentation](https://docs.weblate.org/en/weblate-3.0.1/user/index.html).

{% hint style="info" %}
By default, you will only be able to suggest translations. If you would like permission to save translations directly, [join us on Matrix](https://matrix.to/#/%23elementary-l10n%3Amatrix.org) and message an admin your Weblate username and the language you want to translate.
{% endhint %}

## Style Guides

When translating you may encounter a situation where you have to decide between several ways of saying the same thing. In these situations we refer to the Ubuntu [general translator guide](https://help.launchpad.net/Translations/Guide), and for language specific issues, we follow Ubuntu's [team translation guidelines](https://translations.launchpad.net/+groups/ubuntu-translators). Following these guidelines ensures uniform translations, while also allowing anyone to contribute.

### Specific Language Style Guides

Some language teams have created guides specific to their language to support their own translation efforts. You can check a list of the current available guides here:

{% content-ref url="es/" %}
[es](es/)
{% endcontent-ref %}

{% hint style="info" %}
Each style guide will use their own language to explain their details. Expect these pages to not be available in English.
{% endhint %}

## Using a Desktop Translation App

If you don't want to translate using Weblate, or want to make a lot a changes at once, you can also translate offline. To do so:

1. Go to a project you want to translate
2. Choose your language
3. Click on "Files" and then select "Download translation as gettext PO"
4. Choose your favorite text-, code- or PO-editor (e.g. [Poedit](https://poedit.net/))
5. Start translating
6. Once you've finished, use the "Upload translation" option in the "Files" menu on the same page you downloaded the po files from

## Excluded Projects

Some projects have been excluded from translations for technical or logistic reasons.

* Developer and contributor facing documentation is excluded since developers and contributors will need to be able to read and write in English to do their work.
* The elementary store is excluded since product information is only stored in English on the Printful platform, so it cannot be translated.
