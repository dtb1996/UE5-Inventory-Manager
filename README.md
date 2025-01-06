# UE5 Inventory Manager Plugin

## Overview
The UE5-Inventory-Manager Plugin is a flexible system designed to be the base for a fully-fledged inventory system.

## Features
* Customizable item lists and categories
* Data Table for storing specific item details, such as icon images and 3D meshes
* Global item info lookup function
* Example player controller blueprint and map, demonstrating possible implementation ideas

## Requirements
* Unreal Engine 5.4 or later
* Visual Studio 2019 or 2022 setup for Unreal Engine development

## How to install
1. Add the plugin to your existing UE5 project into the Plugins folder (create one if it does not yet exist). The zip can be downloaded or this repo can be added as a submodule in your project.
2. Right-click your project's .uproject file and select "Generate Visual Studio project files"
3. Open the Visual Studio solution and build the project

## Using the Inventory Manager
1. Attach an instance of the InventoryComponent to whatever you would like to add an inventory to (Player controller, character, chest, etc...)
2. The following functions are included to provide basic inventory management actions: AddItem, RemoveItem, ClearInventory, HasItem, GetItems, and SortItemsByType
3. Two delegates are also included to notify of changes to the inventory: OnInventoryUpdatedDelegate and OnItemAddedDelegate
4. From here it is up to you, use this as a base to build the functionality needed for your game

## Customizing the items
* InventoryItemInfo: struct that provides the item details
* InventoryItemName: enum that specifies item names
* InventoryItemType: enum that specifies item categories
* In the plugin example directory, there is a data table, DT_ItemInfo that is used to store details for available items. If you decide to create a new data table be sure to update the DATA_TABLE_PATH define in InventoryFunctionLibrary.cpp so that the lookup function works correctly.

## Demo Project
[UE5 Inventory Manager Plugin Example](https://github.com/dtb1996/UE5-Inventory-Manager-Example)

## Support
[bitgamingstudio@gmail.com](mailto:bitgamingstudio@gmail.com)

## Attributions
Pixel Art Icon Pack by B3rries (https://b3rries.itch.io/)
Licensed under Creative Commons: By Attribution 4.0 License
http://creativecommons.org/licenses/by/4.0/

Item 3D Models by Kenney (www.kenney.nl)
Licensed under Creative Commons: CC0
https://creativecommons.org/publicdomain/zero/1.0/
