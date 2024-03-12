# Entry 4
##### 3/11/24

Context: My next step to create a 3d video game for a frame was to learn how to animate the components I am using. I already learned how to animate the components by knowing how to make them revolve, rotate, and move in different places. Now I took the initiative to learn how to chnage color and scale the components.

Content: First thing I tried for the learning log 8 was to change the color from darkblue to lightblue as the sun comes up. I also use learning log 9 to add a scale to the a-box while changing the color from green to <a href="https://jsbin.com/ricuzunaki/edit?html,output">brown</a>.
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
I will learn how to make aframe more interactive based on what I would like to design on the website.

Sources: Some of the sources I use is <a href="https://aframe.io/docs/1.5.0/components/animation.html">aframe</a> as always. However I was looking at the new aframe version. I also use
<a href="https://stackoverflow.com/questions/69709964/aframe-color-change">stack overview</a> to see someone's example to see how someone changed their color. Which helped me a lot, because I realized that it did not involve javascript. I just had to do <a href="https://jsbin.com/vavuqoluxu/edit?html,output">this</a>.
```html
<a-sky src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQmuKayjQ5MSvKRRPMEvraM8D_H9Jx6tPovcw&usqp=CAU" color="midnightblue"
            animation="property: components.material.material.color;
                       type: color;
                       to: lightblue;
                       dur: 10000;
                       dir: alternate;
                       loop: true"></a-sky>
```
What I did for this code is set my property to components.material.material.color and just type color from midnightblue to lightblue. I also used these <a href="https://www.youtube.com/watch?v=p3mNNZ356Ko">videos</a> to help me animate a scale so that the height can increase.
So this is how I used the animation scale for my <a href="https://jsbin.com/vavuqoluxu/edit?html,output">learning log</a>.
```html
    <a-box color="green" position="-24 0.5 -10" height="15"  depth="1 "width="2"
        animation="property: scale; to: 2 2 2; dur: 5000; dir: alternate; easing: linear; loop: false"
        animation__2="property: position; to: -24 15 -10; dur: 5000; dir: alternate; easing: linear; loop: false"
        animation__color="property: components.material.material.color;
        type: color;
        to: saddlebrown;
        dur: 5000;
        dir: alternate
        loop: false"></a-box>
    <a-camera position="0 5 52"></a-camera>
        <a-sky src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQmuKayjQ5MSvKRRPMEvraM8D_H9Jx6tPovcw&usqp=CAU" color="midnightblue"
            animation="property: components.material.material.color;
                       type: color;
                       to: lightblue;
                       dur: 10000;
                       dir: alternate;
                       loop: true"></a-sky>
    <a-sphere color="green" position="-24 -30 -8" radius="8" animation="property: position; to: -24 30 -10; dur: 5000; easing: linear; dir: alternate; loop: false"></a-sphere>
    <a-plane position="0 0 -4" rotation="-90 0 0" width="300" height="100" repeat="2 1" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR5Rc2LohplON-jQVZpyTN9jxD0O4SwccJ9-g&usqp=CAU"></a-plane>
    <a-camera position="0 5 52"></a-camera>
```
Engineering Design Process: I am currently in the sixth stage of the Engineering Design Process where I am testing the aframe animations I make for learning logs and I also evaluate how they are used for my code and others people code to get an idea on how I can properly execute them being interactive for the users.

Skills: Some of the skills I developed was creativity where I thought about the sky changing when the sun rises in my code and also showed the tree forming into one while branch goes from green to brown. I also used time management by prioritizing my learning log assignment before I do anything else, because I do not want to forget about it. I also love learning about Aframe.

[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)