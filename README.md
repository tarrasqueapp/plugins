<div align="center">
  <a href="https://tarrasque.app" target="_blank"><img src="https://tarrasque.app/images/logo.svg" width="150" /></a>
  <h1>Tarrasque App</h1>
  <h2>Plugin Repository</h2>
</div>

This is the official plugin repository for [Tarrasque App](https://tarrasque.app). This repository contains the `plugins.json` file, which is used by the app to find and download approved plugins.

## Submitting a plugin

To have your plugin listed on the app, please submit a pull request. The pull request should add a new entry to the `plugins.json` file with the following properties:

| Property       | Description                                                                             |
| -------------- | --------------------------------------------------------------------------------------- |
| `id`           | The identifier/slug of the plugin. This must be unique and cannot contain spaces.       |
| `name`         | The title of the plugin. This is what will be displayed in the app.                     |
| `manifest_url` | The URL to the plugin's manifest file. This is used to fetch metadata about the plugin. |

### Example

```json
{
  "id": "dnd5e-plugin",
  "name": "Dungeons & Dragons 5th Edition Plugin",
  "manifest_url": "https://tarrasqueapp.github.io/dnd5e-plugin/manifest.json"
}
```

Once your pull requested is merged, your plugin will be available to be downloaded from the app automatically.

## Updating a plugin

When you make a change to your plugin, no further action is required on your part. The app will automatically load the latest version of your plugin when it is next opened.

## Removing a plugin

If you no longer want your plugin to be available in the app, you can remove it from `plugins.json` and submit a pull request to have it removed from the app. If you want to re-add your plugin in the future, you can always submit a new pull request to add it back.
