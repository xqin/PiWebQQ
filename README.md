WebQQ-for-Raspberry-Pi
=======================================
运行于Raspberry Pi, 基于WebQQ协议, 使用Python脚本编写.

登陆时需要在py脚本内设置需要登陆的QQ号及密码,
如需使用`二维码`(QRCode)的登陆方式可以了解一下下面这个 Repository.
[SmartQQ-for-Raspberry-Pi](https://github.com/xqin/SmartQQ-for-Raspberry-Pi)

程序运行后,不会有任何输出,因为日志都已经记录在程序所在目录的`qq.log`中,
可通过`tail -f qq.log`查看日志.

登陆时,如果需要验证码, 请在程序所在目录里找到`v.jpg`,认出验证码后,
在程序所在目录里创建一个 `v.txt` 的文件,内容为与图片对应的验证码.
可使用以下命令将验证码输入至`v.txt`中.
```
echo "abcd" > v.txt
```
>因为程序是设计运行在`Raspberry Pi`上且通过后台的方式运行,
>所以不提供交互式的验证码输入功能,而是采用通过每隔3秒(尝试20次)读取特定文件`v.txt`来得到验证码的功能.

对于不会一点`Python`的同学,不建议使用本程序且不接受所提的`issue`.
请各位在提`issue`之前先阅读一遍代码(`WebQQ.py`),以了解程序的流程及处理逻辑.

#####2015-03-25 更新
>因WebQQ更新登陆时密码的加密方式, 在加密时使用了RSA, 所以在使用本程序时确保你的Python中有安装 RSA(https://pypi.python.org/pypi/rsa) 模块.
