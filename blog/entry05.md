# Entry 5
##### 5/1/24

Context: My next step to create a 3d video game for a frame was to learn how to animate the components I am using. I already learned how to animate the components by knowing how to make them revolve, rotate, and move in different places. Now I took the initiative to learn how to add sounds in the aframe website such as music.

Content: First thing I tried for the learning log 12 and 13 is to basically add music in the website. However, I mada a mistake adding music. Before There was no file attached to the <b>IDE</b> and that means no music played. After I added the file in there, the music started playing.
<br>

This is the code I used for the music in aframe for my <a href="https://brucef9965.github.io/sep11-freedom-project/pokemon.html">freedom project</a> so far.
```html

<a-scene>
    <a-camera position="0 0 0">
        <a-cursor></a-cursor>
    </a-camera>
    <a-sky color="gray"></a-sky>
    <a-entity
                geometry="primitive: sphere; radius: 5"
                material="color: red"
                position="0 0 -10"
                change-color="color: purple"
                sound="src: url(champion.mp3); autoplay: true; volume: 3">
    </a-entity>
</a-scene>
```
Now that I know what type of music I wil use, I will basically find an objective for the pokemon game.

Sources: Some of the sources I use is <a href="https://aframe.io/docs/1.5.0/primitives/a-sound.html">aframe</a>. I also looked at this part of <a href="https://aframe.io/docs/1.5.0/components/sound.html">aframe</a> to see more examples of using the sound component while making it to an entity. They are some examples of sounds being used however you can not hear them since they do not have a file for the mp3.
<br>

This code is used for playing sounds on events.
```html
<a-entity cursor position="0 0 -5"></a-entity>

<a-entity id="elmo" geometry="primitive: box" material="src: elmo.png"
ound="src: url(ticklelaugh.mp3); on: click"></a-entity>
```

This code is used for pausing and resuming the sound using javascript.
```js
var entity = document.querySelector('[sound]');
entity.components.sound.stopSound();
entity.components.sound.pauseSound();
entity.components.sound.playSound();
```
Those are the codes I would like to apply in my own website.

Engineering Design Process: I am currently in the seventh stage of the Engineering Design Process where I make improvements on my website when they needed while also working on the game for the freedom project.

Skills: Some of the skills I developed is consideration since pokemon was created by gamefreak and associated with the nintendo. I basically need to come up with my own original idea where I can avoid getting copyrighted by nintendo or gamefreak. Another skill I developed is creativity, because I came up with an objective and a great idea where the user picks a champion pokemon team and then fight the other champion with their pokemon.

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)