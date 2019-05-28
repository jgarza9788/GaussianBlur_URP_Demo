GaussianBlur_CamTransition
-------------------------------------
[GaussianBlur](http://u3d.as/yJk)  
[GaussianBlur+](http://u3d.as/1wQD)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

## Table of Contents

<!-- vscode-markdown-toc -->
- [GaussianBlur_CamTransition](#gaussianblurcamtransition)
- [Table of Contents](#table-of-contents)
- [Description Features](#description-features)
- [How To Use GaussianBlur_CamTransition](#how-to-use-gaussianblurcamtransition)
  - [Intro](#intro)
    - [CamTransition_Controller.cs](#camtransitioncontrollercs)
  - [Additional Info](#additional-info)

<!-- vscode-markdown-toc-config
	numbering=false
	autoSave=true
	/vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc --> 


## Description Features

This uses a modified method used in GaussianBlur_Mobile.
However, two cameras will render two different global textures and a shader will fade between them.

* NOTE: This will not work with Scriptable Render Pipelines (LWRP/HDRP)

## How To Use GaussianBlur_CamTransition

### Intro


#### CamTransition_Controller.cs
this will add BlurRenderer_CamTransition.cs to each camera and control their blurs, and control the transition between them.

![Imgur](https://i.imgur.com/jDsD1SG.png)


### Additional Info
read **CamTransition_Controller.cs**   
& **BlurRenderer_CamTransition.cs**




