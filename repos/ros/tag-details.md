<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ros`

-	[`ros:humble`](#roshumble)
-	[`ros:humble-perception`](#roshumble-perception)
-	[`ros:humble-perception-jammy`](#roshumble-perception-jammy)
-	[`ros:humble-ros-base`](#roshumble-ros-base)
-	[`ros:humble-ros-base-jammy`](#roshumble-ros-base-jammy)
-	[`ros:humble-ros-core`](#roshumble-ros-core)
-	[`ros:humble-ros-core-jammy`](#roshumble-ros-core-jammy)
-	[`ros:iron`](#rosiron)
-	[`ros:iron-perception`](#rosiron-perception)
-	[`ros:iron-perception-jammy`](#rosiron-perception-jammy)
-	[`ros:iron-ros-base`](#rosiron-ros-base)
-	[`ros:iron-ros-base-jammy`](#rosiron-ros-base-jammy)
-	[`ros:iron-ros-core`](#rosiron-ros-core)
-	[`ros:iron-ros-core-jammy`](#rosiron-ros-core-jammy)
-	[`ros:latest`](#roslatest)
-	[`ros:noetic`](#rosnoetic)
-	[`ros:noetic-perception`](#rosnoetic-perception)
-	[`ros:noetic-perception-focal`](#rosnoetic-perception-focal)
-	[`ros:noetic-robot`](#rosnoetic-robot)
-	[`ros:noetic-robot-focal`](#rosnoetic-robot-focal)
-	[`ros:noetic-ros-base`](#rosnoetic-ros-base)
-	[`ros:noetic-ros-base-focal`](#rosnoetic-ros-base-focal)
-	[`ros:noetic-ros-core`](#rosnoetic-ros-core)
-	[`ros:noetic-ros-core-focal`](#rosnoetic-ros-core-focal)
-	[`ros:rolling`](#rosrolling)
-	[`ros:rolling-perception`](#rosrolling-perception)
-	[`ros:rolling-perception-jammy`](#rosrolling-perception-jammy)
-	[`ros:rolling-ros-base`](#rosrolling-ros-base)
-	[`ros:rolling-ros-base-jammy`](#rosrolling-ros-base-jammy)
-	[`ros:rolling-ros-core`](#rosrolling-ros-core)
-	[`ros:rolling-ros-core-jammy`](#rosrolling-ros-core-jammy)

## `ros:humble`

```console
$ docker pull ros@sha256:27637101de8a2a5188fff5ce6115c046ac3251f85ea81c3bdf661da300d205ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble` - linux; amd64

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

### `ros:humble` - linux; arm64 variant v8

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

## `ros:humble-perception`

```console
$ docker pull ros@sha256:7132be68a9a8f20c961c28d1df24eaf8a61da2c384d5da0a186f0b6279f11f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:82b41e780969c23f7d043aea43000a216f695037655a536543e40d0a1bc1f66f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **952.3 MB (952262558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b69c3990c4c87abf41ddfb4115ee8099badca3699553369402ff1f1bc393fc`
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
# Tue, 04 Jul 2023 19:59:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:5a00e162c60da079b7e4481316e9401c7b4cf0675e2d028c8942809b3a61865c`  
		Last Modified: Tue, 04 Jul 2023 20:11:34 GMT  
		Size: 689.1 MB (689096426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cee1350e58a075e0cc06aec2cd279a869821343ddbfdca37f09ffb7b6ad59af8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.1 MB (914091186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b291c29bfee4d818631af16bc57eba0020571ab61e964a4d0756cee05cf86f2b`
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
# Wed, 16 Aug 2023 15:28:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:96f8ef01ca2e225a1f74d8769d8db4e5558ae4ef63e8042b0b217997556b13e5`  
		Last Modified: Wed, 16 Aug 2023 15:40:59 GMT  
		Size: 658.0 MB (658036840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:7132be68a9a8f20c961c28d1df24eaf8a61da2c384d5da0a186f0b6279f11f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:82b41e780969c23f7d043aea43000a216f695037655a536543e40d0a1bc1f66f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **952.3 MB (952262558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b69c3990c4c87abf41ddfb4115ee8099badca3699553369402ff1f1bc393fc`
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
# Tue, 04 Jul 2023 19:59:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:5a00e162c60da079b7e4481316e9401c7b4cf0675e2d028c8942809b3a61865c`  
		Last Modified: Tue, 04 Jul 2023 20:11:34 GMT  
		Size: 689.1 MB (689096426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cee1350e58a075e0cc06aec2cd279a869821343ddbfdca37f09ffb7b6ad59af8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.1 MB (914091186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b291c29bfee4d818631af16bc57eba0020571ab61e964a4d0756cee05cf86f2b`
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
# Wed, 16 Aug 2023 15:28:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:96f8ef01ca2e225a1f74d8769d8db4e5558ae4ef63e8042b0b217997556b13e5`  
		Last Modified: Wed, 16 Aug 2023 15:40:59 GMT  
		Size: 658.0 MB (658036840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:27637101de8a2a5188fff5ce6115c046ac3251f85ea81c3bdf661da300d205ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base` - linux; amd64

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

### `ros:humble-ros-base` - linux; arm64 variant v8

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

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:8266cc5f19c8960f7c8b02a42272cd83034aa351a319051a5435c71b7c86ac32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:00c01c2ee59af1b7cd0667332f1cc7c8ba5c9dda46a2812412544d086b51f1e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141820076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf8329c1fd5ff5cd43d44cfaa0fe95aa812fe452d280fdec75b035ffb8c7ba5`
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

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5f6465b6c7ec7432ea043f6810f89f5d09acdc6e6665287f4183e4a12b7b82bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137544930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b415d51f1ac13111c78516191c20ceefc8fa19e287ac46c91af846f482439a6`
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

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:8266cc5f19c8960f7c8b02a42272cd83034aa351a319051a5435c71b7c86ac32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:00c01c2ee59af1b7cd0667332f1cc7c8ba5c9dda46a2812412544d086b51f1e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141820076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf8329c1fd5ff5cd43d44cfaa0fe95aa812fe452d280fdec75b035ffb8c7ba5`
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

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5f6465b6c7ec7432ea043f6810f89f5d09acdc6e6665287f4183e4a12b7b82bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137544930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b415d51f1ac13111c78516191c20ceefc8fa19e287ac46c91af846f482439a6`
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

## `ros:iron`

```console
$ docker pull ros@sha256:18d9ac3b698d9a6184a866ea6e69a1164bf542997456a4e9efbccea5f83d813a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron` - linux; amd64

```console
$ docker pull ros@sha256:c0d01ca752cc23ddddb389409680c54fb6c85949c79bc4a3bcdd2a266414a313
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268546213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4bee036752b69abd2271fb9ab494ff987a3923d00c355fc8651896a7dc9b00`
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
# Tue, 04 Jul 2023 19:59:50 GMT
ENV ROS_DISTRO=iron
# Tue, 04 Jul 2023 20:00:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:00:34 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 20:00:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 20:00:34 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 20:00:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:00:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 20:01:02 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 04 Jul 2023 20:01:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:2c215437d76e0aa23ad3ad77eacdff757fb515043d5fbc4aaab262edecf0f570`  
		Last Modified: Tue, 04 Jul 2023 20:12:05 GMT  
		Size: 124.1 MB (124106862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83b7644717ba2f3371d754f83f5d74a18227dd0efa3552b47025bd2bb2e7e92`  
		Last Modified: Tue, 04 Jul 2023 20:11:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199be721033556b61121fd3dc17b7e99b7a7f82492d2272ba5b86f84a9ce7fc2`  
		Last Modified: Tue, 04 Jul 2023 20:12:24 GMT  
		Size: 85.0 MB (84994600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ff985aa05405f2f8956ec07b70eae3f30be79fec5c6d3c1617677f4c3696ac`  
		Last Modified: Tue, 04 Jul 2023 20:12:14 GMT  
		Size: 293.8 KB (293837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4dbbe640a7122ac20768a9e899cd6f765aca885c9d8f66066b241d69c62228`  
		Last Modified: Tue, 04 Jul 2023 20:12:14 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad8cd1c41ec878e1b4d38c0b86b45f871a82ec4c846bc1c940a726af567ffa9`  
		Last Modified: Tue, 04 Jul 2023 20:12:18 GMT  
		Size: 23.7 MB (23672931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:abff66cc26ac456d4f7f24bc13108310663e0f64a9fd24646aa30b2f1ac0e573
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261284786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a339b73410a100e8948f172487e9f0172e70fe9481a4fcf91f19c71521d13`
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
# Wed, 16 Aug 2023 15:29:02 GMT
ENV ROS_DISTRO=iron
# Wed, 16 Aug 2023 15:29:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:29:57 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 16 Aug 2023 15:29:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:29:57 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:30:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:30:26 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 16 Aug 2023 15:30:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 16 Aug 2023 15:30:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:693a5185c6732e5ca8e766ca2be9570243a05e66c9c085ee4d7dd35dacad4a73`  
		Last Modified: Wed, 16 Aug 2023 15:41:25 GMT  
		Size: 121.6 MB (121617636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83726072cbc7db22d58a8f03eb01536572a85fa76caebdd61df6f318ed06ee51`  
		Last Modified: Wed, 16 Aug 2023 15:41:09 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a4eda63942c2c3ef94d99c842b03cebea82f1904a1f5b631974a295b7efe37`  
		Last Modified: Wed, 16 Aug 2023 15:41:44 GMT  
		Size: 82.8 MB (82840931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50080694231be65dd9eaf3724f7526680ccbfc58ba778f355aa132dd315de1e`  
		Last Modified: Wed, 16 Aug 2023 15:41:36 GMT  
		Size: 299.8 KB (299847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e728607890e153ce62f3d6cefe5ea39753687001587d366b4e723b1434db1fb`  
		Last Modified: Wed, 16 Aug 2023 15:41:36 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756195b01fe3a6421f90801c97bc4d09c3ce2918293c47f005d0a8a876793811`  
		Last Modified: Wed, 16 Aug 2023 15:41:39 GMT  
		Size: 23.1 MB (23113110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-perception`

```console
$ docker pull ros@sha256:3da9764c05300a1df1d04c55c83a2a8bef853644da8f224362eae5fc66a35341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception` - linux; amd64

```console
$ docker pull ros@sha256:7a1b415a873cdc2fed92f158280d30a77aae1483aa7306f48fd6e295990ad242
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **958.3 MB (958307590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d38ee7ef24d2408be7fd5721c1c92d6423c39d5d508f9f0f0732a40d730d727`
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
# Tue, 04 Jul 2023 19:59:50 GMT
ENV ROS_DISTRO=iron
# Tue, 04 Jul 2023 20:00:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:00:34 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 20:00:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 20:00:34 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 20:00:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:00:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 20:01:02 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 04 Jul 2023 20:01:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:02:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:2c215437d76e0aa23ad3ad77eacdff757fb515043d5fbc4aaab262edecf0f570`  
		Last Modified: Tue, 04 Jul 2023 20:12:05 GMT  
		Size: 124.1 MB (124106862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83b7644717ba2f3371d754f83f5d74a18227dd0efa3552b47025bd2bb2e7e92`  
		Last Modified: Tue, 04 Jul 2023 20:11:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199be721033556b61121fd3dc17b7e99b7a7f82492d2272ba5b86f84a9ce7fc2`  
		Last Modified: Tue, 04 Jul 2023 20:12:24 GMT  
		Size: 85.0 MB (84994600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ff985aa05405f2f8956ec07b70eae3f30be79fec5c6d3c1617677f4c3696ac`  
		Last Modified: Tue, 04 Jul 2023 20:12:14 GMT  
		Size: 293.8 KB (293837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4dbbe640a7122ac20768a9e899cd6f765aca885c9d8f66066b241d69c62228`  
		Last Modified: Tue, 04 Jul 2023 20:12:14 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad8cd1c41ec878e1b4d38c0b86b45f871a82ec4c846bc1c940a726af567ffa9`  
		Last Modified: Tue, 04 Jul 2023 20:12:18 GMT  
		Size: 23.7 MB (23672931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6249bb59c709d10e886ff3cc6d5c5903cdda2650148c37b11f3d87a283223a`  
		Last Modified: Tue, 04 Jul 2023 20:14:03 GMT  
		Size: 689.8 MB (689761377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6c6b22cca3676a9e096c0071aa1a81ceb5f96bd411edccfea496bc3084b9dedd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.0 MB (919992732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42291219f4047c5d86f54e0338e78813d3e30cdc4d01ab0d2b2e2934e22ccaeb`
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
# Wed, 16 Aug 2023 15:29:02 GMT
ENV ROS_DISTRO=iron
# Wed, 16 Aug 2023 15:29:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:29:57 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 16 Aug 2023 15:29:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:29:57 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:30:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:30:26 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 16 Aug 2023 15:30:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 16 Aug 2023 15:30:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:32:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:693a5185c6732e5ca8e766ca2be9570243a05e66c9c085ee4d7dd35dacad4a73`  
		Last Modified: Wed, 16 Aug 2023 15:41:25 GMT  
		Size: 121.6 MB (121617636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83726072cbc7db22d58a8f03eb01536572a85fa76caebdd61df6f318ed06ee51`  
		Last Modified: Wed, 16 Aug 2023 15:41:09 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a4eda63942c2c3ef94d99c842b03cebea82f1904a1f5b631974a295b7efe37`  
		Last Modified: Wed, 16 Aug 2023 15:41:44 GMT  
		Size: 82.8 MB (82840931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50080694231be65dd9eaf3724f7526680ccbfc58ba778f355aa132dd315de1e`  
		Last Modified: Wed, 16 Aug 2023 15:41:36 GMT  
		Size: 299.8 KB (299847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e728607890e153ce62f3d6cefe5ea39753687001587d366b4e723b1434db1fb`  
		Last Modified: Wed, 16 Aug 2023 15:41:36 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756195b01fe3a6421f90801c97bc4d09c3ce2918293c47f005d0a8a876793811`  
		Last Modified: Wed, 16 Aug 2023 15:41:39 GMT  
		Size: 23.1 MB (23113110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab422a6e606450052042a77b59af848ff8e2da734b662425d1c1c80ec07ac65`  
		Last Modified: Wed, 16 Aug 2023 15:42:58 GMT  
		Size: 658.7 MB (658707946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:3da9764c05300a1df1d04c55c83a2a8bef853644da8f224362eae5fc66a35341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:7a1b415a873cdc2fed92f158280d30a77aae1483aa7306f48fd6e295990ad242
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **958.3 MB (958307590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d38ee7ef24d2408be7fd5721c1c92d6423c39d5d508f9f0f0732a40d730d727`
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
# Tue, 04 Jul 2023 19:59:50 GMT
ENV ROS_DISTRO=iron
# Tue, 04 Jul 2023 20:00:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:00:34 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 20:00:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 20:00:34 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 20:00:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:00:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 20:01:02 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 04 Jul 2023 20:01:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:02:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:2c215437d76e0aa23ad3ad77eacdff757fb515043d5fbc4aaab262edecf0f570`  
		Last Modified: Tue, 04 Jul 2023 20:12:05 GMT  
		Size: 124.1 MB (124106862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83b7644717ba2f3371d754f83f5d74a18227dd0efa3552b47025bd2bb2e7e92`  
		Last Modified: Tue, 04 Jul 2023 20:11:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199be721033556b61121fd3dc17b7e99b7a7f82492d2272ba5b86f84a9ce7fc2`  
		Last Modified: Tue, 04 Jul 2023 20:12:24 GMT  
		Size: 85.0 MB (84994600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ff985aa05405f2f8956ec07b70eae3f30be79fec5c6d3c1617677f4c3696ac`  
		Last Modified: Tue, 04 Jul 2023 20:12:14 GMT  
		Size: 293.8 KB (293837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4dbbe640a7122ac20768a9e899cd6f765aca885c9d8f66066b241d69c62228`  
		Last Modified: Tue, 04 Jul 2023 20:12:14 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad8cd1c41ec878e1b4d38c0b86b45f871a82ec4c846bc1c940a726af567ffa9`  
		Last Modified: Tue, 04 Jul 2023 20:12:18 GMT  
		Size: 23.7 MB (23672931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6249bb59c709d10e886ff3cc6d5c5903cdda2650148c37b11f3d87a283223a`  
		Last Modified: Tue, 04 Jul 2023 20:14:03 GMT  
		Size: 689.8 MB (689761377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6c6b22cca3676a9e096c0071aa1a81ceb5f96bd411edccfea496bc3084b9dedd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.0 MB (919992732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42291219f4047c5d86f54e0338e78813d3e30cdc4d01ab0d2b2e2934e22ccaeb`
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
# Wed, 16 Aug 2023 15:29:02 GMT
ENV ROS_DISTRO=iron
# Wed, 16 Aug 2023 15:29:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:29:57 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 16 Aug 2023 15:29:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:29:57 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:30:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:30:26 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 16 Aug 2023 15:30:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 16 Aug 2023 15:30:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:32:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:693a5185c6732e5ca8e766ca2be9570243a05e66c9c085ee4d7dd35dacad4a73`  
		Last Modified: Wed, 16 Aug 2023 15:41:25 GMT  
		Size: 121.6 MB (121617636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83726072cbc7db22d58a8f03eb01536572a85fa76caebdd61df6f318ed06ee51`  
		Last Modified: Wed, 16 Aug 2023 15:41:09 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a4eda63942c2c3ef94d99c842b03cebea82f1904a1f5b631974a295b7efe37`  
		Last Modified: Wed, 16 Aug 2023 15:41:44 GMT  
		Size: 82.8 MB (82840931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50080694231be65dd9eaf3724f7526680ccbfc58ba778f355aa132dd315de1e`  
		Last Modified: Wed, 16 Aug 2023 15:41:36 GMT  
		Size: 299.8 KB (299847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e728607890e153ce62f3d6cefe5ea39753687001587d366b4e723b1434db1fb`  
		Last Modified: Wed, 16 Aug 2023 15:41:36 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756195b01fe3a6421f90801c97bc4d09c3ce2918293c47f005d0a8a876793811`  
		Last Modified: Wed, 16 Aug 2023 15:41:39 GMT  
		Size: 23.1 MB (23113110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab422a6e606450052042a77b59af848ff8e2da734b662425d1c1c80ec07ac65`  
		Last Modified: Wed, 16 Aug 2023 15:42:58 GMT  
		Size: 658.7 MB (658707946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-base`

```console
$ docker pull ros@sha256:18d9ac3b698d9a6184a866ea6e69a1164bf542997456a4e9efbccea5f83d813a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:c0d01ca752cc23ddddb389409680c54fb6c85949c79bc4a3bcdd2a266414a313
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268546213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4bee036752b69abd2271fb9ab494ff987a3923d00c355fc8651896a7dc9b00`
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
# Tue, 04 Jul 2023 19:59:50 GMT
ENV ROS_DISTRO=iron
# Tue, 04 Jul 2023 20:00:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:00:34 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 20:00:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 20:00:34 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 20:00:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:00:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 20:01:02 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 04 Jul 2023 20:01:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:2c215437d76e0aa23ad3ad77eacdff757fb515043d5fbc4aaab262edecf0f570`  
		Last Modified: Tue, 04 Jul 2023 20:12:05 GMT  
		Size: 124.1 MB (124106862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83b7644717ba2f3371d754f83f5d74a18227dd0efa3552b47025bd2bb2e7e92`  
		Last Modified: Tue, 04 Jul 2023 20:11:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199be721033556b61121fd3dc17b7e99b7a7f82492d2272ba5b86f84a9ce7fc2`  
		Last Modified: Tue, 04 Jul 2023 20:12:24 GMT  
		Size: 85.0 MB (84994600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ff985aa05405f2f8956ec07b70eae3f30be79fec5c6d3c1617677f4c3696ac`  
		Last Modified: Tue, 04 Jul 2023 20:12:14 GMT  
		Size: 293.8 KB (293837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4dbbe640a7122ac20768a9e899cd6f765aca885c9d8f66066b241d69c62228`  
		Last Modified: Tue, 04 Jul 2023 20:12:14 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad8cd1c41ec878e1b4d38c0b86b45f871a82ec4c846bc1c940a726af567ffa9`  
		Last Modified: Tue, 04 Jul 2023 20:12:18 GMT  
		Size: 23.7 MB (23672931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:abff66cc26ac456d4f7f24bc13108310663e0f64a9fd24646aa30b2f1ac0e573
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261284786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a339b73410a100e8948f172487e9f0172e70fe9481a4fcf91f19c71521d13`
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
# Wed, 16 Aug 2023 15:29:02 GMT
ENV ROS_DISTRO=iron
# Wed, 16 Aug 2023 15:29:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:29:57 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 16 Aug 2023 15:29:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:29:57 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:30:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:30:26 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 16 Aug 2023 15:30:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 16 Aug 2023 15:30:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:693a5185c6732e5ca8e766ca2be9570243a05e66c9c085ee4d7dd35dacad4a73`  
		Last Modified: Wed, 16 Aug 2023 15:41:25 GMT  
		Size: 121.6 MB (121617636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83726072cbc7db22d58a8f03eb01536572a85fa76caebdd61df6f318ed06ee51`  
		Last Modified: Wed, 16 Aug 2023 15:41:09 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a4eda63942c2c3ef94d99c842b03cebea82f1904a1f5b631974a295b7efe37`  
		Last Modified: Wed, 16 Aug 2023 15:41:44 GMT  
		Size: 82.8 MB (82840931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50080694231be65dd9eaf3724f7526680ccbfc58ba778f355aa132dd315de1e`  
		Last Modified: Wed, 16 Aug 2023 15:41:36 GMT  
		Size: 299.8 KB (299847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e728607890e153ce62f3d6cefe5ea39753687001587d366b4e723b1434db1fb`  
		Last Modified: Wed, 16 Aug 2023 15:41:36 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756195b01fe3a6421f90801c97bc4d09c3ce2918293c47f005d0a8a876793811`  
		Last Modified: Wed, 16 Aug 2023 15:41:39 GMT  
		Size: 23.1 MB (23113110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:18d9ac3b698d9a6184a866ea6e69a1164bf542997456a4e9efbccea5f83d813a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:c0d01ca752cc23ddddb389409680c54fb6c85949c79bc4a3bcdd2a266414a313
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268546213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4bee036752b69abd2271fb9ab494ff987a3923d00c355fc8651896a7dc9b00`
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
# Tue, 04 Jul 2023 19:59:50 GMT
ENV ROS_DISTRO=iron
# Tue, 04 Jul 2023 20:00:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:00:34 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 20:00:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 20:00:34 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 20:00:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:00:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 20:01:02 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 04 Jul 2023 20:01:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:2c215437d76e0aa23ad3ad77eacdff757fb515043d5fbc4aaab262edecf0f570`  
		Last Modified: Tue, 04 Jul 2023 20:12:05 GMT  
		Size: 124.1 MB (124106862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83b7644717ba2f3371d754f83f5d74a18227dd0efa3552b47025bd2bb2e7e92`  
		Last Modified: Tue, 04 Jul 2023 20:11:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199be721033556b61121fd3dc17b7e99b7a7f82492d2272ba5b86f84a9ce7fc2`  
		Last Modified: Tue, 04 Jul 2023 20:12:24 GMT  
		Size: 85.0 MB (84994600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ff985aa05405f2f8956ec07b70eae3f30be79fec5c6d3c1617677f4c3696ac`  
		Last Modified: Tue, 04 Jul 2023 20:12:14 GMT  
		Size: 293.8 KB (293837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4dbbe640a7122ac20768a9e899cd6f765aca885c9d8f66066b241d69c62228`  
		Last Modified: Tue, 04 Jul 2023 20:12:14 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad8cd1c41ec878e1b4d38c0b86b45f871a82ec4c846bc1c940a726af567ffa9`  
		Last Modified: Tue, 04 Jul 2023 20:12:18 GMT  
		Size: 23.7 MB (23672931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:abff66cc26ac456d4f7f24bc13108310663e0f64a9fd24646aa30b2f1ac0e573
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261284786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a339b73410a100e8948f172487e9f0172e70fe9481a4fcf91f19c71521d13`
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
# Wed, 16 Aug 2023 15:29:02 GMT
ENV ROS_DISTRO=iron
# Wed, 16 Aug 2023 15:29:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:29:57 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 16 Aug 2023 15:29:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:29:57 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:30:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:30:26 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 16 Aug 2023 15:30:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 16 Aug 2023 15:30:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:693a5185c6732e5ca8e766ca2be9570243a05e66c9c085ee4d7dd35dacad4a73`  
		Last Modified: Wed, 16 Aug 2023 15:41:25 GMT  
		Size: 121.6 MB (121617636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83726072cbc7db22d58a8f03eb01536572a85fa76caebdd61df6f318ed06ee51`  
		Last Modified: Wed, 16 Aug 2023 15:41:09 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a4eda63942c2c3ef94d99c842b03cebea82f1904a1f5b631974a295b7efe37`  
		Last Modified: Wed, 16 Aug 2023 15:41:44 GMT  
		Size: 82.8 MB (82840931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50080694231be65dd9eaf3724f7526680ccbfc58ba778f355aa132dd315de1e`  
		Last Modified: Wed, 16 Aug 2023 15:41:36 GMT  
		Size: 299.8 KB (299847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e728607890e153ce62f3d6cefe5ea39753687001587d366b4e723b1434db1fb`  
		Last Modified: Wed, 16 Aug 2023 15:41:36 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756195b01fe3a6421f90801c97bc4d09c3ce2918293c47f005d0a8a876793811`  
		Last Modified: Wed, 16 Aug 2023 15:41:39 GMT  
		Size: 23.1 MB (23113110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:e0ee41066afc44253511c135fc3d05ef22680fe9bf9f85327ddad6f516c22bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:18f05ac562c1ebb43ffa4ab507a15e9789fe492b198cd8541a78e01b61602223
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159582399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5e6419d00ad0e5309de29c100ca93f7d87acfa6cdb966031b35b86181d721b`
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
# Tue, 04 Jul 2023 19:59:50 GMT
ENV ROS_DISTRO=iron
# Tue, 04 Jul 2023 20:00:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:00:34 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 20:00:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 20:00:34 GMT
CMD ["bash"]
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
	-	`sha256:2c215437d76e0aa23ad3ad77eacdff757fb515043d5fbc4aaab262edecf0f570`  
		Last Modified: Tue, 04 Jul 2023 20:12:05 GMT  
		Size: 124.1 MB (124106862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83b7644717ba2f3371d754f83f5d74a18227dd0efa3552b47025bd2bb2e7e92`  
		Last Modified: Tue, 04 Jul 2023 20:11:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8abb53d261569686b18feafb805eb0d6bc1ef7f3d484bb36b41731c64cd75859
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155028486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce607efc4cbe9f78af921a43648895fda5b6b43eea249692b090a343fc7110b4`
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
# Wed, 16 Aug 2023 15:29:02 GMT
ENV ROS_DISTRO=iron
# Wed, 16 Aug 2023 15:29:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:29:57 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 16 Aug 2023 15:29:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:29:57 GMT
CMD ["bash"]
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
	-	`sha256:693a5185c6732e5ca8e766ca2be9570243a05e66c9c085ee4d7dd35dacad4a73`  
		Last Modified: Wed, 16 Aug 2023 15:41:25 GMT  
		Size: 121.6 MB (121617636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83726072cbc7db22d58a8f03eb01536572a85fa76caebdd61df6f318ed06ee51`  
		Last Modified: Wed, 16 Aug 2023 15:41:09 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-core-jammy`

```console
$ docker pull ros@sha256:e0ee41066afc44253511c135fc3d05ef22680fe9bf9f85327ddad6f516c22bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:18f05ac562c1ebb43ffa4ab507a15e9789fe492b198cd8541a78e01b61602223
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159582399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5e6419d00ad0e5309de29c100ca93f7d87acfa6cdb966031b35b86181d721b`
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
# Tue, 04 Jul 2023 19:59:50 GMT
ENV ROS_DISTRO=iron
# Tue, 04 Jul 2023 20:00:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:00:34 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 20:00:34 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 20:00:34 GMT
CMD ["bash"]
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
	-	`sha256:2c215437d76e0aa23ad3ad77eacdff757fb515043d5fbc4aaab262edecf0f570`  
		Last Modified: Tue, 04 Jul 2023 20:12:05 GMT  
		Size: 124.1 MB (124106862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83b7644717ba2f3371d754f83f5d74a18227dd0efa3552b47025bd2bb2e7e92`  
		Last Modified: Tue, 04 Jul 2023 20:11:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8abb53d261569686b18feafb805eb0d6bc1ef7f3d484bb36b41731c64cd75859
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155028486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce607efc4cbe9f78af921a43648895fda5b6b43eea249692b090a343fc7110b4`
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
# Wed, 16 Aug 2023 15:29:02 GMT
ENV ROS_DISTRO=iron
# Wed, 16 Aug 2023 15:29:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:29:57 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 16 Aug 2023 15:29:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:29:57 GMT
CMD ["bash"]
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
	-	`sha256:693a5185c6732e5ca8e766ca2be9570243a05e66c9c085ee4d7dd35dacad4a73`  
		Last Modified: Wed, 16 Aug 2023 15:41:25 GMT  
		Size: 121.6 MB (121617636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83726072cbc7db22d58a8f03eb01536572a85fa76caebdd61df6f318ed06ee51`  
		Last Modified: Wed, 16 Aug 2023 15:41:09 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:latest`

```console
$ docker pull ros@sha256:27637101de8a2a5188fff5ce6115c046ac3251f85ea81c3bdf661da300d205ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

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

### `ros:latest` - linux; arm64 variant v8

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

## `ros:noetic`

```console
$ docker pull ros@sha256:f915636e129d884e8b1476c2c4a6784847623f3ec49bab5d7b56383e0f3bf2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:1f2a7d8e59ee5906b1f79b47f293d7458421a6e59561edfa0de0bb678caf0c3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343210185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a98bb7bca647203e46bd29f1e0ab661837100a39f9c592d05459e376a040883`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:38:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:38:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:40:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:40:36 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:40:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:40:36 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 19:41:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:41:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 19:42:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff84dd75ab0363da2809c202391ffc2d59534b4888fb855bfd3e21fba17c6fc`  
		Last Modified: Tue, 04 Jul 2023 20:06:54 GMT  
		Size: 1.2 MB (1198708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564b5c67648727c462a4c2ba9d04cdbfa852b527efa36e4c6a859b58454f1c06`  
		Last Modified: Tue, 04 Jul 2023 20:06:53 GMT  
		Size: 5.6 MB (5553847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d18d779d6732554da8eb52855df2ccfe7921f00655dffb89550af33715f184`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc5d180dd93ee0210935b93b72cc533ed3b35e05a47dc0b20fb5b5b9884e4c3`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac36e4a2604385d7a84264dc122ac61dd1af8f304d486fc983703238a0d02333`  
		Last Modified: Tue, 04 Jul 2023 20:07:19 GMT  
		Size: 177.0 MB (177027946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca272865f67e094abd7a450c446c31552297e72292785448cac9df1ac6bdcd1`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2c2048f289191c959ae1bde0b76c4c37af804966f66c4599e4745a47810cad`  
		Last Modified: Tue, 04 Jul 2023 20:07:35 GMT  
		Size: 50.9 MB (50939858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3ad18f9d687633622e84262935b3873354dcf6c1ce6c32d67568aa7f9c351f`  
		Last Modified: Tue, 04 Jul 2023 20:07:28 GMT  
		Size: 302.7 KB (302667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf9b129af37cdd180a7f4bb7fc69172d71d5bbc7c2e1eb95896ae3fa7a973fe`  
		Last Modified: Tue, 04 Jul 2023 20:07:39 GMT  
		Size: 79.6 MB (79604734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:44d4f5184dee8e1470cef26eb31aaca402a607f556ef3dcfd6695610f10c6d9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289311711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a824034ce70955715c5ad01653744c4c3a0330ad7419be72d21b1dbeb702391`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:58:19 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:58:22 GMT
ADD file:8bedca16bf416520f5df29175a99b07585281465c459544b9f9679016f59762a in / 
# Wed, 28 Jun 2023 09:58:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:51:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:52:11 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:55:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:55:11 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 19:55:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:55:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 19:57:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:06e53fabee8df31622850c604f9242a52a466ec4eb75320019bdfdc8ec311692`  
		Last Modified: Tue, 04 Jul 2023 06:22:20 GMT  
		Size: 24.6 MB (24588135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf8ae4844234b1655ffcc66de6ff4d8fb9d8dc5b263579abf1c0f08fc45c10b`  
		Last Modified: Tue, 04 Jul 2023 20:06:37 GMT  
		Size: 1.2 MB (1198714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f870418e12b4135248455da61f5521096265e859ed7df1641c96d8052c1cd1ed`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 4.7 MB (4679197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb37cb4cc4c6e905769f0ad1f740744e276e496b07b5efc7e4dcfd333e303892`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e584269a8e1f1afb39b1c87e053140430bf059f1a78c8091f862a0a6d7ce9d0`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f17c57312bea1c2c36a5f0b529de68ac63f57144e4e7911f2bfbdaa007f1cc2`  
		Last Modified: Tue, 04 Jul 2023 20:07:03 GMT  
		Size: 157.5 MB (157543123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145cb0493e0b9da981ce0cd0c9aeab054329b78efe17d28f3a208cfe95f617a1`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8ec7ad778d705ac798c8c4e72ac5e0a3d97e71bf31fb07dc28dc1c7dbfde0b`  
		Last Modified: Tue, 04 Jul 2023 20:07:17 GMT  
		Size: 40.5 MB (40503772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4463c21fd1b24a56ceff0c21678439984b89244a4de1cebf2ca5d1e4fe6f6c`  
		Last Modified: Tue, 04 Jul 2023 20:07:12 GMT  
		Size: 302.7 KB (302667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825a9d60f2d0bb1d7c24f20b6232803e0cae89bbd590ec88ddcddd9186193f1a`  
		Last Modified: Tue, 04 Jul 2023 20:07:21 GMT  
		Size: 60.5 MB (60493692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:af745a514f22826555b963a1881e2dccd9c605adb40b1b806c3c8f341f1104ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 MB (322829356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1df96a9ed3cefbb4a8d610a2cddeff2a565833d4813d072eba7794e8537e156`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 15:02:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:02:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:02:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 16 Aug 2023 15:02:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 16 Aug 2023 15:02:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 15:02:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 16 Aug 2023 15:02:38 GMT
ENV ROS_DISTRO=noetic
# Wed, 16 Aug 2023 15:05:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:05:32 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 16 Aug 2023 15:05:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:05:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:06:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:06:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 16 Aug 2023 15:07:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15340a0f1b3eb99199990d967961a6a7095eccee4a7e4b4a73d5f695318b9c0`  
		Last Modified: Wed, 16 Aug 2023 15:36:35 GMT  
		Size: 1.2 MB (1199928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721226cd510b20bfa5e238d93f0c82d74955fe088f6a76baf10edd313c20865d`  
		Last Modified: Wed, 16 Aug 2023 15:36:33 GMT  
		Size: 5.5 MB (5533316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee0e3a60370b22bc9740a59b8aa14fb13ccdff17844a659d622e95eb49aadee`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7439f340ca803a67b808daca6069b8332fb18927cf901c22569e32b8fbbe825d`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72576e868a3e7c4d3fc831d20bce9ee1236edd7e6713b812cecc47fa9bdc66d`  
		Last Modified: Wed, 16 Aug 2023 15:37:06 GMT  
		Size: 171.4 MB (171409809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d637f1ed1675da3f70e7ae5fdd2e2f2b82c99cfb4bfeeec599928e70b238651`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5211a2259bc1478e29b4690b53e5d12a125494f0f9a72cbfeeecbd7ec25e03b`  
		Last Modified: Wed, 16 Aug 2023 15:37:21 GMT  
		Size: 45.2 MB (45205544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7378851344c17811607f8ba6396d28e3461695a329ed8350d4cf455cd5c084`  
		Last Modified: Wed, 16 Aug 2023 15:37:15 GMT  
		Size: 305.0 KB (305028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f3c47600689adaa3ce673c9171bc7b632548702a735bc4ed1b99f651d96fcb`  
		Last Modified: Wed, 16 Aug 2023 15:37:24 GMT  
		Size: 72.0 MB (71972732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:8c9cbede06860b003c6ad967db3170628c58642f129c1a00b27a1275f58c2562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:17c20f8ed1eb9f78a84888c504ff6d817df0cad9639322203443d179a285030f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.2 MB (835187001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b06e83a64c3fe81d8797973d87f5889d6634bd1ad602d7afdea402b4c491aa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:38:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:38:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:40:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:40:36 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:40:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:40:36 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 19:41:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:41:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 19:42:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:47:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff84dd75ab0363da2809c202391ffc2d59534b4888fb855bfd3e21fba17c6fc`  
		Last Modified: Tue, 04 Jul 2023 20:06:54 GMT  
		Size: 1.2 MB (1198708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564b5c67648727c462a4c2ba9d04cdbfa852b527efa36e4c6a859b58454f1c06`  
		Last Modified: Tue, 04 Jul 2023 20:06:53 GMT  
		Size: 5.6 MB (5553847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d18d779d6732554da8eb52855df2ccfe7921f00655dffb89550af33715f184`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc5d180dd93ee0210935b93b72cc533ed3b35e05a47dc0b20fb5b5b9884e4c3`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac36e4a2604385d7a84264dc122ac61dd1af8f304d486fc983703238a0d02333`  
		Last Modified: Tue, 04 Jul 2023 20:07:19 GMT  
		Size: 177.0 MB (177027946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca272865f67e094abd7a450c446c31552297e72292785448cac9df1ac6bdcd1`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2c2048f289191c959ae1bde0b76c4c37af804966f66c4599e4745a47810cad`  
		Last Modified: Tue, 04 Jul 2023 20:07:35 GMT  
		Size: 50.9 MB (50939858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3ad18f9d687633622e84262935b3873354dcf6c1ce6c32d67568aa7f9c351f`  
		Last Modified: Tue, 04 Jul 2023 20:07:28 GMT  
		Size: 302.7 KB (302667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf9b129af37cdd180a7f4bb7fc69172d71d5bbc7c2e1eb95896ae3fa7a973fe`  
		Last Modified: Tue, 04 Jul 2023 20:07:39 GMT  
		Size: 79.6 MB (79604734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fb0bc20f4dc2d238bcb5f4d176ff43fb54f3b5a34458d48581516b9e84f6f1`  
		Last Modified: Tue, 04 Jul 2023 20:09:08 GMT  
		Size: 492.0 MB (491976816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:2e4ad716540593d1c21f58b35bf57b60b8b1425a8b2a1f36f8fe1b0d6ac45c2c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.2 MB (726232769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f295e97a2f32d9cf7b131c884666f3f6efb35416466b359864f85227a14399`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:58:19 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:58:22 GMT
ADD file:8bedca16bf416520f5df29175a99b07585281465c459544b9f9679016f59762a in / 
# Wed, 28 Jun 2023 09:58:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:51:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:52:11 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:55:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:55:11 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 19:55:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:55:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 19:57:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:06:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:06e53fabee8df31622850c604f9242a52a466ec4eb75320019bdfdc8ec311692`  
		Last Modified: Tue, 04 Jul 2023 06:22:20 GMT  
		Size: 24.6 MB (24588135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf8ae4844234b1655ffcc66de6ff4d8fb9d8dc5b263579abf1c0f08fc45c10b`  
		Last Modified: Tue, 04 Jul 2023 20:06:37 GMT  
		Size: 1.2 MB (1198714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f870418e12b4135248455da61f5521096265e859ed7df1641c96d8052c1cd1ed`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 4.7 MB (4679197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb37cb4cc4c6e905769f0ad1f740744e276e496b07b5efc7e4dcfd333e303892`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e584269a8e1f1afb39b1c87e053140430bf059f1a78c8091f862a0a6d7ce9d0`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f17c57312bea1c2c36a5f0b529de68ac63f57144e4e7911f2bfbdaa007f1cc2`  
		Last Modified: Tue, 04 Jul 2023 20:07:03 GMT  
		Size: 157.5 MB (157543123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145cb0493e0b9da981ce0cd0c9aeab054329b78efe17d28f3a208cfe95f617a1`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8ec7ad778d705ac798c8c4e72ac5e0a3d97e71bf31fb07dc28dc1c7dbfde0b`  
		Last Modified: Tue, 04 Jul 2023 20:07:17 GMT  
		Size: 40.5 MB (40503772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4463c21fd1b24a56ceff0c21678439984b89244a4de1cebf2ca5d1e4fe6f6c`  
		Last Modified: Tue, 04 Jul 2023 20:07:12 GMT  
		Size: 302.7 KB (302667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825a9d60f2d0bb1d7c24f20b6232803e0cae89bbd590ec88ddcddd9186193f1a`  
		Last Modified: Tue, 04 Jul 2023 20:07:21 GMT  
		Size: 60.5 MB (60493692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9006a1bc48bc1a39846cdf688a533b775edb084b4f4cd75ab02bcc177fafa96d`  
		Last Modified: Tue, 04 Jul 2023 20:08:44 GMT  
		Size: 436.9 MB (436921058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7eae4b6fc8ff5ef942d83dcc51945e0c990c916ca2d4752a9a6421e1417fbadd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.5 MB (785516952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873edfa41699dd21bb3bdb186b60357ffbe0860cd42dd6ae2524d61469cae46f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 15:02:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:02:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:02:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 16 Aug 2023 15:02:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 16 Aug 2023 15:02:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 15:02:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 16 Aug 2023 15:02:38 GMT
ENV ROS_DISTRO=noetic
# Wed, 16 Aug 2023 15:05:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:05:32 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 16 Aug 2023 15:05:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:05:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:06:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:06:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 16 Aug 2023 15:07:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:16:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15340a0f1b3eb99199990d967961a6a7095eccee4a7e4b4a73d5f695318b9c0`  
		Last Modified: Wed, 16 Aug 2023 15:36:35 GMT  
		Size: 1.2 MB (1199928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721226cd510b20bfa5e238d93f0c82d74955fe088f6a76baf10edd313c20865d`  
		Last Modified: Wed, 16 Aug 2023 15:36:33 GMT  
		Size: 5.5 MB (5533316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee0e3a60370b22bc9740a59b8aa14fb13ccdff17844a659d622e95eb49aadee`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7439f340ca803a67b808daca6069b8332fb18927cf901c22569e32b8fbbe825d`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72576e868a3e7c4d3fc831d20bce9ee1236edd7e6713b812cecc47fa9bdc66d`  
		Last Modified: Wed, 16 Aug 2023 15:37:06 GMT  
		Size: 171.4 MB (171409809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d637f1ed1675da3f70e7ae5fdd2e2f2b82c99cfb4bfeeec599928e70b238651`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5211a2259bc1478e29b4690b53e5d12a125494f0f9a72cbfeeecbd7ec25e03b`  
		Last Modified: Wed, 16 Aug 2023 15:37:21 GMT  
		Size: 45.2 MB (45205544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7378851344c17811607f8ba6396d28e3461695a329ed8350d4cf455cd5c084`  
		Last Modified: Wed, 16 Aug 2023 15:37:15 GMT  
		Size: 305.0 KB (305028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f3c47600689adaa3ce673c9171bc7b632548702a735bc4ed1b99f651d96fcb`  
		Last Modified: Wed, 16 Aug 2023 15:37:24 GMT  
		Size: 72.0 MB (71972732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f409290bb4b094d2c155c6fc2d027cb969bc2ef37077101bc931a340cd2313`  
		Last Modified: Wed, 16 Aug 2023 15:38:46 GMT  
		Size: 462.7 MB (462687596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:8c9cbede06860b003c6ad967db3170628c58642f129c1a00b27a1275f58c2562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:17c20f8ed1eb9f78a84888c504ff6d817df0cad9639322203443d179a285030f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.2 MB (835187001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b06e83a64c3fe81d8797973d87f5889d6634bd1ad602d7afdea402b4c491aa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:38:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:38:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:40:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:40:36 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:40:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:40:36 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 19:41:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:41:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 19:42:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:47:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff84dd75ab0363da2809c202391ffc2d59534b4888fb855bfd3e21fba17c6fc`  
		Last Modified: Tue, 04 Jul 2023 20:06:54 GMT  
		Size: 1.2 MB (1198708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564b5c67648727c462a4c2ba9d04cdbfa852b527efa36e4c6a859b58454f1c06`  
		Last Modified: Tue, 04 Jul 2023 20:06:53 GMT  
		Size: 5.6 MB (5553847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d18d779d6732554da8eb52855df2ccfe7921f00655dffb89550af33715f184`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc5d180dd93ee0210935b93b72cc533ed3b35e05a47dc0b20fb5b5b9884e4c3`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac36e4a2604385d7a84264dc122ac61dd1af8f304d486fc983703238a0d02333`  
		Last Modified: Tue, 04 Jul 2023 20:07:19 GMT  
		Size: 177.0 MB (177027946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca272865f67e094abd7a450c446c31552297e72292785448cac9df1ac6bdcd1`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2c2048f289191c959ae1bde0b76c4c37af804966f66c4599e4745a47810cad`  
		Last Modified: Tue, 04 Jul 2023 20:07:35 GMT  
		Size: 50.9 MB (50939858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3ad18f9d687633622e84262935b3873354dcf6c1ce6c32d67568aa7f9c351f`  
		Last Modified: Tue, 04 Jul 2023 20:07:28 GMT  
		Size: 302.7 KB (302667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf9b129af37cdd180a7f4bb7fc69172d71d5bbc7c2e1eb95896ae3fa7a973fe`  
		Last Modified: Tue, 04 Jul 2023 20:07:39 GMT  
		Size: 79.6 MB (79604734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fb0bc20f4dc2d238bcb5f4d176ff43fb54f3b5a34458d48581516b9e84f6f1`  
		Last Modified: Tue, 04 Jul 2023 20:09:08 GMT  
		Size: 492.0 MB (491976816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:2e4ad716540593d1c21f58b35bf57b60b8b1425a8b2a1f36f8fe1b0d6ac45c2c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.2 MB (726232769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f295e97a2f32d9cf7b131c884666f3f6efb35416466b359864f85227a14399`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:58:19 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:58:22 GMT
ADD file:8bedca16bf416520f5df29175a99b07585281465c459544b9f9679016f59762a in / 
# Wed, 28 Jun 2023 09:58:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:51:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:52:11 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:55:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:55:11 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 19:55:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:55:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 19:57:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:06:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:06e53fabee8df31622850c604f9242a52a466ec4eb75320019bdfdc8ec311692`  
		Last Modified: Tue, 04 Jul 2023 06:22:20 GMT  
		Size: 24.6 MB (24588135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf8ae4844234b1655ffcc66de6ff4d8fb9d8dc5b263579abf1c0f08fc45c10b`  
		Last Modified: Tue, 04 Jul 2023 20:06:37 GMT  
		Size: 1.2 MB (1198714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f870418e12b4135248455da61f5521096265e859ed7df1641c96d8052c1cd1ed`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 4.7 MB (4679197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb37cb4cc4c6e905769f0ad1f740744e276e496b07b5efc7e4dcfd333e303892`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e584269a8e1f1afb39b1c87e053140430bf059f1a78c8091f862a0a6d7ce9d0`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f17c57312bea1c2c36a5f0b529de68ac63f57144e4e7911f2bfbdaa007f1cc2`  
		Last Modified: Tue, 04 Jul 2023 20:07:03 GMT  
		Size: 157.5 MB (157543123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145cb0493e0b9da981ce0cd0c9aeab054329b78efe17d28f3a208cfe95f617a1`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8ec7ad778d705ac798c8c4e72ac5e0a3d97e71bf31fb07dc28dc1c7dbfde0b`  
		Last Modified: Tue, 04 Jul 2023 20:07:17 GMT  
		Size: 40.5 MB (40503772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4463c21fd1b24a56ceff0c21678439984b89244a4de1cebf2ca5d1e4fe6f6c`  
		Last Modified: Tue, 04 Jul 2023 20:07:12 GMT  
		Size: 302.7 KB (302667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825a9d60f2d0bb1d7c24f20b6232803e0cae89bbd590ec88ddcddd9186193f1a`  
		Last Modified: Tue, 04 Jul 2023 20:07:21 GMT  
		Size: 60.5 MB (60493692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9006a1bc48bc1a39846cdf688a533b775edb084b4f4cd75ab02bcc177fafa96d`  
		Last Modified: Tue, 04 Jul 2023 20:08:44 GMT  
		Size: 436.9 MB (436921058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7eae4b6fc8ff5ef942d83dcc51945e0c990c916ca2d4752a9a6421e1417fbadd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.5 MB (785516952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873edfa41699dd21bb3bdb186b60357ffbe0860cd42dd6ae2524d61469cae46f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 15:02:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:02:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:02:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 16 Aug 2023 15:02:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 16 Aug 2023 15:02:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 15:02:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 16 Aug 2023 15:02:38 GMT
ENV ROS_DISTRO=noetic
# Wed, 16 Aug 2023 15:05:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:05:32 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 16 Aug 2023 15:05:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:05:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:06:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:06:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 16 Aug 2023 15:07:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:16:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15340a0f1b3eb99199990d967961a6a7095eccee4a7e4b4a73d5f695318b9c0`  
		Last Modified: Wed, 16 Aug 2023 15:36:35 GMT  
		Size: 1.2 MB (1199928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721226cd510b20bfa5e238d93f0c82d74955fe088f6a76baf10edd313c20865d`  
		Last Modified: Wed, 16 Aug 2023 15:36:33 GMT  
		Size: 5.5 MB (5533316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee0e3a60370b22bc9740a59b8aa14fb13ccdff17844a659d622e95eb49aadee`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7439f340ca803a67b808daca6069b8332fb18927cf901c22569e32b8fbbe825d`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72576e868a3e7c4d3fc831d20bce9ee1236edd7e6713b812cecc47fa9bdc66d`  
		Last Modified: Wed, 16 Aug 2023 15:37:06 GMT  
		Size: 171.4 MB (171409809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d637f1ed1675da3f70e7ae5fdd2e2f2b82c99cfb4bfeeec599928e70b238651`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5211a2259bc1478e29b4690b53e5d12a125494f0f9a72cbfeeecbd7ec25e03b`  
		Last Modified: Wed, 16 Aug 2023 15:37:21 GMT  
		Size: 45.2 MB (45205544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7378851344c17811607f8ba6396d28e3461695a329ed8350d4cf455cd5c084`  
		Last Modified: Wed, 16 Aug 2023 15:37:15 GMT  
		Size: 305.0 KB (305028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f3c47600689adaa3ce673c9171bc7b632548702a735bc4ed1b99f651d96fcb`  
		Last Modified: Wed, 16 Aug 2023 15:37:24 GMT  
		Size: 72.0 MB (71972732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f409290bb4b094d2c155c6fc2d027cb969bc2ef37077101bc931a340cd2313`  
		Last Modified: Wed, 16 Aug 2023 15:38:46 GMT  
		Size: 462.7 MB (462687596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:9e16d9c37c0d49ab96ecabf470d11e704d7c2f106220c011cf07d205684d865f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:74b585c00c52a11bc9ec0958cc34a2a5cc8e7095c64212e77683c08a3a5281d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359072544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e4b1ab66575af3b1bb37ec6aa0a39b517f644917f4a44bfb92ef5c30c0b5c5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:38:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:38:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:40:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:40:36 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:40:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:40:36 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 19:41:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:41:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 19:42:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:43:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff84dd75ab0363da2809c202391ffc2d59534b4888fb855bfd3e21fba17c6fc`  
		Last Modified: Tue, 04 Jul 2023 20:06:54 GMT  
		Size: 1.2 MB (1198708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564b5c67648727c462a4c2ba9d04cdbfa852b527efa36e4c6a859b58454f1c06`  
		Last Modified: Tue, 04 Jul 2023 20:06:53 GMT  
		Size: 5.6 MB (5553847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d18d779d6732554da8eb52855df2ccfe7921f00655dffb89550af33715f184`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc5d180dd93ee0210935b93b72cc533ed3b35e05a47dc0b20fb5b5b9884e4c3`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac36e4a2604385d7a84264dc122ac61dd1af8f304d486fc983703238a0d02333`  
		Last Modified: Tue, 04 Jul 2023 20:07:19 GMT  
		Size: 177.0 MB (177027946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca272865f67e094abd7a450c446c31552297e72292785448cac9df1ac6bdcd1`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2c2048f289191c959ae1bde0b76c4c37af804966f66c4599e4745a47810cad`  
		Last Modified: Tue, 04 Jul 2023 20:07:35 GMT  
		Size: 50.9 MB (50939858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3ad18f9d687633622e84262935b3873354dcf6c1ce6c32d67568aa7f9c351f`  
		Last Modified: Tue, 04 Jul 2023 20:07:28 GMT  
		Size: 302.7 KB (302667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf9b129af37cdd180a7f4bb7fc69172d71d5bbc7c2e1eb95896ae3fa7a973fe`  
		Last Modified: Tue, 04 Jul 2023 20:07:39 GMT  
		Size: 79.6 MB (79604734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c101713292cc95f42a217f6ed45522650943e3e1a114dec8b652fc43e710b2e`  
		Last Modified: Tue, 04 Jul 2023 20:07:52 GMT  
		Size: 15.9 MB (15862359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:9cd1b1ca2f064657e51e039dd1e8d3732503bd9e53154ec28d56e12e567bf580
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303379129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca73e319f53dd262315677632c97c32581d5179f0b30d78bd374e983b43c9e7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:58:19 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:58:22 GMT
ADD file:8bedca16bf416520f5df29175a99b07585281465c459544b9f9679016f59762a in / 
# Wed, 28 Jun 2023 09:58:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:51:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:52:11 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:55:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:55:11 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 19:55:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:55:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 19:57:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:58:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:06e53fabee8df31622850c604f9242a52a466ec4eb75320019bdfdc8ec311692`  
		Last Modified: Tue, 04 Jul 2023 06:22:20 GMT  
		Size: 24.6 MB (24588135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf8ae4844234b1655ffcc66de6ff4d8fb9d8dc5b263579abf1c0f08fc45c10b`  
		Last Modified: Tue, 04 Jul 2023 20:06:37 GMT  
		Size: 1.2 MB (1198714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f870418e12b4135248455da61f5521096265e859ed7df1641c96d8052c1cd1ed`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 4.7 MB (4679197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb37cb4cc4c6e905769f0ad1f740744e276e496b07b5efc7e4dcfd333e303892`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e584269a8e1f1afb39b1c87e053140430bf059f1a78c8091f862a0a6d7ce9d0`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f17c57312bea1c2c36a5f0b529de68ac63f57144e4e7911f2bfbdaa007f1cc2`  
		Last Modified: Tue, 04 Jul 2023 20:07:03 GMT  
		Size: 157.5 MB (157543123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145cb0493e0b9da981ce0cd0c9aeab054329b78efe17d28f3a208cfe95f617a1`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8ec7ad778d705ac798c8c4e72ac5e0a3d97e71bf31fb07dc28dc1c7dbfde0b`  
		Last Modified: Tue, 04 Jul 2023 20:07:17 GMT  
		Size: 40.5 MB (40503772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4463c21fd1b24a56ceff0c21678439984b89244a4de1cebf2ca5d1e4fe6f6c`  
		Last Modified: Tue, 04 Jul 2023 20:07:12 GMT  
		Size: 302.7 KB (302667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825a9d60f2d0bb1d7c24f20b6232803e0cae89bbd590ec88ddcddd9186193f1a`  
		Last Modified: Tue, 04 Jul 2023 20:07:21 GMT  
		Size: 60.5 MB (60493692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e70a84a8ae6597832e2577f2ea351fd41792040b5899b69b5057d9c0f51f2e`  
		Last Modified: Tue, 04 Jul 2023 20:07:35 GMT  
		Size: 14.1 MB (14067418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:48d1881e37fcb8aabdfd93a2ab3aa832f7ca9d42797cbbdbd0ab2b4aac829f2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338288463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6195bda8b1ee1a176e4fbbec8431d1c7cb9f28b870ba66f4696467d40eb15340`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 15:02:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:02:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:02:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 16 Aug 2023 15:02:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 16 Aug 2023 15:02:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 15:02:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 16 Aug 2023 15:02:38 GMT
ENV ROS_DISTRO=noetic
# Wed, 16 Aug 2023 15:05:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:05:32 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 16 Aug 2023 15:05:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:05:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:06:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:06:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 16 Aug 2023 15:07:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:08:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15340a0f1b3eb99199990d967961a6a7095eccee4a7e4b4a73d5f695318b9c0`  
		Last Modified: Wed, 16 Aug 2023 15:36:35 GMT  
		Size: 1.2 MB (1199928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721226cd510b20bfa5e238d93f0c82d74955fe088f6a76baf10edd313c20865d`  
		Last Modified: Wed, 16 Aug 2023 15:36:33 GMT  
		Size: 5.5 MB (5533316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee0e3a60370b22bc9740a59b8aa14fb13ccdff17844a659d622e95eb49aadee`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7439f340ca803a67b808daca6069b8332fb18927cf901c22569e32b8fbbe825d`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72576e868a3e7c4d3fc831d20bce9ee1236edd7e6713b812cecc47fa9bdc66d`  
		Last Modified: Wed, 16 Aug 2023 15:37:06 GMT  
		Size: 171.4 MB (171409809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d637f1ed1675da3f70e7ae5fdd2e2f2b82c99cfb4bfeeec599928e70b238651`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5211a2259bc1478e29b4690b53e5d12a125494f0f9a72cbfeeecbd7ec25e03b`  
		Last Modified: Wed, 16 Aug 2023 15:37:21 GMT  
		Size: 45.2 MB (45205544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7378851344c17811607f8ba6396d28e3461695a329ed8350d4cf455cd5c084`  
		Last Modified: Wed, 16 Aug 2023 15:37:15 GMT  
		Size: 305.0 KB (305028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f3c47600689adaa3ce673c9171bc7b632548702a735bc4ed1b99f651d96fcb`  
		Last Modified: Wed, 16 Aug 2023 15:37:24 GMT  
		Size: 72.0 MB (71972732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b32ed50b6caa08d0a39dad2e4595bc889af7a598fcb07785b3eb4b8dc27869f`  
		Last Modified: Wed, 16 Aug 2023 15:37:38 GMT  
		Size: 15.5 MB (15459107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:9e16d9c37c0d49ab96ecabf470d11e704d7c2f106220c011cf07d205684d865f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:74b585c00c52a11bc9ec0958cc34a2a5cc8e7095c64212e77683c08a3a5281d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359072544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e4b1ab66575af3b1bb37ec6aa0a39b517f644917f4a44bfb92ef5c30c0b5c5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:38:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:38:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:40:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:40:36 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:40:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:40:36 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 19:41:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:41:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 19:42:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:43:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff84dd75ab0363da2809c202391ffc2d59534b4888fb855bfd3e21fba17c6fc`  
		Last Modified: Tue, 04 Jul 2023 20:06:54 GMT  
		Size: 1.2 MB (1198708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564b5c67648727c462a4c2ba9d04cdbfa852b527efa36e4c6a859b58454f1c06`  
		Last Modified: Tue, 04 Jul 2023 20:06:53 GMT  
		Size: 5.6 MB (5553847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d18d779d6732554da8eb52855df2ccfe7921f00655dffb89550af33715f184`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc5d180dd93ee0210935b93b72cc533ed3b35e05a47dc0b20fb5b5b9884e4c3`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac36e4a2604385d7a84264dc122ac61dd1af8f304d486fc983703238a0d02333`  
		Last Modified: Tue, 04 Jul 2023 20:07:19 GMT  
		Size: 177.0 MB (177027946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca272865f67e094abd7a450c446c31552297e72292785448cac9df1ac6bdcd1`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2c2048f289191c959ae1bde0b76c4c37af804966f66c4599e4745a47810cad`  
		Last Modified: Tue, 04 Jul 2023 20:07:35 GMT  
		Size: 50.9 MB (50939858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3ad18f9d687633622e84262935b3873354dcf6c1ce6c32d67568aa7f9c351f`  
		Last Modified: Tue, 04 Jul 2023 20:07:28 GMT  
		Size: 302.7 KB (302667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf9b129af37cdd180a7f4bb7fc69172d71d5bbc7c2e1eb95896ae3fa7a973fe`  
		Last Modified: Tue, 04 Jul 2023 20:07:39 GMT  
		Size: 79.6 MB (79604734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c101713292cc95f42a217f6ed45522650943e3e1a114dec8b652fc43e710b2e`  
		Last Modified: Tue, 04 Jul 2023 20:07:52 GMT  
		Size: 15.9 MB (15862359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:9cd1b1ca2f064657e51e039dd1e8d3732503bd9e53154ec28d56e12e567bf580
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303379129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca73e319f53dd262315677632c97c32581d5179f0b30d78bd374e983b43c9e7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:58:19 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:58:22 GMT
ADD file:8bedca16bf416520f5df29175a99b07585281465c459544b9f9679016f59762a in / 
# Wed, 28 Jun 2023 09:58:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:51:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:52:11 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:55:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:55:11 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 19:55:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:55:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 19:57:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:58:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:06e53fabee8df31622850c604f9242a52a466ec4eb75320019bdfdc8ec311692`  
		Last Modified: Tue, 04 Jul 2023 06:22:20 GMT  
		Size: 24.6 MB (24588135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf8ae4844234b1655ffcc66de6ff4d8fb9d8dc5b263579abf1c0f08fc45c10b`  
		Last Modified: Tue, 04 Jul 2023 20:06:37 GMT  
		Size: 1.2 MB (1198714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f870418e12b4135248455da61f5521096265e859ed7df1641c96d8052c1cd1ed`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 4.7 MB (4679197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb37cb4cc4c6e905769f0ad1f740744e276e496b07b5efc7e4dcfd333e303892`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e584269a8e1f1afb39b1c87e053140430bf059f1a78c8091f862a0a6d7ce9d0`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f17c57312bea1c2c36a5f0b529de68ac63f57144e4e7911f2bfbdaa007f1cc2`  
		Last Modified: Tue, 04 Jul 2023 20:07:03 GMT  
		Size: 157.5 MB (157543123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145cb0493e0b9da981ce0cd0c9aeab054329b78efe17d28f3a208cfe95f617a1`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8ec7ad778d705ac798c8c4e72ac5e0a3d97e71bf31fb07dc28dc1c7dbfde0b`  
		Last Modified: Tue, 04 Jul 2023 20:07:17 GMT  
		Size: 40.5 MB (40503772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4463c21fd1b24a56ceff0c21678439984b89244a4de1cebf2ca5d1e4fe6f6c`  
		Last Modified: Tue, 04 Jul 2023 20:07:12 GMT  
		Size: 302.7 KB (302667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825a9d60f2d0bb1d7c24f20b6232803e0cae89bbd590ec88ddcddd9186193f1a`  
		Last Modified: Tue, 04 Jul 2023 20:07:21 GMT  
		Size: 60.5 MB (60493692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e70a84a8ae6597832e2577f2ea351fd41792040b5899b69b5057d9c0f51f2e`  
		Last Modified: Tue, 04 Jul 2023 20:07:35 GMT  
		Size: 14.1 MB (14067418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:48d1881e37fcb8aabdfd93a2ab3aa832f7ca9d42797cbbdbd0ab2b4aac829f2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338288463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6195bda8b1ee1a176e4fbbec8431d1c7cb9f28b870ba66f4696467d40eb15340`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 15:02:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:02:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:02:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 16 Aug 2023 15:02:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 16 Aug 2023 15:02:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 15:02:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 16 Aug 2023 15:02:38 GMT
ENV ROS_DISTRO=noetic
# Wed, 16 Aug 2023 15:05:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:05:32 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 16 Aug 2023 15:05:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:05:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:06:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:06:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 16 Aug 2023 15:07:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:08:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15340a0f1b3eb99199990d967961a6a7095eccee4a7e4b4a73d5f695318b9c0`  
		Last Modified: Wed, 16 Aug 2023 15:36:35 GMT  
		Size: 1.2 MB (1199928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721226cd510b20bfa5e238d93f0c82d74955fe088f6a76baf10edd313c20865d`  
		Last Modified: Wed, 16 Aug 2023 15:36:33 GMT  
		Size: 5.5 MB (5533316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee0e3a60370b22bc9740a59b8aa14fb13ccdff17844a659d622e95eb49aadee`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7439f340ca803a67b808daca6069b8332fb18927cf901c22569e32b8fbbe825d`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72576e868a3e7c4d3fc831d20bce9ee1236edd7e6713b812cecc47fa9bdc66d`  
		Last Modified: Wed, 16 Aug 2023 15:37:06 GMT  
		Size: 171.4 MB (171409809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d637f1ed1675da3f70e7ae5fdd2e2f2b82c99cfb4bfeeec599928e70b238651`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5211a2259bc1478e29b4690b53e5d12a125494f0f9a72cbfeeecbd7ec25e03b`  
		Last Modified: Wed, 16 Aug 2023 15:37:21 GMT  
		Size: 45.2 MB (45205544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7378851344c17811607f8ba6396d28e3461695a329ed8350d4cf455cd5c084`  
		Last Modified: Wed, 16 Aug 2023 15:37:15 GMT  
		Size: 305.0 KB (305028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f3c47600689adaa3ce673c9171bc7b632548702a735bc4ed1b99f651d96fcb`  
		Last Modified: Wed, 16 Aug 2023 15:37:24 GMT  
		Size: 72.0 MB (71972732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b32ed50b6caa08d0a39dad2e4595bc889af7a598fcb07785b3eb4b8dc27869f`  
		Last Modified: Wed, 16 Aug 2023 15:37:38 GMT  
		Size: 15.5 MB (15459107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:f915636e129d884e8b1476c2c4a6784847623f3ec49bab5d7b56383e0f3bf2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:1f2a7d8e59ee5906b1f79b47f293d7458421a6e59561edfa0de0bb678caf0c3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343210185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a98bb7bca647203e46bd29f1e0ab661837100a39f9c592d05459e376a040883`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:38:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:38:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:40:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:40:36 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:40:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:40:36 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 19:41:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:41:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 19:42:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff84dd75ab0363da2809c202391ffc2d59534b4888fb855bfd3e21fba17c6fc`  
		Last Modified: Tue, 04 Jul 2023 20:06:54 GMT  
		Size: 1.2 MB (1198708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564b5c67648727c462a4c2ba9d04cdbfa852b527efa36e4c6a859b58454f1c06`  
		Last Modified: Tue, 04 Jul 2023 20:06:53 GMT  
		Size: 5.6 MB (5553847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d18d779d6732554da8eb52855df2ccfe7921f00655dffb89550af33715f184`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc5d180dd93ee0210935b93b72cc533ed3b35e05a47dc0b20fb5b5b9884e4c3`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac36e4a2604385d7a84264dc122ac61dd1af8f304d486fc983703238a0d02333`  
		Last Modified: Tue, 04 Jul 2023 20:07:19 GMT  
		Size: 177.0 MB (177027946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca272865f67e094abd7a450c446c31552297e72292785448cac9df1ac6bdcd1`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2c2048f289191c959ae1bde0b76c4c37af804966f66c4599e4745a47810cad`  
		Last Modified: Tue, 04 Jul 2023 20:07:35 GMT  
		Size: 50.9 MB (50939858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3ad18f9d687633622e84262935b3873354dcf6c1ce6c32d67568aa7f9c351f`  
		Last Modified: Tue, 04 Jul 2023 20:07:28 GMT  
		Size: 302.7 KB (302667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf9b129af37cdd180a7f4bb7fc69172d71d5bbc7c2e1eb95896ae3fa7a973fe`  
		Last Modified: Tue, 04 Jul 2023 20:07:39 GMT  
		Size: 79.6 MB (79604734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:44d4f5184dee8e1470cef26eb31aaca402a607f556ef3dcfd6695610f10c6d9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289311711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a824034ce70955715c5ad01653744c4c3a0330ad7419be72d21b1dbeb702391`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:58:19 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:58:22 GMT
ADD file:8bedca16bf416520f5df29175a99b07585281465c459544b9f9679016f59762a in / 
# Wed, 28 Jun 2023 09:58:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:51:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:52:11 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:55:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:55:11 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 19:55:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:55:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 19:57:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:06e53fabee8df31622850c604f9242a52a466ec4eb75320019bdfdc8ec311692`  
		Last Modified: Tue, 04 Jul 2023 06:22:20 GMT  
		Size: 24.6 MB (24588135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf8ae4844234b1655ffcc66de6ff4d8fb9d8dc5b263579abf1c0f08fc45c10b`  
		Last Modified: Tue, 04 Jul 2023 20:06:37 GMT  
		Size: 1.2 MB (1198714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f870418e12b4135248455da61f5521096265e859ed7df1641c96d8052c1cd1ed`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 4.7 MB (4679197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb37cb4cc4c6e905769f0ad1f740744e276e496b07b5efc7e4dcfd333e303892`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e584269a8e1f1afb39b1c87e053140430bf059f1a78c8091f862a0a6d7ce9d0`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f17c57312bea1c2c36a5f0b529de68ac63f57144e4e7911f2bfbdaa007f1cc2`  
		Last Modified: Tue, 04 Jul 2023 20:07:03 GMT  
		Size: 157.5 MB (157543123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145cb0493e0b9da981ce0cd0c9aeab054329b78efe17d28f3a208cfe95f617a1`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8ec7ad778d705ac798c8c4e72ac5e0a3d97e71bf31fb07dc28dc1c7dbfde0b`  
		Last Modified: Tue, 04 Jul 2023 20:07:17 GMT  
		Size: 40.5 MB (40503772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4463c21fd1b24a56ceff0c21678439984b89244a4de1cebf2ca5d1e4fe6f6c`  
		Last Modified: Tue, 04 Jul 2023 20:07:12 GMT  
		Size: 302.7 KB (302667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825a9d60f2d0bb1d7c24f20b6232803e0cae89bbd590ec88ddcddd9186193f1a`  
		Last Modified: Tue, 04 Jul 2023 20:07:21 GMT  
		Size: 60.5 MB (60493692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:af745a514f22826555b963a1881e2dccd9c605adb40b1b806c3c8f341f1104ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 MB (322829356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1df96a9ed3cefbb4a8d610a2cddeff2a565833d4813d072eba7794e8537e156`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 15:02:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:02:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:02:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 16 Aug 2023 15:02:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 16 Aug 2023 15:02:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 15:02:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 16 Aug 2023 15:02:38 GMT
ENV ROS_DISTRO=noetic
# Wed, 16 Aug 2023 15:05:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:05:32 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 16 Aug 2023 15:05:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:05:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:06:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:06:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 16 Aug 2023 15:07:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15340a0f1b3eb99199990d967961a6a7095eccee4a7e4b4a73d5f695318b9c0`  
		Last Modified: Wed, 16 Aug 2023 15:36:35 GMT  
		Size: 1.2 MB (1199928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721226cd510b20bfa5e238d93f0c82d74955fe088f6a76baf10edd313c20865d`  
		Last Modified: Wed, 16 Aug 2023 15:36:33 GMT  
		Size: 5.5 MB (5533316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee0e3a60370b22bc9740a59b8aa14fb13ccdff17844a659d622e95eb49aadee`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7439f340ca803a67b808daca6069b8332fb18927cf901c22569e32b8fbbe825d`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72576e868a3e7c4d3fc831d20bce9ee1236edd7e6713b812cecc47fa9bdc66d`  
		Last Modified: Wed, 16 Aug 2023 15:37:06 GMT  
		Size: 171.4 MB (171409809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d637f1ed1675da3f70e7ae5fdd2e2f2b82c99cfb4bfeeec599928e70b238651`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5211a2259bc1478e29b4690b53e5d12a125494f0f9a72cbfeeecbd7ec25e03b`  
		Last Modified: Wed, 16 Aug 2023 15:37:21 GMT  
		Size: 45.2 MB (45205544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7378851344c17811607f8ba6396d28e3461695a329ed8350d4cf455cd5c084`  
		Last Modified: Wed, 16 Aug 2023 15:37:15 GMT  
		Size: 305.0 KB (305028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f3c47600689adaa3ce673c9171bc7b632548702a735bc4ed1b99f651d96fcb`  
		Last Modified: Wed, 16 Aug 2023 15:37:24 GMT  
		Size: 72.0 MB (71972732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:f915636e129d884e8b1476c2c4a6784847623f3ec49bab5d7b56383e0f3bf2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:1f2a7d8e59ee5906b1f79b47f293d7458421a6e59561edfa0de0bb678caf0c3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343210185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a98bb7bca647203e46bd29f1e0ab661837100a39f9c592d05459e376a040883`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:38:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:38:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:40:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:40:36 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:40:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:40:36 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 19:41:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:41:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 19:42:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff84dd75ab0363da2809c202391ffc2d59534b4888fb855bfd3e21fba17c6fc`  
		Last Modified: Tue, 04 Jul 2023 20:06:54 GMT  
		Size: 1.2 MB (1198708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564b5c67648727c462a4c2ba9d04cdbfa852b527efa36e4c6a859b58454f1c06`  
		Last Modified: Tue, 04 Jul 2023 20:06:53 GMT  
		Size: 5.6 MB (5553847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d18d779d6732554da8eb52855df2ccfe7921f00655dffb89550af33715f184`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc5d180dd93ee0210935b93b72cc533ed3b35e05a47dc0b20fb5b5b9884e4c3`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac36e4a2604385d7a84264dc122ac61dd1af8f304d486fc983703238a0d02333`  
		Last Modified: Tue, 04 Jul 2023 20:07:19 GMT  
		Size: 177.0 MB (177027946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca272865f67e094abd7a450c446c31552297e72292785448cac9df1ac6bdcd1`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2c2048f289191c959ae1bde0b76c4c37af804966f66c4599e4745a47810cad`  
		Last Modified: Tue, 04 Jul 2023 20:07:35 GMT  
		Size: 50.9 MB (50939858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3ad18f9d687633622e84262935b3873354dcf6c1ce6c32d67568aa7f9c351f`  
		Last Modified: Tue, 04 Jul 2023 20:07:28 GMT  
		Size: 302.7 KB (302667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf9b129af37cdd180a7f4bb7fc69172d71d5bbc7c2e1eb95896ae3fa7a973fe`  
		Last Modified: Tue, 04 Jul 2023 20:07:39 GMT  
		Size: 79.6 MB (79604734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:44d4f5184dee8e1470cef26eb31aaca402a607f556ef3dcfd6695610f10c6d9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289311711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a824034ce70955715c5ad01653744c4c3a0330ad7419be72d21b1dbeb702391`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:58:19 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:58:22 GMT
ADD file:8bedca16bf416520f5df29175a99b07585281465c459544b9f9679016f59762a in / 
# Wed, 28 Jun 2023 09:58:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:51:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:52:11 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:55:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:55:11 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 19:55:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:55:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 19:57:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:06e53fabee8df31622850c604f9242a52a466ec4eb75320019bdfdc8ec311692`  
		Last Modified: Tue, 04 Jul 2023 06:22:20 GMT  
		Size: 24.6 MB (24588135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf8ae4844234b1655ffcc66de6ff4d8fb9d8dc5b263579abf1c0f08fc45c10b`  
		Last Modified: Tue, 04 Jul 2023 20:06:37 GMT  
		Size: 1.2 MB (1198714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f870418e12b4135248455da61f5521096265e859ed7df1641c96d8052c1cd1ed`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 4.7 MB (4679197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb37cb4cc4c6e905769f0ad1f740744e276e496b07b5efc7e4dcfd333e303892`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e584269a8e1f1afb39b1c87e053140430bf059f1a78c8091f862a0a6d7ce9d0`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f17c57312bea1c2c36a5f0b529de68ac63f57144e4e7911f2bfbdaa007f1cc2`  
		Last Modified: Tue, 04 Jul 2023 20:07:03 GMT  
		Size: 157.5 MB (157543123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145cb0493e0b9da981ce0cd0c9aeab054329b78efe17d28f3a208cfe95f617a1`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8ec7ad778d705ac798c8c4e72ac5e0a3d97e71bf31fb07dc28dc1c7dbfde0b`  
		Last Modified: Tue, 04 Jul 2023 20:07:17 GMT  
		Size: 40.5 MB (40503772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4463c21fd1b24a56ceff0c21678439984b89244a4de1cebf2ca5d1e4fe6f6c`  
		Last Modified: Tue, 04 Jul 2023 20:07:12 GMT  
		Size: 302.7 KB (302667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825a9d60f2d0bb1d7c24f20b6232803e0cae89bbd590ec88ddcddd9186193f1a`  
		Last Modified: Tue, 04 Jul 2023 20:07:21 GMT  
		Size: 60.5 MB (60493692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:af745a514f22826555b963a1881e2dccd9c605adb40b1b806c3c8f341f1104ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 MB (322829356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1df96a9ed3cefbb4a8d610a2cddeff2a565833d4813d072eba7794e8537e156`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 15:02:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:02:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:02:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 16 Aug 2023 15:02:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 16 Aug 2023 15:02:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 15:02:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 16 Aug 2023 15:02:38 GMT
ENV ROS_DISTRO=noetic
# Wed, 16 Aug 2023 15:05:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:05:32 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 16 Aug 2023 15:05:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:05:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:06:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:06:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 16 Aug 2023 15:07:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15340a0f1b3eb99199990d967961a6a7095eccee4a7e4b4a73d5f695318b9c0`  
		Last Modified: Wed, 16 Aug 2023 15:36:35 GMT  
		Size: 1.2 MB (1199928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721226cd510b20bfa5e238d93f0c82d74955fe088f6a76baf10edd313c20865d`  
		Last Modified: Wed, 16 Aug 2023 15:36:33 GMT  
		Size: 5.5 MB (5533316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee0e3a60370b22bc9740a59b8aa14fb13ccdff17844a659d622e95eb49aadee`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7439f340ca803a67b808daca6069b8332fb18927cf901c22569e32b8fbbe825d`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72576e868a3e7c4d3fc831d20bce9ee1236edd7e6713b812cecc47fa9bdc66d`  
		Last Modified: Wed, 16 Aug 2023 15:37:06 GMT  
		Size: 171.4 MB (171409809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d637f1ed1675da3f70e7ae5fdd2e2f2b82c99cfb4bfeeec599928e70b238651`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5211a2259bc1478e29b4690b53e5d12a125494f0f9a72cbfeeecbd7ec25e03b`  
		Last Modified: Wed, 16 Aug 2023 15:37:21 GMT  
		Size: 45.2 MB (45205544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7378851344c17811607f8ba6396d28e3461695a329ed8350d4cf455cd5c084`  
		Last Modified: Wed, 16 Aug 2023 15:37:15 GMT  
		Size: 305.0 KB (305028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f3c47600689adaa3ce673c9171bc7b632548702a735bc4ed1b99f651d96fcb`  
		Last Modified: Wed, 16 Aug 2023 15:37:24 GMT  
		Size: 72.0 MB (71972732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:eb0f0b232afea34865b29798f09433bff410dd5b28b0a3dfccb4005be34d96f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:ba314e83e1140e38b730ded90897ff4abf9920a365aa66f67bf4442263ae7407
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212362926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c8e3327cb9948f69b0783b7a885aed24c0a9895e05b7e7b560ef3a8d1e4d64`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:38:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:38:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:40:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:40:36 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:40:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:40:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff84dd75ab0363da2809c202391ffc2d59534b4888fb855bfd3e21fba17c6fc`  
		Last Modified: Tue, 04 Jul 2023 20:06:54 GMT  
		Size: 1.2 MB (1198708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564b5c67648727c462a4c2ba9d04cdbfa852b527efa36e4c6a859b58454f1c06`  
		Last Modified: Tue, 04 Jul 2023 20:06:53 GMT  
		Size: 5.6 MB (5553847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d18d779d6732554da8eb52855df2ccfe7921f00655dffb89550af33715f184`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc5d180dd93ee0210935b93b72cc533ed3b35e05a47dc0b20fb5b5b9884e4c3`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac36e4a2604385d7a84264dc122ac61dd1af8f304d486fc983703238a0d02333`  
		Last Modified: Tue, 04 Jul 2023 20:07:19 GMT  
		Size: 177.0 MB (177027946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca272865f67e094abd7a450c446c31552297e72292785448cac9df1ac6bdcd1`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:8a5ac73d28a505b16a86f3e7185d0c1434c7dbf19ba486945d55d589316b5333
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188011580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67480a9eb0025f587eae298a084f3ebb439aa33830002554ff9936d59bdc8b7f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:58:19 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:58:22 GMT
ADD file:8bedca16bf416520f5df29175a99b07585281465c459544b9f9679016f59762a in / 
# Wed, 28 Jun 2023 09:58:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:51:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:52:11 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:55:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:55:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:06e53fabee8df31622850c604f9242a52a466ec4eb75320019bdfdc8ec311692`  
		Last Modified: Tue, 04 Jul 2023 06:22:20 GMT  
		Size: 24.6 MB (24588135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf8ae4844234b1655ffcc66de6ff4d8fb9d8dc5b263579abf1c0f08fc45c10b`  
		Last Modified: Tue, 04 Jul 2023 20:06:37 GMT  
		Size: 1.2 MB (1198714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f870418e12b4135248455da61f5521096265e859ed7df1641c96d8052c1cd1ed`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 4.7 MB (4679197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb37cb4cc4c6e905769f0ad1f740744e276e496b07b5efc7e4dcfd333e303892`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e584269a8e1f1afb39b1c87e053140430bf059f1a78c8091f862a0a6d7ce9d0`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f17c57312bea1c2c36a5f0b529de68ac63f57144e4e7911f2bfbdaa007f1cc2`  
		Last Modified: Tue, 04 Jul 2023 20:07:03 GMT  
		Size: 157.5 MB (157543123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145cb0493e0b9da981ce0cd0c9aeab054329b78efe17d28f3a208cfe95f617a1`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f2439b922cac680e8c6cefcb54a18fa0c06efa19f290e0c7106c287944c9b1b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205346052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f02c719ef94496b7e6b92b6f5e381407904a4ca59c2e0b0fd8efc218cea02ae`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 15:02:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:02:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:02:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 16 Aug 2023 15:02:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 16 Aug 2023 15:02:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 15:02:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 16 Aug 2023 15:02:38 GMT
ENV ROS_DISTRO=noetic
# Wed, 16 Aug 2023 15:05:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:05:32 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 16 Aug 2023 15:05:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:05:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15340a0f1b3eb99199990d967961a6a7095eccee4a7e4b4a73d5f695318b9c0`  
		Last Modified: Wed, 16 Aug 2023 15:36:35 GMT  
		Size: 1.2 MB (1199928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721226cd510b20bfa5e238d93f0c82d74955fe088f6a76baf10edd313c20865d`  
		Last Modified: Wed, 16 Aug 2023 15:36:33 GMT  
		Size: 5.5 MB (5533316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee0e3a60370b22bc9740a59b8aa14fb13ccdff17844a659d622e95eb49aadee`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7439f340ca803a67b808daca6069b8332fb18927cf901c22569e32b8fbbe825d`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72576e868a3e7c4d3fc831d20bce9ee1236edd7e6713b812cecc47fa9bdc66d`  
		Last Modified: Wed, 16 Aug 2023 15:37:06 GMT  
		Size: 171.4 MB (171409809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d637f1ed1675da3f70e7ae5fdd2e2f2b82c99cfb4bfeeec599928e70b238651`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:eb0f0b232afea34865b29798f09433bff410dd5b28b0a3dfccb4005be34d96f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:ba314e83e1140e38b730ded90897ff4abf9920a365aa66f67bf4442263ae7407
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212362926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c8e3327cb9948f69b0783b7a885aed24c0a9895e05b7e7b560ef3a8d1e4d64`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:38:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:38:29 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:38:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:38:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:40:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:40:36 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:40:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:40:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff84dd75ab0363da2809c202391ffc2d59534b4888fb855bfd3e21fba17c6fc`  
		Last Modified: Tue, 04 Jul 2023 20:06:54 GMT  
		Size: 1.2 MB (1198708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564b5c67648727c462a4c2ba9d04cdbfa852b527efa36e4c6a859b58454f1c06`  
		Last Modified: Tue, 04 Jul 2023 20:06:53 GMT  
		Size: 5.6 MB (5553847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d18d779d6732554da8eb52855df2ccfe7921f00655dffb89550af33715f184`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc5d180dd93ee0210935b93b72cc533ed3b35e05a47dc0b20fb5b5b9884e4c3`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac36e4a2604385d7a84264dc122ac61dd1af8f304d486fc983703238a0d02333`  
		Last Modified: Tue, 04 Jul 2023 20:07:19 GMT  
		Size: 177.0 MB (177027946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca272865f67e094abd7a450c446c31552297e72292785448cac9df1ac6bdcd1`  
		Last Modified: Tue, 04 Jul 2023 20:06:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:8a5ac73d28a505b16a86f3e7185d0c1434c7dbf19ba486945d55d589316b5333
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188011580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67480a9eb0025f587eae298a084f3ebb439aa33830002554ff9936d59bdc8b7f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:58:19 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:58:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:58:22 GMT
ADD file:8bedca16bf416520f5df29175a99b07585281465c459544b9f9679016f59762a in / 
# Wed, 28 Jun 2023 09:58:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:51:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:52:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 04 Jul 2023 19:52:11 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV LC_ALL=C.UTF-8
# Tue, 04 Jul 2023 19:52:11 GMT
ENV ROS_DISTRO=noetic
# Tue, 04 Jul 2023 19:55:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 04 Jul 2023 19:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 19:55:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:06e53fabee8df31622850c604f9242a52a466ec4eb75320019bdfdc8ec311692`  
		Last Modified: Tue, 04 Jul 2023 06:22:20 GMT  
		Size: 24.6 MB (24588135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf8ae4844234b1655ffcc66de6ff4d8fb9d8dc5b263579abf1c0f08fc45c10b`  
		Last Modified: Tue, 04 Jul 2023 20:06:37 GMT  
		Size: 1.2 MB (1198714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f870418e12b4135248455da61f5521096265e859ed7df1641c96d8052c1cd1ed`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 4.7 MB (4679197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb37cb4cc4c6e905769f0ad1f740744e276e496b07b5efc7e4dcfd333e303892`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e584269a8e1f1afb39b1c87e053140430bf059f1a78c8091f862a0a6d7ce9d0`  
		Last Modified: Tue, 04 Jul 2023 20:06:34 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f17c57312bea1c2c36a5f0b529de68ac63f57144e4e7911f2bfbdaa007f1cc2`  
		Last Modified: Tue, 04 Jul 2023 20:07:03 GMT  
		Size: 157.5 MB (157543123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145cb0493e0b9da981ce0cd0c9aeab054329b78efe17d28f3a208cfe95f617a1`  
		Last Modified: Tue, 04 Jul 2023 20:06:35 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f2439b922cac680e8c6cefcb54a18fa0c06efa19f290e0c7106c287944c9b1b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205346052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f02c719ef94496b7e6b92b6f5e381407904a4ca59c2e0b0fd8efc218cea02ae`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 15:02:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:02:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:02:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 16 Aug 2023 15:02:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 16 Aug 2023 15:02:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 15:02:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 16 Aug 2023 15:02:38 GMT
ENV ROS_DISTRO=noetic
# Wed, 16 Aug 2023 15:05:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:05:32 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 16 Aug 2023 15:05:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:05:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15340a0f1b3eb99199990d967961a6a7095eccee4a7e4b4a73d5f695318b9c0`  
		Last Modified: Wed, 16 Aug 2023 15:36:35 GMT  
		Size: 1.2 MB (1199928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721226cd510b20bfa5e238d93f0c82d74955fe088f6a76baf10edd313c20865d`  
		Last Modified: Wed, 16 Aug 2023 15:36:33 GMT  
		Size: 5.5 MB (5533316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee0e3a60370b22bc9740a59b8aa14fb13ccdff17844a659d622e95eb49aadee`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7439f340ca803a67b808daca6069b8332fb18927cf901c22569e32b8fbbe825d`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72576e868a3e7c4d3fc831d20bce9ee1236edd7e6713b812cecc47fa9bdc66d`  
		Last Modified: Wed, 16 Aug 2023 15:37:06 GMT  
		Size: 171.4 MB (171409809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d637f1ed1675da3f70e7ae5fdd2e2f2b82c99cfb4bfeeec599928e70b238651`  
		Last Modified: Wed, 16 Aug 2023 15:36:32 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling`

```console
$ docker pull ros@sha256:4d586f0c8586db0352b07ffa1f0304b8011eaf95ca559c52807d8edec497a021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:10ba291dc0ba9e7d80bdd8dc2c6e5b75b9d3b7921a04cd9decc06fa24ae02481
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268621992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06ecd9b25343291ebc10de5b11c044e8298b5d7caca26d6e99fc5f615705ea6`
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
# Tue, 04 Jul 2023 20:02:59 GMT
ENV ROS_DISTRO=rolling
# Tue, 04 Jul 2023 20:03:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:03:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 20:03:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 20:03:41 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 20:04:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:04:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 20:04:10 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 04 Jul 2023 20:04:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:36f56d27fecf4e210a05a82e8866e65c93e56a1c334d05dc920874efb491bc42`  
		Last Modified: Tue, 04 Jul 2023 20:14:32 GMT  
		Size: 124.2 MB (124153171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dfb64b9fd9711f9b089a583e356a45f3db3501069df5009532484efb69ee77`  
		Last Modified: Tue, 04 Jul 2023 20:14:13 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecc8a7939fc2509dd255cb3900f371842f82522c2324050f42a217867f39fd2`  
		Last Modified: Tue, 04 Jul 2023 20:14:51 GMT  
		Size: 85.0 MB (84994763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf34a0e75a6de1feb7201f461d07ea0bbbc2255a4efa547ab968d5b49fc018f6`  
		Last Modified: Tue, 04 Jul 2023 20:14:40 GMT  
		Size: 290.5 KB (290460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888b8a9ac31ed4b14680802a41bf298d370d9a39a1f7942dcc8292beaaa4d200`  
		Last Modified: Tue, 04 Jul 2023 20:14:40 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d93d908b21c5425c4862d4f88c4cf270ae4c5b11118f7f286f07595d9e4b6ca`  
		Last Modified: Tue, 04 Jul 2023 20:14:44 GMT  
		Size: 23.7 MB (23705649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:852b8c15a64c5755fdf166716b115dd53174bfbe95de033ab0f8f4de609a1d5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261296384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0f75803d596392076e9c7e82c722cd8986599749c79306733124ef1a5d105c`
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
# Wed, 16 Aug 2023 15:32:51 GMT
ENV ROS_DISTRO=rolling
# Wed, 16 Aug 2023 15:33:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:33:30 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 16 Aug 2023 15:33:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:33:30 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:33:51 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:33:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 16 Aug 2023 15:33:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 16 Aug 2023 15:34:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:efa5deeb8cd59ceb959c6ec5aa7e733af2980f29e19d1e44c08427388512a83b`  
		Last Modified: Wed, 16 Aug 2023 15:43:22 GMT  
		Size: 121.6 MB (121644205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24342a10adab54d96381198756c317ea13e13e4dca3a7369fb10b15e90a411`  
		Last Modified: Wed, 16 Aug 2023 15:43:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fefcd96171a0c90ad937ce0b207cdc8105ef4ac5a909c0997a4b3eddb272eec`  
		Last Modified: Wed, 16 Aug 2023 15:43:38 GMT  
		Size: 82.8 MB (82841219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06ba8f01394a20b4e6c7f7e2e5e1dc6e1c447a0b33f34dbe0c2f324f2679606`  
		Last Modified: Wed, 16 Aug 2023 15:43:31 GMT  
		Size: 293.9 KB (293862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d0a5ecacf99244783e4891c25cd7276bb93583d2a6855cf0e42d9b6302546d`  
		Last Modified: Wed, 16 Aug 2023 15:43:31 GMT  
		Size: 2.4 KB (2405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f801f916fc7c40a38e17c9be47b08fa18b6e67bb2328e039bcdfda1f0eacdb`  
		Last Modified: Wed, 16 Aug 2023 15:43:33 GMT  
		Size: 23.1 MB (23103844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:c33adf56dbf548a801de7196b0eb39b41469834e40dc291a9dc8469eb764e13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:753fb2d607a0957b322b96f7dae9e829e03fd653b6bbe21f9864cd197237df67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **958.4 MB (958400960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741e5b2b653e13ba8ec5903f9374a3275f0fcb99808da4279779ffd48dad008d`
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
# Tue, 04 Jul 2023 20:02:59 GMT
ENV ROS_DISTRO=rolling
# Tue, 04 Jul 2023 20:03:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:03:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 20:03:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 20:03:41 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 20:04:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:04:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 20:04:10 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 04 Jul 2023 20:04:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:05:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:36f56d27fecf4e210a05a82e8866e65c93e56a1c334d05dc920874efb491bc42`  
		Last Modified: Tue, 04 Jul 2023 20:14:32 GMT  
		Size: 124.2 MB (124153171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dfb64b9fd9711f9b089a583e356a45f3db3501069df5009532484efb69ee77`  
		Last Modified: Tue, 04 Jul 2023 20:14:13 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecc8a7939fc2509dd255cb3900f371842f82522c2324050f42a217867f39fd2`  
		Last Modified: Tue, 04 Jul 2023 20:14:51 GMT  
		Size: 85.0 MB (84994763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf34a0e75a6de1feb7201f461d07ea0bbbc2255a4efa547ab968d5b49fc018f6`  
		Last Modified: Tue, 04 Jul 2023 20:14:40 GMT  
		Size: 290.5 KB (290460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888b8a9ac31ed4b14680802a41bf298d370d9a39a1f7942dcc8292beaaa4d200`  
		Last Modified: Tue, 04 Jul 2023 20:14:40 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d93d908b21c5425c4862d4f88c4cf270ae4c5b11118f7f286f07595d9e4b6ca`  
		Last Modified: Tue, 04 Jul 2023 20:14:44 GMT  
		Size: 23.7 MB (23705649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b042871bb7ac7cfd7dbeb91d80a45cc60535f75e42242d951d3659e04050a8`  
		Last Modified: Tue, 04 Jul 2023 20:16:28 GMT  
		Size: 689.8 MB (689778968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3bd77187cfae18d6c8ba79b55bad5a6cc49d84c950f6c8f6e05e05986e581813
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.0 MB (920012545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f66bf96e0c90a72813cb2db56f63f3547a6e3555709a942df139b6009178528`
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
# Wed, 16 Aug 2023 15:32:51 GMT
ENV ROS_DISTRO=rolling
# Wed, 16 Aug 2023 15:33:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:33:30 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 16 Aug 2023 15:33:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:33:30 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:33:51 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:33:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 16 Aug 2023 15:33:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 16 Aug 2023 15:34:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:35:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:efa5deeb8cd59ceb959c6ec5aa7e733af2980f29e19d1e44c08427388512a83b`  
		Last Modified: Wed, 16 Aug 2023 15:43:22 GMT  
		Size: 121.6 MB (121644205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24342a10adab54d96381198756c317ea13e13e4dca3a7369fb10b15e90a411`  
		Last Modified: Wed, 16 Aug 2023 15:43:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fefcd96171a0c90ad937ce0b207cdc8105ef4ac5a909c0997a4b3eddb272eec`  
		Last Modified: Wed, 16 Aug 2023 15:43:38 GMT  
		Size: 82.8 MB (82841219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06ba8f01394a20b4e6c7f7e2e5e1dc6e1c447a0b33f34dbe0c2f324f2679606`  
		Last Modified: Wed, 16 Aug 2023 15:43:31 GMT  
		Size: 293.9 KB (293862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d0a5ecacf99244783e4891c25cd7276bb93583d2a6855cf0e42d9b6302546d`  
		Last Modified: Wed, 16 Aug 2023 15:43:31 GMT  
		Size: 2.4 KB (2405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f801f916fc7c40a38e17c9be47b08fa18b6e67bb2328e039bcdfda1f0eacdb`  
		Last Modified: Wed, 16 Aug 2023 15:43:33 GMT  
		Size: 23.1 MB (23103844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9215af30951672b767f1a27d171e73c194e24ac51315ceb006cdb37119d4eac4`  
		Last Modified: Wed, 16 Aug 2023 15:44:53 GMT  
		Size: 658.7 MB (658716161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception-jammy`

```console
$ docker pull ros@sha256:c33adf56dbf548a801de7196b0eb39b41469834e40dc291a9dc8469eb764e13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:753fb2d607a0957b322b96f7dae9e829e03fd653b6bbe21f9864cd197237df67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **958.4 MB (958400960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741e5b2b653e13ba8ec5903f9374a3275f0fcb99808da4279779ffd48dad008d`
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
# Tue, 04 Jul 2023 20:02:59 GMT
ENV ROS_DISTRO=rolling
# Tue, 04 Jul 2023 20:03:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:03:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 20:03:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 20:03:41 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 20:04:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:04:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 20:04:10 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 04 Jul 2023 20:04:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:05:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:36f56d27fecf4e210a05a82e8866e65c93e56a1c334d05dc920874efb491bc42`  
		Last Modified: Tue, 04 Jul 2023 20:14:32 GMT  
		Size: 124.2 MB (124153171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dfb64b9fd9711f9b089a583e356a45f3db3501069df5009532484efb69ee77`  
		Last Modified: Tue, 04 Jul 2023 20:14:13 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecc8a7939fc2509dd255cb3900f371842f82522c2324050f42a217867f39fd2`  
		Last Modified: Tue, 04 Jul 2023 20:14:51 GMT  
		Size: 85.0 MB (84994763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf34a0e75a6de1feb7201f461d07ea0bbbc2255a4efa547ab968d5b49fc018f6`  
		Last Modified: Tue, 04 Jul 2023 20:14:40 GMT  
		Size: 290.5 KB (290460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888b8a9ac31ed4b14680802a41bf298d370d9a39a1f7942dcc8292beaaa4d200`  
		Last Modified: Tue, 04 Jul 2023 20:14:40 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d93d908b21c5425c4862d4f88c4cf270ae4c5b11118f7f286f07595d9e4b6ca`  
		Last Modified: Tue, 04 Jul 2023 20:14:44 GMT  
		Size: 23.7 MB (23705649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b042871bb7ac7cfd7dbeb91d80a45cc60535f75e42242d951d3659e04050a8`  
		Last Modified: Tue, 04 Jul 2023 20:16:28 GMT  
		Size: 689.8 MB (689778968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3bd77187cfae18d6c8ba79b55bad5a6cc49d84c950f6c8f6e05e05986e581813
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.0 MB (920012545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f66bf96e0c90a72813cb2db56f63f3547a6e3555709a942df139b6009178528`
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
# Wed, 16 Aug 2023 15:32:51 GMT
ENV ROS_DISTRO=rolling
# Wed, 16 Aug 2023 15:33:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:33:30 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 16 Aug 2023 15:33:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:33:30 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:33:51 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:33:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 16 Aug 2023 15:33:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 16 Aug 2023 15:34:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:35:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:efa5deeb8cd59ceb959c6ec5aa7e733af2980f29e19d1e44c08427388512a83b`  
		Last Modified: Wed, 16 Aug 2023 15:43:22 GMT  
		Size: 121.6 MB (121644205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24342a10adab54d96381198756c317ea13e13e4dca3a7369fb10b15e90a411`  
		Last Modified: Wed, 16 Aug 2023 15:43:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fefcd96171a0c90ad937ce0b207cdc8105ef4ac5a909c0997a4b3eddb272eec`  
		Last Modified: Wed, 16 Aug 2023 15:43:38 GMT  
		Size: 82.8 MB (82841219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06ba8f01394a20b4e6c7f7e2e5e1dc6e1c447a0b33f34dbe0c2f324f2679606`  
		Last Modified: Wed, 16 Aug 2023 15:43:31 GMT  
		Size: 293.9 KB (293862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d0a5ecacf99244783e4891c25cd7276bb93583d2a6855cf0e42d9b6302546d`  
		Last Modified: Wed, 16 Aug 2023 15:43:31 GMT  
		Size: 2.4 KB (2405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f801f916fc7c40a38e17c9be47b08fa18b6e67bb2328e039bcdfda1f0eacdb`  
		Last Modified: Wed, 16 Aug 2023 15:43:33 GMT  
		Size: 23.1 MB (23103844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9215af30951672b767f1a27d171e73c194e24ac51315ceb006cdb37119d4eac4`  
		Last Modified: Wed, 16 Aug 2023 15:44:53 GMT  
		Size: 658.7 MB (658716161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:4d586f0c8586db0352b07ffa1f0304b8011eaf95ca559c52807d8edec497a021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:10ba291dc0ba9e7d80bdd8dc2c6e5b75b9d3b7921a04cd9decc06fa24ae02481
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268621992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06ecd9b25343291ebc10de5b11c044e8298b5d7caca26d6e99fc5f615705ea6`
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
# Tue, 04 Jul 2023 20:02:59 GMT
ENV ROS_DISTRO=rolling
# Tue, 04 Jul 2023 20:03:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:03:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 20:03:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 20:03:41 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 20:04:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:04:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 20:04:10 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 04 Jul 2023 20:04:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:36f56d27fecf4e210a05a82e8866e65c93e56a1c334d05dc920874efb491bc42`  
		Last Modified: Tue, 04 Jul 2023 20:14:32 GMT  
		Size: 124.2 MB (124153171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dfb64b9fd9711f9b089a583e356a45f3db3501069df5009532484efb69ee77`  
		Last Modified: Tue, 04 Jul 2023 20:14:13 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecc8a7939fc2509dd255cb3900f371842f82522c2324050f42a217867f39fd2`  
		Last Modified: Tue, 04 Jul 2023 20:14:51 GMT  
		Size: 85.0 MB (84994763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf34a0e75a6de1feb7201f461d07ea0bbbc2255a4efa547ab968d5b49fc018f6`  
		Last Modified: Tue, 04 Jul 2023 20:14:40 GMT  
		Size: 290.5 KB (290460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888b8a9ac31ed4b14680802a41bf298d370d9a39a1f7942dcc8292beaaa4d200`  
		Last Modified: Tue, 04 Jul 2023 20:14:40 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d93d908b21c5425c4862d4f88c4cf270ae4c5b11118f7f286f07595d9e4b6ca`  
		Last Modified: Tue, 04 Jul 2023 20:14:44 GMT  
		Size: 23.7 MB (23705649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:852b8c15a64c5755fdf166716b115dd53174bfbe95de033ab0f8f4de609a1d5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261296384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0f75803d596392076e9c7e82c722cd8986599749c79306733124ef1a5d105c`
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
# Wed, 16 Aug 2023 15:32:51 GMT
ENV ROS_DISTRO=rolling
# Wed, 16 Aug 2023 15:33:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:33:30 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 16 Aug 2023 15:33:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:33:30 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:33:51 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:33:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 16 Aug 2023 15:33:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 16 Aug 2023 15:34:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:efa5deeb8cd59ceb959c6ec5aa7e733af2980f29e19d1e44c08427388512a83b`  
		Last Modified: Wed, 16 Aug 2023 15:43:22 GMT  
		Size: 121.6 MB (121644205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24342a10adab54d96381198756c317ea13e13e4dca3a7369fb10b15e90a411`  
		Last Modified: Wed, 16 Aug 2023 15:43:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fefcd96171a0c90ad937ce0b207cdc8105ef4ac5a909c0997a4b3eddb272eec`  
		Last Modified: Wed, 16 Aug 2023 15:43:38 GMT  
		Size: 82.8 MB (82841219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06ba8f01394a20b4e6c7f7e2e5e1dc6e1c447a0b33f34dbe0c2f324f2679606`  
		Last Modified: Wed, 16 Aug 2023 15:43:31 GMT  
		Size: 293.9 KB (293862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d0a5ecacf99244783e4891c25cd7276bb93583d2a6855cf0e42d9b6302546d`  
		Last Modified: Wed, 16 Aug 2023 15:43:31 GMT  
		Size: 2.4 KB (2405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f801f916fc7c40a38e17c9be47b08fa18b6e67bb2328e039bcdfda1f0eacdb`  
		Last Modified: Wed, 16 Aug 2023 15:43:33 GMT  
		Size: 23.1 MB (23103844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base-jammy`

```console
$ docker pull ros@sha256:4d586f0c8586db0352b07ffa1f0304b8011eaf95ca559c52807d8edec497a021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:10ba291dc0ba9e7d80bdd8dc2c6e5b75b9d3b7921a04cd9decc06fa24ae02481
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268621992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06ecd9b25343291ebc10de5b11c044e8298b5d7caca26d6e99fc5f615705ea6`
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
# Tue, 04 Jul 2023 20:02:59 GMT
ENV ROS_DISTRO=rolling
# Tue, 04 Jul 2023 20:03:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:03:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 20:03:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 20:03:41 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 20:04:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:04:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 04 Jul 2023 20:04:10 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 04 Jul 2023 20:04:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:36f56d27fecf4e210a05a82e8866e65c93e56a1c334d05dc920874efb491bc42`  
		Last Modified: Tue, 04 Jul 2023 20:14:32 GMT  
		Size: 124.2 MB (124153171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dfb64b9fd9711f9b089a583e356a45f3db3501069df5009532484efb69ee77`  
		Last Modified: Tue, 04 Jul 2023 20:14:13 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecc8a7939fc2509dd255cb3900f371842f82522c2324050f42a217867f39fd2`  
		Last Modified: Tue, 04 Jul 2023 20:14:51 GMT  
		Size: 85.0 MB (84994763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf34a0e75a6de1feb7201f461d07ea0bbbc2255a4efa547ab968d5b49fc018f6`  
		Last Modified: Tue, 04 Jul 2023 20:14:40 GMT  
		Size: 290.5 KB (290460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888b8a9ac31ed4b14680802a41bf298d370d9a39a1f7942dcc8292beaaa4d200`  
		Last Modified: Tue, 04 Jul 2023 20:14:40 GMT  
		Size: 2.4 KB (2411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d93d908b21c5425c4862d4f88c4cf270ae4c5b11118f7f286f07595d9e4b6ca`  
		Last Modified: Tue, 04 Jul 2023 20:14:44 GMT  
		Size: 23.7 MB (23705649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:852b8c15a64c5755fdf166716b115dd53174bfbe95de033ab0f8f4de609a1d5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261296384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0f75803d596392076e9c7e82c722cd8986599749c79306733124ef1a5d105c`
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
# Wed, 16 Aug 2023 15:32:51 GMT
ENV ROS_DISTRO=rolling
# Wed, 16 Aug 2023 15:33:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:33:30 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 16 Aug 2023 15:33:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:33:30 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:33:51 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:33:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 16 Aug 2023 15:33:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 16 Aug 2023 15:34:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:efa5deeb8cd59ceb959c6ec5aa7e733af2980f29e19d1e44c08427388512a83b`  
		Last Modified: Wed, 16 Aug 2023 15:43:22 GMT  
		Size: 121.6 MB (121644205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24342a10adab54d96381198756c317ea13e13e4dca3a7369fb10b15e90a411`  
		Last Modified: Wed, 16 Aug 2023 15:43:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fefcd96171a0c90ad937ce0b207cdc8105ef4ac5a909c0997a4b3eddb272eec`  
		Last Modified: Wed, 16 Aug 2023 15:43:38 GMT  
		Size: 82.8 MB (82841219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06ba8f01394a20b4e6c7f7e2e5e1dc6e1c447a0b33f34dbe0c2f324f2679606`  
		Last Modified: Wed, 16 Aug 2023 15:43:31 GMT  
		Size: 293.9 KB (293862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d0a5ecacf99244783e4891c25cd7276bb93583d2a6855cf0e42d9b6302546d`  
		Last Modified: Wed, 16 Aug 2023 15:43:31 GMT  
		Size: 2.4 KB (2405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f801f916fc7c40a38e17c9be47b08fa18b6e67bb2328e039bcdfda1f0eacdb`  
		Last Modified: Wed, 16 Aug 2023 15:43:33 GMT  
		Size: 23.1 MB (23103844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:0741cd153d233a6928c165fc09f2d69a5cdcdd731b0d9223b2043255fc410b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:39522d03bb05bfa53c0a19441acde188f907f622430592a2b05fd2c07df54403
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159628709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761854bf5e6c928cb47d4c22abd10851d45873226e4a6b73f7e4902604c1cbf0`
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
# Tue, 04 Jul 2023 20:02:59 GMT
ENV ROS_DISTRO=rolling
# Tue, 04 Jul 2023 20:03:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:03:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 20:03:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 20:03:41 GMT
CMD ["bash"]
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
	-	`sha256:36f56d27fecf4e210a05a82e8866e65c93e56a1c334d05dc920874efb491bc42`  
		Last Modified: Tue, 04 Jul 2023 20:14:32 GMT  
		Size: 124.2 MB (124153171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dfb64b9fd9711f9b089a583e356a45f3db3501069df5009532484efb69ee77`  
		Last Modified: Tue, 04 Jul 2023 20:14:13 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f0c4d3616cceea762304a2befda3fa3172661426a12924e0f6207b76343423b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155055054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ba1a5fe8c88b6d64f63d5b7347a0d2a9da74ce7a7be61937adc5384246ca24`
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
# Wed, 16 Aug 2023 15:32:51 GMT
ENV ROS_DISTRO=rolling
# Wed, 16 Aug 2023 15:33:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:33:30 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 16 Aug 2023 15:33:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:33:30 GMT
CMD ["bash"]
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
	-	`sha256:efa5deeb8cd59ceb959c6ec5aa7e733af2980f29e19d1e44c08427388512a83b`  
		Last Modified: Wed, 16 Aug 2023 15:43:22 GMT  
		Size: 121.6 MB (121644205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24342a10adab54d96381198756c317ea13e13e4dca3a7369fb10b15e90a411`  
		Last Modified: Wed, 16 Aug 2023 15:43:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core-jammy`

```console
$ docker pull ros@sha256:0741cd153d233a6928c165fc09f2d69a5cdcdd731b0d9223b2043255fc410b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:39522d03bb05bfa53c0a19441acde188f907f622430592a2b05fd2c07df54403
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159628709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761854bf5e6c928cb47d4c22abd10851d45873226e4a6b73f7e4902604c1cbf0`
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
# Tue, 04 Jul 2023 20:02:59 GMT
ENV ROS_DISTRO=rolling
# Tue, 04 Jul 2023 20:03:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 20:03:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 04 Jul 2023 20:03:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 04 Jul 2023 20:03:41 GMT
CMD ["bash"]
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
	-	`sha256:36f56d27fecf4e210a05a82e8866e65c93e56a1c334d05dc920874efb491bc42`  
		Last Modified: Tue, 04 Jul 2023 20:14:32 GMT  
		Size: 124.2 MB (124153171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dfb64b9fd9711f9b089a583e356a45f3db3501069df5009532484efb69ee77`  
		Last Modified: Tue, 04 Jul 2023 20:14:13 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f0c4d3616cceea762304a2befda3fa3172661426a12924e0f6207b76343423b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155055054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ba1a5fe8c88b6d64f63d5b7347a0d2a9da74ce7a7be61937adc5384246ca24`
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
# Wed, 16 Aug 2023 15:32:51 GMT
ENV ROS_DISTRO=rolling
# Wed, 16 Aug 2023 15:33:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:33:30 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 16 Aug 2023 15:33:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 16 Aug 2023 15:33:30 GMT
CMD ["bash"]
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
	-	`sha256:efa5deeb8cd59ceb959c6ec5aa7e733af2980f29e19d1e44c08427388512a83b`  
		Last Modified: Wed, 16 Aug 2023 15:43:22 GMT  
		Size: 121.6 MB (121644205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24342a10adab54d96381198756c317ea13e13e4dca3a7369fb10b15e90a411`  
		Last Modified: Wed, 16 Aug 2023 15:43:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
