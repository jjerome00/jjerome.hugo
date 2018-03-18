
# jjerome.hugo
Source code for the website of Jason Jerome

* Written with <a href="https://gohugo.io/" target="`_blank`">Hugo CMS</a>

http://www.jjerome.com


## Basics

New blog page: `hugo new posts/my-post.md`   
Run a test server: `hugo server -D` (-D: show all pages marked as draft)   

publish final site:
1. Make sure to remove draft flag for all new content!
2. run `./publishHugo.md` (for my environment only - sorry kids)


## How To

Make a link that opens in a new tab, without the markdown freaking out:
```
<a href="https://imgur.com/gallery/vOlcW/" target="`_blank`"> `https://imgur.com/gallery/vOlcW`</a>
```
*  target="`_blank`" keeps the markdown formatter from freaking out
* if you are going to show a url in the text, then surround it by ````
