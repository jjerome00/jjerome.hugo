---
title: "WA State Toll Tracker, for Android"
date: 2015-09-24
draft: false
updated: 2015-09-24T11:25:10Z
blogimport: true
tags: [Android, Development]
showthedate: true
---

>
> **NOTICE: This post has been IMPORTED from a previous blog.**
>
> _I'm sorry to report that Good To Go have updated their website and it has broken the app. I have been in
> contact with them about a promised API, but it appears one is not in the works. Sadly, I had to unpublish the app._
>
> **I included it here because it was a great experience to build and release the original application.**

<br /><br />

<p>I'm happy to announce the release of another Android application, <b>WA State Toll Tracker</b>!
  <br/>
  <br/>Go install it now at the Google Play Store:
  <ul>
    <li><a href="https://play.google.com/store/apps/details?id=com.mabon.goodtoknow" target="_blank">https://play.google.com/store/apps/details?id=com.mabon.goodtoknow</a></li>
    <li>If you like it, please leave a great review!</li>
  </ul>
  <br/>View the official web page:
  <br/><a href="http://mabonservices.com/tolls" target="_blank">http://mabonservices.com/tolls</a>
  <br/>
  <br/> </p>
<h2>Questions about the project</h2>
<p><b>Where did this idea come from?</b>
  <br/>I came up with the idea for this app while crossing the SR 520 bridge, which is a toll road. All tolling is handled by an automated system that is linked to an online account you setup with the State of Washington. You can read more about the program
  at <a href="http://mygoodtogo.com" target="_blank">http://mygoodtogo.com</a> . You sign up for an account, and provide a credit card to get started. When you cross the bridge (or another tolled area) their system reads your pass and deducts the toll
  from your account. </p>
<p>I had read some stories about people who had racked up large fines for failing to notice they had outstanding tolls and fees on their accounts. I decided to double-check my account, but couldn't remember my username or password. It would be ok if it happened
  once, but every time I wanted to check my account I would have to go through the process of forgetting my username or password and having to reset my account. </p>
<p>So I built this app. It allows me to quickly view my tolling activity without having to reset my password. Now when I want to quickly review my account, I can just open the app and refresh for my most recent activity. </p>
<p>It has also saved us money. We had a car that had problems with a sticker pass. The system would recognize the pass but someone at Good To Go had to visually confirm the toll via a photo. It's called a photo enforcement fee, and you get charged an additional
  25 cents for each time it occurs. It happened so frequently that it became cost effective to get a new pass. </p>
<p><b>How long did it take to build?</b>
  <br/>I think it was about a year. It was done in my spare time, and I allowed some other interests to get in the way if needed, <a href="/posts/tardis-fridge/" target="_blank">like painting my fridge to look like a TARDIS</a>.
  </p>
<p><b>What's your status?</b>
  <br/>I'm a full-time contractor, so I was looking for something to do on the side for fun. I don't do any advertising for my apps, and I feel if I was ever going to look to do this more seriously it would be beneficial for me to keep publishing apps. </p>
<p><b>What got you into Android development?</b>
  <br/>Honestly, I couldn't afford a computer from Apple. I did some robotics development a few years ago that I very much liked. The same bug that might render a web page incorrectly might sent your robot into a ditch. Android development reminded me of that
  past, so I wanted to explore it further. </p>
<p><b>What challenges did you face with building the app?</b>
  <br/>
  <ul>
    <li>My other apps were Activity-based apps, and I wanted to play with fragments. It was a bit of pain, because some things I knew, but not enough to do everything I wanted to do. So I was making jagged progress - some things came quickly, others moved
      forward like a snail.</li>
    <li>InApp billing was a little bit of a pain. For starters, InApp billing needs more real-world examples, and the ability to debug a beta APK with InApp billing enabled</li>
    <li>The technique to implement a Navigation Drawer changed half way through my development of the app. Honestly I'm glad I put the time in to change it because the new way is better. </li>
    <li>It seems petty, but would it kill Android Studio to allow you to set a breakpoint on an empty line? I mean that I want it to stop before the next executable line. Android Studio will let you set the breakpoint on an empty line, but completely ignores
      it come debug time. </li>
  </ul>
</p>
<p><b>What's next?</b>
  <br/>I have a few ideas rolling around in my head, and some friends with ideas of their own. My biggest fear is that since I'm doing this myself that I'm missing out on the collaborative learning I would get if I was working with a team. </p>
<a href="http://1.bp.blogspot.com/-8Z116AfKPzQ/VgQ_atryN3I/AAAAAAAA4PM/rn539XXry84/s1600/ss01.png"
imageanchor="1"><img border="0" src="http://1.bp.blogspot.com/-8Z116AfKPzQ/VgQ_atryN3I/AAAAAAAA4PM/rn539XXry84/s320/ss01.png" /></a>
<a href="http://4.bp.blogspot.com/-e5smxebE4Bk/VgQ_akmHbdI/AAAAAAAA4PI/RO-wtykigDI/s1600/ss02.png" imageanchor="1"><img border="0" src="http://4.bp.blogspot.com/-e5smxebE4Bk/VgQ_akmHbdI/AAAAAAAA4PI/RO-wtykigDI/s320/ss02.png" /></a>
<a href="http://2.bp.blogspot.com/-PB2Abgn48ww/VgQ_aiQI3yI/AAAAAAAA4PU/tjdBF77yAns/s1600/ss03.png" imageanchor="1"><img border="0" src="http://2.bp.blogspot.com/-PB2Abgn48ww/VgQ_aiQI3yI/AAAAAAAA4PU/tjdBF77yAns/s320/ss03.png" /></a>
<a href="http://1.bp.blogspot.com/-v5m6E1QM__Y/VgQ_b1puGxI/AAAAAAAA4PQ/v9QR9QVV3t0/s1600/ss04.png" imageanchor="1"><img border="0" src="http://1.bp.blogspot.com/-v5m6E1QM__Y/VgQ_b1puGxI/AAAAAAAA4PQ/v9QR9QVV3t0/s320/ss04.png" /></a>
