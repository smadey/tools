## 要求
安装好 Brew 和 Shadowsocks


## 配置步骤

#### 1. 安装 proxychains
```
brew install proxychains-ng
```

#### 2. 配置 proxychains.conf
```
socks5  127.0.0.1 1080
```

#### 3. 测试所在城市
```
curl ifconfig.co/city
```

#### 4. 安装 curl (记录安装地址，不安装的话需要再安全模式执行"csrutil disable")
```
brew install curl
```

#### 5. 测试所在城市 (可以配置 alias p-curl='proxychains /path/to/curl')
```
proxychains /path/to/curl ifconfig.co/city
```