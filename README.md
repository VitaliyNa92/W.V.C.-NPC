# W.V.C.-NPC
Working Virtual Class NPC

# DockerFile

`FROM debian`
  
`RUN apt update \`  
  `&& apt install wget -y \`  
 	`&& wget https://zoom.us/client/latest/zoom_amd64.deb \`  
 	`&& dpkg -i zoom_amd64.deb \`  
  `|| apt install -f -y`  
   
`CMD zoom`

# Build Dockerfile

> docker build .
 
# HOST - [ubuntu, debian ... ]
 
 > sudo xhost +SI:localuser:root 

# START DOCKER > ZOOM
 
 in the terminal
 > docker run --name имя_контейнера -it -e DISPLAY=$DISPLAY --net=host название_образа
  
 example 
 > docker run --name debian  -it -e DISPLAY=$DISPLAY --net=host 4j313b1hk 
