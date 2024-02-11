<p align="center">
  <a href="https://tarrasque.app">
    <img src="https://tarrasque.app/images/logo.svg" width="150" />
  </a>

  <h1 align="center">Tarrasque App</h1>
  <h2 align="center">Plugin Repository</h2>
</p>

This is the official plugin repository for [Tarrasque App](https://tarrasque.app). This repository contains the `plugins.json` file, which is used by the app to find and download approved plugins.

## Submitting a plugin

To have your plugin listed on the app, please submit a pull request. The pull request should add a new entry at the bottom of the `plugins.json` file with a link to your plugin's manifest file. Once your pull request is merged, your plugin will be available to be downloaded from the app automatically.

### Creating a manifest file

Your manifest file should be hosted on a public URL and should be a JSON file with the following properties:

| Property       | Description                                             |
| -------------- | ------------------------------------------------------- |
| `name`         | The title of the plugin                                 |
| `description`  | A short description of the plugin                       |
| `author`       | The name of the plugin's author                         |
| `icon_url`     | The image file that will be used as the plugin's icon   |
| `plugin_url`   | The URL that will be used to load the plugin in the app |
| `homepage_url` | The URL of the plugin's repository or documentation     |

These properties will be used to display information about your plugin in the app. Here is an example of a manifest file for the [dnd5e](https://github.com/tarrasqueapp/dnd5e) plugin:

```json
{
  "name": "Dungeons & Dragons 5th Edition",
  "description": "A plugin for the Dungeons & Dragons 5th Edition ruleset",
  "author": "Tarrasque App",
  "icon_url": "https://tarrasqueapp.github.io/dnd5e/icon.svg",
  "plugin_url": "https://tarrasqueapp.github.io/dnd5e",
  "homepage_url": "https://github.com/tarrasqueapp/dnd5e"
}
```

## Updating a plugin

When you make a change to your plugin, no further action is required on your part. The app will automatically load the latest version of your plugin when it is next opened.

## Removing a plugin

If you no longer want your plugin to be available in the app, you can submit a pull request to have it removed from the app. If you want to re-add your plugin in the future, you can always submit a new pull request to add it back.
