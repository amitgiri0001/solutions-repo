# Delete all containers

docker rm $(docker ps -a -q)

# Delete all images

docker rmi $(docker images -q)

# docker network
 docker network ls

# docker grep container(all, both running and steady) by name
 docker ps -a | grep <container name>
 
# restart conatiner   
 docker restart <container-id>
 
# docker log on container
 docker logs <container-id>

# docker container tree with dependency
 pstree -pa | less
 pstree -pa | grep elastic

# get occupied port
 netstat -pa 
 netstat -pa  | grep 9200
