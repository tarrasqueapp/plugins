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

Your plugin's manifest file should be hosted on a public URL, as it is responsible for instructing the app what to display and where. Here is an example of a manifest file for the [dnd5e](https://github.com/tarrasqueapp/dnd5e) plugin:

```json
{
  // A unique identifier for the plugin (usually in the format `username/repo`)
  "id": "tarrasqueapp/dnd5e",
  // The title of the plugin
  "name": "Dungeons & Dragons 5th Edition",
  // A short description of the plugin
  "description": "A plugin for the Dungeons & Dragons 5th Edition ruleset",
  // The name of the plugin's author
  "author": "Tarrasque App",
  // An array of URLs where the plugin's files can be accessed
  "urls": [
    // The image file that will be used as the plugin's icon (at least 32x32 pixels)
    {
      "name": "icon",
      "url": "https://dnd5e.tarrasque.app/icon.svg"
    },
    // The URL that will be used to load the plugin in the map overlay
    // Optional, only needed if the plugin displays a map overlay (e.g. dice roller, character sheet, etc.)
    {
      "name": "map_iframe",
      "url": "https://dnd5e.tarrasque.app/overlay",
      // The width and height of the iframe where the plugin will be shown
      "width": 300,
      "height": 300
    },
    // The URL that will be used to load the plugin in the compendium
    // Optional, only needed if the plugin has compendium data (e.g. spells, monsters, abilities, etc.)
    {
      "name": "compendium_iframe",
      "url": "https://dnd5e.tarrasque.app/compendium"
    },
    // The URL of the plugin's repository or documentation for more information (optional)
    {
      "name": "homepage",
      "url": "https://github.com/tarrasqueapp/dnd5e"
    }
  ]
}
```

## Updating a plugin

When you make a change to your plugin, no further action is required on your part. The app will automatically load the latest version of your plugin when it is next opened.

## Removing a plugin

If you no longer want your plugin to be available in the app, you can submit a pull request to have it removed from the app. If you want to re-add your plugin in the future, you can always submit a new pull request to add it back.
