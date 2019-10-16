# 一、docker基本命令  
----
### 1、docker images    
----
查看所有docker镜像  

### 2、docker ps
----
查看目前存活的docker容器实例  
`docker ps -a`  表示查看所有的docker容器  

### 3、docker run -it --name self_def_name -v path1:path2 docker_image_name:tag /bin/bash  
-----
上述命令是根据docker_image_name这个docker镜像新建一个docker容器，self_def_name是自定义的docker容器的名字，-v 是挂载实际path1到docker容器中path2的意思，-it是交互式新建的意思，具体意思查看help  

### 4、docker stop docker_name  
-----
stop目前存活的docker容器  

### 5、docker start docker_name  
----
将挂起的docker容器重新保持alive状态  

### 6、docker exec -it docker_name /bin/bash  
----
运行alive状态的docker容器，如果容器是挂起状态的，需要先start  

### 7、docker pull docker_image_name  
----
下载一个名字叫做docker_image_name的新镜像到本地  

### 8、docker search docker_image_name  
----
查找docker镜像有两种方式，一种是去Docker Hub([https://hub.docker.com/])网站查找镜像，第二种是docker search命令来查找   

#### next page[]
