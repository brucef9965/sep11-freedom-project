

# Entry 3
##### 2/5/24

Context: My next step to create a 3d video game for a frame was to learn how to animate the components I am using. The animation that can be done to a component is moving something from any direction you like, rotating it, and making dit revolve.


Content: First thing I wanted to try was to create a pacman component that moves back and forth in a small box. At first I was confused why my component did not move back and forth and then I found out why. This code below represents the mistake I made. This caused the <a href="https://jsbin.com/liyizebuto/edit?html,output">component</a> to move to a certain path and go
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
What I realized was that before I was getting help learning how to animate my components by watching a video that teaches you about the different types of animations you can use for the components you used. However since that was not the version that a frame was using, I had to get to the a frame website and look at the animation page to see what I did wrong. It turns out that instead of using <b>direction</b> I just had to type in <b>dir</b>. So this caused <a href="https://jsbin.com/liyizebuto/edit?html,output">pacman</a> to move back and forth.
```html
<a-scene background="color: black">
           <a-box color="midnightblue" position="0 2.5 -10" height="2"  depth="2 "width="30"></a-box>
           <a-box color="midnightblue" position="-14 0.5 -10" height="5"  depth="2 "width="2"></a-box>
           <a-box color="midnightblue" position="14 0.5 -10" height="5"  depth="2 "width="2"></a-box>
           <a-cylinder position="12 0 -10" animation="property: position; to: -12 0 -10; repeat: indefinite; dir: alternate; dur: 2000; easing: linear; loop: true" color="yellow" theta-start="50" theta-length="280" side="double" rotation="10 -90 90"></a-cylinder>
           <a-box color="midnightblue" position="0 -2.5 -10" height="2" depth="2" width="30"></a-box>
</a-scene>
```
Sources: Some of the sources I used to help me with my aframe animation is the <a href="https://aframe.io/docs/1.5.0/components/animation.html">aframe</a> website itself and that <a href="https://www.youtube.com/watch?v=p3mNNZ356Ko">youtube</a> video you saw before. However, I do not really recommend that youtube video I saw, because it shows you code for the old version of aframe and it is pretty much outdated for animation. I do recommend looking at the aframe page since it teaches you about all of the attributes for animation. This website all showed me how to make a component do multiple animations at once. Not only did I learn how to do that, I learned how to make a component revolve and rotate. But first
I decided to try out the multiple animations by adding two more pac man <a href="https://jsbin.com/xufumeyuho/edit?html,output">components</a> in order to see the rotation they move in.
```html
<a-scene background="color: black">
           <a-camera position="0 0 10"></a-camera>
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
After I tinkered more on rotating I got rid of the two pacmans and made the pac man in the center rotate right and left instead of it pointing to the left all the time. This <a href="https://jsbin.com/xufumeyuho/edit?html,output">link</a> will show you what it looks like.
```html
<a-scene background="color: black">
            <a-box color="blue" position="-9 9 -10" height="2"  depth="2" width="12" animation="property: position; to: 1 9  -10; dur: 1000; dir: alternate; easing: linear; loop: true"></a-box>
           <a-box color="blue" position="9 9 -10" height="2"  depth="2" width="12" animation="property: position; to: 19 9  -10; dur: 1000; dir: alternate; easing: linear; loop: true"></a-box>
           <a-box color="blue" position="-14 0.5 -10" height="15"  depth="2 "width="2" animation="property: position; to: -4 0.5  -10; dur: 1000; dir: alternate; easing: linear; loop: true"></a-box>
           <a-box color="blue" position="14 0.5 -10" height="15"  depth="2 "width="2" animation="property: position; to: 24 0.5  -10; dur: 1000; dir: alternate; easing: linear; loop: true"></a-box>
           <a-box color="pink" position="0 9 -10" height="2" depth="2" width="6" animation="property: position; to: 10 9 -10; dur: 1000; dir: alternate; easing: linear; loop: true"></a-box>
           <a-camera position ="0 0 20"></a-camera>
           <a-cylinder color="yellow" position="-12 0 -10" theta-start="130" theta-length="280" side="double" rotation="90 0 0" animation="property: position; to: 22 0  -10; dur: 1000; dir: alternate; easing: linear; loop: true"
           animation__2="property: rotation; loop: true; to: 90 180 0; dur: 1000; easing: linear; dir: alternate"></a-cylinder>
           <a-box color="blue" position="0 -8 -10" height="2"  depth="2 "width="30" animation="property: position; to: 10 -8 -10; dur: 1000; dir: alternate; easing: linear; loop: true"></a-box>
 </a-scene>
```
Now I am going to talk about orbiting the components. This is an example of something revolving around something such as the earth revolving around the sun.
<img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExODkyZ3MzeHNmZHRnbzRnZDlzb3p4bzV0cXhicmsza3Z2MW53dHVuYSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/VGbUTteIsJG4QwCUen/giphy.gif" alt="revolving" style="width:600px;height:600px;">
So I learned while tinkering with my tool that to make a component revolve or orbit something that you need to use this element <b>a-entity</b> then use the properties rotation and then do what you will normally do when making your animation.
This is an example of the <a href="https://jsbin.com/biresotado/edit?html,output">codes</a> used to orbit a component.
```html
<a-entity rotation="0 0 0" animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
       <a-sphere position="5 0 0" color="mediumseagreen"></a-sphere>
</a-entity>
```
As you can see, since the sphere wants to orbit in a 5 meter radius it is assigned to position="5 0 0". However I did something similar but instead I decided to tinker with the components a bit more by making them orbit in different directions by using these <a href="https://jsbin.com/biresotado/edit?html,output">codes</a>.
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
Now that I have told you the past stuff I have been learning about aframe now I will tell you my next step. My next step is to learn how to make components interact with each other using this page on <a href="https://aframe.io/docs/1.5.0/introduction/interactions-and-controllers.html">Aframe</a>.


Engineering Design Process: I am currently in the fourth stage of the engineering design process where I am always planning on how I will learn to create a 3d video game by taking the initiative to learn new things that may require me to know in order to create that 3d video game. However, I am not sure on what type of 3d video game I will want to make yet. I also would like to plan on being in the sixth stage of the engineering design process so that I can test my website to see if the methods I used to effectively work make the components interact with each other using Javascript.


Skills: Some of the skills I developed are <b>problem decomposition</b> and <b>creativity</b>. I used problem decomposition to take the initiative to focus on one topic like animating the components until I feel ready to move on to the next topic that leads to my main subject that requires me to know a lot about the topics that I have learned about. I also use creativity to become original or come up with new ideas that can interest people in this 3d game I plan on making soon.




[Previous](entry02.md) | [Next](entry04.md)


[Home](../README.md)

