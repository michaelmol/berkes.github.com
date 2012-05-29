---
layout: post_archive
title: Sage alternative stylesheet
created: 1093966075
tags:
- Coding Corner
lang: nl
---
[![screenshot of the alternative stylesheet](http://bler.webschuur.com/sites/bler.webschuur.com/files/images/thumb_cc93c35c6670d7c01bc4f5fce46ba55c-141.png)](/node/view/141)[Sage](http://sage.mozdev.org/index.html) is an rss newsreader for mozilla. It works really nice, mostly because you read everything inside the browser. And also, because it intergrates seamlessly into your bookmarks. <br />Another great feature, is that you can edit the look of the inline rendered newspage with a custom CSS file. [Scott Kingery](http://users.tns.net/~skingery/weblog/fox.htm) made a cool css stylesheet that works great as alternative to the default CSS.<br /><br />I modified this one, to make it more useable, in my opinion, that is. My stylesheet hides all the info and description by default. And shows you only the title of the newsarticle. Great for a good overview. When you move the mouse over an article it pops open and you can read all of it. <br /><br />What you must do, is copy the text below, and paste it in an empty textfile, modify it a bit to suit your needs for colors and save it somewhere. Then from sage-configuration dialog you canselect the userdefined css file you just saved. <br /><br /><pre>html * /*Sage.css file developed by Scott Kingery*//*Modified from the original to format vertically and have unread links be red*//* Im not sure yet. Possibly mozilla specific formatting? */{-moz-box-sizing: border-box;}html /* General Html formatting */{line-height: 1.3; background-color: #ddd;}body /* Body formatting */{background:#ddd;margin: 5em 1em 1em 1em;color: #222;font-family: verdana;font: "Trebuchet MS",Verdana,Arial,Sans-serif;}/* Paragraph tag */p {margin: 0px 0px 10px 0px;}a:link/* Link properties */{text-decoration: none;color: /*#436976*/red;}a:visited/* Visited link properties */{text-decoration: none;color: #537986;}a:hover/* Over link properties */{text-decoration: underline;}a:active/* Link as it is being clicked properties */{text-decoration: none;}p.item-desc a:link/*Paragraph and paragraph link properties */{color: #029;}#rss-header/* This is the global title of the site. rss-title and rss-desc are children to this one */{position: fixed; background-color: #357; color:#abc;border: 1px solid #cccccc;padding: 6px 8px;margin: 10px 2%;margin: -4em -1em 1em 1em;        height:2.3em;        overflow:hidden;}#rss-header:hover {        height:auto;        overflow:visible;        visibility:visible;}#rss-title/* The RSS header properties. Basically the where the */{/*background-color: red;  *//* uncomment to see effect */color:white;font-size: large; line-height: 1;margin: 0px;padding: 0px;}#rss-title a{color:white}#rss-desc/* The description of the RSS. Not all sites have this, but a lot do. */{/* color: red; */ /* uncomment to see what it does */font-size: 1.75em;margin: 0px;padding: 5px 0px 0px 20px;}div.item/* Global news table properties */{background-color: #000000; /* uncomment to see effect */background-color: #fff; border: 1px solid #8cacbb;border: 1px solid #000000;width: 96%; /* if you want it to be one right after another instead comment or remove this line */min-width: 14em;margin: 0px 0px 6px 2%;padding: 0px;float: left;}span.item-ordinal/* The news's entry number properties */{/* color: red; */ /* uncomment to see what it does */padding-right: 0.2em;}div.item-desc/* The news's body properties */{/* color: red; */ /* uncomment to see what it does */font-size: 1em;margin: 0;padding:0;        visibility:collapse;        height:0;}div.item:hover div.item-desc,div.item:hover div.item-pubDate,div.item:hover div.item-technocrati {        height:auto;        overflow:visible;        padding: 8px 10px;        visibility:visible;}h2.item-title/* The div.item's header properties */{background-color: #dee7ec; /* change around to see what cell it's changing */font-size: 1em;font-weight: normal;line-height: 1.1;margin: 0px;padding: 5px 5px 8px 8px;        height:auto;        overflow:visible;    }/*Changes the feed title background when you hover over it so you can see where you are*/div.item:hover h2.item-title {background-color: #CCCCCC;}div.item-pubDate/* Date which it was released */{/* background-color: #FF0000; */ /* Uncomment to see where it is */font:1em "Trebuchet MS",Verdana,Arial,Sans-serif;margin: 0px;padding:0width: 80%;float: left;        height:0;        overflow:hidden;}div.item-technorati/* Bottom cell where respond bubble is */{        margin: 0px;padding:0;float: right;text-align: right;        height:0;        visibility:hidden;}</pre>