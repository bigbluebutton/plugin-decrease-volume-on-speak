# Decrease external video's volume on speak

## What is it?

This plugin is one of the official bbb plugins. It basically decreases the external video's volume when a user is speaking in the meeting.


## Building the Plugin

To build the plugin for production use, follow these steps:

```bash
cd $HOME/src/plugin-decrease-volume-on-speak
npm ci
npm run build-bundle
```

The above commands will generate the `dist` folder, containing the bundled JavaScript file named `DecreaseVolumeOnSpeak.js`. This file can be hosted on any HTTPS server along with its `manifest.json`.

If you install the plugin separated from the manifest, remember to change the `javascriptEntrypointUrl` in the `manifest.json` to the correct endpoint.

To use the plugin in BigBlueButton, send this parameter along in create call:

```
pluginManifests=[{"url":"<your-domain>/path/to/manifest.json"}]
```

Or additionally, you can add this same configuration in the `.properties` file from `bbb-web` in `/usr/share/bbb-web/WEB-INF/classes/bigbluebutton.properties`


## Development mode

As for development mode (running this plugin from source), please, refer back to https://github.com/bigbluebutton/bigbluebutton-html-plugin-sdk section `Running the Plugin from Source`
