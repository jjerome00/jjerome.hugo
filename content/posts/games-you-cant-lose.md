---
title: "Games You Can't Lose"
date: 2018-01-19
tags: [Projects, Android, Development]
draft: true
showthedate: true
---

Recently I've been having a lot of fun playing around with other people's code.  

I've been forking games on Github to learn a little about how they work.  I then change them so that they are impossible to lose.  They turn out to be very short and completely useless beyond a couple laughs.  Messing around with the code is almost more fun than the end result.

This started when a coworker was telling me that he had never won a video game.  A few of us started coming up with ideas for games where it was impossible to lose.  They seemed pretty funny, so I decided to play around with the idea a little bit.

I've only done a couple games so far.  I've had some challenges along the way:

* Most of these projects are stale and need a little work to get them working again.  I spent a lot of time importing Eclipse projects into Android studio and working out the details
* I had to pull apart a lot of conveniences: game options, number of lives, difficulty settings  

I'm impressed how entertaining they are to put them together when I have no regards for playing it safe.  Every hack is on the table as a possibility.  I only have to worry about one thing - never lose.   

<br />

## "Tetris Can't Lose"   

<table width="100%">
<tr align="center">
<td><iframe width="100%" height="315" src="https://www.youtube.com/embed/4gqsz21l8m8" frameborder="0" allowfullscreen></iframe></td>
<tr>
<tr align="center">
<td><a href="https://youtu.be/4gqsz21l8m8" target="`_blank`">`https://youtu.be/4gqsz21l8m8`</a></td>
<tr>
</table>

<br />


I named this game after the old tv show "Parker Lewis Can't Lose"

This was my first attempt at changing a game.  It had a couple of surprises:

* Tetris isn't designed to win!  You keep playing until you lose.  So I had to come up with a way to win the game, and add it as an option in the game play.  
* I decided to add a funny "TaDa!" sound, so I had to add MediaPlayer and SoundPool.  This change has become my exclamation point, and has made it into the other games as well.
* I had to clean up some code, create a new launch icon, etc

One thing I regret is that I didn't fork the repo correctly.  I ended up losing some history that I wanted to show in Github.  It's not a big deal, but I wanted to make sure whoever ran into the project knew that I based it off someone else's work.  I ended up adding a note to the project's readme.

You can view the code here: <a href="https://github.com/jjerome00/tetris-cant-lose" target="`_blank`">`https://github.com/jjerome00/tetris-cant-lose`</a>


## "Can't lose Breakout"

<table width="100%">
<tr align="center">
<td><iframe width="100%" height="315" src="https://www.youtube.com/embed/4FDZtsKBhvI" frameborder="0" allowfullscreen></iframe></td>
<tr>
<tr align="center">
<td><a href="https://youtu.be/4FDZtsKBhvI" target="`_blank`">`https://youtu.be/4FDZtsKBhvI`</a></td>
<tr>
</table>

<br />

I ran across this breakout game on Github.  It had all the parts that I was looking for, and as a bonus it included lots of documentation.  It was a sample game that explained a lot about how to write a game for Android.

* It was rather stale, so it took a bit to import it into Android Studio and get it to work
* It had a lot of game options I had to remove or change for my needs
* I had to play around with the settings to get the most humor out of it

This one was different in that you don't win immediately like in the Tetris game.  You can move the paddle around and try to make the process faster, but it doesn't matter.   

Keeping the game play intact was a good idea - it makes the game a little more fun.  The ball can't fit past the paddle, but it looks like it could.  It's amazing to see people's first reaction when they play.  They have an initial sense of urgency to save the ball even though it's impossible for it to fit past the paddle.  

You can view the code here: <a href="https://github.com/jjerome00/cant-lose-breakout" target="`_blank`">`https://github.com/jjerome00/cant-lose-breakout`</a>
