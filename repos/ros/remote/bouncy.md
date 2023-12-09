## `ros:bouncy`

```console
$ docker pull ros@sha256:7f75ed7bd17bc17a0f778c1a8743c3e8d73ca3bea88d17fb34b26eec5b4f7308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:bouncy` - linux; amd64

```console
$ docker pull ros@sha256:b5881cc59e37937c097465bae6f12dbdcf3446141d76277795a1f5ff0d9dacd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266791401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c7ae0c82c7e30a355c49784093c01ee1deba2978ad4850d5592cb376f2626dd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
# Sat, 09 Dec 2023 03:40:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:42:13 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:42:14 GMT
RUN echo "deb http://snapshots.ros.org/bouncy/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:42:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:42:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:42:58 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:42:58 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:43:22 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Sat, 09 Dec 2023 03:43:27 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:43:30 GMT
RUN pip3 install -U     argcomplete
# Sat, 09 Dec 2023 03:43:30 GMT
ENV ROS_DISTRO=bouncy
# Sat, 09 Dec 2023 03:44:20 GMT
RUN apt-get update && apt-get install -y     ros-bouncy-ros-core=0.5.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:44:22 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 09 Dec 2023 03:44:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:44:22 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:44:45 GMT
RUN apt-get update && apt-get install -y     ros-bouncy-ros-base=0.5.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:41af1b5f0f51947706ae712999cf098bef968a7799e7cb4bb2268829e62a6ab3`  
		Last Modified: Fri, 02 Jun 2023 00:09:06 GMT  
		Size: 26.7 MB (26717357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a87e4a919bbb35ba9d44fc4cfc4ad95f0e50f0b9f7781c55d60a93226fbadaa`  
		Last Modified: Sat, 09 Dec 2023 04:45:49 GMT  
		Size: 818.9 KB (818901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75db07ca811323aee4149a004b7840679984582866b7ae0c8d6c342da3faecac`  
		Last Modified: Sat, 09 Dec 2023 04:46:08 GMT  
		Size: 159.1 MB (159073267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab09d63566b4f464ced7b9bf02962026021a62c1051d15d43f3a4d7070b7243`  
		Last Modified: Sat, 09 Dec 2023 04:45:46 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1aaf5cbea93f8b7ea9663b2f53c830184eebad3f57d523d0595c98ab36e3d6`  
		Last Modified: Sat, 09 Dec 2023 04:45:46 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c47349301c878c09ccbb7e9f84636b25d002b0e52d42fd52c155588614c314`  
		Last Modified: Sat, 09 Dec 2023 04:45:52 GMT  
		Size: 28.2 MB (28182709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54aaadb34d0cabea2de9877bc88d4457915de16073692b2f9e778393b971c6c6`  
		Last Modified: Sat, 09 Dec 2023 04:45:45 GMT  
		Size: 1.6 MB (1552372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f5c2409ea9d88a532d143d5a2291779fee410321850b3aff3be79e13b71c21`  
		Last Modified: Sat, 09 Dec 2023 04:45:44 GMT  
		Size: 2.6 KB (2556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5ad7a8d9f121dcb95e03d5417a4b627512aad96fb1fe523b0afdac66f89655`  
		Last Modified: Sat, 09 Dec 2023 04:45:44 GMT  
		Size: 321.5 KB (321469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001092c9cf8e93ac17dd03b54608d44a6b1916f08118ca578adb4498dfeda671`  
		Last Modified: Sat, 09 Dec 2023 04:45:57 GMT  
		Size: 47.0 MB (46981629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf967499a05da4727fd41fdcdeb21d3e4e5c6598de5e3cb0471eb4d3d03ac9eb`  
		Last Modified: Sat, 09 Dec 2023 04:45:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e5b66834e5c00166ff97daad18799fcca21f05bcdb25648a8cc2a39b4f2516`  
		Last Modified: Sat, 09 Dec 2023 04:46:18 GMT  
		Size: 3.1 MB (3138300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:bouncy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:54ab7605b8977ad6fc43c48b38101907f23dba7deca41d0098178e1b5234c0e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243824587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f63ea7b7d761332e95b6c6de7088b51c01cebb27644744c2fb62e951f3519e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Sat, 09 Dec 2023 03:05:03 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update && apt-get install -q -y tzdata && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:07:06 GMT
RUN apt-get update && apt-get install -q -y     dirmngr     gnupg2     python3-pip     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:07:09 GMT
RUN echo "deb http://snapshots.ros.org/bouncy/final/ubuntu bionic main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:07:10 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:07:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:07:54 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:07:54 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:08:23 GMT
RUN rosdep init     && rosdep update --include-eol-distros
# Sat, 09 Dec 2023 03:08:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:08:35 GMT
RUN pip3 install -U     argcomplete
# Sat, 09 Dec 2023 03:08:35 GMT
ENV ROS_DISTRO=bouncy
# Sat, 09 Dec 2023 03:09:28 GMT
RUN apt-get update && apt-get install -y     ros-bouncy-ros-core=0.5.1-0*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:09:29 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Sat, 09 Dec 2023 03:09:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:09:29 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:09:45 GMT
RUN apt-get update && apt-get install -y     ros-bouncy-ros-base=0.5.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0cc86ec3df331c06cddc9c328d020ffb34c14bab428cb58722dc03f6982888`  
		Last Modified: Sat, 09 Dec 2023 04:01:36 GMT  
		Size: 819.0 KB (818954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50eb46c25f1edfc37ec8bac2e81e8f79c91edbb61d3c83828b49c8429b82eccd`  
		Last Modified: Sat, 09 Dec 2023 04:01:51 GMT  
		Size: 150.7 MB (150702502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ec34700d99f770020291efe66511637004cb24e515211e4c23d4efc332e0e`  
		Last Modified: Sat, 09 Dec 2023 04:01:34 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7729af233a2dba2f5fcb3b13baddc380d9091db88aa7af40812a8aeffcfc8570`  
		Last Modified: Sat, 09 Dec 2023 04:01:33 GMT  
		Size: 2.4 KB (2405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2530c0945e827ac2c20c8d769f61a17a9397938d4199604cbd7778847688ac51`  
		Last Modified: Sat, 09 Dec 2023 04:01:39 GMT  
		Size: 26.9 MB (26878075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eeeedb0b6bed22a753f6a1c280bfda6767565d4c7eac9d52957b3eb47d6bed`  
		Last Modified: Sat, 09 Dec 2023 04:01:32 GMT  
		Size: 1.6 MB (1552370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512c2d9636d8e8f1478f12a3d0859076bce5f0236122b79a8ba848d9c7a12d40`  
		Last Modified: Sat, 09 Dec 2023 04:01:31 GMT  
		Size: 2.5 KB (2537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8a26d223ab5be28f389bafc53e0f2f429a56b8d9f25ad8c1ad76648204f330`  
		Last Modified: Sat, 09 Dec 2023 04:01:32 GMT  
		Size: 321.6 KB (321571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784a4a51985b006e43aa02f38bfe77e35e24c64f1bfb2cd77c73bd1689cd6c18`  
		Last Modified: Sat, 09 Dec 2023 04:01:42 GMT  
		Size: 36.9 MB (36911798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c689be6b0cc60d79c06dae8facf352d612f158b961ca0915b85ae48ba6a58773`  
		Last Modified: Sat, 09 Dec 2023 04:01:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ad83c9c22092c6781ce6457f28464953a659a17ad695a5d0077209425f1929`  
		Last Modified: Sat, 09 Dec 2023 04:02:01 GMT  
		Size: 2.9 MB (2893045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
