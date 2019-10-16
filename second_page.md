# docker进阶  
----
### 1、docker commit  
----
更新docker镜像使用commit命令，有点像git commit -m "your message"  
例如：  
docker commit -m="message" -a="author" docker_id(docker_name) docker_image_name:tag  
（1）"message"是你这一次提交的描述信息  
（2）使用docker_id或者docker_name都可以，这两个东西是一一对应的（如果有docker name的话），但是docker name明显比较方便  
（3）docker_image:tag是指要创建的目标镜像名字，其实更新docker镜像相当与新建了一个

### 2、Dockerfile  
----
如果需要从零开始构建    
