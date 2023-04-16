<p align="center">
  <h1 align="center">IpsuShade.</h1>
  <h3 align="center"> ReShade / GShade presets for Final Fantasy XIV.</h3>
</p>
<!-- <p align="center"> <img width="50%" src="https://i.imgur.com/vGikwdM.png"> </p> -->

## Table of Contents

- [What is IpsuShade?](#what-is-ipsushade)
- Software Install Guides:
  - [Brief ReShade install guide for FFXIV.](#brief-reshade-install-guide-for-ffxiv)
- Preset/Shader Install Guides:
  - [How do I use the Ipsusu Presets (IpsuShade) on a fresh ReShade install?](#how-do-i-use-the-ipsusu-presets-ipsushade-on-a-fresh-reshade-install)
  - [How do I use the Ipsusu Presets (IpsuShade) if I migrated to ReShade from a GShade install?](#how-do-i-use-the-ipsusu-presets-ipsushade-if-i-migrated-to-reshade-from-a-gshade-install)
  - [How do I use the Ipsusu Presets (IpsuShade) with a GShade install?](#how-do-i-use-the-ipsusu-presets-ipsushade-with-a-gshade-install)
- Settings and Troubleshooting:
  - [Troubleshooting and Common Issues (especially when migrating from GShade).](#troubleshooting-and-common-issues-especially-when-migrating-from-gshade)
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


## What is IpsuShade?

IpsuShade is a ReShade preset collection (with GShade support) that aims to deliver maximum quality at maximum FPS with the `Gameplay`, `GameplayLite` and `Questing` preset types, but also provide high fidelity screenshots with the `Screenie` and `Ultimate` preset types.

<img src="https://i.imgur.com/0h3bTyM.png">

Each preset type comes in a range of 7 included colour variants.
These colours are: 

<img src="https://i.imgur.com/wr2tvRH.png">



<hr>

### Brief ReShade install guide for FFXIV.

1. Click <a href='http://static.reshade.me/#download' target='_blank'>here</a> to download the latest version of ReShade, specifically the `with full add-on support` version. 
    - This is the version which allows use of add-ons and an unlocked depth buffer for Depth of Field effects and improved lighting and shadows.

2. Select `FINAL FANTASY XIV (ffxiv_dx11.exe)` in the game/application list. 
    - Ensure it's `ffxiv_dx11.exe` and not `ffxiv.exe` or `ffxivboot.exe`. 

3. For the rendering API step, select `Microsoft DirectX 10/11/12`. 

4. `Skip` the preset installation step, we will do this manually.

5. When it asks you to select effect packages to install, you must click the `Uncheck All` in the top right of the window. 
    - We don't want to install any additional shaders at this point as it may cause a conflict with the ones included with my IpsuShade package.
    - But, if we simply `Skip` this step, it doesn't create the links we need in ReShade to automatically detect the shader files in IpsuShade. (So, don't do that!)

6. You should now have a working ReShade install for FFXIV. However, it will have no presets or shaders. 
    - Follow the steps below to install IpsuShade!

<hr>

## How do I use the Ipsusu Presets (IpsuShade) on a fresh ReShade install?

<h3 align="center"> <a href='https://raw.githubusercontent.com/ipsusu/IpsuShade/master/IpsuShade_ReShadeFolderRelease.zip' target='_blank'> Click here to download IpsuShade files for a fresh ReShade install. </a> </h3>

1. Download the `.zip` of IpsuShade with ReShade folder names through the link above.
2. Drag and drop the two folders found inside the `IpsuShade_ReShadeFolderRelease.zip` into your FFXIV installation `\game\` directory. Be sure to merge and overwrite the existing `reshade-presets` and `reshade-shaders` folders. 

    - For the Steam version, your directory is most likely: `C:\Program Files (x86)\Steam\steamapps\common\FINAL FANTASY XIV Online\game\`

    - For the Windows version, your directory is most likely: `C:\Program Files (x86)\SquareEnix\FINAL FANTASY XIV - A Realm Reborn\game\`

#### Note. The existing folders should be named `reshade-presets` and `reshade-shaders`. If they are called `gshade-presets` and `gshade-shaders` please read the <a href="https://github.com/ipsusu/IpsuShade#how-do-i-use-the-ipsusu-presets-ipsushade-if-i-migrated-from-a-gshade-install">section below</a> as you have an installation that has been migrated from a GShade install.

<!-- 3. ***TEMPORARY STEP FROM THE ABOVE  Marty Mcfly qUINT  DISCLAIMER***: Make sure you also install the qUINT shaders from <a href='https://github.com/martymcmodding/qUINT/archive/refs/heads/master.zip' target='_black'>  - HERE - </a> and drag + merge the <code>Shaders</code> folder found inside that .zip download into your <code>reshade-shaders</code> folder. -->

3. Once in-game, open the ReShade overlay (by pressing the `Home` key by default) and navigate to the `Ipsusu` folder inside your `reshade-presets` folder.
    - If you dragged the files while the game was still open, you need to press `Reload` on the bottom left of the overlay to get them to show up.

4. Simply double click any of the `.ini` presets to enable them. See <a href="https://github.com/ipsusu/IpsuShade#what-is-ipsushade">here</a> about an explaination of the presets.
    - Click the two dots at the top (the "..") to go back to the main folder if you would like to swap to another creator's preset (if you have any installed).
 
5. You should now have a perfectly working install of IpsuShade.
<br>

## How do I use the Ipsusu Presets (IpsuShade) if I migrated to ReShade from a GShade install?

The Ipsusu presets were originally (and currently) included with a GShade install. 

As such, <i>you should already have the presets</i> and you will be able to find them in the `gshade-presets\Ipsusu\` folder!

1. Click the `gshade-presets` folder from your migrated install and scroll down to find the `Ipsusu` folder.

2. Simply double click any of the `.ini` presets to enable them. See <a href="https://github.com/ipsusu/IpsuShade#what-is-ipsushade">here</a> for an explaination of the presets!

    - Click the two dots at the top (the "..") to go back to the main folder if you would like to swap to another creator's preset.

<h3>If you haven't installed GShade since 2023-02-07, my <code>Screenie</code> and <code>Ultimate</code> presets have been updated from the version included with GShade. </h3>

Due to the status of many GShade installs, you may need to manually update these by downloading the folder below and overwriting these presets in your `gshade-presets\Ipsusu` folder. You should not need to update the `gshade-shaders` but there is no harm in this as they are the exact same versions as included.

If the guide you followed or program you used to migrate renamed your presets and shader folders from `gshade-xxxxxx` to `reshade-xxxxxx`, use the download in the <a href="https://github.com/ipsusu/IpsuShade#how-do-i-use-the-ipsusu-presets-ipsushade-on-a-fresh-reshade-install">prior section</a>.

If you still have a `gshade-presets` and `gshade-shaders` folder: 

<a href='https://raw.githubusercontent.com/ipsusu/IpsuShade/master/IpsuShade_GShadeFolderRelease.zip' target='_blank'> Click here to download IpsuShade files using the gshade-presets and gshade-shaders folder names. </a>

## How do I use the Ipsusu Presets (IpsuShade) with a GShade install?

The Ipsusu presets are included with <a href="https://github.com/Mortalitas/GShade/releases">GShade</a> installs by default through their installer. 

**Disclaimer:**

>GShade is a *closed source* fork of ReShade that includes specific improvements to usability and compatibility with whitelisted games. There was an incident in early Feburary 2023 where a poor decision was made through the inclusion of anti-tampering code that would restart Windows if a specific 3rd-party program was used to trigger functions within the GShade installer to download certain assets independently (in an attempt to bypass a new GShade license agreement for certain textures and shaders). This code was removed after the obvious extremely negative reaction to the restart function from the community, but the reputational damage was already done. Therefore, do use this program at your own judgement. However, I do not want to punish innocent users who may not be able to use ReShade (e.g., Linux and Mac users) or may not have the technical ability to follow the install guides above. I have always held the stance that anyone may use and redistribute my presets or textures (as explained in my <a href="https://github.com/ipsusu/IpsuShade/blob/master/LICENSE.md">license<a>). I encourage my presets to be bundled with any future ReShade forks in the future.

<a href="https://github.com/Mortalitas/GShade/releases/latest">Click here to download the latest release of GShade, which includes IpsuShade by default.</a>

After installation, you will be able to find the Ipsusu presets in the `gshade-presets\Ipsusu\` folder!

1. Click the `gshade-presets` folder if it is not already selected, and scroll down to find the `Ipsusu` folder.

2. Simply double click any of the `.ini` presets to enable them. See <a href="https://github.com/ipsusu/IpsuShade#what-is-ipsushade">here</a> for an explaination of the presets.

    - Click the two dots at the top (the "..") to go back to the main folder if you would like to swap to another creator's preset.

<br>

## Troubleshooting and Common Issues (especially when migrating from GShade).

Certain people's installations of ReShade are a bit borked because early guides missed important steps and the <a href="https://github.com/eqbot/ReReShade">ReReShade</a> tool had a bug where it didn't bring your textures over from GShade.

Here are a couple of common issues and solutions:

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
         - Please be sure to read the "Notes" section on their README or stuff will look very weird. (i.e., changing in-game gamma setting)
         
     OR
     - By using <a href="https://github.com/Mortalitas/GShade/releases/latest">GShade</a> instead of ReShade.


- <b>The shadows on the Screenie and Ultimate presets are too dark.</b>

    Due to how the GShade and ReShade versions of `qUINT_mxao.fx` are named internally, my preset must enable the file if named simply `MXAO` (the official name) or `qMXAO` (what GShade calls the shader). If you have both `gshade-shaders` and another folder (i.e., `reshade-shaders`) linked in your install with the IpsuShade release of this shader, both versions of this shader will be enabled at once, and as such will apply double the effect of this shader (adding shadows).

    **Solution**: Disable either one of the `MXAO [qUINT_mxao.fx]` or `qMXAO [qUINT_mxao.fx]` found in the shader list of the preset. You should probably also delete the `reshade-shaders` folder entry under `Effect search paths` in the ReShade overlay while ingame. It would be a good idea to also delete the `reshade-shaders` folder in your XIV `game` folder so you don't get confused and try installing something to it in the future.
    
- <b>There is a weird ghost effect of my character and shadows when ReShade/IpsuShade is enabled?</b>

  This is an issue with ReShade not being compatible with the dynamic resolution setting ingame. Please disable this ingame setting if you are having ghosting issues.

    **Solution**: In-game FFXIV Graphics Settings -> Enable dynamic resolution: `Off`

## Required FFXIV in-game graphics settings:

- Enable dynamic resolution: `Off`

- Edge Smoothing (Anti-Aliasing): `FXAA`

- Naturally darken the edges of the screen. (Limb Darkening): `Off`

## Donate

You can donate or tip me some lunch money here:

<a href='https://ko-fi.com/ipsusu' target='_blank'><img height='35' style='border:0px;height:46px;' src='https://az743702.vo.msecnd.net/cdn/kofi3.png?v=0' border='0' alt='Buy Me a Coffee at ko-fi.com'/></a>
  
## Contact

You can contact me easiest on my <a href='https://twitter.com/ipsusu'>Twitter</a>. Just send me a DM.

If you don't have Twitter you can find and DM me on Discord. 
 - I'm "ipsusu" in most XIV community servers (not putting my Discord ID here for bot scraping reasons!)

I also check my <a href="https://reddit.com/user/ipsusu/">Reddit</a> DMs semi-regularly.

## XIV Materials Usage

FINAL FANTASY is a registered trademark of Square Enix Holdings Co., Ltd.
© SQUARE ENIX CO., LTD. All Rights Reserved.


