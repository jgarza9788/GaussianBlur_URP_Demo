GaussianBlur_SRP (only in GaussianBlur+)
-------------------------------------
[GaussianBlur+](http://u3d.as/1wQD)  
[GaussianBlur](http://u3d.as/yJk)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

## Table of Contents

<!--TOC-->
* [GaussianBlur_SRP (only in GaussianBlur+)](#gaussianblur_srp-(only-in-gaussianblur+))
	* [Table of Contents](#table-of-contents)
	* [Description Features](#description-features)
	* [two shaders](#two-shaders)
		* [GaussianBlur_SRP.shader](#gaussianblur_srp.shader)
			* [LWRP Asset (aka Pipeline Asset)](#lwrp-asset-(aka-pipeline-asset))
		* [GaussianBlur_SRP_RT](#gaussianblur_srp_rt)
			* [Render Texture](#render-texture)
		* [VIDEO](#video)

<!--TOC-->

## Description Features

A GaussianBlur effect for UI Components.

* Mobile Friendly
* Adjust Blur, Lightness, Saturation, and TintColor using C# or JS
* Add alpha mask for different shapes!
* Unity Free friendly.
* Compatible with Unity's Scriptable Rendering Pipelines


## two shaders 

there are two versions of the shader.

### GaussianBlur_SRP.shader
This version will used the CameraOpaqueTexture from the LWRP settings to render the blur 
 
#### LWRP Asset (aka Pipeline Asset)

- [x] Opaque Texture  
this needs to be checked so we can access the camera's texture.

- [ ] Opaque Downsampling (Optional)  
If you're planning to publish to mobile, consider downsampling.  
i.e. switch this to: 2x Bilinear, 4x Box, or 4x Bilinear

![Imgur](https://i.imgur.com/WLDUX1ym.png)


### GaussianBlur_SRP_RT
This version will use a render texture from a second camera to render the blur.

#### Render Texture
Create a second camera and set it's target texture to the render texture.  
Then make sure the material gets this blur to use.

![Imgur](https://i.imgur.com/4WDOwql.png)


### VIDEO
[Video Demo](https://youtu.be/0SPwN2RAnkE)


