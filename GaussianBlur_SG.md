GaussianBlur_SG (only in GaussianBlur+)
-------------------------------------
[GaussianBlur+](http://u3d.as/1wQD)  
[GaussianBlur](http://u3d.as/yJk)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

## Table of Contents

- [GaussianBlur_SG (only in GaussianBlur+)](#gaussianblursg-only-in-gaussianblur)
- [Table of Contents](#table-of-contents)
- [Description Features](#description-features)
- [How To Use GaussianBlur_SG](#how-to-use-gaussianblursg)
    - [Set Up](#set-up)
        - [Use Package Manager](#use-package-manager)
        - [place LWRP_forGaussianBlur in Project Settings](#place-lwrpforgaussianblur-in-project-settings)
        - [Tag Objects with "GaussianBlur" and they will render using this custom shader.](#tag-objects-with-%22gaussianblur%22-and-they-will-render-using-this-custom-shader)
    - [Misc Info](#misc-info)

## Description Features

A GaussianBlur effect for UI Components.

* Adjust Blur, Lightness, Saturation, and TintColor 
* Made using Unity's ShaderGraph
* Compatible with Unity's Scriptable Rendering Pipelines 


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

#### Tag Objects with "GaussianBlur" and they will render using this custom shader.


### Misc Info

1. BlurShader_11x11.shader **Deprecated**
    * this used many shader graph nodes to create the blurred effect, and your computer might freeze on opening it (this will be removed in future versions of the asset) 
2. BlurShader_CN.shader 
    * this uses a custom node in shader graph.




