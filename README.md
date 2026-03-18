# Archipelago for Spyro 2: Ripto's Rage

## Introduction

Archipelago is a game randomization library that allows you to create and play custom worlds in Spyro 2: Ripto's Rage. This README provides a comprehensive guide to getting started with Archipelago for Spyro 2.

## System Requirements

### Supported Platforms

* Windows (Duckstation client required)

### Required Software

* [Duckstation](https://www.duckstation.org) - A PlayStation emulator that supports Spyro 2: Ripto's Rage
* Archipelago version 0.6.1 or later
* The [Spyro 2 Archipelago Client and .apworld](https://github.com/Uroogla/S2AP/releases)
* A legal US Spyro 2: Ripto's Rage ROM

## Getting Started

### Creating a Config File

A config file is required to set up your Archipelago game. This file contains settings for your game, such as the number of gems and talismans to collect.

* See the [Archipelago setup guide](https://archipelago.gg/tutorial/Archipelago/setup_en) for instructions on creating a basic YAML file.
* Run `ArchipelagoLauncher.exe` to generate a template file, and copy `Spyro 2.yaml` to the `players` folder.
* Fill out the config file with your desired settings and place it in the `players` folder.

### Generating and Hosting Your World

Once you have created your config file, you can generate and host your world using the following steps:

* Run `ArchipelagoGenerate.exe` to build a world from the YAML files in your `players` folder.
* This will create a `.zip` file in the `output` folder.
* You can upload this file to the [Archipelago website](https://archipelago.gg/uploads) or host the game locally with `ArchipelagoHost.exe`.

### Setting Up Spyro 2 for Archipelago

To set up Spyro 2 for Archipelago, follow these steps:

1. Download the S2AP.zip and spyro2.apworld from the GitHub page linked above.
2. Double click the apworld to install to your Archipelago installation.
3. Extract S2AP.zip and note where S2AP.Desktop.exe is.
4. Open Duckstation and load into Spyro 2: Ripto's Rage.
5. In Duckstation, navigate to Settings > Game Properties > Console and select "Interpreter" under "Execution Mode".
6. Start a new game (or if continuing an existing seed, load into that save file).
7. Open S2AP.Desktop.exe, the Spyro 2 client. You will likely want to do so as an administrator.
8. In the top left of the Spyro 2 client, click the "burger" menu to open the settings page.
9. Enter your host, slot, and optionally your password.
10. Click Connect. The first time you connect, a few error messages may appear - these are okay.
11. Start playing!

## Optional Setup

There are several optional setup options available for Archipelago:

* [Poptracker](https://poptracker.github.io) package for this game, which can help you identify which checks are available.
* [Universal Tracker](https://github.com/FarisTheAncient/Archipelago/releases) is partially supported as well, but you may encounter issues with random settings, gemsanity, and world keys.

## Randomization Options

When playing with Archipelago, you can choose to randomize certain aspects of the game, such as:

* Talismans and orbs
* Skill points and milestones for reaching certain numbers of gems per level or overall
* Moneybags unlocks

You can also choose to allow certain colors as filler items, such as red, blue, green, purple, or yellow.

## Known Issues and Tentative Roadmap

As of v1.1.1, 1 Mar 2026:

### Known Issues

* If your goal doesn't send, restart+reconnect the client.
* In full gemsanity, there is a small chance that a sent gem will not be received. If this happens, send `clearSpyroGameState` as a message in your client and follow the reconnect instructions to fix it.
* Easy Bombo has odd behavior. Interact only with the Bombo closest to the end of level.
* Sharks in Aquaria Towers do not trigger Death Link.
* During Gemsanity, loading into an existing save may release some gem% checks incorrectly, based on what you've collected rather than received.
* Connecting to the client in a homeworld may warp Spyro or unlock doors based on your vanilla completion, not what you have received.
* If your YAML file allows Archipelago to randomly pick settings, Universal Tracker may not track correctly.

### Current Roadmap

* Add trick logic
* Sparx powerups as items (extended range, always point to nearest gem, extra hit point cheat code)
* Add locks around powerups
* Implement Entrance Randomizer
* Client should inform user on disconnect
* Support PAL and NTSC-J
* Support Mac and Linux
* Client performance improvements

For latest list of known issues and desired features, see https://github.com/Uroogla/S2AP/issues. Reporting issues in the Archipelago Discord thread for Spyro 2 is preferred, but reports to this link will be read as well.