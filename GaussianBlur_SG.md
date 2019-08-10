GaussianBlur_SG (only in GaussianBlur+)
-------------------------------------
[GaussianBlur+](http://u3d.as/1wQD)  
[GaussianBlur](http://u3d.as/yJk)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

## Table of Contents

<!--TOC-->
- [GaussianBlur_SG (only in GaussianBlur+)](#gaussianblursg-only-in-gaussianblur)
- [Table of Contents](#table-of-contents)
- [Description Features](#description-features)
- [Requirements](#requirements)
- [How To Use GaussianBlur_SG](#how-to-use-gaussianblursg)
    - [Set Up](#set-up)
        - [Use Package Manager](#use-package-manager)
        - [place LWRP_forGaussianBlur in Project Settings](#place-lwrpforgaussianblur-in-project-settings)
        - [Add BlurMaterial_SG to objects](#add-blurmaterialsg-to-objects)
        - [Tag Objects with "GaussianBlur"](#tag-objects-with-%22gaussianblur%22)
        - [Video](#video)
    - [Misc Info](#misc-info)
- [Demos](#demos)
    - [Demo_SG.unity](#demosgunity)
    - [Demo_SG_RenderTexture.unity](#demosgrendertextureunity)

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

### Demo_SG.unity
displays the material while using the CameraOpaqueTexture from the LWRP

### Demo_SG_RenderTexture.unity
displays the material while using a RenderTexture from a camera

![Imgur](https://i.imgur.com/4WDOwql.png)

A camera has a target texture set to a RenderedTexture. That RenderedTexture is then used in a Shader Graph Shader to produce the blur effect on the screen.
