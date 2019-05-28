 GaussianBlur_Live
-------------------------------------
[GaussianBlur](http://u3d.as/yJk)  
[GaussianBlur+](http://u3d.as/1wQD)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

## Table of Contents

- [GaussianBlur_Live](#gaussianblurlive)
- [Table of Contents](#table-of-contents)
- [Description Features](#description-features)
- [How To Use GaussianBlur_Live](#how-to-use-gaussianblurlive)
  - [Create Material](#create-material)
  - [Use Material](#use-material)
  - [Change Material via Script](#change-material-via-script)
- [Troubleshooting](#troubleshooting)
  - [What is edge smear?](#what-is-edge-smear)
  - [It's Black?](#its-black)
  - [It's Blocky?](#its-blocky)
  - [I've got a ton of Errors!](#ive-got-a-ton-of-errors)


## Description Features

A GaussianBlur_Live effect for UI Components.

* [Layered Blur](https://i.imgur.com/ekGzwvL.png)
* [WorldSpace Rendering](https://i.imgur.com/ZAOf3dy.png)
* Add alpha mask for different shapes!
* Updates Every Frame
* Adjust Blur and Lightness using C# or JS
* Adjust Quality (to use less resources)
* Unity Free friendly.
* Fully commented C# code.
* Awesome demos!
* NOTE: This will not work with Scriptable Render Pipelines (LWRP/HDRP)

## How To Use GaussianBlur_Live

### Create Material
Create a new material, name it as needed.  
Assign the GaussianBlur shader to it.

~~>**WARNING!**  
GaussianBlur\_LiveBlur.shader and GaussianBlur\_LiveBlur\_NoSmear.shader replaced the old versions (GaussianBlurV1 and GaussianBlurV2)~~

![Imgur](http://i.imgur.com/qoy3uyxm.png)

### Use Material
Assign the new material to an image within your canvas.

![Imgur](http://i.imgur.com/XIshcrMm.png)

Note: if you used GaussianBlur_LiveBlur_NoSmear.shader make sure to add SyncCoordinates.cs to the same image in your canvas.

### Change Material via Script
This Shader has 5 properties.  

1. _Color  
 * This is the Tint Color of the shader.
 * For best uses maintain a low alpha.  
2. _BlurSize  
 * Amount of Blur
3. _Lightness  
 * How light/dark the material should be.
4. _Quality  
 * the Quality of the blur.
 * to use less resources


**Examples:**

~~~cs  
//set the color
ScreenBlurLayer.SetColor("_Color",Color.red);
        
//set the BlurSize
ScreenBlurLayer.SetFloat("_BlurSize",30f);
     
//Set the Lightness   
ScreenBlurLayer.SetFloat("_Lightness",0.2f);

//Set the Quality
ScreenBlurLayer.SetFloat("_Quality",4.0f);

~~~
 

Please see the DemoSliderControl.cs script for more information.

For more information about materials please see
https://docs.unity3d.com/ScriptReference/Material.html


## Troubleshooting

### What is edge smear?   
Edge Smear is the name of an issue where objects outside of the UI get smeared in from the edge and effect the blur. 

Edge Smear only occurs if you decided to use the GaussianBlur_LiveBlur.shader.  
![Imgur](http://i.imgur.com/OGPs9vFm.png)

To stop edge smear please use GaussianBlur_LiveBlur_NoSmear.shader.
It doesn't suffer from the Edge Smear, however it needs more information to render properly. (see SyncCoordinates.cs for more info) 

![Imgur](http://i.imgur.com/kwOaR5Gm.png)

### It's Black?
If GaussianBlur_LiveBlur_NoSmear.shader is being used and the values like ScreenWidth, ScreenHeight, PanelWidth, PanelHeight..etc are not correct than the shader might render as black.

### It's Blocky?  
If the Shader seems blocky (like in the image below), increase the Quality value in the shader.

![Imgur](http://i.imgur.com/5xclyZ4m.png)

### I've got a ton of Errors!
The Shaders written in Unity get recompiled into 8 different shaders for each rendering engine. Unfortunately  this shader doesn't work with DirectX9 (D3D9), therefore please disable it in the inspector.

![Imgur](http://i.imgur.com/weoBIhh.png)

If compiling for windows you can choose the graphical API in PlayerSettings
![Imgur](http://i.imgur.com/V909vba.png)

*If need this to work with DirectX9 please let me know, so i can make that more of a priority.*
