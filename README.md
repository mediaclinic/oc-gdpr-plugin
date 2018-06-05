# oc-gdpr-plugin
October CMS plugin to make websites GDPR compliant.

## Cookie constent

This plugin provides an easy integration of [Klaro! A Simple Consent Manager](https://github.com/KIProtect/klaro). 

All Klaro! settings can be managed via October's backend.

Information on how to use Klaro! can be found on the official website
[https://klaro.kiprotect.com/](https://klaro.kiprotect.com/). 

### Configuration

You can configure all Klaro! settings via the October CMS backend settings. 

If you are more of a code person you can overwrite the `config.js` partial
via your theme and use your own configuration file instead.

If you only want to define your applications manually you can overwrite the `apps.js` partial via your theme.

A configuration example is hosted on
[https://klaro.kiprotect.com/config.js](https://klaro.kiprotect.com/config.js).


#### Translations

You can add custom translation strings via the backend settings page. Create a new translation, give it a 2-char 
language code (`de`, `en`, etc.) and paste and modify the following json code in the code editor:

```json
{
    consentModal: {
        description: 'Hier können Sie einsehen und anpassen, welche Information wir über Sie sammeln. Einträge die als "Beispiel" gekennzeichnet sind dienen lediglich zu Demonstrationszwecken und werden nicht wirklich verwendet.',
    },
    inlineTracker: {
        description: 'Beispiel für ein Inline-Tracking Skript',
    },
    externalTracker: {
        description: 'Beispiel für ein externes Tracking Skript',
    },
    adsense: {
        description: 'Anzeigen von Werbeanzeigen (Beispiel)',
    },
    matomo: {
        description: 'Sammeln von Besucherstatistiken',
    },
    camera: {
        description: 'Eine Ãœberwachungskamera (nur ein Beispiel zu IMG-Tags)',
    },
    cloudflare: {
        description: 'Schutz gegen DDoS-Angriffe',
    },
    intercom: {
        description: 'Chat Widget & Sammeln von Besucherstatistiken (nur ein Beispiel)',
    },
    mouseflow: {
        description: 'Echtzeit-Benutzeranalyse (nur ein Beispiel)',
    },
    purposes: {
        analytics: 'Besucher-Statistiken',
        security: 'Sicherheit',
        livechat: 'Live Chat',
        advertising: 'Anzeigen von Werbung',
    }
}
```

You can find all possible translation keys in [Klaro's example config file](https://klaro.kiprotect.com/config.js).

### `consentManager` component

Place this component on your layout file to display the Klaro! Consent Manager.

#### Properties

#### `include_assets`

Enable this option to automatically include the klaro.js file.
You can disable this option if you want to take full control over how the script is included.