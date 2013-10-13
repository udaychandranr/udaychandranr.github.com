---
published: true
layout: post
tags: 
  - Blogger
  - Google
  - Super
  - Tutorials
---

The 404 error message is a HTTP standard response code indicating that the client was able to communicate with the server, but the server could not find what was requested.

By Default, Blogger(BlogSpot) Error page will display an generic message as 404 error page.
	![404.png](http://cdn.luysec.com/img/404.png)
**404 Blogger**

Each type of error has an HTTP error code dedicated to it. For example, if you try to access a non-existing page on a website, you will be met by the familiar 404 error.

**Click here to know List of HTTP error code**

**Steps to create Custom 404 Error page – Blogger(BlogSpot)**

**Login to Blogger account**

1. Go to Settings > Search Preferences
2. Under Errors and redirections , Edit the Custom Page Not Found option
3. Now Enter an HTML message to be displayed on the Page Not Found page instead of the generic message.

**HTML message Page Not Found Example**

    <style type="text/css" >
    body {background:white url('http://themes.luysec.com/files/theme/404.png')  50% 0% no-repeat !important;z-index:10000400;}
    #widget-name {display:none;}
    body {min-width: 0px !important;}
    </style>
