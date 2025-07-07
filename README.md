# linux-useful-aliases

> Usefull aliases for linux terminal

### Better basics

##### Faster clear command

```bash
alias c="clear"
```

##### Opens the file explorer in the current directory

```bash
alias o="xdg-open ."
```


---

### Git better log command

```bash
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
```

---

### ROS2 aliases

##### Build and source

```bash
alias cb="colcon build && source install/setup.bash"
```

##### Clean build and source

```bash
alias cbc="rm -rf /build /log /install && colcon build && source install/setup.bash"
```

---

### Docker Aliases
Make sure you are using the docker.io build from apt

```bash
export CURRENT_CONTAINER="CONTAINER_NAME_HERE"
export BUILD_NAME="BUILD_NAME_HERE/VERSION"
alias save='sudo docker commit $CURRENT_CONTAINER $BUILD_NAME'  #Save changes to image
alias enter='sudo docker exec -it $CURRENT_CONTAINER bash'    #Enter containers bash
alias run='sudo docker run -it -d --dns 10.0.0.1 --net=host --name $CURRENT_CONTAINER --privileged $BUILD_NAME'   # Open the container with network access and file access
alias close='sudo docker kill $CURRENT_CONTAINER && sudo docker container prune -f'   # Close the container and prune it
alias prune='sudo docker container prune -f'          # Faster prune command
alias build='sudo docker build -t $BUILD_NAME .'      # for building
```
---

### Misc. aliases

```bash
alias py="python3"
```

## FULL FILE
```bash
alias c="clear"
alias o="xdg-open ."
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
alias cb="colcon build && source install/setup.bash"
alias cbc="rm -rf /build /log /install && colcon build && source install/setup.bash"
alias py="python3"


export CURRENT_CONTAINER="CONTAINER_NAME_HERE"
export BUILD_NAME="BUILD_NAME_HERE/VERSION"
alias save='sudo docker commit $CURRENT_CONTAINER $BUILD_NAME'  #Save changes to image
alias enter='sudo docker exec -it $CURRENT_CONTAINER bash'    #Enter containers bash
alias run='sudo docker run -it -d --dns 10.0.0.1 --net=host --name $CURRENT_CONTAINER --privileged $BUILD_NAME'   # Open the container with network access and file access
alias close='sudo docker kill $CURRENT_CONTAINER && sudo docker container prune -f'   # Close the container and prune it
alias prune='sudo docker container prune -f'          # Faster prune command
alias build='sudo docker build -t $BUILD_NAME .'      # for building
```
