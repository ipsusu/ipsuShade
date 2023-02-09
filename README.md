<p align="center">
  <h1 align="center">IpsuShade.</h1>
  <h3 align="center"> ReShade / GShade presets for Final Fantasy XIV.</p>
<!--- <p align="center">
    <img width="50%" src="https://i.imgur.com/vGikwdM.png">
  </p> ---!>
</p>

<br>


<h1 align="center">  !!! DISCLAIMER - PLEASE READ BEFORE CONTINUING !!! </h1>

<h3 align="center">
At the current time I am unsure about permission to redistribute the Marty Mcfly qUINT shader collection, which is used in my Screenie and Ultimate presets. 
</h3>
<h3 align="center">
While I wait for a response, you must download them from <a href='https://github.com/martymcmodding/qUINT/archive/refs/heads/master.zip' target='_black'>  - HERE - </a> and merge the <code>Shaders</code> folder with the one found inside your <code>reshade-shaders</code> or <code>gshade-shaders</code>. This is explained in the guide below, so you are okay just to follow those steps.  
</h3>
<h4 align="center">
My presets will NOT WORK AS INTENDED if you skip these steps, and certain presets will lack shadows and may look too dark (especially Ultimate Crystal & Vanilla)
</h4>
<br>

## What is IpsuShade?

IpsuShade is a ReShade preset collection that aims to deliver both maximum quality at maximum FPS with the `Gameplay`, `GameplayLite` and `Questing` preset types, but also with high fidelity screenshot preset types such as `Screenie` and `Ultimate`.

<img src="https://i.imgur.com/0h3bTyM.png">

Each preset type comes in a range of 7 included colour variants.
These colours are: 

<img src="https://i.imgur.com/wr2tvRH.png">



<hr>

### Brief ReShade install guide for FFXIV.

1. Click <a href='http://static.reshade.me/#download' target='_blank'>here</a> to download the latest version of ReShade, specifically the `with full add-on support` version. 
    - This is version which allows use of add-ons and an unlocked depth buffer for Depth of Field effects and nice things to do with lighting and shadows.

2. Select the `FINAL FANTASY XIV (ffxiv_dx11.exe)` in the game/application list. 
    - Ensure it's the `ffxiv_dx11.exe` one and not `ffxiv.exe` or `ffxivboot.exe`. 

3. For the rending API step, select `Microsoft DirectX 10/11/12`. 

4. `Skip` the preset installation step, we will do this manually.

5. When it asks you to select effect packages to install, you must click the `Uncheck All` in the top right of the window. 
    - We don't want to install the SweetFX shaders as it causes a conflict with the ones included with my IpsuShade package.
    - If we simply `Skip` this step, it doesn't create the links we need in ReShade to automatically detect the shader files in IpsuShade. 

6. You should now have a working ReShade install for FFXIV. However, it will have no presets or shaders. 
    - Follow the steps below to install IpsuShade!

<hr>

## How do I use the Ipsusu Presets (IpsuShade) on a fresh ReShade install?

<h3 align="center"> <a href='https://raw.githubusercontent.com/ipsusu/IpsuShade/master/IpsuShade_ReShadeFolderRelease.zip' target='_blank'> Click here to download IpsuShade files for a fresh ReShade install. </a> </h3>

1. Download the zip of IpsuShade for ReShade folder names in the link above.
2. While FFXIV is not running, drag and drop the two folders found inside in the `IpsuShade_ReShadeFolderRelease.zip` into your FFXIV installation directory. Be sure to and merge / overwrite the existing `reshade-presets` and `reshade-shaders` folders. 

    - For the Steam version, your directory is most likely: `C:\Program Files (x86)\Steam\steamapps\common\FINAL FANTASY XIV Online\game\`

    - For the Windows version, your directory is most likely: `C:\Program Files (x86)\SquareEnix\FINAL FANTASY XIV - A Realm Reborn\game\`

#### Note. The existing folders should be named `reshade-presets` and `reshade-shaders`. If they are called `gshade-presets` and `gshade-shaders` please read the <a href="https://github.com/ipsusu/IpsuShade#how-do-i-use-the-ipsusu-presets-ipsushade-if-i-migrated-from-a-gshade-install">section below</a> as you have an installation that has been migrated from a GShade install.

3. ***TEMPORARY STEP FROM THE ABOVE  Marty Mcfly qUINT  DISCLAIMER***: Make sure you also install the qUINT shaders from <a href='https://github.com/martymcmodding/qUINT/archive/refs/heads/master.zip' target='_black'>  - HERE - </a> and drag + merge the <code>Shaders</code> folder found inside that .zip download into your <code>reshade-shaders</code> folder. 

4. Once in-game, open the ReShade overlay (by pressing the `Home` key by default) and navigate to the `Ipsusu` folder inside your `reshade-presets` folder.

5. Simply double click any of the `.ini` presets to enable them. See <a href="https://github.com/ipsusu/IpsuShade#what-is-ipsushade">here</a> about an explaination of the presets.
    - Click the two dots at the top (the "..") to go back to the main folder if you would like to swap to another creator's preset (if you have any installed).
 
6. You should now have a perfectly working install of IpsuShade.
<br>

## How do I use the Ipsusu Presets (IpsuShade) if I migrated from a GShade install?

The Ipsusu presets were originally (and, technically currently) included with a GShade install. 

As such, <i>you should already have the presets</i> and you will be able to find them in the `gshade-presets\Ipsusu\` folder!

1. Click the `gshade-presets` folder from your migrated install and scroll down to find the `Ipsusu` folder.

2. Simply double click any of the `.ini` presets to enable them. See <a href="https://github.com/ipsusu/IpsuShade#what-is-ipsushade">here</a> about an explaination of the presets.

    - Click the two dots at the top (the "..") to go back to the main folder if you would like to swap to another creator's preset.

<h3>At the time of writing (2023-02-07), my <code>Screenie</code> and <code>Ultimate</code> presets have been updated from the included GShade release. </h3>

Due to the current state of GShade, you must manually update these by downloading the folder below and overwriting these presets in your `gshade-presets\Ipsusu` folder. You should not need to update the `gshade-shaders` but there is no harm in this as they are the exact same versions as included.

If the guide you followed or program you used to migrate renamed your presets and shader folders from `gshade-xxxxxx` to `reshade-xxxxxx`, use the download in the <a href="https://github.com/ipsusu/IpsuShade#how-do-i-use-the-ipsusu-presets-ipsushade-on-a-fresh-reshade-install">prior section</a>.

If you still have a `gshade-presets` and `gshade-shaders` folder: 

<a href='https://raw.githubusercontent.com/ipsusu/IpsuShade/master/IpsuShade_GShadeFolderRelease.zip' target='_blank'> Click here to download IpsuShade files using the gshade-presets and gshade-shaders folder names. </a>

<br>

## Troubleshooting and Common Issues (especially when migrating from GShade).

Certain people's installations of ReShade are a bit borked because early guides missed important steps and the <a href="https://github.com/eqbot/ReReShade">ReReShade</a> tool had a bug where it didn't bring your textures over from GShade.

Here are a couple of common issues and solutions:

- <b>My screen is black when I try and load your presets!!!</b>

    This is due to the MultiLUT shader not being able to find the <a href="https://github.com/ipsusu/IpsuShade/blob/master/Textures/MultiLut_Ipsusu.png">MultiLUT_Ipsusu.png</a> texture file. This is either due to your installation not having a `Texture search path` set in the ReShade settings overlay, or you somehow do not have my texture file in the linked folder.

    **Solution**: Link the `gshade-shaders\Textures` or `reshade-shaders\Textures`  folder under `Texture search paths` in the ReShade overlay while ingame. (if you don't have this folder, it is included in the download in the above step). If you don't have the texture file somehow, it's also included in this download.

- <b>I try and load one of your presets and the colours are all messed up / way brighter than I remember!!!</b>

    This seems to be exclusively a GShade to ReShade migration issue.
    This (is probably) due to you having multiple copies of certain shaders linked in the `Effect search paths` in the ReShade settings tab of the Overlay.
    This (is probably) caused by doing a "default" install of ReShade which installs the SweetFX shaders meaning you have both `reshade-shaders` and `gshade-shaders` linked in your ReShade settings.
    As such, you're applying 2x the `MultiLUT` shader's colour and it's not enjoying itself.

    **Solution**: If you have a `gshade-shaders` folder, unlink/delete the `reshade-shaders` folder under `Effect search paths` in the ReShade overlay while ingame. It would be a good idea to also delete the `reshade-shaders` folder in your XIV `game` folder so you don't get confused and try installing something to it in the future.
    
    If you only have a `reshade-shaders` folder, you might have duplicate MultiLUT shaders in that folder somehow.

- <b>My XIV HUD job gauges have a weird grey box around them! This didn't happen in GShade!</b> (image below)

    <img src="https://i.imgur.com/tANpywx.png"></img>

    I believe this a bug with ReShade / is occuring due to how GShade had some special code that interfaced with the `FFKeepUI` shader to avoid applying the shader to certain UI elements.

    **This can be solved by either**:
    
     - Turning the HUD element into it's "simple" mode through the ingame HUD Layout settings.
     
     OR
     - Disabling the `FFKeepUI` and `FFRestoreUI` shaders in the preset.


## Donate

You can donate or tip me some lunch money here:

<a href='https://ko-fi.com/ipsusu' target='_blank'><img height='35' style='border:0px;height:46px;' src='https://az743702.vo.msecnd.net/cdn/kofi3.png?v=0' border='0' alt='Buy Me a Coffee at ko-fi.com'/></a>
  
## Contact

You can contact me easiest on my <a href='https://twitter.com/ipsusu'>Twitter</a>. Just send me a DM.

## XIV Materials Usage

FINAL FANTASY is a registered trademark of Square Enix Holdings Co., Ltd.
© SQUARE ENIX CO., LTD. All Rights Reserved.


