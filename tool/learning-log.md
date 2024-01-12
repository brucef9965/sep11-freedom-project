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
* So I decided to create a component that moves back and forth from one place to another.
```html
<a-scene background="color: black">
            <a-box color="midnightblue" position="0 2.5 -10" height="2"  depth="2 "width="30"></a-box>
            <a-box color="midnightblue" position="-14 0.5 -10" height="5"  depth="2 "width="2"></a-box>
            <a-box color="midnightblue" position="14 0.5 -10" height="5"  depth="2 "width="2"></a-box>
            <a-cylinder position="12 0 -10" animation="property: position; to: -12 0 -10; repeat: indefinite; dir: alternate; dur: 2000; easing: linear; loop: true" color="yellow" theta-start="50" theta-length="280" side="double" rotation="10 -90 90"></a-cylinder>
            <a-box color="midnightblue" position="0 -2.5 -10" height="2" depth="2" width="30"></a-box>
        </a-scene>
```
---
12/18/23: Learning Log 5

* Since I learned how to animate my model I decided to get the same pac man component to do multiple animations. Now this is the code I tried. This code shows the difference between the duration of the pac man components while showing the direction of where it spins.
```html
<a-scene background="color: black">
            <a-box color="blue" position="0 9 -10" height="2"  depth="2" width="30"></a-box>
            <a-box color="blue" position="-14 0.5 -10" height="15"  depth="2 "width="2"></a-box>
            <a-box color="blue" position="14 0.5 -10" height="15"  depth="2 "width="2"></a-box>
            <a-box color="pink" position="0 9 -10" height="2" depth="2" width="6"></a-box>
            <a-cylinder color="yellow" position="-12 6 -10" theta-start="130" theta-length="280" side="double" rotation="90 0 0" animation="property: position; to: 12 6 -10; dur: 1000; dir: alternate; easing: linear; loop: true"
            animation__2="property: rotation; loop: true; to: 360 0 0 dur: 1000; easing: linear; dir: alternate"></a-cylinder>
            <a-cylinder color="yellow" position="-12 0 -10" theta-start="130" theta-length="280" side="double" rotation="90 0 0" animation="property: position; to: 12 0 -10; dur: 2000; dir: alternate; easing: linear; loop: true"
            animation__2="property: rotation; loop: true; to: 0 360 0 dur: 2000; easing: linear; dir: alternate"></a-cylinder>
            <a-cylinder color="yellow" position="-12 -5 -10" theta-start="130" theta-length="280" side="double" rotation="90 0 0" animation="property: position; to: 12 -5 -10; dur: 3000; dir: alternate; easing: linear; loop: true"
            animation__2="property: rotation; loop: true; to: 0 0 360 dur: 3000; easing: linear; dir: alternate"></a-cylinder>
            <a-box color="blue" position="0 -8 -10" height="2"  depth="2 "width="30"></a-box>
        </a-scene>
``` 
---
01/11/24: Learning Log 6

* Now I am going to figure out how to rotate my pacman position from right to left.
* I tried to create an orbiting cone while moving from right to left but that did not work.
* So instead I decided to make the maze move while having pac man still in the moving box.
```html
<a-scene background="color: black">
            <a-box color="blue" position="-9 9 -10" height="2"  depth="2" width="12" animation="property: position; to: 1 9  -10; dur: 1000; dir: alternate; easing: linear; loop: true"></a-box>
            <a-box color="blue" position="9 9 -10" height="2"  depth="2" width="12" animation="property: position; to: 19 9  -10; dur: 1000; dir: alternate; easing: linear; loop: true"></a-box>
            <a-box color="blue" position="-14 0.5 -10" height="15"  depth="2 "width="2" animation="property: position; to: -4 0.5  -10; dur: 1000; dir: alternate; easing: linear; loop: true"></a-box>
            <a-box color="blue" position="14 0.5 -10" height="15"  depth="2 "width="2" animation="property: position; to: 24 0.5  -10; dur: 1000; dir: alternate; easing: linear; loop: true"></a-box>
            <a-box color="pink" position="0 9 -10" height="2" depth="2" width="6" animation="property: position; to: 10 9 -10; dur: 1000; dir: alternate; easing: linear; loop: true"></a-box>
            <a-camera position ="0 0 20"></a-camera>
            <a-cylinder color="yellow" position="-10 0 -10" theta-start="130" theta-length="280" side="double" rotation="90 0 0" animation="property: position; to: 22 0  -10; dur: 1000; dir: alternate; easing: linear; loop: true"
            animation__2="property: rotation; loop: true; to: 90 180 0; dur: 1000; easing: linear; dir: alternate"></a-cylinder>
            <a-box color="blue" position="0 -8 -10" height="2"  depth="2 "width="30" animation="property: position; to: 10 -8 -10; dur: 1000; dir: alternate; easing: linear; loop: true"></a-box>
        </a-scene>
```