GaussianBlur_SG (only in GaussianBlur+)
-------------------------------------
[GaussianBlur+](http://u3d.as/1wQD)  
[GaussianBlur](http://u3d.as/yJk)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

## Table of Contents

<!--TOC-->
* [GaussianBlur_SG (only in GaussianBlur+)](#gaussianblur_sg-(only-in-gaussianblur+))
	* [Table of Contents](#table-of-contents)
	* [Description Features](#description-features)
	* [Requirements](#requirements)
	* [How To Use GaussianBlur_SG](#how-to-use-gaussianblur_sg)
		* [Set Up](#set-up)
			* [Use Package Manager](#use-package-manager)
			* [place LWRP_forGaussianBlur in Project Settings](#place-lwrp_forgaussianblur-in-project-settings)
			* [Add BlurMaterial_SG to objects](#add-blurmaterial_sg-to-objects)
			* [Change the Object's Layer to "GaussianBlur"](#change-the-object's-layer-to-"gaussianblur")
			* [Video](#video)
		* [Misc Info](#misc-info)
	* [Demos](#demos)
		* [Demo_SG.unity](#demo_sg.unity)
		* [Demo_SG_RenderTexture.unity](#demo_sg_rendertexture.unity)

<!--TOC-->

## Description Features

A GaussianBlur effect for **GameObjects (meshes)**

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

#### Change the Object's Layer to "GaussianBlur"

#### Video
[youtube video](https://youtu.be/_d0XQOhKUwE)

### Misc Info

In LWRP the camera automatically creates a texture of the scene. Whoever this might not work if you are using transparent shaders in your scene. The solution would be to use a render texture, as an alternative texture in the GaussianBlur_SG_RT.shader.

Please see the Demo_SG_RenderTexture.unity to see it in action.
  
## Demos

### Demo_SG.unity
displays the material while using the CameraOpaqueTexture from the LWRP

### Demo_SG_RenderTexture.unity
displays the material while using a RenderTexture from a camera

![Imgur](https://i.imgur.com/4WDOwql.png)

A camera has a target texture set to a RenderedTexture. That RenderedTexture is then used in a Shader Graph Shader to produce the blur effect on the screen.
