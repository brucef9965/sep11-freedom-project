
# Entry 3
##### 2/5/24

Context: My next step to create a 3d video game for aframe was to learn how to animate the components I am using. The animation that can be done to a component is moving something from any direction you like, rotating it, and make it revolve.

Content: First thing I wanted to try was to create a pacman component that moves back and forth in a small box. At first I was confused why my component did not move back and forth and then I found out why. This code below represents the mistake I made. This caused the <a href="https://jsbin.com/cukonikexo/edit?html,output">component</a> to move to a certain path and go
```html
<html>
    <head>
        <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
    </head>
    <body>
        <a-scene background="color: black">
            <a-box color="midnightblue" position="0 2.5 -10" height="2"  depth="2 "width="30"></a-box>
            <a-box color="midnightblue" position="-14 0.5 -10" height="5"  depth="2 "width="2"></a-box>
            <a-box color="midnightblue" position="14 0.5 -10" height="5"  depth="2 "width="2"></a-box>
            <a-cylinder position="12 0 -10" animation="property: position; to: -12 0 -10; repeat: indefinite; direction: alternate; dur: 2000; easing: linear; loop: true" color="yellow" theta-start="50" theta-length="280" side="double" rotation="10 -90 90"></a-cylinder>
            <a-box color="midnightblue" position="0 -2.5 -10" height="2" depth="2" width="30"></a-box>
        </a-scene>
    </body>
</html>
```
What I realized was that before I was getting help learning how to animate my components by watching this <a href="https://www.youtube.com/watch?v=p3mNNZ356Ko">video</a>. However since that was not the versian that aframe was using, I had to got to the <a href="https://aframe.io/docs/1.5.0/components/animation.html">aframe</a> website and look at the animation page to see what I did wrong. It turns out that instead of using <b>direction</b> I just haded to type in <b>dir</b>. So this caused <a href="https://jsbin.com/cukonikexo/edit?html,output">pacman</a> to move back and forth.
```html
<a-scene background="color: black">
            <a-box color="midnightblue" position="0 2.5 -10" height="2"  depth="2 "width="30"></a-box>
            <a-box color="midnightblue" position="-14 0.5 -10" height="5"  depth="2 "width="2"></a-box>
            <a-box color="midnightblue" position="14 0.5 -10" height="5"  depth="2 "width="2"></a-box>
            <a-cylinder position="12 0 -10" animation="property: position; to: -12 0 -10; repeat: indefinite; dir: alternate; dur: 2000; easing: linear; loop: true" color="yellow" theta-start="50" theta-length="280" side="double" rotation="10 -90 90"></a-cylinder>
            <a-box color="midnightblue" position="0 -2.5 -10" height="2" depth="2" width="30"></a-box>
</a-scene>
```

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)