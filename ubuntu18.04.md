# ubuntu 配置环境问题（包含多个版本）
按自己的版本需求查找。
## buntu18.04版本安装过程中遇到的问题：
### one.卡在启动界面：
原因：1.显卡驱动问题，可以先禁用显卡驱动，找到“quiet splash”，在本段的最后面加上"acpi_osi=Linux nomodeset"(直接加"nomodeset"即可)，接着按F10保存并启动.
### 开机重启问题：
降低ubuntu的小版本，如ubuntu18.04.5->ubuntu18.04.2
### two.显卡驱动问题：
建议：1.通过软件和更新先把源换成中国的，推荐ustc，然后更新一下，sudo apt-get update，看看能不能通过软件和更新的附加驱动找到可用的显卡驱动，如果能找到建议选个版本高点的，如果找不到可以去网上查找如何通过PPA仓库安装。
nvida-smi 检验安装是否完成
### three.cuda+cudnn安装:
建议：其实网上的教程挺多的一般不会出错，可以用nvida-smi检测推荐的cuda版本。cudnn版本只要对应就行了，网上教程挺多的，不容易出错。
### four.深度学习框架的安装：
网上去找吧，pytorch挺好装的,tensorflow要用anaconda。

### five.opencv安装:
 版本:
opencv3或opencv4加上其扩展库
 问题：
配置cmake，不需要配置那么多，(如cuda版本的，没必要)
网上的有很多坑的，我忘了都有哪些了，交给后面的人补
解决cmake安装导致python3不能使用opencv的问题：
sudo pip3 install -i https://pypi.tuna.tsinghua.edu.cn/simple opencv-python
sudo pip3 install -i https://pypi.tuna.tsinghua.edu.cn/simple opencv-contrib-python

