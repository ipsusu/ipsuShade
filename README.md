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
At the current time I am unsure about permission to redistribute the Marty Mcfly qUINT shader collection, which is used in my Questing, Screenie and Ultimate presets. 
</h3>
<h3 align="center">
While I wait for a response, you must download them from <a href='https://github.com/martymcmodding/qUINT/archive/refs/heads/master.zip' target='_black'>  - HERE - </a> and merge the <code>Shaders</code> folder with the one found inside your <code>reshade-shaders</code> or <code>gshade-shaders</code> folder after following the appropriate guide below.  
</h3>
<h3 align="center">There is also currently an issue where my Ultimate presets will not enable <code>qUINT_mxao.fx</code> above <code>MXAO 4.0.2 EX.fx</code> due to the shader name of the version in the qUINT .zip being slightly different from the GShade version.</h3>
<h4 align="center">
To fix this: Simply scroll down the list, enable <code>MXAO [qUINT_mxao.fx]</code> and drag it above <code>MXAO [MXAO 4.0.2 EX.fx]</code> (you can also right click and "Move to top" to make this easier).
</h4>
<h3 align="center">
My presets will NOT WORK AS INTENDED if you skip these steps.
</h3>
<br>

## What is IpsuShade?

IpsuShade is a ReShade preset collection that aims to deliver both maximum quality at maximum FPS with the `Gameplay`, `GameplayLite` and `Questing` preset types, but also with high fidelity screenshot preset types such as `Screenie` and `Ultimate`.

<img src="https://i.imgur.com/0h3bTyM.png">

Each preset type comes in a range of 7 included colour types.
These colours are: 

<img src="https://i.imgur.com/wr2tvRH.png">

## How do I use the Ipsusu Presets on a fresh ReShade install?

<h3 align="center"> <a href='https://raw.githubusercontent.com/ipsusu/IpsuShade/master/IpsuShade_ReShadeFolderRelease.zip' target='_blank'> Click here to download IpsuShade files for a fresh ReShade install. </a> </h3>

When installing to a fresh ReShade install, simply drag and drop the folders included in the .zip file downloaded by clicking the link above into your FFXIV installation directory and merge / overwrite the existing `reshade-presets` and `reshade-shaders` folders. 

For the Steam version, this is most likely: `C:\Program Files (x86)\Steam\steamapps\common\FINAL FANTASY XIV Online\game\`

For the Windows version, this is most likely: `C:\Program Files (x86)\SquareEnix\FINAL FANTASY XIV - A Realm Reborn\game\`

### Note: The existing folders should be named `reshade-presets` and `reshade-shaders`. If they are called `gshade-presets` and `gshade-shaders` please read the section below as you have an installation that has been migrated from a GShade install.

<h3> TEMPORARY DISCLAIMER STEP: Make sure you also install the qUINT shaders from <a href='https://github.com/martymcmodding/qUINT/archive/refs/heads/master.zip' target='_black'>  - HERE - </a> and drag + merge the <code>Shaders</code> folder into your <code>reshade-shaders</code> folder </h3>

Once in-game, open the ReShade overlay (by pressing the `Home` key by default) and navigate to the `Ipsusu` folder inside your `reshade-presets` folder.

Simply double click any of the `.ini` presets to enable them. Click the two dots at the top (the "..") to go back to the main folder if you would like to swap to another creator's preset (if you have any installed).

<br>

## How do I use the Ipsusu Presets if I migrated from a GShade install?

The Ipsusu presets were originally (and, technically currently) included with a GShade install. 

As such, <i>you should already have the presets</i> and you will be able to find them in the <b>gshade-presets\Ipsusu\ </b> folder (just scroll down a bit and click the "Ipsusu" folder). Simply double click any of the .ini presets to enable them. 

Click the two dots at the top (the "..") to go back to the main folder if you would like to swap to another creator's preset.

<h3>At the time of writing (2023-02-07), my <code>Screenie</code> and <code>Ultimate</code> presets have been updated from the included GShade release. </h3>

Due to the current state of GShade, you must manually update these by downloading the folder below and overwriting these presets in your `gshade-presets\Ipsusu` folder. You should not need to update the `gshade-shaders` but there is no harm in this as they are the exact same versions as included.  

#### <a href='https://raw.githubusercontent.com/ipsusu/IpsuShade/master/IpsuShade_GShadeFolderRelease.zip' target='_blank'> Click here to download IpsuShade files for a ReShade install migrated from GShade. </a>

<br>

## Common issues when migrating from a GShade install to ReShade.

Certain people's installations of ReShade are a bit borked because early guides missed important steps and the <a href="https://github.com/eqbot/ReReShade">ReReshade</a> tool had a bug where it didn't bring your textures over from GShade.

Here are a couple of common issues and solutions:

- <b>My screen is black when I try and load your presets!!!</b>

This is due to the MultiLUT shader not being able to find the <a href="https://github.com/ipsusu/IpsuShade/blob/master/Textures/MultiLut_Ipsusu.png">MultiLUT_Ipsusu.png</a> texture file. This is either due to your installation not having a `Texture search path` set in the ReShade settings overlay, or you somehow do not have my texture file in the linked folder.

Solution: Link the `gshade-shaders\Textures` or `reshade-shaders\Textures`  folder under `Texture search paths` in the ReShade overlay while ingame. (if you don't have this folder, it is included in the download in the above step). If you don't have the texture file somehow, it's also included in this download.

- <b>I try and load one of your presets and the colours are all messed up / way brighter than I remember!!!</b>

This (is probably) due to you having multiple copies of certain shaders linked in the `Effect search paths` in the ReShade settings tab of the Overlay.
This (is probably) caused by doing a "default" install of ReShade, and having both `reshade-shaders` and `gshade-shaders` linked in your ReShade settings.
As such, you're applying 2x the MultiLUT colour and it's not enjoying itself.

Solution: Unlink/delete the `reshade-shaders` folder under `Effect search paths` in the ReShade overlay while ingame. It would be a good idea to also delete the reshade-shaders folder in your XIV `game` folder so you don't get confused and try installing something to it in the future. 

## Donate

You can donate or tip me some lunch money here:

<a href='https://ko-fi.com/ipsusu' target='_blank'><img height='35' style='border:0px;height:46px;' src='https://az743702.vo.msecnd.net/cdn/kofi3.png?v=0' border='0' alt='Buy Me a Coffee at ko-fi.com'/></a>
  
## Contact

You can contact me easiest on my <a href='https://twitter.com/ipsusu'>Twitter</a>. Just send me a DM.

FINAL FANTASY is a registered trademark of Square Enix Holdings Co., Ltd.
© SQUARE ENIX CO., LTD. All Rights Reserved.


