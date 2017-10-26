---
title: "Hugo CMS"
date: 2017-10-21
tags: [Development]
draft: false
showthedate: true
---

## Hugo

The following is my summary about how I setup Hugo for my needs.  If you are looking for basic information, please refer to the <a href="https://gohugo.io/documentation/" target="`_blank`">official documentation</a>.  Sometimes it helps to view the same content in someone else's words.

This page represents a quick summary of my notes.  I am not an expert in Hugo, nor do I know all its features.  If you are here looking for help doing something, you should read this **and other** sources to gain a good understanding of what you want to do.

<br/>
### Quick Summary

Setup a new hugo site:
  ```
  hugo new site mywebsite
  ```
  * Don't forget to download a theme from their website
  * The site's main configuration file: `config.toml` (you set the theme here)

Create a page:
  ```
  hugo new posts/my-first-post.md
  ```
  * Notice you include the location of where to create the file   

Run a test server:
  ```
  hugo server -D`   
  ```
  * `-D` means to show all pages marked as `draft`
  * Leave the -D off if you want to only see published content (i.e. pages not marked as draft)   
  <br/>

Build the final site:

  1. Remove anything in the `/public` folder
  2. Run command `hugo`
  3. Copy everything in `/public` folder to your web host

<br/><br/>

## Themes

Browse and download a theme from Hugo's website.   
I choose a theme called <a href="https://github.com/calintat/minimal/" target="`_blank`">Minimal</a>

* A good theme has a good README on their github page explaining how best to customize it
* Themes want you to `git clone` their project.  This hasn't been the greatest experience for me.  Instead I download the theme myself and place it in the theme folder

<br/>
#### Customize your theme
With Hugo you can override any file in the theme by making a corresponding file under the `/layouts` folder.

For example, to change the theme's footer file:

1. Find the file in the theme: `/themes/minimal/layouts/partials/footer.html`
2. Copy it to your layouts folder: `/layouts/partials/footer.html`
3. Edit the copy in the layouts folder
4. You're done!

<br/>
## Pages
Each page in Hugo defaults as a `list` type.

* If you create one file in a folder, then it's the only one and acts like the index.html file.  
* As soon as you create 2 files, the index of that folder changes and it lists all files in the folder in blog-like fashion

All pages have a small section at the top for settings and variables called "Front Matter"

* All new pages have a `draft: true`.  The page will not show on your published site until you change it to false.

<br/>
## Customizations

<br/>
#### An About page with no date
I created an About page.  I noticed that a single page in Hugo (with theme Minimal) still shows the date.  I thought that looked rather silly so I made some modifications.  This might not be the best way to achieve what I wanted.

1. Hugo as a section called "archetypes", which are default settings for the type of pages you can build.  I modified my `/archetypes/default.md` to include a new variable: `showthedate: true`.  Every new page I make has this variable in it.
2. I found the file in the theme that was displaying the date.  In my case it was a file called `/themes/minimal/layouts/partials/list-item.html`.  I copied the file into my layouts folder: `/layouts/partials/list-item.html`
3. I made this change in the file itself:

  ```
  {{ if .Params.showthedate }}
  {{ .Date.Format (.Site.Params.dateFormat | default "January 2, 2006") | $.Scratch.Set "subtitle" }}
  {{ end }}
  ```
  * All this does is hide the date if my page has my `showthedate` variable set to false

4. In my `about.md` page, I set the variable:

  ```
  ---
  title: "About"
  date: 2017-10-20T21:56:50-07:00
  draft: false
  showthedate: false
  ---

  I have been making...
  ```

<br/>
#### Open Header icons in new tab
(instead of in the same page)

I wanted all icons in my header, such as Twitter, Stacked Overflow, etc, to open in a new tab (or window).  This is another example of finding the file in the theme, and overriding it by placing a modified copy in the `/layouts` folder

1. I found the spot where the theme generates the icon links: `/themes/minimal/layouts/partials/header.html`
2. I copied it to my local layouts folder: `/layouts/partials/header.html`
3. I added a `target="_blank"` parameter to the link tag (super simple MVP-like stuff)

  ```
  <li class="navbar-icon"><a target="_blank" href="{{ .URL }}"><i class="fa fa-{{ .Name }}"></i></a></li>
  ```
<br/>
#### Create a static landing page
By default the theme shows your blog posts on the main landing page (i.e. http://www.jjerome.com/).  I wanted my main landing page to just show a welcome message.  Again, fairly easy to do by overriding the theme.

1. I found the spot in the theme: `/themes/minimal/layouts/index.html`
2. I copied it to my layouts folder: `/layouts/index.html`

This page is a little weird, because it's not a markdown file like the rest of the site.  I didn't dwell on that fact for too long.  I just made my changes and moved on.

<br/><br/>
**You can see all my code in my <a href="https://github.com/jjerome00/jjerome.hugo" target="_blank">github repo</a>**
