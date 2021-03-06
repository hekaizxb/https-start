## IIS7.5如何开启TSL1.2

## 第一步
### 源站下载
点击下面链接下载 `IISCrypto`
[IIS Crypto GUI](https://www.nartac.com/Downloads/IISCrypto/IISCrypto.exe)
[IIS Crypto CLI](href="https://www.nartac.com/Downloads/IISCrypto/IISCryptoCli.exe)

### 本地下载
点击下面链接下载 `IISCrypto`
[IIS Crypto GUI](https://files.drixn.com/IIS/IISCrypto.exe)
[IIS Crypto CLI](https://files.drixn.com/IIS/IISCryptoCli.exe)

将下载好的 `IISCrypto` 放在桌面待用
## 第二步
右键单击以管理员身份运行
![图1](https://cdn.drixn.com/img/src/IIS7TLS000.png)

## 第三步
勾选需要开启的协议，建议只开启 `TLS1.2`,关闭其他协议
![图2](https://cdn.drixn.com/img/src/IIS7TLS001.png)

## 第四步
然后点击 `Apply`
![图3](https://cdn.drixn.com/img/src/IIS7TLS002.png)

## 第五步
弹出重启提示，重启服务器
![图4](https://cdn.drixn.com/img/src/IIS7TLS004.png)

## 第六步
验证是否开启
### 方法一
调出运行窗口，输入 `regedit`

打开注册表并定位到 `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\` 目录下

如下图，出现上面步骤勾选协议则证明成功开启
![图5](https://cdn.drixn.com/img/src/IIS7TLS003.png)

### 方法二：
打开浏览器，查看`协议版本`,如下图出现 `TLSv1.2` 说明开启成功
![图6](https://cdn.drixn.com/img/src/IIS7TLS005.png)