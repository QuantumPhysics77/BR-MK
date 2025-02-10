# Brick Rigs Mod Kit (BRMK)

# Copyright
- Code and assets contained within this mod kit are copyrighted material
- You are allowed to use this mod kit to create mods for the game Brick Rigs
- You are allowed to distribute your mods to owners of the game Brick Rigs
- You are **NOT** allowed to redistribute this mod kit or parts of it to others
- You are **NOT** allowed to use assets or code of this mod kit in other game projects
- In general: Use common sense, if in doubt, ask Fluppi

# Installation

## Prerequisites
- Get access to Unreal Engine source code on GitHub: https://www.unrealengine.com/de/ue-on-github
- Make sure you have at least **200GB** of free disk space
- Download and install **Visual Studio 2022** Community Edition
    - Enable the **Game Development with C++** and **.NET Desktop Development** workloads
    - Enable the **.NET Framework 4.8.1-SDK** and **.NET Framework 4.8.1-Targeting-Pack** components
- Download and install git from https://git-scm.com/downloads
- Download and install git lfs (large file storage) from https://git-lfs.com/

## Download
- Create a root folder for the mod kit, for example **C:\BRMK**
- Open Windows command prompt
- Navigate to your root folder, for example with the command: `cd C:\BRMK`
- Initialize git lfs: `git lfs install`
- Clone the Unreal Engine repository from GitHub: `git clone -b 4.27 --depth 1 https://github.com/EpicGames/UnrealEngine.git`
- Wait for the download to finish, this could take a while
- While still in the root folder, clone the Brick Rigs Mod Kit from Bitbucket: `git clone https://bitbucket.org/fluppisoft/brickrigsmodkit.git`
- Your folder structure should now look like this:


```
C:\BRMK\
    UnrealEngine\
        Engine\
        Setup.bat
        ...
    BrickRigsModKit\
        Binaries\
        Source\
        BrickRigs.uproject
        ...
```

## Initial Setup
- Go to your BrickRigs folder and execute **SetupModKit.bat**
    - This will setup and build Unreal for you
    - Depending on your system the first time build could take upwards of an hour
- Launch the Brick Rigs Mod Kit by double clicking the **BrickRigs.uproject** file

# Creating a Mod
- Click the **Create UGC** button at the top of the editor
- Enter the name of your mod and click 'Create'
- You will now have a folder for your mod in the content browser where you can place all of your assets
- When you are finished with your mod, click the **Package UGC** button at the top of the editor and select your mod

# Updating the Mod Kit
- Open the Windows command prompt
- Navigate to your mod kit folder, e.g.: `cd C:\BRMK\BrickRigsModKit`
- Update the repository with git: `git pull`
  - If this fails due to uncommitted changes, you can discard your changes with this command and try again (**WARNING:** This overwrites any changes you have made to game assets!): `git reset --hard`
- Rerun the setup: `SetupModKit.bat`