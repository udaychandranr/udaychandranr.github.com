---
published: true
layout: post
tags: 
  - Blogger
  - Blogger Plugin
  - Blogger Plugins
  - Blogger Widgets
  - CSS
  - jQuery
  - Notification Bar
  - Sticky Bar
  - Trending Bar
  - Tutorials
---

Sticky Notification bar is like an Trending bar plugin used in various platforms. There are many sticky, fixed or floating bar plugins. But this tutorial will help you use a light weight code which can be used for both blogs and websites running on any platform with close button. So lets start the tutorial.
Live Demo Here
bar

Step 1 — In order to give a best visual appeal to the Sticky Notification bar,  we are going to use CSS style for it. If you want to custom the CSS below to your own style.

    #stickybar {
        border - bottom: 1px solid#ECF1EF;
        background: #151715;
        font-size:16px;
        color:# FFF;
        padding: 10px 20px;
        position: fixed;
        bottom: 0;
        left: 0;
        z - index: 2000;
        width: 100 % ;
        text - align: center;
    }#stickybar a {
        color: #FFF;
        text - decoration: none;
    }#closebtn {
        background: url('http://goo.gl/3cCdJ') top no - repeat;
        border: none;
        margin - left: 15px;
        position: absolute;
    }

You can change the position of the Sticky Notification bar to appear.

	#stickybar {
		bottom: 0;
	}

Step 2 — Now in order to achieve the opacity and close button  purpose, we are using this jQuery code.

    <script type='text/javascript'>
    $(document).ready(function() {
    (function() {
    //settings
    var fadeSpeed = 200, fadeTo = 0.5, topDistance = 30;
    var sibar = function() { $('#stickybar').fadeTo(fadeSpeed,1); }, stbar = function() { $('#stickybar').fadeTo(fadeSpeed,fadeTo); };
    var inside = false;
    //do
    $(window).scroll(function() {
    position = $(window).scrollTop();
    if(position > topDistance && !inside) {
    //add mouseover events
    stbar();
    $('#stickybar').bind('mouseenter',sibar);
    $('#stickybar').bind('mouseleave',stbar);
    inside = true;
    }
    });
    //close
    $('#closebtn').live('click', function(event) {
    $('#stickybar').toggle('show');
    });
    })();
    });
    </script>

Note: Before adding this ensure that you already have jQuery initialized on your blog. If not add `<script src="http://code.jquery.com/jquery-1.5.js"></script>` or latest jquery.js before `</head>`

Step 3 — Finally add the HTML section which has the content to be display on your blog or website.

    <div id='stickybar'>
	Trending: <a href='YOUR CUSTOM URL'>Your custom message goes here</a>
    <input type='button' id='closebtn' >
    </div>

Blogger and WordPress users ensures that the code is placed within `</head>` selection.
 
After following the three steps carefully you can see the sticky notification bar in your blog or website. If you any query, drop in your comments.
