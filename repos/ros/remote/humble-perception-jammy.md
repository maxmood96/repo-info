## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:56138acbbe86f498d2e6ab8472dc83ebea6ab568b2348ac6fed156337b9b74e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:d91c515fe46450f257d09356ae0785cd30983f5b2ca067429f27df7982d94009
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **953.6 MB (953633741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6593ec940b8bf781984ec88689d8d5b6d3ebfecc860260bd35f30e69acee13a6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 09:10:43 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 09:11:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 09:11:04 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 09:11:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 09:11:05 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 09:11:05 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 09:11:05 GMT
ENV ROS_DISTRO=humble
# Fri, 13 Oct 2023 09:12:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 09:12:55 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 09:12:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 09:12:55 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 09:13:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 09:14:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 09:14:07 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 13 Oct 2023 09:14:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 09:23:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88f4f42a82353a9c0283985de717a459b19bfb2efc359c4829a806484d20e81`  
		Last Modified: Fri, 13 Oct 2023 09:33:58 GMT  
		Size: 1.2 MB (1212966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c891fc2128fdc51ff82124d6dd8772e6f15b9d49b492bcffcb32904fad3d37`  
		Last Modified: Fri, 13 Oct 2023 09:33:57 GMT  
		Size: 3.8 MB (3828820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348881bc17ed1b5cc9deae183d10e21fd2c2b23014d9af63f6a686117b20f7ab`  
		Last Modified: Fri, 13 Oct 2023 09:33:56 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d3a94e39139da8a88b5221c31a1e2766e0377f2fe424397759e44d36322beb`  
		Last Modified: Fri, 13 Oct 2023 09:33:56 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6b2e939dfbaac050f695269fed8f78e71c7edfcb69b2bea9454640e59c9e33`  
		Last Modified: Fri, 13 Oct 2023 09:34:12 GMT  
		Size: 106.4 MB (106425018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f412cc149ae7450dcbdd33db4da85f6b0e7cd0e6a56b3969524404cd6d0f86a`  
		Last Modified: Fri, 13 Oct 2023 09:33:56 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbacf3e734a9c9f8200cfb244bdbe56bbd067efa556125fd792d71a9f8b5cfc`  
		Last Modified: Fri, 13 Oct 2023 09:34:33 GMT  
		Size: 98.1 MB (98134043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19f73d6c8c54ac9e58c58bf63a116a0228edfc4fb285fe8b03917d71d6c5b44`  
		Last Modified: Fri, 13 Oct 2023 09:34:20 GMT  
		Size: 319.5 KB (319467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f40e7344f2529219c72c0c4b428336cee0be5de94d227d7b0ed762a0365369`  
		Last Modified: Fri, 13 Oct 2023 09:34:20 GMT  
		Size: 2.5 KB (2484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad05623917e0cc88af8a802dbf6c8ee7e15bb05385a0216d0c4be5c13e4c9051`  
		Last Modified: Fri, 13 Oct 2023 09:34:23 GMT  
		Size: 23.1 MB (23094047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b977c5181da1c0a859692e2b62ecc94debc80a7f45c451d9dbc2950b7355dbc`  
		Last Modified: Fri, 13 Oct 2023 09:36:16 GMT  
		Size: 690.2 MB (690175369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:75716a5acc09696b2d5f8ad6804782f5f6dfb2677f69b358cd0e91aa15d6e4cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.1 MB (914137086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c8f194e90b0756bf36dbf4619c86c30124506ffe90254c9b861055ce34b828`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:38:07 GMT
ENV ROS_DISTRO=humble
# Fri, 13 Oct 2023 04:39:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:39:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:39:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:39:35 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:40:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:40:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:40:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 13 Oct 2023 04:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:50:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c023537795c860c51cdc51a826448aa3f98423714b84b95dea685761f8e013d6`  
		Last Modified: Fri, 13 Oct 2023 05:00:48 GMT  
		Size: 104.2 MB (104151928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfda3e7987bf657d0a886fc085e34ebecaca449450d6b705392eb5c3170fe318`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0a489e10cbdefdd5f5cadbefeb08d5ebd7f0f8888a9aa8868bf249e7ba9498`  
		Last Modified: Fri, 13 Oct 2023 05:01:08 GMT  
		Size: 95.7 MB (95684475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ce9ac65ade437d7a093f3b80dcbc88126a337e45ce69f99234c87019c1bc35`  
		Last Modified: Fri, 13 Oct 2023 05:00:57 GMT  
		Size: 319.3 KB (319340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfb5ed159e80825a9155603a7778bb0cd6f9f024fd0113561edcedd3909b8ed`  
		Last Modified: Fri, 13 Oct 2023 05:00:57 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab14f4c10d226ff941d9d47bc4cef0f2f27c6612233a208ec6a18ac86a96daf`  
		Last Modified: Fri, 13 Oct 2023 05:01:01 GMT  
		Size: 22.5 MB (22516571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7bc1ce33b1d69bab7e7619d5315fe767059a16a897d044c75626a48cd0c209`  
		Last Modified: Fri, 13 Oct 2023 05:02:46 GMT  
		Size: 658.1 MB (658051569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
