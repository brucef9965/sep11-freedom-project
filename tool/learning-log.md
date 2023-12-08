# Tool Learning Log

Tool: Aframe

Project: A 3d video game

---

10/23/23: Learning Log 1
 
* I used <a href = "https://aframe.io/">Aframe</a> and <a href = "https://threejs.org/">Three.js</a>
* I used an aframe code, put it to jsbin, and then replace the shapes with a stick figure.
* I have no challenges for now.
* I don't have any questions yet.
* I will try to tinker with a code on three.js
---
12/4/23: Learning Log 3

* This the basic code in order for your aframe project to work.
```html
<html>
    <head>
        <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
    </head>
</html>
```
* So I want to learn how to animate my 3D model below. So I decided to make a 3d structure where the primitives are moving. Some of these challenges is learning how to animate a certain primitive. I looked at an example of an <a-box></a-box> code being animated to rotate 360 degrees.
```html
<a-entity rotation="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
        <a-sphere position="5 0 0" color="mediumseagreen"></a-sphere>
</a-entity>
```
* So I decided to create a component that moves back and returns into it's original position on repeat.
```html
<a-scene background="color: black">
            <a-box color="midnightblue" position="0 2.5 -10" height="2"  depth="2 "width="30"></a-box>
            <a-box color="midnightblue" position="-14 0.5 -10" height="5"  depth="2 "width="2"></a-box>
            <a-box color="midnightblue" position="14 0.5 -10" height="5"  depth="2 "width="2"></a-box>
            <a-cylinder position="12 0 -10" animation="property: position; to: -12 0 -10; repeat: indefinite; direction: alternate; dur: 2000; easing: linear; loop: true" color="yellow" theta-start="50" theta-length="280" side="double" rotation="10 -90 90"></a-cylinder>
            <a-box color="midnightblue" position="0 -2.5 -10" height="2" depth="2" width="30"></a-box>
        </a-scene>
```

