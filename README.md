# linux-useful-aliases

> Usefull aliases for linux terminal

### Better basics

##### Faster clear command

`alias c="clear"`

##### Opens the file explorer in the current directory

`alias o="xdg-open ."`


---

### Git better log command

`git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"`

---

### ROS2 aliases

##### Build and source

`alias cb="colcon build && source install/setup.bash"`

##### Clean build and source

`alias cbc="rm -rf /build /log /install && colcon build && source install/setup.bash"`

---

### Docker Aliases
Make sure you are using the docker.io build from apt

`export CURRENT_CONTAINER="CONTAINER_NAME_HERE"`

`export BUILD_NAME="BUILD_NAME_HERE"`

To build with docker, run the following to set a name (in the directory with the Dockerfile)
`sudo docker build -t BUILD_NAME_HERE:VERSION_HERE`
creates an image, one time use if Dockerfile is unchanged

##### Save changes to image

`alias save='sudo docker commit $CURRENT_CONTAINER $BUILD_NAME'`

##### Enter containers bash

`alias enter='sudo docker exec -it $CURRENT_CONTAINER bash'`

##### Open the container with network access and file access

`alias run='sudo docker run -it -d --dns 10.0.0.1 --net=host --name $CURRENT_CONTAINER --privileged $BUILD_NAME'`

##### Close the container and prune it

`alias close='sudo docker kill multisense && docker container prune -f'`

##### Faster prune command

`alias prune='sudo docker container prune -f'`

---

### Misc. aliases

`alias py="python3"`
