---
title: "Flappy Ghost"
date: 2018-04-17
tags: [Projects, Android, Development]
draft: false
showthedate: true
---

In my series of games you can't lose, I modified a version of <a href="https://en.wikipedia.org/wiki/Flappy_Bird" target="`_blank`">Flappy Bird</a> and made it so you can't lose.  

This is an overview of the funnest parts of the project for me.  If  you want to see the details, review my code on github: <a href="https://github.com/jjerome00/FlappyGhost" target="`_blank`"> `https://github.com/jjerome00/FlappyGhost`</a>

<iframe width="560" height="315" src="https://www.youtube.com/embed/gMiZGcjPErI?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
<br />

I started with a clone of Flappy Bird called <a href="https://github.com/cubei/FlappyCow" target="`_blank`">Flappy Cow</a>, written by Lars Harmsen. I have never met Lars, but he seems to be a very talented developer.

His clone has a different theme than the original <a href="https://en.wikipedia.org/wiki/Flappy_Bird" target="`_blank`">Flappy Bird</a>. He uses trees and spiders for the obstacles, and a cow instead of a bird.  You could also die.  I had to change all these things.

## Sprite sheet

My first order of business was to make the clone look more like the original game.  This meant tracking down a lot of the artwork from the original game.  I also got to play around with a sprite sheet.

The cow shown on the screen is using what's called a sprite sheet.  A sprite sheet is one big image that contains all the movements of a character.  This way you only need to use one file for all your character's movements.  It's easier to deal with.

I constructed my own sprite sheet for the bird using the same pattern in the sheet to make the bird's wings flap.  It involved lots of fun with <a href="https://www.gimp.org/" target="`_blank`">Gimp</a>.  

<table cellpadding="0" cellspacing="0" align="center">
  <tbody>
    <tr>
      <td style="text-align: center;">
        <a href="/images/blog/flappy-ghost/FlappyGhost-bird-spritesheet.png" imageanchor="1" style="clear: left; margin-bottom: 1em; margin-left: auto; margin-right: auto;"><img border="0"  src="/images/blog/flappy-ghost/FlappyGhost-bird-spritesheet.png" /></a>
      </td>
    </tr>
    <tr>
      <td style="text-align: center;">Lining up the birds.  Notice the wings moving from top to bottom.</td>
    </tr>
  </tbody>
</table>

## Death becomes her

There are a few ways you could die in the game:   

**Touching the sky**   
A side effect of not being able to die is that the bird can fly off the screen.  You continue flying higher and higher without any repercussions.

I fixed this by modifying the collision checking and touch events.  If you touched the top of the screen, that meant you were tapping too much. So I ignore the next tap.  This gives the bird enough time to drop from the sky to avoid going off screen.

**Touching the ground**   
When the game detects a collision with the ground, I add an extra tap to keep the bird from ever touching the ground.

**Running into a pipe**   
When the bird runs into a pipe, I thought it would be funny to have the bird change into a ghost.  It would glide right through the pipe as if it wasn't there.  That's where the "Flappy Ghost" name came from.


**Ghost Bird**   
I wanted the bird to change into a ghost when it ran into a pipe.  I thought it would be funny for the bird to look like it turned into a silly representation of a ghost.  I added a little bit of translucency and a silhouette of a sheet over top.

It turns out the code already provided a nice way to achieve this.  There was a feature to add accomplishments to the cow in the original Flappy Cow game.  At a certain score the cow would get a hat or sunglasses.  There was even a score that would change the cow to a NyanCat.  I used that same logic to switch the bird sprite to the ghost sprite.  After the collision with the pipe wasn't detected anymore, I switch it back to the bird.

![Ghost Bird](https://raw.githubusercontent.com/jjerome00/FlappyGhost/master/app/src/main/res/drawable-nodpi/ghost_bird.png "The Ghost Bird sprite")

## Clean up

There were a lot of features in the clone that you would want in a real game - such as an ads, analytics and Play Services.  I had to remove everything without breaking the game. It was an interesting mix of learning how the APIs were added, and then figuring out how to remove them without crashing the app.

## In Conclusion

I had a lot of fun breaking this app down and building it back up.  I learned a few things about writing games, and made changes by leaning on existing features.

As a consultant, I am always writing, testing, and refactoring code to make it the best it can be. It's fun to ignore most of that and make things work as quick as possible.  I think the big lesson is that making something perfect does not always fit the client's needs.
