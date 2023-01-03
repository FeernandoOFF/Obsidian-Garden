---
draft: false
title: Three.js
type: note
publishDate: 02-01-2023
lang: en
tags:
- PreMoc/JavaScript
---

# Three.js

## What is Threejs?
Is a library wrapper to joining 3D graphics in the browser with WebGL
- Geometry
- Material
- Lights
- Camera

Animation
- Loop
- Scrollbar
- GSAP
No create complex models use [[Blender]] instead

## Alternatives?

## The library

To start **displaying things** in the document, we need **three** things: [[#Scene]] which will be the **container** for all the items of out composition, a [[#Camera]] which will be the user POV and a [[#Renderer]] which will **mount**  the scene into an [[HTML#Element]].

#### Scene
- Create Scene
##### Adding things to the scene
`scene.add()`


#### Camera
Types of camera
- `PerspectiveCamera`
	- **FieldOfView**: No more than 50
	- AspectRatio: 
- `Orthographic`

Methods:
- aspect
- updateProejctionMatrix

#### Renderer
`WebGLRenderer(canvas)`
`setSize(width,height)`
`render(scene,camera)`
`setPixelRatio(number)`

#### Controls
`orbitControls(camera,canvas)`

`enableDamping = bool ` -> Smooth movement
`enablePan = bool` -> Movement
`enableZoom = bool` -> Zoom
`autoRotate = bool` -> Autorotation
`update()` -> in the main loop


### Helpers
Up to this point is possible that you need some kind of help or guide to know what is happening in your 3D scene, here you can use
#### PointLightHelper
#### GridHelper
#### [[#Controls]]

---
#### Geometry

Technically the geometry is the **set of vectors** that compose a object; it doesn't have a texture nor reflection. 
In summary; **It is the Shape of an object**.

#### Material
Is the material and it includes things like **light interactions** - Wrapping paper
- `MeshBasicMaterial` -> **No** light interaction
- `MeshStandardMaterial` -> Light interaction


#### Mesh
Is the combination of [[#Geometry]] and a [[#Material]]

#### Light
The light source, can be **more than one** and must be **added to the scene**
- `PointLight(color,intensity,distance)`
##### Moving the lights in the environment

You can move a light by calling the function `light.position.set(x,y,z)`

### ETC

#### Texture loader
```js
const bgtexture = Three.TextureLoader().load('pathtoyourpng/jpg')
scene.background = bgtexture
```


### RequestAnimationFrame
Tells the browser that you want to perform an animation whenever the browser repaints the screen it'll call the function that you passed - game loop

``

## References
