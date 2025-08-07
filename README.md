ipsuShade - Guidance on Pro Suite Supported Shaders:  
- [iMMERSE Pro 2403 (or higher)](https://www.martysmods.com/rtgi/)
- [iMMERSE Ultimate 2403 (or higher)](https://www.martysmods.com/relight/)
- qUINT_rtgi.fx (v0.36.1, but lower versions will work.)
- [NiceGuy COMPLETE_RT (outdated)](https://www.patreon.com/NiceGuy147)

<p align="center">
  <h1 align="center">ipsuShade.</h1>
  <h3 align="center"> ReShade / GShade presets for Final Fantasy XIV.</h3>
</p>
<p align="center"> <img width="66%" src="https://i.imgur.com/B2iuPjD.png"> </p>

## Table of Contents

- [What is ipsuShade?](#what-is-ipsushade)
- Software Install Guides:
  - [ReShade install guide for FFXIV.](#reshade-install-guide-for-ffxiv)
- ipsuShade Install Guides:
  - [How do I use ipsuShade on a fresh ReShade install?](#how-do-i-use-ipsushade-on-a-fresh-reshade-install)
  - [How do I use ipsuShade if I migrated to ReShade from a GShade install?](#how-do-i-use-ipsushade-if-i-migrated-to-reshade-from-a-gshade-install)
  - [How do I use ipsuShade with a GShade install?](#how-do-i-use-ipsushade-with-a-gshade-install)
  - [How do I update from ipsuShade v1.0.1 to v2.0.0+?](#how-do-i-update-from-ipsushade-v101-to-v200)
- In-Game settings and Troubleshooting:
  - [Troubleshooting and Common Issues (Updated for Dawntrail Graphics Update)](#troubleshooting-and-common-issues-updated-for-dawntrail-graphics-update)
  - [Required FFXIV in-game graphics settings.](#required-ffxiv-in-game-graphics-settings)
- Misc:
  - [Donate](#donate)
  - [Contact](#contact)

<!-- <h1 align="center">  !!! DISCLAIMER - PLEASE READ BEFORE CONTINUING !!! </h1>
<h3 align="center">
At the current time I am unsure about permission to redistribute the Marty Mcfly qUINT shader collection, which is used in my Ultimate presets. 
</h3>
<h3 align="center">
While I wait for a response, you must download them from <a href='https://github.com/martymcmodding/qUINT/archive/refs/heads/master.zip' target='_black'>  - HERE - </a> and merge the <code>Shaders</code> folder with the one found inside your <code>reshade-shaders</code> or <code>gshade-shaders</code>. This is explained in the guide below, so you are okay just to follow those steps.  
</h3>
<h4 align="center">
My Ultimate presets will lack certain intended shadows if you skip these steps, and certain presets may look too dark (Crystal & Vanilla).
</h4> -->


## What is ipsuShade?

ipsuShade is a <b>ReShade</b> preset collection (with <b>GShade</b> support) that aims to deliver maximum quality at maximum FPS with the `Gameplay`, `Questing` and `Lite` variant presets, but also provide the highest fidelity screenshots with the `Screenie`, `Ultimate` and `Pro Suite` preset types.

<!-- <img src="https://i.imgur.com/0h3bTyM.png"> -->

Each preset type comes in a range of 7 included colour variants.
<!-- These colours are: -->

<!-- <img src="https://i.imgur.com/wr2tvRH.png"> -->



<hr>

### ReShade install guide for FFXIV.

1. Click <a href='http://static.reshade.me/#download' target='_blank'>here</a> to download the latest version of ReShade, specifically the `with full add-on support` version.
    - This is the version which allows use of add-ons and an unlocked depth buffer for Depth of Field effects and improved lighting and shadows.
  <p align="center"> <img width="75%" src="https://i.imgur.com/U4U8wsl.png"> </p>


2. Run the ReShade Setup executuable and select `FINAL FANTASY XIV (ffxiv_dx11.exe)` in the game/application list.  
   You can search using the text input box above `Browse...`.  
    - Ensure it's `ffxiv_dx11.exe` and not `ffxiv.exe` or `ffxivboot.exe` or `ffxivsysinfo.exe` etc.
    - You may have to click the `Browse...` button and navigate to your FFXIV `/game/` folder to find the correct installation.
  <p align="center"> <img width="50%" src="https://i.imgur.com/7REZK1S.png"> </p>


3. For the rendering API step, select `Microsoft DirectX 10/11/12`. 

4. <b>This step is a bit counterintuitive, but:</b>  
   When it asks you to select the effects (Shaders) you wish to install, you please first click  `Uncheck All` in the top right of the window.  
   - Please then click the same box again, which should have changed to `Check All`.  
   - Every shader package should now be checked to download. Please ensure it looks like the image below:
   <p align="center"> <img width="50%" src="https://i.imgur.com/MFzJ7vw.png"> </p>
  - This step is required for ipsuShade, and ensures maximum compatibility with other all other presets. The file size increase is minimal.
  - For some reason, SweetFX is checked by default, and this hides the `Check All` option, hence needing to click it twice.
  
5. Please now click `Next` after ensuring all the effects have a checkmark next to them. The ReShade installer will now download these shaders. Please wait for this process to finish, and it will bring you to the Addon step.
  
6. <b>(OPTIONAL)</b> For the add-ons step, you may want to check and install `ReshadeEffectShaderToggler (REST) by 4lex4nder` to allow the exclusion of UI / HUD elements from the preset filtering (FFKeepUI in GShade).
    - If you check this, <b>you need to download the FFXIV preconfigured `ReshadeEffectShaderToggler.ini` found <a href="https://github.com/4lex4nder/ReshadeEffectShaderToggler-FFXIV/blob/main/ReshadeEffectShaderToggler.ini">here</a> to get it working.</b> Just place it next to the `ReshadeEffectShaderToggler.addon64` in your `/game/` folder.
    - To remove this addon, just delete the `ReshadeEffectShaderToggler.addon64` from your game folder.
   <p align="center"> <img width="50%" src="https://i.imgur.com/0OxKNxB.png"> </p>

7. Click `Next` on the add-ons page.
   - You can manually install add-ons later if needed, just put the `.addon64` files in your FFXIV `/game/` folder.

8. You should now have a working ReShade install for FFXIV. However, it will have no presets, only shaders. 
    - Follow the steps below to install <b>ipsuShade!</b>

9. **For XIV Dawntrail and onwards, due to the Graphics Update, you require one last ReShade configuration step.**
    - Boot into FFXIV, and open the ReShade overlay (By default, the keybind for this is the `Home` key, above your arrow keys.)
    - Click the `Edit global preprocessor definitions` box in the middle of the overlay.
    - In this menu, under the `RESHADE_DEPTH_INPUT_IS_REVERSED` section, change the value from `0` to `1`.
    - Now click away from the menu, and your shaders should recompile. The depth buffer should now be working in Dawntrail (required for Depth of Field, MXAO shaders etc.)
   <p align="center"> <img width="50%" src="https://i.imgur.com/pQDN5bo.png"> </p>

10. To update ReShade in the future, simply repeat this process with the new installer `.exe`, but instead select the `Update ReShade and effects` option after Step 3.
<p align="center"> <img width="50%" src="https://i.imgur.com/RtBlBj4.png"> </p>
<hr>

## How do I use ipsuShade on a fresh ReShade install?

There are two methods:

1. **GPosingway** - best compatibility, easy updates, other creators' presets included!
2. **Standalone Install** - if you just want ipsuShade.

<h2>Install ipsuShade with GPosingway -</h2>

[GPosingway](https://github.com/gposingway/gposingway) is a drop-in package for Final Fantasy XIV containing a stable collection of shaders, textures, and presets gathered from the community and beyond. GPosingway aims to ensure that presets will work as intended by its creators by avoiding conflicts, mismatches and missing files, giving users a consistent experience.


**Install:**  
You must already have ReShade installed to use GPosingway!  
Please follow the `Installation Script` instructions listed here to add GPosingway to your ReShade install: [GPosingway Latest Release](https://github.com/gposingway/gposingway/releases/latest)  


**Note.** You must say yes to the `iMMERSE` and `METEOR` optional packages when prompted by the installation script, as they are required by ipsuShade! 

<h2>Standalone ipsuShade Installation Steps -</h2>
<h3 align="center"> <a href='https://github.com/ipsusu/ipsuShade/releases/download/v2.0.0/ipsuShade_2406.zip' target='_blank'> Click here to download ipsuShade files for a fresh ReShade install. </a> </h3>

1. After ensuring you have downloaded ReShade as specified by the guide above, please download the `.zip` of the ipsuShade files using the link above.
   - It's important that you've installed ReShade with <b>all of the avaliable effects</b>, as there are only a very few shaders provided with ipsuShade. The vast majority of shaders are provided via the ReShade installer.</b>
3. Drag and drop the two ReShade folders found inside the `ipsuShade_2406.zip` into your FFXIV installation `\game\` directory. Be sure to merge and overwrite the existing `reshade-presets` and `reshade-shaders` folders.

    - For the Steam version, your directory is most likely: `C:\Program Files (x86)\Steam\steamapps\common\FINAL FANTASY XIV Online\game\`

    - For the Windows version, your directory is most likely: `C:\Program Files (x86)\SquareEnix\FINAL FANTASY XIV - A Realm Reborn\game\`
  

#### Note. The existing folders should be named `reshade-presets` and `reshade-shaders`. If they are called `gshade-presets` and `gshade-shaders` please read the <a href="https://github.com/ipsusu/IpsuShade#how-do-i-use-the-ipsusu-presets-ipsushade-if-i-migrated-from-a-gshade-install">section below</a> as you have an installation that has been migrated from a GShade install.

3. Once in-game, open the ReShade overlay (by pressing the `Home` key by default) and navigate to the `ipsuShade` folder inside your `reshade-presets` folder.
    - If you dragged the files while the game was still open, you need to press `Reload` on the bottom left of the overlay to get them to show up.

4. Simply double click to navigate the ipsuShade folders, and click any of the `.ini` presets to enable them. See <a href="https://github.com/ipsusu/ipsuShade#what-is-ipsushade">here</a> about an explanation of the presets.
    - Click the two dots at the top (the "..") to go up / back one folder.
      
5. You should now have a perfectly working install of ipsuShade.
<br>

## How do I use ipsuShade if I migrated to ReShade from a GShade install?

The simplest way forward here would be to just install ReShade again from scratch using the guide above, and then only use presets verified to work with this standard. The problem is that people are using a bunch of outdated shaders in the GShade file structure format, which causes shader duplication issues when using the proper ReShade standard.

However, the majority of other creators presets are only compatible with GShade, and will have issues working with the ReShade standrard adopted by ipsuShade 2.0.0. It's a big problem, and it's why packages like [GPosingway](https://github.com/gposingway/gposingway) now exist. 

As of ipsuShade version 2.0.0, my presets use shaders that will not be included in any old GShade installs. If you add these specific shader packages to your `gshade-shaders` folder, and then use my new preset files, it will work:
- [iMMERSE](https://github.com/martymcmodding/iMMERSE)
- [METEOR](https://github.com/martymcmodding/METEOR)
- [ZN_FX](https://github.com/Zenteon/ZN_FX)

## How do I use ipsuShade with a GShade install?

ipsuShade is included with <a href="https://github.com/Mortalitas/GShade/releases">GShade</a> by default.


**Disclaimer:**

>GShade is a *closed source* fork of ReShade that includes specific improvements to usability and compatibility with whitelisted games. There was an incident in Feburary 2023 where a poor decision was made by GShade's sole developer. The 4.1.1 update included anti-tampering code within the GShade installer that would restart Windows if a specific 3rd-party program was used to trigger functions within the installer to download certain assets independently (in an attempt to bypass a new GShade license agreement for certain textures and shaders). This code was removed after the obvious extremely negative reaction to the restart function from the community, but the reputational damage was already done. Therefore, *do use this program at your own judgement*. However, I do not want to punish innocent users who may not be able to use ReShade (e.g., Linux and Mac users) or may not have the technical ability to follow the install guides above. I have always held the stance that anyone may use and redistribute my presets or textures (as explained in my <a href="https://github.com/ipsusu/IpsuShade/blob/master/LICENSE.md">license<a>). My assets were excluded from the GShade license as they have always been offered freely and independently on my GitHub. I encourage my presets to be bundled with any possible ReShade forks in the future (please do get in touch!).


<p align="center"><a href="https://github.com/Mortalitas/GShade/releases/latest">Click here to download the latest release of GShade, which includes ipsuShade by default.</a></p>

After installation, you will be able to find the ipsuShade presets in the `gshade-presets\ipsuShade\` folder.

1. Click the `gshade-presets` folder if it is not already selected, and scroll down to find the `ipsuShade` folder.

2. Simply browse into your desired folder, and click any of the `.ini` presets to enable them. See <a href="https://github.com/ipsusu/ipsuShade#what-is-ipsushade">here</a> for an explanation of the presets.

    - Click the two dots at the top (the "..") to go back to the main folder if you would like to swap to another creator's preset.

<br>

## How do I update from ipsuShade v1.0.1 to v2.0.0+?

**1. GPosingway.**   
   - [GPosingway](https://github.com/gposingway/gposingway) will automatically clean up your install and install ipsuShade.
   - Please follow the `Installation Script` instructions listed here: [GPosingway Latest Release](https://github.com/gposingway/gposingway/releases/latest)  
   - **Note.** You must say yes to the `iMMERSE` and `METEOR` optional packages when prompted by the installation script, as they are required by ipsuShade!

     
**2. GShade.**
   - [GShade](https://github.com/Mortalitas/GShade/releases/latest) will automatically clean up your install and install ipsuShade.
   - Download the latest release: [here.](https://github.com/Mortalitas/GShade/releases/latest)

     
**3. Manually Update (Not Recommended)**
   - Due to the significant changes between ipsuShade 1.0.1 and 2.0.0, your old `/reshade-shaders/` folder is incompatible with the update.
   - As such you must backup (copy it to a safe place) and delete then your old `/reshade-shaders/` folder, located in your FFXIV `/game/` folder.
     - I just create a new `backup` folder and then drag and drop the old `reshade-shaders` into it, like this: 
     <p align="center"> <img width="75%" src="https://i.imgur.com/UUoxHdb.png"> </p>
   - Then, you need to download the latest version of ReShade: <a href='http://static.reshade.me/#download' target='_blank'>here</a>. Specifically the `with full add-on support` version.
   - Run the ReShade Setup executuable and select `FINAL FANTASY XIV (ffxiv_dx11.exe)` in the game/application list.  
   You can search using the text input box above `Browse...`.
-  Ensure it's `ffxiv_dx11.exe` and not `ffxiv.exe` or `ffxivboot.exe` or `ffxivsysinfo.exe` etc.
    - You may have to click the `Browse...` button and navigate to your FFXIV `/game/` folder to find the correct installation.
     <p align="center"> <img width="50%" src="https://i.imgur.com/7REZK1S.png"> </p>
  - For the rendering API step, select `Microsoft DirectX 10/11/12`.
  - If you've selected the correct `ffxiv_dx11.exe`, it should detect your previous ReShade installation and show the screen in the image below. You need to select the `Update ReShade and effects` option, then click `Next`.
<p align="center"> <img width="50%" src="https://i.imgur.com/RtBlBj4.png"> </p>
 - <b>This step is a bit counterintuitive, but:</b>  


   When it asks you to select the effects (Shaders) you wish to install, you please first click  `Uncheck All` in the top right of the window.  
  - Please then click the same box again, which should have changed to `Check All`.  
  - Every shader package should now be checked to download. Please ensure it looks like the image below:
   <p align="center"> <img width="50%" src="https://i.imgur.com/MFzJ7vw.png"> </p>

  - Click `Next` on the add-ons page.
     - You can manually install add-ons later if needed, just put the `.addon64` files in your FFXIV `/game/` folder.

  - You should now have a working ReShade install for FFXIV with the correct shaders, however **you now need to update to the new ipsuShade v2.0.0 presets.**
  - Click [HERE](https://github.com/ipsusu/ipsuShade/archive/refs/heads/master.zip) to download a `.zip` of the current ipsuShade files.
  - You need to open your FFXIV `/game/` folder and navigate inside the `/reshade-presets/` folder.
  - Open the the  ipsuShade `.zip` you just downloaded, navigate inside it's `/reshade-presets/` folder.
  - Copy the `ipsuShade` folder from inside here, into the `/reshade-presets/` folder inside your FFXIV `/game/` folder.
    <p align="center"> <img width="75%" src="https://i.imgur.com/mSqMYKp.png"> </p>
  - You can now safely delete the old `Ipsusu` folder from the game presets folder also, this is the old folder containing the v1.0.1 presets. These will no longer work properly with the new shaders, so you should probably do this.
  - You should now have manually updated your ReShade to use the standard ReShade shaders and installed the new ipsuShade presets!

- **For XIV Dawntrail and onwards, due to the Graphics Update, you require one last ReShade configuration step.**
    - Boot into FFXIV, and open the ReShade overlay (By default, the keybind for this is the `Home` key, above your arrow keys.)
    - Click the `Edit global preprocessor definitions` box in the middle of the overlay.
    - In this menu, under the `RESHADE_DEPTH_INPUT_IS_REVERSED` section, change the value from `0` to `1`.
    - Now click away from the menu, and your shaders should recompile. The depth buffer should now be working in Dawntrail (required for Depth of Field, MXAO shaders etc.)
   <p align="center"> <img width="50%" src="https://i.imgur.com/pQDN5bo.png"> </p>
   
## Troubleshooting and Common Issues (Updated for Dawntrail Graphics Update)

**Please first ensure your install is correct:**

**1. Check that you don't have duplicate shaders.**
  - If you have multiple of the exact same shader enabled (shown in the ReShade overlay), this means you have duplicates of shaders in your `reshade-shaders/Shaders` folder.
    - This is likely caused by trying to manually merge shader packages or update shaders in an imprecise way.
    
    <img src="https://i.imgur.com/7zlVhnc.png"></img>

    - To solve this, either manually clean your `reshade-shaders/Shaders` by searching for and deleting duplicates (for example, delete one of the `MultiLUT.fx` files), or entirely delete your `reshade-shaders/Shaders` folder and reinstall the shaders fresh via one of the methods listed at the start of this document.

**2. Make sure you are using the "with full add-on support" version of ReShade.**
  - You can check this by going to the "Add-ons" tab in the ReShade overlay and checking if you see this message at the top:

    <img src="https://i.imgur.com/rKct8Tt.png"></img>

  - If you see this message, you are using the wrong version of ReShade. You need to reinstall with the "full add-on support" version, which can be [found here.](https://reshade.me/#download)
  
**3. Make sure your ReShade has a reversed depth buffer.**
   - The depth buffer (the thing that ReShade reads for depth information) has been reversed with the Dawntrail Graphics Update.
   - You can check if your ReShade install has been configured to accept the reversed depth buffer by checking here:

     <img width="50%" src="https://i.imgur.com/pQDN5bo.png">

     If you cannot see the "Edit Global Preprocessor Definitions" button, disable `Performance Mode` by unchecking the box at the bottom of the overlay)
  
  - The value should be `1`, if it is `0`, you need to set it to `1` for it to work in FFXIV. 
   


### My shaders are not lined up with the edge of my character, they're floating to the top left!

<img width="25%" src="https://i.imgur.com/yasNvWQ.png"></img>

This is because of the in-game Graphics Upscaling setting amd/or 3D Resolution Scaling settings. This is currently most often the issue after the early popular recommendation to set FSR ingame to 99, to enable the built in sharpening filter of FSR. This setting should not be used in conjunction with ReShade, as it causes issues for ReShade (You can instead just enable a shader like `iMMERSE: Sharpen` and get a better quality effect anyway!). As for this issue: FSR will be "static" and just respect your resolution scaling percentage, offsetting the effects by a fixed amount. DLSS will vary to the demands of the current scene, making the effects scale and move.

**To fix this you can:**

- Select the upscaled scaled depth buffer value in the settings of the "Generic Depth" addon.
  - To do this, go to the "Add-ons" tab in your ReShade overlay, and look under the `Generic Depth` addon.
  - You need to click the checkbox next to one of the values that match your monitor's native resolution (for me, in this screenshot, it's 2560x1440).
    - It's normally the top one, but use trial and error and iterate through these settings until you can see the shaders line up properly with the in-game image.
    - For me, it was this one:
  
    <img src="https://i.imgur.com/n2fSASw.png"></img>

    - Your stuff should now work!
    - If not, you may need to simply disable the Graphics Upscaling. You can currently do this by turning the `Graphics Upscaling` value to `FSR` and then setting the `3D Resolution Scaling` slider to `100`.

**Alternative Method:** I think you can instead add  `﻿RESHADE_DEPTH_INPUT_X_SCALE` and `RESHADE_DEPTH_INPUT_Y_SCALE` to in the global preprocessor settings, and then set their values to a value above 1 to scale the depth buffer to match the native resolution. For the FSR at 99 trick, it would be setting these to `1.01` or `1.02` etc. until everything matches up. If you're scaling staticly via DLSSTweaks and have disabled the dynamic resolution, you can set this again to your static scaling. A 0.75 internal scaling preset requires a `1.33` scaling via the ReShade preprocessors, for some reason, so idk how that works.

### My game is green! (or Pink!)

<img width="33%" src="https://i.imgur.com/mGTAvfV.jpeg"></img>

**FIRST ENSURE YOUR INSTALL IS CORRECT BY FOLLOWING THE [3 STEPS AT THE START OF THIS SECTION!!!](#troubleshooting-and-common-issues-updated-for-dawntrail-graphics-update)**

This issue can also be caused by duplicate shaders. If your install is seemingly fine, then:

**If you are using GPosingway:**
- Update your MultiLUT.fx file (found in `/game/reshade-shaders/Shaders/MultiLut.fx`) with the latest version from GShade: [https://github.com/Mortalitas/GShade/blob/master/Shaders/MultiLUT.fx](https://github.com/Mortalitas/GShade/blob/master/Shaders/MultiLUT.fx)
- Ensure you are using the most up-to-date version of my `MultiLut_Ipsusu.png` file. Replace the one found in your `/game/reshade-shaders/Textures/MultiLut_Ipsusu.png` directory with the one downloaded from [here.](https://github.com/ipsusu/ipsuShade/blob/master/reshade-shaders/Textures/MultiLut_Ipsusu.png)

**If you are using a standalone install of ipsuShade:**
- Update your MultiLUT.fx file (found in `/game/reshade-shaders/Shaders/MultiLut.fx`) with the latest version from the offical repo: [https://github.com/FransBouma/OtisFX/blob/master/Shaders/MultiLUT.fx](https://github.com/FransBouma/OtisFX/blob/master/Shaders/MultiLUT.fx)
- Ensure you are using the most up-to-date version of my `MultiLut_Ipsusu.png` file. Replace the one found in your `/game/reshade-shaders/Textures/MultiLut_Ipsusu.png` directory with the one downloaded from [here.](https://github.com/ipsusu/ipsuShade/blob/master/reshade-shaders/Textures/MultiLut_Ipsusu.png)

### My game is super dark! OR My ReShade keeps getting disabled every time a dialog box opens!

<img width="33%" src="https://i.imgur.com/AD9t6jO.jpeg"></img>

This seems to be an issue with the ReShade installer downloading an old version of the REST (ReshadeEffectShaderToggler) add-on for exclusion of UI filtering, that doesn't play well with the Glamarye Fast Effects shader.

This can be fixed by updating your REST add-on and it's FFXIV specific config. Both the `ReshadeEffectShaderToggler.addon64` and `ReshadeEffectShaderToggler.ini` should be copied into your `/game/` folder. Replace/overwrite.

**Update your REST here:** [https://github.com/4lex4nder/ReshadeEffectShaderToggler/releases/latest/](https://github.com/4lex4nder/ReshadeEffectShaderToggler/releases/latest/)

**Update your REST FFXIV specific config here:** [https://github.com/4lex4nder/ReshadeEffectShaderToggler-FFXIV](https://github.com/4lex4nder/ReshadeEffectShaderToggler-FFXIV)

### Shadows and the shaders of the preset are rendering through the HUD and UI!

<img width="50%" src="https://i.imgur.com/D1icd2T.png"></img>

This issue is caused by ReShade not having a way of detecting the UI and HUD of the game. Therefore, it renders through it. You can fix this by the following methods:

**If you are using ReShade:** You need to use the [REST (ReshadeEffectShaderToggler) add-on](https://github.com/4lex4nder/ReshadeEffectShaderToggler-FFXIV) for exclusion of UI in the filtering. Or, if you are using GPosingway, you can optionally enable both FFKeepUI and FFRestoreUI in the preset instead of using REST. Don't use both at the same time. 

>*Bear in mind, the FFKeepUI shader relies on GShade specific code to function, so it will not work on certain HUD elements in ReShade. This method also requires FXAA to be enabled for the ingame settings, so it is less than ideal. Do use REST if you can.*

**If you are using GShade:** Enable FFKeepUI and FFRestoreUI in the preset. If you want to use [REST](https://github.com/4lex4nder/ReshadeEffectShaderToggler-FFXIV) instead (lets you use an AA method other than FXAA among other benefits, so I recommend it) disable FFKeepUI and FFRestoreUI in the preset. Just put the addon file in your `gshade-addons` folder alongside the specific FFXIV.ini config for it from, the linked repo.

### There are weird unshaded boxes around certain transparencies and particle effects!

<img width="50%" src="https://i.imgur.com/7BgsgWs.jpeg"></img>

This is due to the use of FFKeepUI under ReShade, which is done by default with GPosingway. I don't particularly agree with this choice, due to this very reason. FFKeepUI is a GShade specific shader, and has these issues under ReShade. Instead, REST should be used to stop applying your filters to the base game's HUD and transparencies. 

**To fix this:**

You need to use the [REST (ReshadeEffectShaderToggler) add-on](https://github.com/4lex4nder/ReshadeEffectShaderToggler-FFXIV) for exclusion of UI in the filtering rather than FFKeepUI. Follow the steps in that guide, and download it's recommended version of the REST addon and the FFXIV specific config .ini provided. You need to put both the REST `.addon64` file and it's FFXIV config `.ini` in your FFXIV `/game/` folder. For GShade, you need to put these in your `gshade-addons` folder, which should be in the same location. Ensure you disable the `FFKeepUI` and `FFRestoreUI` shaders in all of your presets after enabling REST.

### There is a checkerboard pattern beneath my glasses or the glasses of an NPC.

<img width="50%" src="https://i.imgur.com/UDXj46b.png"></img>

Along with the graphics updates in Dawntrail, they changed how the rendering worked on certain glass materials. As such, ReShade now will see these as opaque objects, and attempt to render a shadow behind them if any Ambient Occlusion (AO) shaders are enabled. In my presets, these shaders would be the `Fast AO` checkbox under Glamarye Fast Effects, and the entire `iMMERSE: MXAO` shader and the `qUINT MXAO` shader, mainly.

**To fix this:**

Unfortunately, there is no perfect fix to this if you want to keep the AO shaders enabled. There is the possibility of this being fixed via the [REST (ReshadeEffectShaderToggler) add-on](https://github.com/4lex4nder/ReshadeEffectShaderToggler-FFXIV), but I am not smart enough to make this fix myself (I've tried!). DM me if you have experience with REST and want to collaborate on fixing this issue!

**To fix this while disabling AO:** 

Disable the `Fast AO` checkbox under Glamarye and also any MXAO shaders used in the preset to add additional shadows to the game. Bear in mind, this means ReShade will no longer contribute any additonal shadows to your game. You might want to use the `GTAO Quality` Ambient Occlusion setting in-game to somewhat counteract this.
<!--
**To fix this while keeping AO shaders enabled:** 

You need to use the [experimental REST transparency fix](#experimental-rest-transparency-fix) as detailed below in this document. It is a custom config for the REST addon that includes some of the shaders of the preset before the in-game transparencies of the game, by detecting the in-game shaders used and giving that information back to the shader. However, it gives it to the shader in a very raw way that it doesn't expect, so it causes significant flickering issues and black clipping with `iMMERSE MXAO` and causes glitching of black squares when used with the `with_Fake_GI` version of Glamarye. Instead, use the `without_Fake_GI` version. 

If this config is not up-to-date, simply take the default FFXIV config and then ingame edit the "Before Effects" group in the `Add-ons` tab to include any of the AO shaders you use. To do this, just click the checkboxes next to the list of shaders on the first panel of the edit screen. You must click `Save toggle groups` after, otherwise this change will revert once you reset your game.
-->
<!--
Certain people's installations of ReShade are a bit borked because early guides missed important steps and the <a href="https://github.com/eqbot/ReReShade">ReReShade</a> tool had a bug where it didn't bring your textures over from GShade.

Here are a couple of common issues and solutions:

- <b>Some of the shaders in the preset failed to compile! (Glamarye_Fast_Effects.fx and qUINT_ssr.fx)</b>

  <img src="https://i.imgur.com/lqXG2om.png"></img>

  This is an issue with ReShade 5.9.0+ causing incompatibility with older versions these shaders.

  As of `2023-08-09`, I have updated IpsuShade to fix this issue! (IpsuShade v1.0.1)

  The easiest way to fix this issue would to download the appropriate `IpsuShade v1.0.1` zip from the <a href="https://github.com/ipsusu/IpsuShade/releases">IpsuShade releases page</a> and copy and overwrite your current `reshade-shaders`/`gshade-shaders` folder with the new version from the `.zip`. Everything should now properly compile.

  If you want to manually update only the changed files, please download the `Glamarye_Fast_Effects.fx` and `ReShadeUI.fx` shaders from the <a href="https://github.com/ipsusu/IpsuShade/tree/master/Shaders">IpsuShade GitHub Shaders</a> folder and place them in your `reshade-shaders`/`gshade-shaders`, overwriting the old versions. You also need to delete `qUINT_ssr.fx` as this shader from the same folder, as can't be updated in IpsuShade due to licensing and it isn't actually used in any of my presets anyway. Everything should now properly compile.
  
  You can also fix this issue without messing with the shaders by <a href="https://reshade.me/forum/general-discussion/294-reshade-repository">installing ReShade 5.8.0 instead</a> (specifically, with full add-on support).

- <b>My screen is black when I try and load your presets.</b>

    This is due to the MultiLUT shader not being able to find the <a href="https://github.com/ipsusu/IpsuShade/blob/master/Textures/MultiLut_Ipsusu.png">MultiLUT_Ipsusu.png</a> texture file. This is either due to your installation not having a `Texture search path` set in the ReShade settings overlay, or you somehow do not have my texture file in the linked folder.

    **Solution**: Link the `gshade-shaders\Textures` or `reshade-shaders\Textures`  folder under `Texture search paths` in the ReShade overlay while ingame. (if you don't have this folder, it is included in the download in the above step). If you don't have the texture file somehow, it's also included in this download.

- <b>I try and load one of your presets and the colours are all messed up / way brighter than I remember.</b>

    This due to you having multiple copies of certain shaders linked in the `Effect search paths` in the ReShade settings tab of the Overlay.
    This (is probably) caused by doing a "default" install of ReShade which installs some additional shaders, meaning you have `reshade-shaders` with a bunch of subdirectories linked in your ReShade settings. The `OtisFX` pack is most likely causing this issue, as includes a different version of MultiLUT which may break stuff if included alongisde the IpsuShade version (makes stuff look super weird).

    **Solution**: If you have a `gshade-shaders` folder, delete the `reshade-shaders` folder entry under `Effect search paths` in the ReShade overlay while ingame. It would be a good idea to also delete the `reshade-shaders` folder in your XIV `game` folder so you don't get confused and try installing something to it in the future.
    
    If you only have a `reshade-shaders` folder, you might have duplicate shaders in that folder from doing an install with optional shaders. 
    Check to see if you have a `reshade-shaders\Shaders\OtisFX` folder. If so, delete the `OtisFX` folder, or to be safer (but may break compat. with other preset releases), delete the whole `reshade-shaders` folder and replace it with the one included in the `IpsuShade_ReShadeFolderRelease.zip`.
    
    This could also be an issue where if you link `.\reshade-shaders\**` as an `Effect search path`, some users may have an `reshade-shaders\Intermediate` folder which may cause shader duplication issues. Try and use specific folder name links like `.\reshade-shaders\Shaders` to avoid this.

- <b>My XIV HUD job gauges have a weird grey box around them, this didn't happen in GShade!</b> (image below)

    <img src="https://i.imgur.com/tANpywx.png"></img>

    I believe this a bug with ReShade / is occuring due to how GShade had some special code that interfaced with the `FFKeepUI` shader to avoid applying the shader to certain UI elements.

    **This can be solved by either**:
    
     - Turning the HUD element into it's "simple" mode through the ingame HUD Layout settings.
     
     OR
     - Disabling the `FFKeepUI` and `FFRestoreUI` shaders in the preset.
     
     OR
     - Experimental solution: Using the experimental `ReshadeEffectShaderToggler-FFXIV_UIONLY` addon for ReShade: <a href="https://github.com/4lex4nder/ReshadeEffectShaderToggler-FFXIV_UIONLY">Here.</a>
         - Please be sure to read the "IMPORTANT" section on their README or stuff will look very weird. (i.e., changing in-game gamma setting)
         
     OR
     - By using <a href="https://github.com/Mortalitas/GShade/releases/latest">GShade</a> instead of ReShade. (See the disclaimer <a href="#how-do-i-use-the-ipsusu-presets-ipsushade-with-a-gshade-install">here</a> first!)


- <b>The shadows on the Screenie and Ultimate presets are too dark.</b>

    Due to how the GShade and ReShade versions of `qUINT_mxao.fx` are named internally, my preset must enable the file if named simply `MXAO` (the official name) or `qMXAO` (what GShade calls the shader). If you have both `gshade-shaders` and another folder (i.e., `reshade-shaders`) linked in your install with the IpsuShade release of this shader, both versions of this shader will be enabled at once, and as such will apply double the effect of this shader (adding shadows).

    **Solution**: Disable either one of the `MXAO [qUINT_mxao.fx]` or `qMXAO [qUINT_mxao.fx]` found in the shader list of the preset. You should probably also delete the `reshade-shaders` folder entry under `Effect search paths` in the ReShade overlay while ingame. It would be a good idea to also delete the `reshade-shaders` folder in your XIV `game` folder so you don't get confused and try installing something to it in the future.
    
- <b>There is a weird ghost effect of my character and shadows when ReShade/IpsuShade is enabled?</b>

  This is an issue with ReShade not being compatible with the dynamic resolution setting ingame. Please disable this ingame setting if you are having ghosting issues.

    **Solution**: In-game FFXIV Graphics Settings -> Enable dynamic resolution: `Off`
-->
## Required FFXIV in-game graphics settings:

Recommended: 

- [https://github.com/optiscaler/OptiScaler](https://github.com/optiscaler/OptiScaler)

Required:
WIP FOR DAWNTRAIL
<!--
- Enable dynamic resolution: `Off`

- Edge Smoothing (Anti-Aliasing): `FXAA`

- Naturally darken the edges of the screen. (Limb Darkening): `Off`
-->
<!--
## Experimental REST Transparency fix.

Please report to me any issues you have with this!

***Required REST version: [1.3.20](https://github.com/4lex4nder/ReshadeEffectShaderToggler/releases/tag/v1.3.20)***

**Last updated:** 2024-07-13

**Download:** [1.3.20 ReshadeEffectShaderToggler.ini config.](https://gist.github.com/ipsusu/4210da2c0296f48d45dcdb895ee36155)

Example preset to use with the config - Download: [ipsusuQuestingLite - Melon.ini](https://gist.github.com/ipsusu/dca929d0d52a56f16d8b81c6afab0e7b)

**NOTE:**  I've significantly increased the sharpening in the preset to counteract some of the softening caused by DLSS (DLAA, specifically), and also the depth blur and fog that the shaders now render underneath.

if the game looks fucked up to you, turn the "Sharpen Strength" slider down under the "Effects Intensity" tab of the Glamarye settings.

**Known bugs:**
- Seems to be a flickering issue with iMMERSE MXAO. Disabling iMMERSE fixes this.
- There's another issue with Glamarye's Fake GI. Use the Glamarye version without FakeGI to fix this. 
-->
## Donate

You can donate or tip me some lunch money here:

<a href='https://ko-fi.com/ipsusu' target='_blank'><img height='35' style='border:0px;height:46px;' src='https://i.imgur.com/7bleA40.png' border='0' alt='Buy Me a Coffee at ko-fi.com'/></a>


## Contact

You can contact me easiest on my <a href='https://twitter.com/ipsusu'>Twitter</a>. Just send me a DM.

If you don't have Twitter you can find and DM me on Discord @ ipsusu.

I also check my <a href="https://reddit.com/user/ipsusu/">Reddit</a> DMs semi-regularly.

## XIV Materials Usage

FINAL FANTASY is a registered trademark of Square Enix Holdings Co., Ltd.
© SQUARE ENIX CO., LTD. All Rights Reserved.


