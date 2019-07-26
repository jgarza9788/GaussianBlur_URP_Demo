GaussianBlur_SRP (only in GaussianBlur+)
-------------------------------------
[GaussianBlur+](http://u3d.as/1wQD)  
[GaussianBlur](http://u3d.as/yJk)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

## Table of Contents

- [GaussianBlur_SRP (only in GaussianBlur+)](#GaussianBlurSRP-only-in-GaussianBlur)
- [Table of Contents](#Table-of-Contents)
- [Description Features](#Description-Features)
- [How To Use GaussianBlur_SRP](#How-To-Use-GaussianBlurSRP)
    - [Intro](#Intro)
        - [LWRP Asset (aka Pipeline Asset)](#LWRP-Asset-aka-Pipeline-Asset)
        - [GaussianBlur_SRP.shader](#GaussianBlurSRPshader)

## Description Features

A GaussianBlur effect for UI Components.

* Mobile Friendly
* Adjust Blur, Lightness, Saturation, and TintColor using C# or JS
* Add alpha mask for different shapes!
* Unity Free friendly.
* Compatible with Unity's Scriptable Rendering Pipelines


## How To Use GaussianBlur_SRP

### Intro

**GaussianBlur_SRP.shader** will color UI components based on a blurred image of whatever is behind it.

There are Two things that allow this Shader to work.
1. A texture of what is rendered by the camera, this can be obtained using the LWRP Asset.
2. The Shader that will Blur the texture and set the color of the UI Component.


#### LWRP Asset (aka Pipeline Asset)

- [x] Opaque Texture  
this needs to be checked so we can access the camera's texture.

- [ ] Opaque Downsampling (Optional)  
If you're planning to publish to mobile, consider downsampling.  
i.e. switch this to: 2x Bilinear, 4x Box, or 4x Bilinear

![Imgur](https://i.imgur.com/WLDUX1y.png)


#### GaussianBlur_SRP.shader
Use this shader in any material you attach to a UI Object.  
_see DemoBlur.mat as an example_

This Shader has 4 Properties

* _Iterations
  * Blur Amount
* _Lightness
  * Darkness/Lightness
* _Saturation
  * How much Color or Add/Subtract
* _TintColor
  * Color to Tint it by
* _AlphaIsBlurAmount
    * this uses the alpha of the image to control the blur amount.
    * thus allowing you to fade the blur

![Video Demo](https://youtu.be/0SPwN2RAnkE)




