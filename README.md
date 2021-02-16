# English



![](https://media.discordapp.net/attachments/719560298847273030/778079166968365056/btetechguide.gif)

## Introduction

Welcome to BTE's Technical Guide! In this guide, you'll learn how to install the modpack, host a server, and more. If you encounter any issues, please feel free to contact us via our [Discord](https://discord.gg/3mrQBYd) and ask in the [\#support](https://discord.com/channels/690908396404080650/691034211464773684) channel, or send a message to the **BTE Support** bot to get help directly from the staff team.

{% hint style="info" %}
This guide is only for the Java edition of Minecraft! If you'd like to read a similar guide for Bedrock, check out the [Bedrock Server Setup Guide](https://bteguides.gitbook.io/bedrock-server-setup-guide/).
{% endhint %}

## 1. Installing the modpack

This section will explain the process of installing the BTE modpack that is required for contributing to the project.

This page is split into 2 parts: using the automated installer, and performing a manual installation. Use the contents on the right side of the page to easily navigate through the page.

### 1.1. Using the automated installer

To begin, you will need to download the correct installer for your operating system. These can be found on our Discord server, or below.

* [Windows installer](https://bte-installer.s3.amazonaws.com/public/installer/v1.11/BTEInstaller-1.11-windows.zip)
* [macOS installer](https://bte-installer.s3.amazonaws.com/public/installer/v1.11/BTEInstaller-1.11-mac.dmg) \(requires macOS 10.15\)
* [Linux installer](https://bte-installer.s3.amazonaws.com/public/installer/v1.11/BTEInstaller-1.11-linux.tar.gz)
* [Universal installer](https://bte-installer.s3.amazonaws.com/public/installer/v1.11/BTEInstaller-1.11-universal.jar) \(requires Java 8\)

After you’ve completed the installation process, start your Minecraft launcher. You’ll see a new profile called **Build the Earth**. Select that profile and click on **Play** to start. You’ll also see that it has created a pre-generated world for you to start building.

### 1.2. Performing a manual installation

Here, you'll learn how to download the required mods and add them to your mods manually.

{% hint style="info" %}
Please note that this method will have a harder time updating if any updates come. A manual install may also have issues with worlds. The automated installer is always recommended over a manual install if possible.
{% endhint %}

There are two ways to perform a manual install:

* With [MultiMC](./#1-2-1-multimc)
* With [Forge](./#1-2-2-forge)

We recommend MultiMC for use with the modpack, as the install won't affect your existing Minecraft installation.

#### 1.2.1. MultiMC

* On **Windows:**
  1. [Download MultiMC](https://multimc.org/#Download) for Windows
  2. Follow the instructions in the installer and launch MultiMC
* On **macOS:**
  1. [Download MultiMC](https://multimc.org/#Download) for macOS
  2. Extract the app and launch MultiMC
* On **Debian-based Linux:**
  1. [Download MultiMC](https://multimc.org/#Download) for Ubuntu \(`.deb` package\)
  2. Double click on the package to install it via the app store, or open a terminal and run `sudo dpkg -i /path/to/file`
* On **Arch-based Linux:**
  1. Make sure you can download packages from the AUR \(Arch User Respository\)
  2. Open a terminal and run `yay -S multimc5` to install the package
* On **Other Linux:**
  1. Download the .tar.gz package [here](https://files.multimc.org/downloads/mmc-stable-lin64.tar.gz)

**Setting the modpack up:**

1. First, set your account by clicking on **Accounts** in the top right corner by clicking **Manage Accounts**.
2. Click on the **Add** button and log in using your Mojang username and password.
3. Create a new profile by pressing **Add Instance** in the top left corner.
4. Go to the **Import from zip** tab and paste`installer.s3.amazonaws.com/public/modpack_versions/BuildTheEarthPack_1.6.zip` into the text box.
5. Once the import is done, click on the **Edit Instance** button and go to the **Settings** tab.
6. Tick the **Memory** box and use the arrows to change the maximum amount of RAM allocated. We recommend somewhere between 4 GB and 8 GB.
7. Launch the modpack by double-clicking its icon.

#### 1.2.2. Forge

1. Download and install Forge for your operating system [here](https://files.minecraftforge.net/maven/net/minecraftforge/forge/index_1.12.2.html).
2. Download our modpack [here](https://bte-installer.s3.amazonaws.com/public/modpack_versions/BuildTheEarthPack_1.6.zip).
3. Extract the downloaded file from step 2 and open it.
4. Once there, go to the `overrides` → `mods` folder.
5. Copy all the mods from this folder to:
   * On **Windows:** `%APPDATA%\.minecraft\mods`
   * On **macOS:** `~/Library/Application Support/minecraft/mods`
   * On **Linux:** `~/.minecraft/mods`
6. Go back to the extracted folder and from the `saves` folder, copy **Build The Earth \(new projection\)** to:
   * On **Windows:** `%APPDATA%\.minecraft\saves`
   * On **macOS:** `~/Library/Application Support/minecraft/saves`
   * On **Linux:** `~/.minecraft/saves`
7. Open the Minecraft launcher, choose the **Forge 1.12.2** profile and launch the game!

### 1.3. Creating a new world

If you decide to create a new world, follow this:

1. Launch the game and go into the **Create New World** menu.
2. Go to **More World Options**, set the world type to **Planet Earth**, and click on the **Customize** button.
3. Once you're there, make sure that these are your settings:

![](https://media.discordapp.net/attachments/705285820822847518/777164731986870282/pic1.png?width=1279&height=684)

## 2. Installing and running a server

This section will explain how to setup your own BTE server with permissions and plugins, with our pre-configured server pack for build teams.

### 2.1. Setting the server up

Follow the instructions below to successfully set up the server pack:

1. Download our server pack from [here](https://github.com/Rickleuf/BTE-Server/releases) \(`Modded.only.zip`\).
2. Extract the file and go into the extracted folder.
3. Edit the `RUN.bat` file like this:
   * Change the **`-Xmx`** option according to how much RAM you want to allocate to the server. The value should be in the format `nG`, so, for example, if you want to allocate 6 GB, you would edit the option to say `-Xmx6G`.
   * Remove the `-nogui` option if you don't want the Minecraft server interface to show.
4. Save the `RUN.bat` file and start the server by double-clicking said file. The initial server start might take some time, so please be patient!
5. At some point, the server will ask whether you want to accept the [EULA](https://account.mojang.com/documents/minecraft_eula). Type in `true` and press Enter to accept it.
6. If at any point you'd like to stop the server, type `stop` in the server prompt and press Enter.

#### 2.1.1. Using your own world

If you've already started working on a single-player world and you'd like to move it to your new server, follow this section.

**2.1.1.1 Using a CubicChunks world**

1. Go into the server folder and delete the `TerraPreGenerated` folder.
2. Move your own world to the server folder.
3. Rename the world to `TerraPreGenerated`, so that the settings are kept.

**2.1.1.2. Using a vanilla world**

1. Download the CubicChunks Converter from [here](https://github.com/OpenCubicChunks/CubicChunksConverter/releases/download/v1/cubicchunksconverter-1.0.0-SNAPSHOT-all.jar).
2. Run the converter.
3. In the **Source:** directory, paste the location to the world you wish to use for your server, for example:
   * `C:\Users\USERNAME\AppData\Roaming\.minecraft\saves\New World`
4. In the **Destination:** directory, paste the same location as you did in the source but rename the actual world name, for example:
   * `C:\Users\USERNAME\AppData\Roaming\.minecraft\saves\CC World`
5. Make sure the **Converter** option is set to `Anvil` → `CubicChunks`.
6. Press the **Convert** button and wait for the **Done!** message in blue.
7. Go to the server folder and delete the `TerraPreGenerated` folder.
8. Go back to the newly-created world, and copy it into the server folder.
9. Rename the world to`TerraPreGenerated` so that the settings are kept.

### 2.2. Joining the server

Once you setup your server, you'll want to join it to actually start building! Read this section to learn how to.

#### 2.1.1. From the host computer

{% hint style="warning" %}
Never do this unless you have at least **12 GB** of RAM, since you'll be running both a client and a server on the same machine, which can be quite tasking for your computer.
{% endhint %}

If you do decide to run this setup, you can join your server by typing `localhost` in the IP field.

#### 2.1.2. From another computer

Before anyone can connect to the server running on your computer, you first have to set up a port forward of the server port:

1. Follow [these instructions](https://www.noip.com/support/knowledgebase/general-port-forwarding-guide/) to forward the port. The default Minecraft server port is `25565`.
2. To check whether the port forward worked, go to [this website](https://www.portchecktool.com/).
3. Write down the IP and port of the server. You can find your public IP by going to [this website](https://api.ipify.org). You will need to share that with other people for them to be able to connect, as shown in the following picture:

![](https://media.discordapp.net/attachments/731573774507442211/777217784039604264/ipport.png)

### 2.3. Using the server

You're almost done! As soon as you finish this last bit of setup, you'll be ready to start building.

#### 2.3.1. Granting OP permissions

In order to give yourself OP permissions, type `/op MINECRAFT_USERNAME` in the Minecraft chat, or `op MINECRAFT_USERNAME` in the server console.

#### 2.3.2. Managing permissions

Our server pack uses a plugin called **LuckPerms** for permission management. We've setup some handy permission groups for you to use:

| Permission Group | Command |
| :--- | :--- |
| Builder | `/lp user [USERNAME] group [ACTION] builder` |
| Helper | `/lp user [USERNAME] group [ACTION] helper` |
| Moderator | `/lp user [USERNAME] group [ACTION] moderator` |
| Administrator | `/lp user [USERNAME] group [ACTION] administrator` |

Make sure to replace the `[USERNAME]` field, with the user's Minecraft username and the `[ACTION]` field with either `add` or `remove` depending on whether you want to add or remove the role.

Here is another table explaining which permissions each of the roles have:

| Permission Group | Permissions |
| :--- | :--- |
| Builder | All WorldEdit commands, `/back`, `/tp`, `/setwarp`, `/gamemode`, and Essentials commands. |
| Helper | `/speed`, `/delwarp`, Essentials commands, kick, temporary ban, temporary mute, and warn. |
| Moderator | Permanent mute, temporary IP ban, history, check, and permanent ban. |
| Administrator | Full access to all commands and actions. |

{% hint style="info" %}
These are default permissions and can be changed within LuckPerms' configuration
{% endhint %}

#### 2.3.3. Teleporting

Our modpack comes with a custom command called `/tpll`. It allows teleportation using latitude and longitude. Users who do not have OP permissions will not be able to use this command. If this applies, you can use the `/cs tpll [LATITUDE] [LONGITUDE]` command.

#### 2.3.4. World Backups

If you wish to have automatic world backups, move the mods from the `extra-mods` folder to the `mods` folder. After that, restart the server. A backup will be created every 15 minutes. You can change this in the `config` folder.

## 3. Installing additional mods

### 3.1. OptiFine

First, you'll have to download OptiFine from [here](http://adfoc.us/serve/sitelinks/?id=475250&url=http://optifine.net/adloadx?f=OptiFine_1.12.2_HD_U_F5.jar&x=961f). You may need to click a **Skip** button in the top right corner to skip the ads when downloading.

The next sections will depend on how you installed the BTE modpack:

* If you used the [Automated installer](./#3-1-1-automated-installer)
* If you used [MultiMC](./#3-1-2-multimc)
* If you used [Forge](./#3-1-3-forge)

#### 3.1.1 Automated installer

We'll list common folders for each operating system which you will use as reference points throughout the guide depending on your operating system:

* On **Windows:** `%APPDATA%\.buildtheearth`
* On **macOS:** `~/Library/Application Support/Build The Earth`
* On **Linux:** `~/.buildtheearth`

Copy the downloaded OptiFine `.jar` file and move it into the `mods` folder in the reference folder depending on your operating system.

#### 3.1.2. MultiMC

1. Open MultiMC, select the **Build The Earth** profile and click on the **Edit Instance** button.
2. Go to the **Loader Mods** tab and click on the **Add** button.
3. Using the file selector, navigate to the location of your OptiFine `.jar` file and select it.

#### 3.1.3. Forge

The way you install OptiFine on forge is almost identical to the one for the automated installer. Follow the steps outlined there, but in the following folders:

* On **Windows:** `%APPDATA%\.minecraft`
* On **macOS:** `~/Library/Application Support/minecraft`
* On **Linux:** `~/.minecraft`

### 3.2. Shaders

Shaders require OptiFine to be installed, so please do so before continuing.

The installation process for shaders is pretty similar to that for mods, only you'll be placing files in a different folder, and shaders come in a `.zip` file rather than a `.jar`.

1. There are a variety of shaders to choose from, so find the one that you like the best and download it. Once done you should have a `.zip` file.
2. Place the `.zip` file in the shaders folder:
   * On **Windows:**`%APPDATA%\.buildtheearth\shaderpacks`
   * On **macOS:** `~/Library/Application Support/Build The Earth/shaderpacks`
   * On **Linux:** `~/.buildtheearth/shaderpacks`
3. You can now open Minecraft and go to `Options` → `Video Settings` → `Shaders` and switch to your desired shader pack as shown in the picture:

![](https://media.discordapp.net/attachments/731573774507442211/777239369119170590/shaderpic.png?width=1279&height=684)

You can also adjust shader settings according to your preferences, but we recommend leaving them at the default values to balance quality and performance.

{% hint style="info" %}
Depending on whether you used the automated installer, MultiMC or Forge, the `shaderpacks` folder location might change.
{% endhint %}

### 3.3. Other mods

If you'd like to install extra mods, follow the OptiFine guide with the mods you want to install.

## 4. Troubleshooting

This section explains some common errors you can experience when installing or running the modpack.

### 4.1. Installer

Before checking these errors, make sure that all Minecraft processes \(including the launcher\) are closed before attempting an installation. Also make sure that no other application is using the JVM \(Java Virtual Machine\).

* **An error occurred while running installer. Error code: 0:** The installation was unsuccessful and there may be need to do a manual installation, however it's still worth to try using the [Universal Installer](https://bte-installer.s3.amazonaws.com/public/installer/v1.11/BTEInstaller-1.11-universal.jar)
* **An error occurred while running installer. Error code: \(any non-0 number\):** The cause of this error is unknown, and you will have to perform a manual install.
* **Unable to replace invaild library:** This could be due to either Minecraft or some other program using the JVM being open. Close any of those programs and try again.
* **VCRUNTIME140.dll was not found:** This is a Windows-only issue. To fix it, download and install this [Visual C++ Redistributable](https://www.microsoft.com/en-us/download/details.aspx?id=52685).
* **Unable to download library:** This is likely because of your Internet connection being unstable, slow or offline. Check it and try again.

For a more comprehensive list of installer issues, read [this document](https://gist.github.com/Barteks2x/06e971a3126f53bfe5e3e65a4e530764).

### 4.2. Minecraft

The most common Minecraft error is an instant crash. Before proceeding make sure you dedicate enough RAM to your Minecraft installation by changing the JVM arguments:

1. Open the Minecraft launcher.
2. Go to the **Installations** tab.
3. Find the profile you want to edit, ideally **Build The Earth**.
4. On the right side of the profile, click on the 3 dots and then the **Edit** button.
5. Click on the **More Options** button at the bottom.
6. Then, in the **JVM Arguments** field, find the `-Xmx` argument. Change the number next to it to the amount of GB you want to use, as shown in the  picture:

![](https://media.discordapp.net/attachments/731573774507442211/777246044982476830/jvmargpic.PNG)

If that still hasn't solved your problem, you can follow this potential fix:

* On **Windows:**
  * Open the `options.txt` file in `%APPDATA%\.buildtheearth`.
  * Use the `Ctrl` + `F` keyboard shortcut to bring up the Find dialog and search for `fullscreen`.
  * Once you find the parameter, replace the `true` next to it with `false`.
* **macOS:**
  * Open the `options.txt` file in `~/Library/Application Support/Build The Earth`.
  * Use the `⌘ + F` shortcut to bring up the Find dialog and search for `fullscreen`.
  * Once you find the parameter, replace the `true` next to it with `false`. ****
* **Linux:**
  * Open a terminal and run the command:`sed 's/fullscreen:true/fullscreen:false/' ~/.buildtheearth/options.txt`

Restart Minecraft and check if the issue has been resolved!

### 4.3. WorldEdit

#### 4.3.1 Schematics folder

In some cases, the WorldEdit schematics folder doesn't exist by default, which causes problems related to them. To fix it, create a new folder called `schematics`:

* On **Windows:**
  * `%APPDATA%\.buildtheearth\config\worldedit`
* On **macOS:**
  * `~/Library/Application Support/Build The Earth/config/worldedit`
* On **Linux:**
  * `~/.buildtheearth/config/worldedit`

#### 4.3.2. Large operations being slow

Since WorldEdit operates on individual blocks and requires chunks to be loaded, it can be very slow. There is an experimental solution for this, but it's still in development and we will announce it when it's ready.

