# 一、docker基本命令  
----
### 1、docker images    
查看所有docker镜像  

----   

### 2、docker pull docker_image_name    
下载一个名字叫做docker_image_name的新镜像到本地  

-----

### 3、docker ps 
 
查看目前存活的docker容器实例  
`docker ps -a`  表示查看所有的docker容器   

----

### 4、docker run -it --name self_def_name -v path1:path2 docker_image_name:tag /bin/bash
上述命令是根据docker_image_name这个docker镜像新建一个docker容器  
（1）--name self_def_name 是自定义的docker容器的名字  
（2）-v 是挂载实际path1到docker容器中path2的意思   
（3）-it 是交互式新建的意思，具体意思查看help  
（4） --device 是制定挂载的外设，比如 --device /dev/nvidia0:/dev/nvidia0 意思就是将nvidia0显卡挂载到docker   

-----

### 5、docker stop docker_name  
stop目前存活的docker容器  

----

### 6、docker start docker_name  
将挂起的docker容器重新保持alive状态  

----

### 7、docker exec -it docker_name /bin/bash  
bash交互式运行alive状态的docker容器，如果容器是挂起状态的，需要先start  

----

### 8、exit  
退出当前docker容器    

----

### 9、docker search docker_image_name  
查找docker镜像有两种方式  
（1）一种是去Docker Hub([https://hub.docker.com/])网站查找镜像  
（2）第二种是docker search命令来查找     

---

#### [next page](second_page.md)   


--- 

### Reference   
[https://zhuanlan.zhihu.com/p/23599229]   
[https://yeasy.gitbook.io/docker_practice/]  

