# nvidia-docker  
nvidia-docker是英伟达专门为在docker中利用GPU创建的docker工具，docker本身是面向CPU的，没有办法直接利用GPU，所以英伟达在docker的基础上进行了包装，通过挂载device和内置nvcc、cuda等来实现对显卡的利用    

# 1、安装docker-ce   
安装nvidia-docker需要先安装docker-ce  
（1）卸载原来安装的docker  
（2）安装docker-ce   

若中间存在问题，则关掉终端重新链接服务器试试   

----   

# 2、安装nvidia-docker   
（1）卸载原来的nvidia-docker及其它GPU容器  

若中间存在问题，则关掉终端重新链接服务器试试   

-----  

# 3、拉取nvidia/cuda镜像   
去docker-hub中寻找合适的nvidia/cuda镜像  
（1）10.1-cudnn7-devel-ubuntu16.04和10.1-cudnn7-runtime-ubuntu16.04的区别  
devel容器更大，里面有cudnn，不需要重新安装，runtime中没有cudnn  

（2）nvidia-docker pull nvidia/cuda:10.1-cudnn7-devel-ubuntu16.04   
建议不要从官网拉取镜像，官网很慢，建议更改源到阿里云或者中科院的源   

[添加阿里云镜像源指南1](https://blog.csdn.net/qq_28612967/article/details/102838808)   

-----  

# 4、构建nvidia/cuda容器   
（1）nvidia-docker run -it --name=nvidia_docker1 --runtime=nvidia -v /home/macong:/home/macong nvidia/cuda:10.1-cudnn7-devel-ubuntu16.04 /bin/bash   
- run命令构建docker容器  
- name指定容器名字  
- runtimex必须指定是nvidia  
- v代表挂载目录  


----   

# 可能遇到的问题   
（1）/bin/bash找不到的问题  
可能docker容器里面没有这个命令，没有安装基础的bash，所以需要拉取一个有bash的docker   

----   

#### [next page](first_page.md)   

-----   

# Reference  
[知乎教程](https://zhuanlan.zhihu.com/p/88351963)   
[nvidia-docker2安装教程博客](https://blog.csdn.net/quantum7/article/details/86416600)   

