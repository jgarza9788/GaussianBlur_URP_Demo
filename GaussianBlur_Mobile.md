 GaussianBlur_Mobile
-------------------------------------
[GaussianBlur](http://u3d.as/yJk)  
[GaussianBlur+](http://u3d.as/1wQD)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

## Table of Contents


- [GaussianBlur_Mobile](#gaussianblurmobile)
- [Table of Contents](#table-of-contents)
- [Description Features](#description-features)
- [How To Use GaussianBlur_Mobile](#how-to-use-gaussianblurmobile)
  - [Intro](#intro)
  - [Create or Update the Global Texture](#create-or-update-the-global-texture)
  - [Use the Global Texture](#use-the-global-texture)
- [Using Blur in ScreenSpace-Camera Canvas](#using-blur-in-screenspace-camera-canvas)
- [Using Blur for DropShadow/DropGlow](#using-blur-for-dropshadowdropglow)
- [Troubleshooting](#troubleshooting)
  - [Doesn't Do WorldSpace](#doesnt-do-worldspace)
  - [Jumpy Update](#jumpy-update)
  - [Blurring Other UI](#blurring-other-ui)



## Description Features

A GaussianBlur effect for UI Components.

* Mobile Friendly
* Adjust Blur, Lightness, Saturation, and TintColor using C# or JS
* Add alpha mask for different shapes!
* Works in ScreenSpace-Camera Mode 
* DropShadow/DropGlow (Alternate Use)
* Unity Free friendly.
* Fully commented C# code.
* Awesome demos!
* NOTE: This will not work with Scriptable Render Pipelines (LWRP/HDRP)
  
## How To Use GaussianBlur_Mobile

### Intro

**GaussianBlur_Mobile** (folder)  
Contains a Gaussian Blur shader(s), and script(s), that updates global textures when called on.  

Therefore there are two parts:  
1. a Script that creates or updates the global texture.
2. a Shader to use that global texture.


### Create or Update the Global Texture

You can set up the BlurRenderer using the Create() method. (Example below) 
~~~cs
//make sure to use GaussianBlur_Mobile
using GaussianBlur_Mobile;

public BlurRenderer BRM;

void Start()
{
	BR = BlurRenderer.Create();

	////or Add to the camera of your choice 
	//BR = BlurRenderer.Create(ThisCamera);
}

void Update() 
{
	//...

	//change how many Iterations
	BR.Iterations = (int)Iterations.value;

	//change DownRes number
	BR.DownRes = (int)DownRes.value;

	//turn UpdateBlur on or off
	BR.UpdateBlur = UpdateBlur.isOn;

	//change the update rate
	BR.UpdateRate = UpdateRate.value;

	/*NEW*/
	//you can now choose to use the gametime (i.e. deltaTime) or real time (i.e. unscaled time)
	BR.updateUsingGameTime = true

	//...
}

~~~

See **/Assets/GaussianBlur/GaussianBlur_Mobile/Demo/Scripts/DemoSliderControl.cs** for a more complete example.

An alternative method would be to add the BlurRenderer.cs to your main camera.

### Use the Global Texture

To use the global texture a material will be set up.  
One is already set up for the Demo. (i.e. DemoBlur.mat)  

1. You can create a new material by **Assets > Create > Material**  
2. And using the **Custom/GaussianBlur_Mobile** Shader.  
3. And Add this Material to your UI Image.

![Imgur](https://i.imgur.com/5aJb2D4m.png)  

![Imgur](https://i.imgur.com/bpOggyxm.png)

![Imgur](https://i.imgur.com/pB5K7Y4m.png)


## Using Blur in ScreenSpace-Camera Canvas

If you plan to use the blur in a Canvas SpaceSpace-Camera mode, please mimic the set up you'll find in the "Demo_ScreenSpaceCamera" Scene.

>Note: You'll need one Camera to render the blur (everything except for the Canvas and it's children), and another to render everything.

![Imgur](https://i.imgur.com/x3zwRcQ.gif)

## Using Blur for DropShadow/DropGlow

If you plan to use the blur in a Canvas SpaceSpace-Camera mode, please mimic the set up you'll find in the "Demo_DropShadow" or "Demo_DropGlow" Scenes.

>Note: You'll need one Camera to render the blur (All the sprites), and another to render everything.

![Imgur](https://i.imgur.com/I9jWc4Gm.png)
![Imgur](https://i.imgur.com/ZeYsy2am.png)

## Troubleshooting

### Doesn't Do WorldSpace

Sorry, but this method doesn't support WorldSpace canvasses.
*Please let me know if you want this and I will do my best.*

### Jumpy Update

You might want to decrease the UpdateRate, or Lower the DownRes.  

### Blurring Other UI

Blurring other UI can be tricky.
The UI that should be blurred should be in the worldspace.
If this UI is transparent, please use the Sprites-Default material.
_See **Demo_OtherUI.scene** for example_
