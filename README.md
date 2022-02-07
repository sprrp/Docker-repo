# Docker-repo
Run command for docker:

```
launchctl start com.docker.helper
```
How to check for Docker Client and Docker Server version?
The following command gives you information about Docker Client and Server versions:

`docker version`

How do you get the number of containers running, paused and stopped?
You can use the following command to get detailed information about the docker installed on your system.

`docker info`
You can get the number of containers running, paused, stopped, the number of images and a lot more.

If you vaguely remember the command and you’d like to confirm it, how will you get help on that particular command?
The following command is very useful as it gives you help on how to use a command, the syntax, etc.

`docker --help`

The above command lists all Docker commands. If you need help with one specific command, you can use the following syntax:

`docker <command> --help`

How to login into docker repository?
You can use the following command to login into hub.docker.com:

`docker login`

You’ll be prompted for your username and password, insert those and congratulations, you’re logged in.

If you wish to use a base image and make modifications or personalize it, how do you do that?
You pull an image from docker hub onto your local system

It’s one simple command to pull an image from docker hub:

`docker pull <image_name>`

How do you create a docker container from an image?
Pull an image from docker repository with the above command and run it to create a container. Use the following command:

`docker run -it -d <image_name>`

Most probably the next question would be, what does the ‘-d’ flag mean in the command?

-d means the container needs to start in the detached mode. Explain a little about the detach mode. Have a look at this blog to get a better understanding of different docker commands.

How do you list all the running containers?
The following command lists down all the running containers:

`docker ps`

Suppose you have 3 containers running and out of these, you wish to access one of them. How do you access a running container?
The following command lets us access a running container:

`docker exec -it <container id> bash`

The exec command lets you get inside a container and work with it.

How to start, stop and kill a container?

The following command is used to start a docker container:

`docker start <container_id>`

and the following for stopping a running container:

`docker stop <container_id>`

kill a container with the following command:

`docker kill <container_id>`

Can you use a container, edit it, and update it? Also, how do you make it a new and store it on the local system?
Of course, you can use a container, edit it and update it. This sounds complicated but its actually just one command.

`docker commit <conatainer id> <username/imagename>`

Once you’ve worked with an image, how do you push it to docker hub?

`docker push <username/image name>`

How to delete a stopped container?
Use the following command to delete a stopped container:

`docker rm <container id>`

How to delete an image from the local storage system?
The following command lets you delete an image from the local system:

`docker rmi <image-id>`

How to build a Dockerfile?
Once you’ve written a Dockerfile, you need to build it to create an image with those specifications. Use the following command to build a Dockerfile:

`docker build <path to docker file>`

The next question would be when do you use “.dockerfile_name” and when to use the entire path?

Use “.dockerfile_name” when the dockerfile exits in the same file directory and you use the entire path if it lives somewhere else.

Do you know why docker system prune is used? What does it do?

`docker system prune`

The above command is used to remove all the stopped containers, all the networks that are not used, all dangling images and all build caches. It’s one of the most useful docker commands.


Can I use JSON instead of YAML for my compose file in Docker?
You can use JSON instead of YAML for your compose file, to use JSON file with compose, specify the JSON filename to use, for eg:

`docker-compose -f docker-compose.json up`

Is there a way to identify the status of a Docker container?
There are six possible states a container can be at any given point – Created, Running, Paused, Restarting, Exited, Dead.

Use the following command to check for docker state at any given point:

`docker ps`

The above command lists down only running containers by default. To look for all containers, use the following command:

`docker ps -a`


Is it better to directly remove the container using the rm command or stop the container followed by remove container?
Its always better to stop the container and then remove it using the remove command.

`docker stop <coontainer_id>`
`docker rm -f <container_id>`

