---
layout: post
title:  "index.html in a yeoman project"
subtitle: "Confusion about comments of index.html in a yeoman project"
date:   2016-01-13 18:20:01
categories: [frontend]
---

This post aim to give a brief explanation of some comments in index.html of a yeoman project.

## 1. comments for bower
{% highlight html %}
<!-- - bower:css -->
<link rel="stylesheet" href="bower_components/bootstrap/dist/css/bootstrap.css">
<!-- - endbower -->

<!-- bower:js -->
<script src="bower_components/jquery/dist/jquery.js"></script>
<!-- - endbower -->
{% endhighlight %}

This kind of blocks is to help [wiredep](https://github.com/taptapship/wiredep)(click the link to learn more) to automatically put the dependencies code to the index.html file.


## 2. conments for usemin
{% highlight html %}
<!-- build:js({.tmp,app,.}) scripts/vendor.js -->
<script src="bower_components/jquery/dist/jquery.js"></script>
<script src="bower_components/moment/moment.js"></script>
<!-- endbuild -->
{% endhighlight %}

This kind of blocks is to help [usemin](https://github.com/yeoman/grunt-usemin)(click the link to learn more) to determine which block of javascript files to be packaged and uglified. 


## 3. comments for IE
{% highlight html %}
<!--[if lt IE 9]>
<script src="bower_components/es5-shim/es5-shim.js"></script>
<![endif]-->
{% endhighlight %}

And this block will work when users' IE browser version is less than 9.