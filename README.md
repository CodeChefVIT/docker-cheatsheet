<p align="center"><img width="90%" src="/banner.jpg"/></p>

# :star: Docker Cheatsheet  :star:

This Repository is a guide to all the Docker CLI commands you need to use in case any of these situations arise

## Index :books:
* [Create Container :sparkles:](#create-containers-sparkles)
* [Start Container :running:](#start-container-running)
* [Stop Running :red_circle:](#stop-running-container-red_circle)
* [Container Management :briefcase:](#container-management-briefcase)
* [Logs :page_with_curl:](#logs-page_with_curl)
* [DOCKERFILE :whale:](#dockerfile-whale)

<br>

## Create Containers :sparkles:

- ### Create container from image and start it
```sh
> docker container run <image name>
```
NOTE: *Replace ```<image name>``` with required image name ignoring <>*

<br>

- ### Create container from image but not run it
```sh
> docker container create <image name>
```
NOTE: *Replace ```<image name>``` with required image name ignoring <>*

<br>

**[⬆ Back to Index](#index-books)**

<br>

## Start Container :running:

- ### Start container which is currently not running
```sh
> docker container start <container id>
```
NOTE: *Replace ```<container id>``` with target container id ignoring <>*

<br>

- ### Start container which is currently not running and show output
```sh
> docker container start -a <container id>
```
NOTE: *Replace ```<container id>``` with target container id ignoring <>*

<br>

- ### Start container with shell access (*ssh style*)
```sh
> docker container run -it <container_id> sh
```
NOTE: *Replace ```<container_id>``` with target container id ignoring <>*

<br>

- ### Start container with port mapping
```sh
> docker container run -p <to_port:from_port> <image_name>
```
NOTE: *Replace ```<image_name>``` with target image name and replace ```to_port``` with the port you want to access from your machine and replace ```from_port``` with the port in which the container uses*
*Ignore ```<>```*

<br>

**[⬆ Back to Index](#index-books)**

<br>

## Stop Running Container :red_circle:

- ### Stop container after executing
```sh
> docker container stop <container id>
```
NOTE: *Replace ```<container id>``` with target container id ignoring <>*

<br>

- ### Intstantly terminate running container (force stop)
```sh
> docker container kill <container id>
```
NOTE: *Replace ```<container id>``` with target container id ignoring <>*

<br>

**[⬆ Back to Index](#index-books)**

<br>

## Container Management :briefcase:

- ### View list of all running containers
```sh
> docker container ls
```
NOTE: *Add parameter ```-a``` to list all containers ever created*

<br>

- ### Remove all stopped containers from list
```sh
> docker system prune
```

<br>

- ### Clear list
```sh
> docker system prune --all
```

<br>

- ### Remove specific container from list
```sh
> docker container rm <continer_id>
```
NOTE: *Replace ```<container_id>``` with target container id ignoring <>*
*This might fail if the container is currently running. In that case view force delete command below*

<br>

- ### Force delete container from list
```sh
> docker container rm -f <container_id>
```
NOTE: *Replace ```<container_id>``` with target container id ignoring <>*

<br>

**[⬆ Back to Index](#index-books)**

<br>

## Logs :page_with_curl:

- ### View specific container logs
```sh
> docker container logs <container id>
```
NOTE: *Replace ```<container id>``` with target container id ignoring <>*

<br>

**[⬆ Back to Index](#index-books)**

<br>

## Dockerfile :whale:

- ### Set base image
```sh
FROM <image>
```

NOTE: *Replace ```<image>``` with base image*

<br>

- ### Set Author Name
```sh
MAINTAINER <name>
```

NOTE: *Replace ```<name>``` with the name you want to set for the author field*

<br>

- ### Execute shell command

```sh
RUN <command>
```

NOTE: *Replace ```<command>``` with the command you want to execute on the containers shell*

<br>

[Click here](https://github.com/CodeChefVIT/Docker-deployment-templates) to visit the repository containing language and framework specific templates for docker and docker compose

**[⬆ Back to Index](#index-books)**

<br>

## Contributors

<table>
	<tr align="center" style="font-weight:bold">
		<td>
      <p>
		Gowtham Karthikeyan
        </p>
		<p align="center">
			<img src = "https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgXVvViVaEUfbiTgGxPyB15LN_y3SwJBMBfUmwnNHe1Q9K76y7d2VRJzxXwNyILNqlUFL07Op3hY1kr0n1-5_cFEC5RAlZ2m2eW1l9FXJZ-r7MCIm_jUjIGOr4z1Kb6Sjd_3b7fMVJhmsw3COGi_eZm_029F4ig09e4_B1adWH2c2zkln6VouAr0K6Z/s1600/GK.jpeg" width="150" height="150" alt="Gowtham Karthikeyan">
		</p>
			<p align="center">
				<a href = "https://github.com/inboxsgk">
					<img src = "http://www.iconninja.com/files/241/825/211/round-collaboration-social-github-code-circle-network-icon.svg" width="36" height = "36" alt="GitHub"/>
				</a>
			</p>
		</td>
	</tr>
</table>
