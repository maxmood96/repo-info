## `ros:foxy-ros-base`

```console
$ docker pull ros@sha256:3d6b6264663c04faa9b842b99f05ce2b764ebf62d7a8bd78c503807e634141df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:d3ec5672bded3c6013dd0b0e84f9834c27086e0b183ae07c2068a72262707ea0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250919416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e94dae160a999c00d79942337d225c1c58699174b0ecbb07bd746a00ad4502`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jan 2023 13:19:55 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:19:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:19:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:19:55 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:19:57 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Thu, 26 Jan 2023 13:19:57 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 19:29:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:30:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:43:09 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Jan 2023 19:43:10 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Jan 2023 19:43:10 GMT
ENV LANG=C.UTF-8
# Tue, 31 Jan 2023 19:43:10 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Jan 2023 19:43:11 GMT
ENV ROS_DISTRO=foxy
# Tue, 31 Jan 2023 19:44:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:44:11 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 31 Jan 2023 19:44:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Jan 2023 19:44:11 GMT
CMD ["bash"]
# Tue, 31 Jan 2023 19:44:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:44:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Jan 2023 19:44:51 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 31 Jan 2023 19:45:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c07949706a41bd26517c40195af4c4877c4a94497526c106a6293763dc1765b`  
		Last Modified: Tue, 31 Jan 2023 20:08:43 GMT  
		Size: 1.2 MB (1154542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2670e9e05f7f793dd7dbe48fba615b13142ad5665135c312378240da79579b`  
		Last Modified: Tue, 31 Jan 2023 20:08:41 GMT  
		Size: 5.6 MB (5553673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf152e9a4db74f9930ac09483751214af9a1f226e0fb2a2d70369627cb6ddf8`  
		Last Modified: Tue, 31 Jan 2023 20:11:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59cc39066911af026fbfacd58275ced54dc5087430530321ace88cd70eb17d4`  
		Last Modified: Tue, 31 Jan 2023 20:11:16 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53c5af39e4f0d50dd2e34266f9a2a903ddf6ff3fb23360d78ab392d946b5115`  
		Last Modified: Tue, 31 Jan 2023 20:11:36 GMT  
		Size: 120.4 MB (120354163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f77ccef24b2168378b7993b994be148d7ccc81dcc0dd6af02b3498a508ad4a`  
		Last Modified: Tue, 31 Jan 2023 20:11:16 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c587bd24e6d3bd17af2906318935c23cec69372158c04d4c0e2276c45f79a1f8`  
		Last Modified: Tue, 31 Jan 2023 20:11:55 GMT  
		Size: 73.3 MB (73334209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9589f9c9bae39b4cbb571d2095fa9e20972d7bedf34f56c71cb377b234aa7207`  
		Last Modified: Tue, 31 Jan 2023 20:11:45 GMT  
		Size: 277.8 KB (277778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a06edf09eaea7b0d1b06ccd74d1c8af33e67656d5a32341b70f778dfa2fc7e17`  
		Last Modified: Tue, 31 Jan 2023 20:11:45 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20917058504694a3791959dd4dc87db6cd42cf6c632019971eea5c6474b355c2`  
		Last Modified: Tue, 31 Jan 2023 20:11:48 GMT  
		Size: 21.7 MB (21662318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:766d9589b3e39fc91df6bce5b625a442371dab10da8b2f561faf276b2746b73f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226787006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3160e4dfd3e7c217a468d3c9954c507e3d75b0234525dab0b4c5e32900cba769`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 26 Jan 2023 13:50:26 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:50:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:50:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:50:26 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:50:33 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Thu, 26 Jan 2023 13:50:33 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 19:21:57 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:22:10 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:35:41 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Jan 2023 19:35:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Jan 2023 19:35:42 GMT
ENV LANG=C.UTF-8
# Tue, 31 Jan 2023 19:35:42 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Jan 2023 19:35:42 GMT
ENV ROS_DISTRO=foxy
# Tue, 31 Jan 2023 19:36:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:36:36 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 31 Jan 2023 19:36:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Jan 2023 19:36:36 GMT
CMD ["bash"]
# Tue, 31 Jan 2023 19:37:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 19:37:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Jan 2023 19:37:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 31 Jan 2023 19:37:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e6380b087085d9b7d1b6b0f477cb1118d8dc3c23beed89295043bc3b4c7b7d`  
		Last Modified: Tue, 31 Jan 2023 19:59:21 GMT  
		Size: 1.2 MB (1154598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cd0e27783c2fceeab20da4ff5fb069eeabebd04b81c662745ccaf81f8bd59e`  
		Last Modified: Tue, 31 Jan 2023 19:59:19 GMT  
		Size: 5.5 MB (5532024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a354b6ceee7f7b41c047b4c2edd4fd0045ffc756ce42541d1b698664a6055fe`  
		Last Modified: Tue, 31 Jan 2023 20:01:37 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9724c3f6877f10cd7384fc9d5f6de87e8f88a965e8bffd8b1b5ec44f2bb33b0c`  
		Last Modified: Tue, 31 Jan 2023 20:01:37 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047fa9b69c7a14be5b571934ca35b75d2e06be4ed259bdcfebfb95cf7ffc719d`  
		Last Modified: Tue, 31 Jan 2023 20:01:53 GMT  
		Size: 104.6 MB (104557428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0898f38b8edb1eaa71c1c51c59e1c87ade87c2b27c0282ae29bddbf49a0e4c28`  
		Last Modified: Tue, 31 Jan 2023 20:01:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d25843e860f623285954214a4cc16ed71a69039e48ec1ad797e9ba42113448a`  
		Last Modified: Tue, 31 Jan 2023 20:02:10 GMT  
		Size: 67.7 MB (67681766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73aacabc5a79a5799ad79b6b792fa3e74455dee1055cf0ebe2664a513b8265be`  
		Last Modified: Tue, 31 Jan 2023 20:02:01 GMT  
		Size: 277.8 KB (277781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09dc8897f4631566f73404b0629507c381bb183a2e4d09306d2bcd5f922ca1f7`  
		Last Modified: Tue, 31 Jan 2023 20:02:01 GMT  
		Size: 2.4 KB (2427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c37c182aa88b331a17ce6abb19553fbb202118c8d60850325c87e095e7e5625`  
		Last Modified: Tue, 31 Jan 2023 20:02:04 GMT  
		Size: 20.4 MB (20384833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
