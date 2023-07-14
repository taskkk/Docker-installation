# Docker-installation
###将Docker安装在D盘，节省系统盘空间
安装Docker在D盘
分俩种情况：
一、已经安装好Docker
步骤一
找到自己安装Docker的文件夹，一般是 C:\Program Files\Docker，将该路径下的Docker文件夹拷贝到你需要安装的位置下。
原始位置

我改的是 D:\Program Files\Docker。
更改后的位置

\color{red}{重要！！！删掉C盘中的Docker文件夹。要是不删除会导致后面在终端输入命令的时候失败。}
步骤二
找到Docker建立项目会存储的位置（只是我的理解），我的是 C:\Users\29440\AppData\Local\Docker，一般通用的路径是 C:\用户\用户名\AppData\Local\Docker，将该路径下的Docker文件夹拷贝到你需要安装的位置下。（忽略我的快捷符号，因为这是我已经更改后的。要是没更改的话，这个就是正常的文件夹图标）
原始位置

我改的路径是 D:\ProgramData\Docker
更改后的位置

\color{red}{和步骤一相同，一定要删掉C盘原始路径下的Docker文件夹。}
步骤三
win + R 打开命令终端，依次输入：

>mklink /J  "C:\Program Files\Docker（原始路径）"  "D:\Program Files\Docker（更改的路径）"
>mklink /J  "C:\Users\29440\AppData\Local\Docker（原始路径）"  "D:\ProgramData\Docker（需要实际安装的路径）"
绿色框住的就是成功的，红色框就是忘记删除原始路径下的文件夹会出现的错误。


结果图
二、还没有安装Docker
步骤一
在需要安装Docker以及Docker项目的路径下建立Docker文件夹。
比如我的就在 D:\Program Files\Docker 和 D:\ProgramData\Docker下。

步骤二
如第一种情况下的步骤三，输入俩个命令，将C盘的文件夹。

步骤三
安装Docker。

结果
环境变量的路径还有原始路径下都会是默认的路径，但是我们可以看到的是，原始路径下的Docker这个文件图标已经是快捷方式了。之后的所有实际内容都会在D盘，但是会映射到C盘。
