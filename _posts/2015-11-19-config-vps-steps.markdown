---
layout: post
title:  "Config a VPS by Shadowsocks"
subtitle: "this is a Go version shadowsocks guide, Node or Python version is similar"
date:   2015-11-19 18:23:01
categories: [black]
---

## 1. install go

### install gvm

1). 安装gvm-installer
{% highlight bash %}
bash < <(curl -s -S -L https://raw.githubusercontent.com/moovweb/gvm/master/binscripts/gvm-installer)
{% endhighlight %}

2). vim ~/.bashrc and source gvm
{% highlight bash %}
[[ -s "$HOME/.gvm/scripts/gvm" ]] && source "$HOME/.gvm/scripts/gvm"
{% endhighlight %}

3). Logout and Login with Your User

4). checkto make sure gvm is installed
{% highlight bash %}
gvm version
{% endhighlight %}
And see something like:
{% highlight bash %}
Go Version Manager v1.0.22 installed at /home/myuser/.gvm
{% endhighlight %}

5). install go
{% highlight bash %}
gvm listall
gvm install go1.4
gvm use go1.4
{% endhighlight %}

6). verify go is installed correctly
{% highlight bash %}
go version 
{% endhighlight %}

## 2. install shadowsocks-go
{% highlight bash %}
wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-go.sh
chmod +x shadowsocks-go.sh
./shadowsocks-go.sh 2>&1 | tee shadowsocks-go.log
{% endhighlight %}

uninstall shadowsocks
{% highlight bash %}
./shadowsocks-go.sh uninstall
{% endhighlight %}

启动：/etc/init.d/shadowsocks start
停止：/etc/init.d/shadowsocks stop
重启：/etc/init.d/shadowsocks restart
状态：/etc/init.d/shadowsocks status

shadowsocks config file : /etc/shadowsocks.json

## 3. config shadowsocks client