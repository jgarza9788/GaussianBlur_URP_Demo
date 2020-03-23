 GaussianBlur_URP
-------------------------------------
[Asset Store Link](http://u3d.as/1wQD)  
[HRP version](http://u3d.as/1EMR)  
[non-ShaderGraph version](http://u3d.as/yJk)  

© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)


## Table of Contents

<!-- TOC -->

- [GaussianBlur_URP](#gaussianblururp)
- [Table of Contents](#table-of-contents)
- [Contact](#contact)
- [Description Features](#description-features)
- [Set Up](#set-up)
- [GaussianBlur_IU](#gaussianbluriu)
- [GaussianBlur_IUEffect](#gaussianbluriueffect)
- [GaussianBlur_WS](#gaussianblurws)
- [Videos](#videos)
- [Terms of Use / License](#terms-of-use--license)

<!-- /TOC -->

## Contact

Questions, suggestions, help needed?  
Contact me at:  
Email: jgarza9788@gmail.com  
Cell: 1-818-251-0647  
Contact Info: [justingarza.info/contact](http://justingarza.info/contact/)  
Alternate Website: [jgarza9788 - UnityPortfolio](https://github.com/jgarza9788/UnityPortfolio)  


## Description Features

* Alpha Mask
* Mobile Friendly
* Adjust Blur, Lightness, Saturation, and TintColor 
* Built on URP
* easily modifiable/editable Shader Graph
* 3 Shaders
    * GaussianBlur_IU
    * GaussianBlur_IUEffect
    * GaussianBlur_WS (WorldSpace, or Objects)

## Set Up
Use the URP_Asset  
it's in ***\GaussianBlur_URP\Assets\URP**

note: this will do several things.
1. Allow us to use _CameraOpaqueTexture (our default texture for blurring)
    1. a custom texture can be used (i.e. a render texture or any 2D texture)
2. Enable Custom rendering for WorldSpaced objects we want blurred.

![Imgur](https://i.imgur.com/B7s0p8Ls.png)

## GaussianBlur_IU
To use the shader on the UI, just use the material.  
(or create you're own material and use my shader)

CustomTexture:  
pass in any texture you'd like (i.e. a Render Texture or 2D Texture)

useCameraOpaqueTexture:  
this will be used as a default texture for blurring.  
note: this will not render transparent objects (you might want to use a Render Texture)

BlurScale:  
This is how much to blur the texture.  
(This will automatically adjust two other variables)

Lightness:  
how light or dark the UI should be.

Tint:  
a color tint to be applied to the UI.

Saturation:  
adjusts the saturation (color) of the UI.

![Imgur](https://i.imgur.com/CPsRJI8s.png)


## GaussianBlur_IUEffect
This will use the Source Image.
So you can fade the blur depending on where it is on the screen.

note:  
edges will be blurred, but less in the center  
![Imgur](https://i.imgur.com/vZ7FJoNs.png)

## GaussianBlur_WS
This is for Objects in the WorldSpace.

note: The Layer should be set to BlurObject.

Metallic & Smoothness:  
these are used to adjust the shinny-ness of the object.  

if this is not working we might want to double check our custom-renderer.
it's in ***\GaussianBlur_URP\Assets\URP**

![Imgur](https://i.imgur.com/X4vxYgks.png)  
![Imgur](https://i.imgur.com/isubyX3s.png)


## Videos
[GaussianBlur_UI](https://youtu.be/v11TBFgPKD)  
[GaussianBlur_WS](https://youtu.be/lwK_AaKw4kc)    
[GaussianBlur_UIEffect](https://youtu.be/2delOzh9Wt8)

## Terms of Use / License 

> Copyright (c) 2018-2020 Justin Garza
> 
> You have the right to use, and modify this code for use in a personal or commercial project, however you do not have the right to re-distribute this source code.
> 
> The above copyright notice and this permission notice shall be included in all
> copies or substantial portions of the Software.
> 
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
> IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
> FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
> AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
> LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
> OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
> SOFTWARE.



