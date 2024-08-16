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

export CURRENT_CONTAINER="CONTAINER_NAME_HERE"

##### Save changes to image

`alias save='docker commit $CURRENT_CONTAINER mackscohn/noetic-multisense:latest'`

##### Enter containers bash

`alias enter='docker exec -it $CURRENT_CONTAINER bash`

##### Open the container with network access and file access

`alias run='docker run -it -d --dns 10.0.0.1 --net=host --name $CURRENT_CONTAINER --privileged mackscohn/noetic-multisense:latest'`

##### Close the container and prune it

`alias close='docker kill multisense && docker container prune -f'`

##### Faster prune command

`alias prune='docker container prune -f'`

---

### Misc. aliases

`alias py="python3"`
