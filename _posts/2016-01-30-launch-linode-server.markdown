---
layout: post
<<<<<<< 569056b8bbfd25594bff5a46e25ae57d50ffaff1
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
=======
title:  "launch a linode server"
subtitle: "分享一下我在linode开启一台服务器的经验"
date:   2016-01-13 18:20:01
categories: [black]
---


## 1. 必须要有一个可以支付美元的信用卡
这个和在亚马逊开账户一样，必须要绑定一张信用卡，用来支付服务器的费用。信用卡的选择当然很多了，普通玩家就办个普通的visa或者master card什么的信用卡就好了。


## 2. 申请账号，填写信息
去linode 网站申请一个账号，然后大概是完善信息，一次填入什么姓名地址信用卡信息之类的。这些信息填完提交之后，会有一定的时间等待别人确认信息的过程，大概一两个小时
也算正常。这期间是没办法进行任何在网站上的操作的。不要惊慌，不要觉得钱被骗了的感觉（预先充值最低$5）。


## 3. 选择一个node
然后就可以选择开一台服务器了，根据个人需要选择一个类型的node，选择服务器所在地，新加坡到国内速度貌似并不是很好，不知道别的地方是不是更惨。。 这个步骤完了，就只是相当于买了台电脑
作为服务器，但是并没有开机，并没有装系统！（好像是废话。。。当时我就傻乎乎的就ssh去连了。。。）

## 4. 开机并装系统
在网页上看到自己开的机器，先点击boot 按钮，然后选择一个镜像，安装系统。这个启动安装的过程都可以在页面上看的很清楚。一切就绪了貌似再设置一些root账户的密码，就可以ssh登录了！接下来的事情
就隨意了
>>>>>>> launch server at linode
