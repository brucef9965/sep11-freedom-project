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
* So I want to learn how to animate my 3D model below. So I decided to make a 3d structure where the primitives are moving. Some of these challenges is learning how to animate a certain primitive. I looked at an example of an <b>a-box</b> code being animated to rotate 360 degrees.
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
---
01/22/24: Learning Log 7

* My final step on animating my components is making my component revolve or orbit a specific component.
* I decided to remove the moving box and make pacman become a brown square while the sphere orbits it.
* I used this <a href = "https://www.youtube.com/watch?v=p3mNNZ356Ko&list=PL8MkBHej75fJD-HveDzm4xKrciC5VfYuV&index=14">video</a> to help me animate my components.
* In order for me to learn how a component rotates, I put eight different types of sphere to rotate in a certain path while all of them were together.
```html
<a-scene background="color: black">
            <a-camera position ="0 0 15"></a-camera>

            <a-entity position="0 0 -10" animation="property: rotation; loop: true; to: 360 360 0; dur: 2000; easing: linear">
                <a-sphere position="0 0 -10" color="indigo" radius="2" animation="property: rotation; loop: true; to: 0 0 0; dur: 2000; easing: linear">
                </a-sphere>
            </a-entity>

            <a-entity position="0 0 -10" animation="property: rotation; loop: true; to: -360 360 0; dur: 2000; easing: linear">
                <a-sphere position="0 0 -10" color="indigo" radius="2" animation="property: rotation; loop: true; to: 0 0 0; dur: 2000; easing: linear">
                </a-sphere>
            </a-entity>

            <a-entity position="0 0 -10" animation="property: rotation; loop: true; to: 360 -360 0; dur: 2000; easing: linear">
                <a-sphere position="0 0 -10" color="indigo" radius="2" animation="property: rotation; loop: true; to: 0 0 0; dur: 2000; easing: linear">
                </a-sphere>
            </a-entity>

            <a-entity position="0 0 -10" animation="property: rotation; loop: true; to: -360 -360 0; dur: 2000; easing: linear">
                <a-sphere position="0 0 -10" color="indigo" radius="2" animation="property: rotation; loop: true; to: 0 0 0; dur: 2000; easing: linear">
                </a-sphere>
            </a-entity>

            <a-entity position="0 0 -10" animation="property: rotation; loop: true; to: 0 360 0; dur: 2000; easing: linear">
                <a-sphere position="0 0 -10" color="purple" radius="3" animation="property: rotation; loop: true; to: 0 0 0; dur: 2000; easing: linear">
                </a-sphere>
            </a-entity>

            <a-entity position="0 0 -10" animation="property: rotation; loop: true; to: 0 -360 0; dur: 2000; easing: linear">
                <a-sphere position="0 0 -10" color="purple" radius="3" animation="property: rotation; loop: true; to: 0 0 0; dur: 2000; easing: linear">
                </a-sphere>
            </a-entity>

            <a-entity position="0 0 -10" animation="property: rotation; loop: true; to: -360 0 0; dur: 2000; easing: linear">
                <a-sphere position="0 0 -10" color="purple" radius="3" animation="property: rotation; loop: true; to: 0 0 0; dur: 2000; easing: linear">
                </a-sphere>
            </a-entity>

            <a-entity position="0 0 -10" animation="property: rotation; loop: true; to: 360 0 0; dur: 2000; easing: linear">
                <a-sphere position="0 0 -10" color="purple" radius="3" animation="property: rotation; loop: true; to: 0 0 0; dur: 2000; easing: linear">
                </a-sphere>
            </a-entity>
        </a-scene>
```
---
02/12/24: Learning Log 8

* For the past other learning logs, I have been using a cylinder component shaped like pac man to help me learn how animating my components work.
* I then tested out all the sphere by making them orbit in different directions.
* Now I will attempt to change the color of <a-sky> primitive. The purpose of this is to learn how to use js on aframe and also may be useful to create a 3d game.
* Unfortunately, I was having struggles and difficulties figuring out on how to change colors in Aframe. I tried stuff such as looking at videos like <a href="https://www.youtube.com/watch?v=JDAdQV4YWRc">this</a>. However, I overcame this challenge by finally looking at an example on <a href="https://stackoverflow.com/questions/55777043/how-can-i-animate-change-the-color-of-a-torus-in-a-frame">Slack overview </a>to see the mistake I made and finally saw my <a href="https://jsbin.com/nocereboqe/edit?html,output">progress.</a> This required no javascript.
```html
<a-scene>
        <a-camera position="0 5 52"></a-camera>
        <a-sky src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQmuKayjQ5MSvKRRPMEvraM8D_H9Jx6tPovcw&usqp=CAU" color="midnightblue"
            animation="property: components.material.material.color;
                       type: color;
                       to: lightblue;
                       dur: 10000;
                       dir: alternate;
                       loop: true"></a-sky>
        <a-sphere src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTpL29-azKl8xrOtZoq7oh7oT4oVnJdfdIuqA&usqp=CAU" position="0 -50 -30" radius="9" animation="property: position; to: 0 60 -30; dur: 10000; easing: linear; dir: alternate; loop: true"></a-sphere>

        <a-plane position="0 0 -4" rotation="-90 0 0" width="300" height="100" repeat="2 1" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR5Rc2LohplON-jQVZpyTN9jxD0O4SwccJ9-g&usqp=CAU"></a-plane>
    </a-scene>
```
---
03/04/24: Learning Log 9

* Well I finally did, I learned how to animate the <b>primitives</b> such as <b>a-box</b> and <b>a-sky</b>. 
* First I tried <a href="https://jsbin.com/fayuvewuso/edit?html,output">moving</a> the box from one place to another such as right, left, up , and down.
* Then I <a href="https://jsbin.com/fayuvewuso/edit?html,output">rotated</a> the box, while making the primitive revolve also as well.
* I finally created an <a href="https://jsbin.com/fayuvewuso/edit?html,output">a-scene</a> that shows that the <b>a-sky</b> primitive changing color from lightblue to darkblue.
* Now I plan on animating a scale using an <b>a-box</b>. This is what I did, I used an <b>a-box</b> to scale the primitive to see the size of the primitive increase by  height, width, and depth one time. 
This is the <a href="https://jsbin.com/?html,output">codes</a> below of me animating using a scale. 
```html
<a-scene>
        <a-camera position="0 5 52"></a-camera>
        <a-sky src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQmuKayjQ5MSvKRRPMEvraM8D_H9Jx6tPovcw&usqp=CAU" color="midnightblue"
            animation="property: components.material.material.color;
                       type: color;
                       to: lightblue;
                       dur: 10000;
                       dir: alternate;
                       loop: true"></a-sky>
        <a-sphere src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTpL29-azKl8xrOtZoq7oh7oT4oVnJdfdIuqA&usqp=CAU" position="0 -50 -30" radius="10" animation="property: position; to: 0 140 -140; dur: 10000; easing: linear; dir: alternate; loop: true"></a-sphere>

        <a-box color="green" position="-24 0.5 -10" height="15"  depth="1 "width="2"
        animation="property: scale; to: 2 2 2; dur: 5000; dir: alternate; easing: linear; loop: false"
        animation__2="property: position; to: -24 15 -10; dur: 5000; dir: alternate; easing: linear; loop: false"
        animation__color="property: components.material.material.color;
        type: color;
        to: saddlebrown;
        dur: 5000;
        dir: alternate
        loop: false"></a-box>

        <a-box color="green" position="24 0.5 -10" height="15"  depth="1 "width="2"
        animation="property: scale; to: 2 2 2; dur: 5000; dir: alternate; easing: linear; loop: false"
        animation__2="property: position; to: 24 15 -10; dur: 5000; dir: alternate; easing: linear; loop: false"
        animation__color="property: components.material.material.color;
        type: color;
        to: saddlebrown;
        dur: 5000;
        dir: alternate;
        loop: false"></a-box>
        <a-sphere color="green" position="24 -30 -8" radius="8" animation="property: position; to: 24 30 -10; dur: 5000; easing: linear; dir: alternate; loop: false"></a-sphere>
        <a-sphere color="green" position="-24 -30 -8" radius="8" animation="property: position; to: -24 30 -10; dur: 5000; easing: linear; dir: alternate; loop: false"></a-sphere>
        <a-plane position="0 0 -4" rotation="-90 0 0" width="300" height="100" repeat="2 1" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR5Rc2LohplON-jQVZpyTN9jxD0O4SwccJ9-g&usqp=CAU"></a-plane>
    </a-scene>
```
03/18/24: Learning Log 10

* Javascript and DOM are often used for Aframe websites and projects.

* I found a basic <b>Aframe</b> javascript setup.
```html
<a-scene log="Hello, Scene!">
  <a-box log="Hello, Box!"></a-box>
</a-scene>
```
```js
AFRAME.registerComponent('log', {
  schema: {type: 'string'},

  init: function () {
    var stringToLog = this.data;
    console.log(stringToLog);
  }
});
``` 
* This code shows console log component being registered before <b>a-scene</b> and applying it to the HTML components from Aframe.

* So I decide to learn how to make a component while using javascript.
* This is the code I used and tinkered with.
```html
<a-scene>
              <a-box color="#EF2D5E" position="0 1 -4" change-color-on-hover="color: blue"></a-box>

              <a-camera><a-cursor></a-cursor></a-camera>
            </a-scene>

        <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
        <!-- <script src="script.js"></script> -->
        <script>
            // JS
            AFRAME.registerComponent('change-color-on-hover', {
    schema: {
      color: {default: 'red'}
    },

    init: function () {
      var data = this.data;
      var el = this.el;  // <a-box>
      var defaultColor = el.getAttribute('material').color;

      el.addEventListener('mouseenter', function () {
        el.setAttribute('color', data.color);
      });

      el.addEventListener('mouseleave', function () {
        el.setAttribute('color', defaultColor);
      });
    }
  });
```
* So basically the above is about the mouse with a circle that can be controlled and everytime it touches the box it changes color.
---

03/25/34 Learning Log 11

* It turns out the Javascript examples is still confusing. So I decided to learn more about entities and how to use them. 

* This is an example on how we can make a square using the entity component.
```html
  <a-scene>
              <a-camera position="0 0 5"></a-camera>
              <a-entity geometry="primitive: box" material="color: red">
  </a-scene>
```
* You can use <b>geometry</b> and add primitive to get any shape you like such as sphere and cone.
```html
            <a-scene>
                <a-camera position="0 0 5">
                    <a-cursor></a-cursor>
                </a-camera>
                <a-entity position="-2 0 0" geometry="primitive: sphere" material="color: red">
                <a-entity position="2 0 0" geometry="primitive: box" material="color: orangered">
                <a-entity position="2 0 0" geometry="primitive: octahedron" material="color: orange">
            </a-scene>
```

* However I decided to create an a-scene where the animation involves an event.
```html
<a-scene>

            <a-entity look-controls cursor="rayOrigin: mouse"></a-entity>

            <a-box position="-1 0.5 -3" rotation="0 45 0" color="#4CC3D9" shadow
                   event-set__enter="_event: mouseenter; color: #026fc9"
                   animation="property: rotation;
                     pauseEvents: mouseenter;
                     resumeEvents: mouseleave;
                     dur: 1000;
                     fill: forwards;
                     to: 0 360 0;
                     dir: alternate;
                     loop: true"
                   event-set__leave="_event: mouseleave; color: #4CC3D9">
            </a-box>

            

            <a-plane position="0 0 -4" rotation="-90 0 0" width="4" height="4" color="#7BC8A4" shadow></a-plane>
            <a-sky color="#ECECEC"></a-sky>
          </a-scene>
```
---

04/8/24: Learning Log 12

* I learned how to make aframe interact with the mouse with it by changing colors, and now I must learn how to use aframe with keyboards.

* I notice that the keyboard will involve this primitive <b>a-camera</b>.

* I was having difficulties with the keys for Aframe so I instead decided to do sound.

* This is how an <b>a-sound</a> is used.

```html
<a-scene>
  <a-sound src="src: url(click.mp3)" autoplay="true" position="0 2 5"></a-sound>
</a-scene>
```

* This is the code I used to make a sound with music.

```html
<!DOCTYPE html>
<html>
    <head>
        <!-- Required meta tags -->
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
        <script src="https://unpkg.com/aframe-event-set-component@^4.0.0/dist/aframe-event-set-component.min.js"></script>
        <script src="//cdn.rawgit.com/donmccurdy/aframe-physics-system/v4.0.1/dist/aframe-physics-system.min.js"></script>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet" />
        <link href="style.css" rel="stylesheet" type="text/css"/>
        <style>
            /* CSS */

        </style>

        <title>Pokemon</title>
    </head>
    <body>
        <!-- HTML -->

        <a-scene>
            <a-camera position="0 0 0">
                <a-cursor></a-cursor>
            </a-camera>
                <a-sky color="gray"></a-sky>
            <a-sphere
                    radius="5"
                    material="color: red"
                    position="0 0 -10"
                    change-color="color: purple">
            </a-sphere>

            <a-assets>
                <a-audio id="cynthia" src="https://epsilon.vgmsite.com/soundtracks/pokemon-diamond-and-pearl-super-music-collection/agmpuios/2-67%20Battle%21%20Champion.mp3" preload="auto"></a-audio>
            </a-assets>

            <a-entity sound="src: #cynthia"></a-entity>

        </a-scene>

        <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
        <!-- <script src="script.js"></script> -->
        <script>
            // JS
            AFRAME.registerComponent('change-color', {
                schema: {
                    color: {default: 'red'}
                },

                init: function () {
                    var data = this.data;
                    var el = this.el;  // <a-box>
                    var defaultColor = el.getAttribute('material').color;

                    el.addEventListener('mouseenter', function () {
                        el.setAttribute('color', data.color);
                    });

                    el.addEventListener('mouseleave', function () {
                        el.setAttribute('color', defaultColor);
                    });
                }
            });



        </script>
    </body>
</html>
```