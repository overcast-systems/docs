---
sidebar_position: 1

title: Installation
description: Quick and easy installation process
---

# Installation

## Downloading The Script
After you have bought the script from our tebex store you can find it right **[here](https://portal.cfx.re/assets/granted-assets?page=1&sort=asset.updated_at&direction=asc)**.

Simply click on **download** and you should have the files on your computer.

## Installing The Script
After the download you should have received a .zip folder. Extract the files of this folder to a location of your liking.


Once the files have been extracted, locate your FiveM server's resources folder and open it.

Choose a folder to install the script in or if you don't want to you can just install it in the root folder.

Drag and drop <u>only</u> the `ocs_vitalcore` folder from the extracted files into your resources folder or a subfolder of such.

Finished, you have successfully installed the script.

## Starting The Script

If you are starting whole folders in your server.cfg with ```ensure [esx]``` for example, simply make sure that the script is in one of the folders specified in your server.cfg. You don't have to do any further steps.

Otherwise, copy this code:
```lua
    ensure ocs_vitalcore
```
and paste it to the bottom of your server.cfg. 

You don't have to paste it at the bottom if you don't like to but make sure to paste it <u>below</u> any **ESX**, **QB-Core**, **oxmysql** or **any other framework** specific resources or folders.

---
## Configuration
Congrats, you successfully installed the script. Go to the next page to start configuring.
