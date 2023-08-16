## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:27637101de8a2a5188fff5ce6115c046ac3251f85ea81c3bdf661da300d205ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:79355f8f337bde9a35328ba7420e384bce739fd7d7b5b7ade27b59b15c6334c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263166132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8dfee577ee17a0c0e4684c4ec3da6340c072da1c3969377404d15e3526aec12`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:48:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:48:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:48:30 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 04 Jul 2023 19:48:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:48:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:48:31 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:48:31 GMT
ENV ROS_DISTRO=humble
# Tue, 04 Jul 2023 19:50:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:50:04 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 19:50:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:50:04 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 19:51:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:51:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 19:51:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 04 Jul 2023 19:52:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b96b181e03e7c00f9ff313a35cb309648ea7a63a12165e78d4298df8d842ef7`  
		Last Modified: Tue, 04 Jul 2023 20:09:20 GMT  
		Size: 1.2 MB (1213029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981b99f5f99f37d026fe791185912ef266fd67d841915968d7f58e1e21aa67dd`  
		Last Modified: Tue, 04 Jul 2023 20:09:18 GMT  
		Size: 3.8 MB (3828864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457911032da59063f35f0ed9962d1f7235ab9b54c6a1b2434538945c43049d6d`  
		Last Modified: Tue, 04 Jul 2023 20:09:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca97964148324558ddeb21e9e1395cff5cbcb0443e2d4b59209fa6930ea226d`  
		Last Modified: Tue, 04 Jul 2023 20:09:18 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd524cf7754594d911fa06358015cf1327cb43355eb465f630a366e97dedef5b`  
		Last Modified: Tue, 04 Jul 2023 20:09:34 GMT  
		Size: 106.3 MB (106344539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a0ac1a73dab9eca6d1d3cb5656032709291067b9f54a573c4a4730296d262b`  
		Last Modified: Tue, 04 Jul 2023 20:09:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b3c2bf65a5f88854a4e9b3c40f16e67b119af543d6656867ff27174e1d8f45`  
		Last Modified: Tue, 04 Jul 2023 20:09:55 GMT  
		Size: 97.9 MB (97949653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fd7ea32c23c962d34cd70e32ac496fa75bc603430e4b70172a78380d217e5d`  
		Last Modified: Tue, 04 Jul 2023 20:09:42 GMT  
		Size: 307.1 KB (307140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773f4fc51f45ba73bbf97b10b39b54b7e6b43063a0e37c48e847b48a62a4bf11`  
		Last Modified: Tue, 04 Jul 2023 20:09:42 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dbf8cf19eabafc2081cdee9cc9873550fd53aac2bcdc52b1cccca47f3b7976`  
		Last Modified: Tue, 04 Jul 2023 20:09:46 GMT  
		Size: 23.1 MB (23086815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5151e74dfba7897ee5fd08461fca273ce8889b464f444805bc39f9636849ac89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256054346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61115bc3f20c79765b431c77ffe1423e3c308450d037fdaff6078cef19b34f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 15:16:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:16:39 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:16:40 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 16 Aug 2023 15:16:41 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 16 Aug 2023 15:16:41 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 15:16:41 GMT
ENV LC_ALL=C.UTF-8
# Wed, 16 Aug 2023 15:16:41 GMT
ENV ROS_DISTRO=humble
# Wed, 16 Aug 2023 15:18:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:18:11 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 16 Aug 2023 15:18:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:18:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:18:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:18:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 16 Aug 2023 15:18:55 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 16 Aug 2023 15:19:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeb23ce0adf8021e5f112c4ebb6b7985390219367991abf52dc7c9e4a59d4e5`  
		Last Modified: Wed, 16 Aug 2023 15:38:58 GMT  
		Size: 1.2 MB (1214567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9e5d7e79405f9ead5346e83d4f49c73608d784a30ccea5e9f0a1cb44319e56`  
		Last Modified: Wed, 16 Aug 2023 15:38:56 GMT  
		Size: 3.8 MB (3801963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61556f61e2363012e91a6b26a6d4854861844ae4d453b2e94e69a8cedb8bd75c`  
		Last Modified: Wed, 16 Aug 2023 15:38:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341a3b77ddbf45ba0b2711355c528b654f522ef0e6f08211fb17a01e1d8cc114`  
		Last Modified: Wed, 16 Aug 2023 15:38:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8d16cf4626b88f51269b779ec210c233b939c6fd312ef437d166e1d21de979`  
		Last Modified: Wed, 16 Aug 2023 15:39:08 GMT  
		Size: 104.1 MB (104134081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10891661248957cb4be16727c1a8f8182ff1cc1b5b3cc48fe93960c67ba2c66a`  
		Last Modified: Wed, 16 Aug 2023 15:38:55 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0ac3e8cac74e1c854de60590856f113ce6a795b527e66d55b2f84d12e3565e`  
		Last Modified: Wed, 16 Aug 2023 15:39:26 GMT  
		Size: 95.7 MB (95678087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e92a56ea84860698ec58149a4616bc24133ef8fd7d3cc842f244ec69c49bac`  
		Last Modified: Wed, 16 Aug 2023 15:39:17 GMT  
		Size: 312.3 KB (312347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6321eb63ce71fb3fd53382203bd04e0a821c008f42307883f01deac328bc09`  
		Last Modified: Wed, 16 Aug 2023 15:39:17 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52895b11f4900195a192aa49e100f07c8f48957f21293a0c1e7058358307f8ef`  
		Last Modified: Wed, 16 Aug 2023 15:39:19 GMT  
		Size: 22.5 MB (22516550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
