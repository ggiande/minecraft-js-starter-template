# Minecraft TypeScript Starter Project

This sample demonstrates a simple build process and TypeScript compilation for Minecraft. This readme shows how you can use Betas APIs experiment to build out simple gameplay styles. You can use this project as a starter for your own scripting projects.

## Prerequisites

**Install Node.js tools**

Node package manager [npm](https://www.npmjs.com/package/npm).

Download the version with "LTS" next to the number and install it.

**Install Visual Studio Code, if you haven't already**

Visit the [Visual Studio Code website](https://code.visualstudio.com) and install Visual Studio Code.

## Getting Started

1. Use npm to install depencies and to install a new one globally:

   ```powershell
   npm i
   npm i gulp-cli --global
   ```

### Chapter 1. Customize the behavior pack

In Visual Studio Code, expand the `behavior_packs` node in the treeview to the left, and rename the **starterbp** folder to "project_name".

Use the Find/Replace command (Ctrl-Shift-F) to search for "starterbp" and replace the instance in **gulpfile.js** and the instance in **launch.json** with "project_name."

- [ ] behavior_packs/"folder_name"/
- [ ] launch.json
- [ ] behavior_packs/"folder_name"/manifest.json
  - [ ] name
  - [ ] description
- [ ] Create new UUIDs from the [Online UUID Generator](https://www.uuidgenerator.net/)

### Chapter 2. Let's test the parts of our project

The following powershell command should only run once.
`Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass`

Gulp in "watch mode" allows gulp to sit in the background and watch for changes,and if they happen, they will automatically compile and deploy to the Minecraft folder. This way, we won't have to worry about separately compiling every time we make a change to code.

> IMPORTANT:
> You may also need to update the version of Beta APIs in your `dependencies` section to match your version of Minecraft.
> Versions 1.19.40 feature `1.0.0-beta` APIs
> Versions 1.19.50 feature `1.1.0-beta` APIs
> Future versions will likely require updated versions of Beta APIs.

## Manifest

- [gulpfile.js](https://github.com/microsoft/minecraft-scripting-samples/blob/main/ts-starter/gulpfile.js): This file contains build instructions for Gulp, for building out TypeScript code.
- [scripts](https://github.com/microsoft/minecraft-scripting-samples/blob/main/ts-starter/scripts): This contains all of your TypeScript files, that will be compiled and built into your projects.
- [behavior_packs](https://github.com/microsoft/minecraft-scripting-samples/blob/main/ts-starter/behavior_packs): This contains resources and JSON files that define your behavior pack.
