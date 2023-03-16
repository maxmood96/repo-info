## `ros:noetic-perception`

```console
$ docker pull ros@sha256:7a2a28827571d9b99ccae998d72566029852f2107abf1c152029885bee8c6e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:96fd163c12a7b98719686f7e2bd2254c72b8113f23c563f305a92e01cffdc4c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.1 MB (835137037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a90707807cb54af5c80b8e1afcaa6d3dde3e7b431af07f0be2cf5fd44597483`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:41:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:41:26 GMT
ADD file:20f2ff22b9a8ca9bec5178036c9ebc525a12cd4312daf5d14a9a631a30be20e1 in / 
# Wed, 08 Mar 2023 04:41:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:03:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:09:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:09:04 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 16 Mar 2023 04:09:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 16 Mar 2023 04:09:05 GMT
ENV LANG=C.UTF-8
# Thu, 16 Mar 2023 04:09:05 GMT
ENV LC_ALL=C.UTF-8
# Thu, 16 Mar 2023 04:09:06 GMT
ENV ROS_DISTRO=noetic
# Thu, 16 Mar 2023 04:11:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:11:04 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 16 Mar 2023 04:11:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 16 Mar 2023 04:11:04 GMT
CMD ["bash"]
# Thu, 16 Mar 2023 04:11:43 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:11:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 16 Mar 2023 04:13:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:19:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5544ebdc0c7b82aa6901eae124b1d220914d2629a9bde25396d7ee9cfd273a8f`  
		Last Modified: Wed, 08 Mar 2023 09:02:58 GMT  
		Size: 28.6 MB (28578068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03a3bf9c2e8661d0de58d4a85390b5a17d80f3abf64250efc0769650aa9ab69`  
		Last Modified: Thu, 16 Mar 2023 03:13:05 GMT  
		Size: 1.2 MB (1154522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd341efe0542b6414a62580c02a19287b22de0f35bfdd76fb24d84ae342511e`  
		Last Modified: Thu, 16 Mar 2023 04:43:26 GMT  
		Size: 5.6 MB (5553614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1adae176e5cd2a30cf1122ee112b4b721b01ea9b4c0ac5e541d66c07aaaec48`  
		Last Modified: Thu, 16 Mar 2023 04:43:25 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0adccda1b6439c0a801a24fa60738b89782e4c7193200f6f27ce29713715eb56`  
		Last Modified: Thu, 16 Mar 2023 04:43:25 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82508576a99a0a8d8797589d2c709fa671510864b5270428799fc45a75007041`  
		Last Modified: Thu, 16 Mar 2023 04:43:53 GMT  
		Size: 177.0 MB (177011633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581df5fa2a83d010d48e7b47f737a951bda847f9ee5c724e9ccc3856cf28ee08`  
		Last Modified: Thu, 16 Mar 2023 04:43:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32822115c02183cc93979e5eb6530d84df2e5871996db9b7dc7c65443966bf1`  
		Last Modified: Thu, 16 Mar 2023 04:44:11 GMT  
		Size: 50.9 MB (50940109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d2b3f91c40b14acd615fbc7eb23e2ae46a9e339e795fc221fdc21561270f58`  
		Last Modified: Thu, 16 Mar 2023 04:44:03 GMT  
		Size: 317.4 KB (317353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304ec1393d4ab6577989c766d2b4172d18d06a2d05bc1685889432e70a066f40`  
		Last Modified: Thu, 16 Mar 2023 04:44:15 GMT  
		Size: 79.6 MB (79606953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abaa602089cfc9a551e4c6c4314ef7fd36039fd36229a50dfd4a220a9ea30d5d`  
		Last Modified: Thu, 16 Mar 2023 04:45:49 GMT  
		Size: 492.0 MB (491972372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:5d712eee029d47a123de2fe7bcec5f7c0e875c3025bc80b7d54a80112df0f2d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.2 MB (726168090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5512c37a43ed1d0f691ed805b8439660ea4acb411e6a500894893f74530f589e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:31:46 GMT
ADD file:99d501af7a191308f8fe3dc3f33c63bd8b54fb749d061b1a901c423b85f8cec2 in / 
# Wed, 08 Mar 2023 04:31:46 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:25:18 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:25:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:25:24 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 16 Mar 2023 03:25:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 16 Mar 2023 03:25:25 GMT
ENV LANG=C.UTF-8
# Thu, 16 Mar 2023 03:25:25 GMT
ENV LC_ALL=C.UTF-8
# Thu, 16 Mar 2023 03:25:25 GMT
ENV ROS_DISTRO=noetic
# Thu, 16 Mar 2023 03:27:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:27:54 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 16 Mar 2023 03:27:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 16 Mar 2023 03:27:55 GMT
CMD ["bash"]
# Thu, 16 Mar 2023 03:28:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:28:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 16 Mar 2023 03:29:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:38:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5806a4b978689b82c0b1e370978a89d1fb81519414294a062ee8cdaae68d4cf9`  
		Last Modified: Thu, 09 Mar 2023 05:45:04 GMT  
		Size: 24.6 MB (24586482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07a04d14911f425c252acad00ad16f68336179fdb2bd057ecbc008654d4a9dc`  
		Last Modified: Thu, 16 Mar 2023 03:41:09 GMT  
		Size: 1.2 MB (1154620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3bf1f4e2e473ac685bd824bf2830576a48ab98791369a09fea2d0dbd4a929f`  
		Last Modified: Thu, 16 Mar 2023 03:41:07 GMT  
		Size: 4.7 MB (4679050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca6ed9de687ca448ae7407bb48c22de4deda7d30a973cef11a4b6d8d8fb38e7`  
		Last Modified: Thu, 16 Mar 2023 03:41:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fa126a480cce3f126ceba011ffee67346db673365bb738950073ba2ba74783`  
		Last Modified: Thu, 16 Mar 2023 03:41:07 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0c85b3c21b15d3eb1f9e6b0b89b695ba25d60a4591c501019a1276bc0fd1e5`  
		Last Modified: Thu, 16 Mar 2023 03:41:35 GMT  
		Size: 157.5 MB (157508946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5015ee579e11221f21424f6a032081a7ccc05e90c3115b747cd39125644bd52f`  
		Last Modified: Thu, 16 Mar 2023 03:41:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502398c5b962c956411f0c9bb61dc5d8cb53a75a822beab1a67338a6040844da`  
		Last Modified: Thu, 16 Mar 2023 03:41:51 GMT  
		Size: 40.5 MB (40502661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4016c5932fe61d99fdb58e6cc4986e20a201b4c0ebac799059f2dd4d5f430ab`  
		Last Modified: Thu, 16 Mar 2023 03:41:46 GMT  
		Size: 317.3 KB (317345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5a37a447e1f58827e4f91f66e94e8e7a186d73e26aed5bd96060931f145801`  
		Last Modified: Thu, 16 Mar 2023 03:41:55 GMT  
		Size: 60.5 MB (60496457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b343405c024c81c76c2c966618c8481c0c72a9e06d4e2224ce21057a8d82adf`  
		Last Modified: Thu, 16 Mar 2023 03:43:21 GMT  
		Size: 436.9 MB (436920118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:aed092d7100de07fd7543975f1ad590fec1fcb887b86dbf59943d5cecb560ab7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.4 MB (785439188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27e47e27f2d7226090a303ab88411198eaf7d451074be86bccec15bfc4e7d77`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:10:11 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:10:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:10:21 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 16 Mar 2023 03:10:22 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 16 Mar 2023 03:10:22 GMT
ENV LANG=C.UTF-8
# Thu, 16 Mar 2023 03:10:22 GMT
ENV LC_ALL=C.UTF-8
# Thu, 16 Mar 2023 03:10:22 GMT
ENV ROS_DISTRO=noetic
# Thu, 16 Mar 2023 03:12:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:12:47 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 16 Mar 2023 03:12:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 16 Mar 2023 03:12:47 GMT
CMD ["bash"]
# Thu, 16 Mar 2023 03:13:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:13:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 16 Mar 2023 03:14:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:22:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c235c7a3c272479c47e3fdeef457877dd1bce12f4b4d8726aeb2b8e16d6acae4`  
		Last Modified: Thu, 16 Mar 2023 03:46:17 GMT  
		Size: 1.2 MB (1155462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25e62e51f71a010b6fdbdb16725b3bbfca6a13fca1e447d14e311d361db90f4`  
		Last Modified: Thu, 16 Mar 2023 03:46:15 GMT  
		Size: 5.5 MB (5532807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b33d380951389d9d1ce91514fb73e120ca3b974c248cd2f314992c3465b2b9`  
		Last Modified: Thu, 16 Mar 2023 03:46:15 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fbfba233f21202f1db01a89b8102baef60e3122f36c4d66830892d50d49066`  
		Last Modified: Thu, 16 Mar 2023 03:46:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e709008824e0a6b98c808a5f0f85b444a3e58e2c5b46f6addc72a67e87ae918`  
		Last Modified: Thu, 16 Mar 2023 03:46:40 GMT  
		Size: 171.5 MB (171493131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111abfb9fbc2b0549a5f36a5dfe15229955477056115fe93d5630e6dcbf67970`  
		Last Modified: Thu, 16 Mar 2023 03:46:15 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2d073551834d896f537facf3e35341eb2ab136a5aaf7fb5c935c3bb5c7126e`  
		Last Modified: Thu, 16 Mar 2023 03:46:55 GMT  
		Size: 45.2 MB (45203778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518a989d6dba523fd6a7f2604b03c29146262b03f347c30dfd5e306f8de1c10c`  
		Last Modified: Thu, 16 Mar 2023 03:46:50 GMT  
		Size: 317.4 KB (317350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17de9a769b38ea53a05082bc632c3a08673f269fff61bb683575c1ef260f8862`  
		Last Modified: Thu, 16 Mar 2023 03:47:00 GMT  
		Size: 72.0 MB (71974610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c222849614ae4a8fe5d83b4fe2e00757edc0d9d8c21a6d2b2500dff1c7d1bddb`  
		Last Modified: Thu, 16 Mar 2023 03:48:17 GMT  
		Size: 462.6 MB (462563476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
