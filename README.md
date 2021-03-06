

[![Pod version](https://img.shields.io/cocoapods/v/ImageOpenTransition.svg?style=flat)](http://cocoadocs.org/docsets/ImageOpenTransition)

<img src="https://s31.postimg.org/6x43rb7h7/Icon_Image_Scale_Transition_3x.png" alt="ImageOpenTransition Icon" align="center" />


## Description
Beautiful and precise transitions between ViewControllers images written in Swift.

* **Supports multiple images transition**

* **Simply provide the imageView you would like to transition from, and to, and all the rest is free** 

* **No need to dig in transition API for a beautiful transition**

## Demo

<img src="https://media.giphy.com/media/z4Y5tuT7LUISI/giphy.gif" alt="ImageOpenTransition Icon" align="center" />
<img src="https://media.giphy.com/media/P8uMGwNDxsr04/giphy.gif" alt="ImageOpenTransition Icon" align="center" />

## Code



```Swift

let transitionObjectAvatar = ImageScaleTransitionObject(viewToAnimateFrom: cell.imgAvater,
  viewToAnimateTo: vc.imgAvatar,
  duration: 0.4, 
  frameToAnimateTo: frameToAnimateToAvatar)

//Example of explicitly define a final frame:
let transitionObjectCover = ImageScaleTransitionObject(viewToAnimateFrom: cell.imgCover,
  viewToAnimateTo: vc.imgCover,
  duration: 0.4)

self.imageScalePresentTransition = ImageScaleTransitionDelegate(transitionObjects: [transitionObjectCover ,transitionObjectAvatar], 
  usingNavigationController: usingNavigationController, duration: 0.4)
```

## Usage

* Create "ImageScaleTransitionObject" For each image you woould like to animate.
Pass the UIImageView to animate from, and the UIImageView to animate to.


* You must pass the ImageView you would like to animate to. You can or allocate it before the controller is presented,
or call "loadView", it's your choice.

* The frame you would like to animate to, is optional. 
You can use it in cases the UIImageView you would like to animate to, has no frame yet, and you rather calculate it programmatically.

**Use the example project for better reference.

## Supports 

*Story boards/non story-board*
*Translucent/non-translucent*
*NavigationController/ non-navigationController*


## Installation

#### Cocoapods
**ImageScaleTransition** is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'ImageScaleTransition'
```

#### Manually

1. Download and drop All 5 .swift files to your project:

ImageScaleTransitionDelegate.swift, ImageScaleTransitionDismiss.swift, ImageScaleTransitionExntentions.swift, ImageScaleTransitionObject.swift,ImageScaleTransitionPresent.swift.

2. Congratulations!

## Author

[Matan](https://github.com/mcmatan) made this with ❤️.

##License

```
Copyright 2013-2016 Jive Software, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
