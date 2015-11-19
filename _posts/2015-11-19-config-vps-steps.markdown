## 1. install go

### install gvm

1). 安装gvm-installer
```
bash < <(curl -s -S -L https://raw.githubusercontent.com/moovweb/gvm/master/binscripts/gvm-installer)
```

2). vim ~/.bashrc and source gvm
```
[[ -s "$HOME/.gvm/scripts/gvm" ]] && source "$HOME/.gvm/scripts/gvm"
```

3). Logout and Login with Your User

4). checkto make sure gvm is installed
```
gvm version
```
And see something like:
```
Go Version Manager v1.0.22 installed at /home/myuser/.gvm
```

5). install go
```
gvm listall
gvm install go1.4
gvm use go1.4
```

6). verify go is installed correctly
```
go version 
```

## 2. install shadowsocks-go
```
wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-go.sh
chmod +x shadowsocks-go.sh
./shadowsocks-go.sh 2>&1 | tee shadowsocks-go.log
```

uninstall shadowsocks
```
./shadowsocks-go.sh uninstall
```

启动：/etc/init.d/shadowsocks start
停止：/etc/init.d/shadowsocks stop
重启：/etc/init.d/shadowsocks restart
状态：/etc/init.d/shadowsocks status

shadowsocks config file : /etc/shadowsocks.json

## 3. config shadowsocks client