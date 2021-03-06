# ChestCounter

[![Build Status](https://travis-ci.org/henne90gen/ChestCounter.svg?branch=master)](https://travis-ci.org/henne90gen/ChestCounter)

This is a Minecraft mod that allows you to count all the items that you have in your chests.
Items are counted by simply opening chests.
Later on you can query for specific items or search for a certain key word.
The mod will list all items that you have in various chests.

## Setup

To use this mod, you first need to install Forge.
Then simply drag the `.jar` file for this mod into the `mods` folder.

## Usage

Every time you open a chest, it is automatically added to the internal database.
You can query the internal database at any time by typing into the search field that can be found in any inventory or chest screen.
You can also give labels to your chests. This can be done by typing the label into the text field in the header of the chest screen.

## Keyboard Shortcuts

- F8: enables/disables the mod (same as setting `enabled` in the config)
- Ctrl+C: shows/hides the inventory search result (same as setting `showSearchResultInInventory` in the config)
- Alt+C: shows/hides the in game search result (same as setting `showSearchResultInGame` in the config)

## Config

The configuration is stored in the `chestcount.json` file in the root folder of your minecraft installation (usually `<HOME_DIR>/.minecraft`).
This file also contains all the data that the mod has accumulated about your chests and items, so be careful when editing this file.

Example file:
```json
{
    "version": 2,
    "config": {
        "enabled": true,
        "searchResultPlacement": "RIGHT_OF_INVENTORY",
        "showSearchResultInInventory": true,
        "showSearchResultInGame": true
    },
    "worlds": {}
}
```

| Value                         | Default            | Description                                                       |
| ----------------------------- | ------------------ | ----------------------------------------------------------------- |
| `enabled`                     | true               | Disabling the mod means that no additional UI will be rendered and it will also no longer collect data on your items |
| `searchResultPlacement`       | RIGHT_OF_INVENTORY | Available values: `RIGHT_OF_INVENTORY`, `LEFT_OF_INVENTORY`       |
| `showSearchResultInInventory` | true               | Whether the search result should be shown in the inventory or not |
| `showSearchResultInGame`      | true               | Whether the search result should be shown in game or not          |
