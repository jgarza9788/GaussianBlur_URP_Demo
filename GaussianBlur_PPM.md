GaussianBlur_PPM (only in GaussianBlur+)
-------------------------------------
[GaussianBlur](http://u3d.as/yJk)  
[GaussianBlur+](http://u3d.as/1wQD)   
© 2017 Justin Garza


PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

## Table of Contents

- [GaussianBlur_PPM (only in GaussianBlur+)](#gaussianblurppm-only-in-gaussianblur)
- [Table of Contents](#table-of-contents)
- [Description Features](#description-features)
- [How To Use GaussianBlur_PPM](#how-to-use-gaussianblurppm)
    - [Intro](#intro)
        - [BlurEffect.cs](#blureffectcs)
        - [Postprocessing Layer and Postprocessing Volume](#postprocessing-layer-and-postprocessing-volume)
- [Troubleshooting](#troubleshooting)

  

## Description Features

* Alpha Mask
* Mobile Friendly 
* Adjust Blur, Lightness, Saturation, and TintColor 
* Layered Blur
* WorldSpace
* Uses Unity's Post Processing Method 
* NOTE: This will not work with Scriptable Render Pipelines (LWRP/HDRP)


## How To Use GaussianBlur_PPM

### Intro

a gameObject will be set up with a special #C script that will create a texture that our camera will use to know which pixels it will need to blur.

This is how the demo looks

![Imgur](https://i.imgur.com/fuX6Fj9.png)

#### BlurEffect.cs
Attach this script to objects that you want to be blurred. 

This Script will create a texture where the pixels that should be blurred are more white then the pixels that should not be blurred.

![Imgur](https://i.imgur.com/Hs9cWUN.png)

#### Postprocessing Layer and Postprocessing Volume

Now we need to attach the Post Processing Layer and the Post Processing Volumne to our camera.

Then add the GaussianBlur_PPM to your Post Processing Profile.

![Imgur](https://i.imgur.com/Mvcr3WC.png)

> Note: if you don't have Post Processing installed you can get it from the menu (i.e. Window -> Package Manager -> Post Processing)

## Troubleshooting

This method currently doesn't work in in a Canvas.
