GaussianBlur_SG (only in GaussianBlur+)
-------------------------------------
[GaussianBlur+](http://u3d.as/1wQD)  
[GaussianBlur](http://u3d.as/yJk)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

## Table of Contents

<!--TOC-->
- [GaussianBlur_SG (only in GaussianBlur+)](#GaussianBlurSG-only-in-GaussianBlur)
- [Table of Contents](#Table-of-Contents)
- [Description Features](#Description-Features)
- [Requirements](#Requirements)
- [How To Use GaussianBlur_SG](#How-To-Use-GaussianBlurSG)
    - [Set Up](#Set-Up)
        - [Use Package Manager](#Use-Package-Manager)
        - [place LWRP_forGaussianBlur in Project Settings](#place-LWRPforGaussianBlur-in-Project-Settings)
        - [Add BlurMaterial_SG to objects](#Add-BlurMaterialSG-to-objects)
        - [Tag Objects with "GaussianBlur"](#Tag-Objects-with-%22GaussianBlur%22)
        - [Video](#Video)
    - [Misc Info](#Misc-Info)
- [Demos](#Demos)

<!--TOC-->

## Description Features

A GaussianBlur effect for UI Components.

* Adjust Blur, Lightness, Saturation, and TintColor 
* Made using Unity's ShaderGraph
* Compatible with Unity's Scriptable Rendering Pipelines 


## Requirements

Below are the list of packages i'm using.  
Using the exact version is recommended, but might not be required.

* Unity 2019.1.4
* Core RP Library 5.13.0
* Lightweight RP 5.13.0
* Shader Graph 5.13.0


## How To Use GaussianBlur_SG

### Set Up

#### Use Package Manager
Use the package manager to obtain 
* Lightweight RP
* Shader Graph

![Imgur](https://i.imgur.com/gJp0iWZm.png)

#### place LWRP_forGaussianBlur in Project Settings
This will tell the project how to render our project  
![Imgur](https://i.imgur.com/0V4h0xAm.png)

**note that LWRP_forGaussianBlur has some custom data.**
LWRP_GaussianBlurredObjects contains instructions on how to blur the objects.  
Therefore, if you decide to merge this asset with other custom renderers we'll need to change this.  

![Imgur](https://i.imgur.com/dRybf88m.png)

#### Add BlurMaterial_SG to objects

#### Tag Objects with "GaussianBlur"

#### Video
[youtube video](https://youtu.be/_d0XQOhKUwE)

### Misc Info

1. BlurShader_CN.shader 
    * this uses a custom node in shader graph.
2. BlurShaderAltTexture_CN.shader 
    * this will render a blur using a renderedTexture (updated by a camera)
  
## Demos

1. Demo_SG.unity
    * displays the material while using the CameraOpaqueTexture
2. Demo_SG_RenderTexture.unity
   * displays the material while using a RenderTexture from a camera

