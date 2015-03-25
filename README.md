WebQQ-for-Raspberry-Pi
=======================================
运行于Raspberry Pi, 基于WebQQ协议, 使用Python脚本编写.

登陆时需要在py脚本内设置需要登陆的QQ号及密码,
如需使用`二维码`(QRCode)的登陆方式可以了解一下下面这个 Repository.
[SmartQQ-for-Raspberry-Pi](https://github.com/xqin/SmartQQ-for-Raspberry-Pi)


#####2015-03-25 更新
>因WebQQ更新登陆时密码的加密方式, 在加密时使用了RSA, 所以在使用本程序时确保你的Python中有安装 RSA(https://pypi.python.org/pypi/rsa) 模块.