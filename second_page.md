# 二、docker进阶  
----
### 1、docker commit  
----
更新docker镜像使用commit命令，有点像git commit -m "your message"  
例如：  
docker commit -m="message" -a="author" docker_id(docker_name) docker_image_name:tag  
（1）-m="message" 是你这一次提交的描述信息   
（2）-a=""author" 是指明提交作者  
（2）使用docker_id或者docker_name都可以，这两个东西是一一对应的（如果有docker name的话），但是docker name明显比较方便  
（3）docker_image:tag是指要创建的目标镜像名字，其实更新docker镜像相当于新建了一个docker镜像  

### 2、docker build    
----
如果需要从零开始构建一个docker镜像，需要使用docker build命令并配合Dockerfile文件来创建  
示例：  
docker build -t docker_image_name Dockerfile_path  
（1） -t 指明新建的docker镜像名称  
（2）Dockerfile_path是指代Dockerfile的**绝对路径**  

### 3、Todo  
---
