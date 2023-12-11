# Entry 2 How I tinkered with Aframe
##### 12/11/23

Context: After choosing my tool for my <b>freedom project</b> I decided to go to the next of making my components. So I have to learn how to make them move. Thankfully Aframe has sources to teach you how to animate. My FP goal for the winter break is learning how to make multiple animations with the components.
<br>
Sources: Some of the sources I used to help me to learn how to animate the components in aframe is this section called <a href = "https://aframe.io/docs/1.4.0/components/animation.html">animation</a>. This showed me an example on how an Aframe animation work such as orbiting a sphere in a 5 meter radius.

[Aframe cylinder example rotating](https://jsbin.com/gevuganiqe/edit?html,output)
```html
<!DOCTYPE html>
<html>
    <head>
        <!-- Required meta tags -->
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet" />
        <link href="style.css" rel="stylesheet" type="text/css" />
        <style>
            /* CSS */

        </style>

        <title>Title</title>
    </head>
    <body>
        <!-- HTML -->
        <a-scene background="color: black">
            <a-entity rotation="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
        <a-sphere position="5 0 0" color="mediumseagreen"></a-sphere>
        </a-entity>
        </a-scene>
        <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
        <!-- <script src="script.js"></script> -->
        <script>

        </script>
    </body>
</html>
```
Now after I saw that example I decided to do my own animation. I did an animation where pac man moved from one position to another position and make it repeat it.
<br>
[My Aframe animation](https://jsbin.com/ripimadoqi/edit?html,output)
```html
<!DOCTYPE html>
<html>
    <head>
        <!-- Required meta tags -->
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet" />
        <link href="style.css" rel="stylesheet" type="text/css" />
        <style>
            /* CSS */

        </style>

        <title>Primitive</title>
    </head>
    <body>
        <!-- HTML -->
        <a-scene background="color: black">
            <a-box color="midnightblue" position="0 2.5 -10" height="2"  depth="2 "width="30"></a-box>
            <a-box color="midnightblue" position="-14 0.5 -10" height="5"  depth="2 "width="2"></a-box>
            <a-box color="midnightblue" position="14 0.5 -10" height="5"  depth="2 "width="2"></a-box>

            <a-cylinder position="12 0 -10" animation="property: position; to: -12 0 -10; repeat: indefinite; direction: alternate; dur: 2000; easing: linear; loop: true" color="yellow" theta-start="50" theta-length="280" side="double" rotation="10 -90 90"></a-cylinder>



            <a-box color="midnightblue" position="0 -2.5 -10" height="2" depth="2" width="30"></a-box>
        </a-scene>
        <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
        <!-- <script src="script.js"></script> -->
        <script>

        </script>
    </body>
</html>
```
Engineering Design Process: I am currently in the fourth stage of engineering design process where I am planning on how will I keep tinkering with Aframe by creating a pac man animation that moves from one place to another place and cause it to repeat over and over again.
<br>
Skills: Some of the skills I developed while doing this blog is <b>creativity</b> and knowing <b>how to read.</b> I used creativity by making the a-cylinder component to look like pacman and created four a-box component and coloring it blue to make it look like a part of a maze. So I used the skill to learn how to read by reading the instructions on Aframe on different ways that I can animate my Aframe code.

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)