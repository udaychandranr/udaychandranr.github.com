---
published: true
layout: post
tags: 
  - 404 Error
  - Client Error
  - HTTP Status Codes
  - Redirection
  - Server Error
  - Successful
---

Note: Disabling text selection prevent users to copy the content and images on your Web page. It decrease the copyright violations from your readers “Coping” or “republish” content without your knowledge (most likely more than a typical Amazon affiliate site does).

Disable Text Selection With CSS – Click here

DisableTextSelectionThis type of duplication is fairly common on web, And here are some example's to avoid It.

This example demonstrates how to Disable Text Selection on your Web page or how you can protect your content from “Coping”.

Add this script to the HEAD section of your page:

    <script language='JavaScript1.2'>
    function disableselect(e){
    return false
    }
    function reEnable(){
    return true
    }
    //if IE4+
    document.onselectstart=new Function (&quot;return false&quot;)
    //if NS6
    if (window.sidebar){
    document.onmousedown=disableselect
    document.onclick=reEnable
    }
    </script>
