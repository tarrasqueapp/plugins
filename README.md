<div align="center">
  <a href="https://tarrasque.app" target="_blank"><img src="https://tarrasque.app/images/logo.svg" width="150" /></a>
  <h1>Tarrasque App</h1>
  <h2>Plugin Repository</h2>
</div>

This is the official plugin repository for [Tarrasque App](https://tarrasque.app). This repository contains the `plugins.json` file, which is used by the app to find and download approved plugins.

## Submitting a plugin

To have your plugin listed on the app, please submit a pull request. The pull request should add a new entry to the `plugins.json` file with the following properties:

| Property      | Description                                                                                                                                 |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| `name`        | The identifier/slug of the plugin. This must be unique and cannot contain spaces.                                                           |
| `author`      | The name of the author of the plugin. This can be your name, your GitHub username, or anything else.                                        |
| `version`     | The version of the plugin. This should be updated whenever you make a change to the plugin to ensure that users are notified of the update. |
| `title`       | The title of the plugin. This is what will be displayed in the app.                                                                         |
| `description` | A short description of the plugin and what it does.                                                                                         |
| `keywords`    | An array of keywords that describe the plugin. These are used to help users find the plugin.                                                |
| `repository`  | The URL to the plugin's repository. This is used to link to the plugin's repository from the app.                                           |
| `download`    | The URL to download the plugin. This should be a `.zip` file containing the plugin's distributable files.                                   |

### Example

```json
{
  "name": "dnd5e-plugin",
  "author": "tarrasqueapp",
  "version": "0.0.1",
  "title": "Dungeons & Dragons 5th Edition Plugin",
  "description": "This plugin adds support for the world's greatest roleplaying game.",
  "keywords": ["dnd", "dnd5e"],
  "repository": "https://github.com/tarrasqueapp/dnd5e-plugin",
  "download": "https://github.com/tarrasqueapp/dnd5e-plugin/releases/download/latest/dnd5e-plugin.zip"
}
```

Once your pull requested is merged, your plugin will be available to be downloaded from the app automatically.

> **Note**
> Reviews are done manually to ensure that all plugins are safe to use, but it shouldn't take more than a few hours for your plugin to be approved. If your pull request has been open for more than a day, please feel free to ping me on Discord.

## Updating a plugin

When you make a change to your plugin, you should update the `version` property of your plugin in `plugins.json`, and submit a pull request with the change to this repository to update the plugin version in the app. This is so that users are notified of the update and can download the latest version of your plugin.

## Removing a plugin

If you no longer want your plugin to be available in the app, you can remove it from `plugins.json` and submit a pull request to have it removed from the app. If you want to re-add your plugin in the future, you can always submit a new pull request to add it back.
