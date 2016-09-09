# Bigdata class的vagrant配置
## 如何部署
1. 找一个合适的位置，在`git bash`中运行`git clone https://github.com/IornL/Vagrant-for-bigdata-class`,这个命令会从远程仓库中下载vagrantfile等文件，没有特殊说明，下面步骤中的命令都在Git bash中运行
2. 进入刚刚clone下来的文件夹`Vagrant-for-bigdata-class`
3. 运行`vagrant up`,部署虚拟机
4. 运行`vagrant ssh`，通过SSH进入虚拟机
5. `sudo curl -sSL https://get.docker.com (https://get.docker.com/) | sh`，安装Docker
6. [参考这里配置Hadoop](https://github.com/ninechapter/hadoop-cluster-docker)  
## 如何在Docker的`root/src`中得到实机的文件
将代码放入`src`文件夹中(这个文件夹在第二步进入的文件夹中)， 会自动映射到Docker的 `root/src`中
## 对于之前已经配置好vagrant的同学，如何实现映射
1. 找个另外的地方clone下代码后用里面的文件覆盖掉原来的文件
2. 在`git bash`中运行 vagrant reload
## 常见问题
- `vagrant up`或`vagrant reload` 红字提示如下
```Failed to mount folders in Linux guest. This is usually because
    the "vboxsf" file system is not available. Please verify that
    the guest additions are properly installed in the guest and
    can work properly. The command attempted was:
```  
### 解决方法
在git bash中输入`vagrant plugin install vagrant-vbguest`
- 欢迎补充
