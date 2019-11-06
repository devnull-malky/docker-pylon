[![linuxserver.io](https://raw.githubusercontent.com/linuxserver/docker-templates/master/linuxserver.io/img/linuxserver_medium.png)](https://linuxserver.io)

[![Blog](https://img.shields.io/static/v1.svg?style=flat-square&color=E68523&label=linuxserver.io&message=Blog)](https://blog.linuxserver.io "all the things you can do with our containers including How-To guides, opinions and much more!")
[![Discord](https://img.shields.io/discord/354974912613449730.svg?style=flat-square&color=E68523&label=Discord&logo=discord&logoColor=FFFFFF)](https://discord.gg/YWrKVTn "realtime support / chat with the community and the team.")
[![Discourse](https://img.shields.io/discourse/https/discourse.linuxserver.io/topics.svg?style=flat-square&color=E68523&logo=discourse&logoColor=FFFFFF)](https://discourse.linuxserver.io "post on our community forum.")
[![Fleet](https://img.shields.io/static/v1.svg?style=flat-square&color=E68523&label=linuxserver.io&message=Fleet)](https://fleet.linuxserver.io "an online web interface which displays all of our maintained images.")
[![GitHub](https://img.shields.io/static/v1.svg?style=flat-square&color=E68523&label=linuxserver.io&message=GitHub&logo=github&logoColor=FFFFFF)](https://github.com/linuxserver "view the source for all of our repositories.")
[![Podcast](https://img.shields.io/static/v1.svg?style=flat-square&color=E68523&label=linuxserver.io&message=Podcast)](https://anchor.fm/linuxserverio "on hiatus. Coming back soon (late 2018).")
[![Open Collective](https://img.shields.io/opencollective/all/linuxserver.svg?style=flat-square&color=E68523&label=Supporters&logo=open%20collective&logoColor=FFFFFF)](https://opencollective.com/linuxserver "please consider helping us by either donating or contributing to our budget")

The [LinuxServer.io](https://linuxserver.io) team brings you another container release featuring :-

 * regular and timely application updates
 * easy user mappings (PGID, PUID)
 * custom base image with s6 overlay
 * weekly base OS updates with common layers across the entire LinuxServer.io ecosystem to minimise space usage, down time and bandwidth
 * regular security updates

Find us at:
* [Blog](https://blog.linuxserver.io) - all the things you can do with our containers including How-To guides, opinions and much more!
* [Discord](https://discord.gg/YWrKVTn) - realtime support / chat with the community and the team.
* [Discourse](https://discourse.linuxserver.io) - post on our community forum.
* [Fleet](https://fleet.linuxserver.io) - an online web interface which displays all of our maintained images.
* [GitHub](https://github.com/linuxserver) - view the source for all of our repositories.
* [Podcast](https://anchor.fm/linuxserverio) - on hiatus. Coming back soon (late 2018).
* [Open Collective](https://opencollective.com/linuxserver) - please consider helping us by either donating or contributing to our budget

# [linuxserver/pylon](https://github.com/linuxserver/docker-pylon)

[![GitHub Stars](https://img.shields.io/github/stars/linuxserver/docker-pylon.svg?style=flat-square&color=E68523&logo=github&logoColor=FFFFFF)](https://github.com/linuxserver/docker-pylon)
[![GitHub Release](https://img.shields.io/github/release/linuxserver/docker-pylon.svg?style=flat-square&color=E68523&logo=github&logoColor=FFFFFF)](https://github.com/linuxserver/docker-pylon/releases)
[![GitHub Package Repository](https://img.shields.io/static/v1.svg?style=flat-square&color=E68523&label=linuxserver.io&message=GitHub%20Package&logo=github&logoColor=FFFFFF)](https://github.com/linuxserver/docker-pylon/packages)
[![GitLab Container Registry](https://img.shields.io/static/v1.svg?style=flat-square&color=E68523&label=linuxserver.io&message=GitLab%20Registry&logo=gitlab&logoColor=FFFFFF)](https://gitlab.com/Linuxserver.io/docker-pylon/container_registry)
[![Quay.io](https://img.shields.io/static/v1.svg?style=flat-square&color=E68523&label=linuxserver.io&message=Quay.io)](https://quay.io/repository/linuxserver.io/pylon)
[![MicroBadger Layers](https://img.shields.io/microbadger/layers/linuxserver/pylon.svg?style=flat-square&color=E68523)](https://microbadger.com/images/linuxserver/pylon "Get your own version badge on microbadger.com")
[![Docker Pulls](https://img.shields.io/docker/pulls/linuxserver/pylon.svg?style=flat-square&color=E68523&label=pulls&logo=docker&logoColor=FFFFFF)](https://hub.docker.com/r/linuxserver/pylon)
[![Docker Stars](https://img.shields.io/docker/stars/linuxserver/pylon.svg?style=flat-square&color=E68523&label=stars&logo=docker&logoColor=FFFFFF)](https://hub.docker.com/r/linuxserver/pylon)
[![Build Status](https://ci.linuxserver.io/view/all/job/Docker-Pipeline-Builders/job/docker-pylon/job/master/badge/icon?style=flat-square)](https://ci.linuxserver.io/job/Docker-Pipeline-Builders/job/docker-pylon/job/master/)
[![](https://lsio-ci.ams3.digitaloceanspaces.com/linuxserver/pylon/latest/badge.svg)](https://lsio-ci.ams3.digitaloceanspaces.com/linuxserver/pylon/latest/index.html)

[Pylon](https://github.com/pylonide/pylon) is a web based integrated development environment built with Node.js as a backend and with a supercharged JavaScript/HTML5 frontend, licensed under GPL version 3. This project originates from Cloud9 v2 project.


[![pylon](https://raw.githubusercontent.com/pylonide/pylon/master/doc/screenshot02.png)](https://github.com/pylonide/pylon)

## Supported Architectures

Our images support multiple architectures such as `x86-64`, `arm64` and `armhf`. We utilise the docker manifest for multi-platform awareness. More information is available from docker [here](https://github.com/docker/distribution/blob/master/docs/spec/manifest-v2-2.md#manifest-list) and our announcement [here](https://blog.linuxserver.io/2019/02/21/the-lsio-pipeline-project/).

Simply pulling `linuxserver/pylon` should retrieve the correct image for your arch, but you can also pull specific arch images via tags.

The architectures supported by this image are:

| Architecture | Tag |
| :----: | --- |
| x86-64 | amd64-latest |
| arm64 | arm64v8-latest |
| armhf | arm32v7-latest |


## Usage

Here are some example snippets to help you get started creating a container.

### docker

```
docker create \
  --name=pylon \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Europe/London \
  -e GITURL=https://github.com/linuxserver/docker-pylon.git `#optional` \
  -e PYUSER=myuser `#optional` \
  -e PYPASS=mypass `#optional` \
  -p 3131:3131 \
  -v <path to your code>:/code `#optional` \
  --restart unless-stopped \
  linuxserver/pylon
```


### docker-compose

Compatible with docker-compose v2 schemas.

```
---
version: "2"
services:
  pylon:
    image: linuxserver/pylon
    container_name: pylon
    environment:
      - PUID=1000
      - PGID=1000
      - TZ=Europe/London
      - GITURL=https://github.com/linuxserver/docker-pylon.git #optional
      - PYUSER=myuser #optional
      - PYPASS=mypass #optional
    volumes:
      - <path to your code>:/code #optional
    ports:
      - 3131:3131
    restart: unless-stopped
```

## Parameters

Container images are configured using parameters passed at runtime (such as those above). These parameters are separated by a colon and indicate `<external>:<internal>` respectively. For example, `-p 8080:80` would expose port `80` from inside the container to be accessible from the host's IP on port `8080` outside the container.

| Parameter | Function |
| :----: | --- |
| `-p 3131` | The port for the Pylon web interface |
| `-e PUID=1000` | for UserID - see below for explanation |
| `-e PGID=1000` | for GroupID - see below for explanation |
| `-e TZ=Europe/London` | Specify a timezone to use EG Europe/London |
| `-e GITURL=https://github.com/linuxserver/docker-pylon.git` | Specify a git repo to checkout on first startup |
| `-e PYUSER=myuser` | Specify a basic auth user. |
| `-e PYPASS=mypass` | Specify a basic auth password. |
| `-v /code` | Optionally if you want the bind mount your own code and have changes survive container upgrades. |

## User / Group Identifiers

When using volumes (`-v` flags) permissions issues can arise between the host OS and the container, we avoid this issue by allowing you to specify the user `PUID` and group `PGID`.

Ensure any volume directories on the host are owned by the same user you specify and any permissions issues will vanish like magic.

In this instance `PUID=1000` and `PGID=1000`, to find yours use `id user` as below:

```
  $ id username
    uid=1000(dockeruser) gid=1000(dockergroup) groups=1000(dockergroup)
```


&nbsp;
## Application Setup

Access the webui at http://your-ip:3131, more information [here](https://github.com/pylonide/pylon).



## Support Info

* Shell access whilst the container is running: `docker exec -it pylon /bin/bash`
* To monitor the logs of the container in realtime: `docker logs -f pylon`
* container version number
  * `docker inspect -f '{{ index .Config.Labels "build_version" }}' pylon`
* image version number
  * `docker inspect -f '{{ index .Config.Labels "build_version" }}' linuxserver/pylon`

## Updating Info

Most of our images are static, versioned, and require an image update and container recreation to update the app inside. With some exceptions (ie. nextcloud, plex), we do not recommend or support updating apps inside the container. Please consult the [Application Setup](#application-setup) section above to see if it is recommended for the image.

Below are the instructions for updating containers:

### Via Docker Run/Create
* Update the image: `docker pull linuxserver/pylon`
* Stop the running container: `docker stop pylon`
* Delete the container: `docker rm pylon`
* Recreate a new container with the same docker create parameters as instructed above (if mapped correctly to a host folder, your `/config` folder and settings will be preserved)
* Start the new container: `docker start pylon`
* You can also remove the old dangling images: `docker image prune`

### Via Docker Compose
* Update all images: `docker-compose pull`
  * or update a single image: `docker-compose pull pylon`
* Let compose update all containers as necessary: `docker-compose up -d`
  * or update a single container: `docker-compose up -d pylon`
* You can also remove the old dangling images: `docker image prune`

### Via Watchtower auto-updater (especially useful if you don't remember the original parameters)
* Pull the latest image at its tag and replace it with the same env variables in one run:
  ```
  docker run --rm \
  -v /var/run/docker.sock:/var/run/docker.sock \
  containrrr/watchtower \
  --run-once pylon
  ```

**Note:** We do not endorse the use of Watchtower as a solution to automated updates of existing Docker containers. In fact we generally discourage automated updates. However, this is a useful tool for one-time manual updates of containers where you have forgotten the original parameters. In the long term, we highly recommend using Docker Compose.

* You can also remove the old dangling images: `docker image prune`

## Building locally

If you want to make local modifications to these images for development purposes or just to customize the logic:
```
git clone https://github.com/linuxserver/docker-pylon.git
cd docker-pylon
docker build \
  --no-cache \
  --pull \
  -t linuxserver/pylon:latest .
```

The ARM variants can be built on x86_64 hardware using `multiarch/qemu-user-static`
```
docker run --rm --privileged multiarch/qemu-user-static:register --reset
```

Once registered you can define the dockerfile to use with `-f Dockerfile.aarch64`.

## Versions

* **19.09.19:** - Initial Release.
