# Entry 1: Deciding on a tool to used for my project.
##### 11/6/23

Context: I decided to have fun and make an Aframe interactive 3D game instead of a vr showcase. My backup tool used to be three.js.org but I decided to use Kaboom.js as a backup instead of three.js.org, because it was not the resource I was looking for. Three.js is used to create and display animated 3D graphics in the browser using WebGL. WebGl is  a JavaScript API for rendering interactive 2D and 3D graphics within any compatible web browser without the use of plug-ins. I tried to use Aframe and three.js. Last week to make sure something happens to the aframe but nothing happened.
<br>
Here are my results for tinkering
![Aframe](image.png)
```html
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>JS Bin</title>
  <script src="https://aframe.io/releases/1.4.0/aframe.min.js"></script>
</head>
<body>
  <a-scene>
      <a-box position="-1 0.5 -3" rotation="0 45 0" color="#4CC3D9"></a-box>
      <a-sphere position="0 1.25 -5" radius="1.25" color="#EF2D5E"></a-sphere>
      <a-cylinder position="1 0.75 -3" radius="0.5" height="1.5" color="#FFC65D"></a-cylinder>
      <a-plane position="0 0 -4" rotation="-90 0 0" width="4" height="4" color="#7BC8A4"></a-plane>
      <a-sky color="#ECECEC"></a-sky>
      <a-entity position="1 2 3"></a-entity>
    </a-scene>
</body>
</html>
```
```js
document.querySelector('a-scene').object3D;
document.querySelector('a-entity').sceneEl.object3D;
console.log(entityEl.object3DMap);
entityEl.getObject3D('mesh');  // THREE.Mesh
entityEl.getObject3D('light');  // THREE.Light
```
As you can see nothing happened. So my main project idea is to create an endless fun 3D game using Aframe that is flappy bird but more challenging where you have to worry about moving pipes and etc, My backup idea for kaboom.js is a challenging platformer game where you have to reach the goal by avoiding traps, bad guys, and cliffs.
<br>
Sources: Some of the sources I discovered while tinkering is <a href="https://threejs.org/">three.js</a>, <a href="https://aframe.io/">Aframe.io</a>, and <a href="https://kaboomjs.com/">kaboom.js</a>.
<br>
Engineering Design Process:

[Next](entry02.md)

[Home](../README.md)