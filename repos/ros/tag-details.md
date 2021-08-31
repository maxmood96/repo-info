<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ros`

-	[`ros:foxy`](#rosfoxy)
-	[`ros:foxy-ros-base`](#rosfoxy-ros-base)
-	[`ros:foxy-ros-base-focal`](#rosfoxy-ros-base-focal)
-	[`ros:foxy-ros-core`](#rosfoxy-ros-core)
-	[`ros:foxy-ros-core-focal`](#rosfoxy-ros-core-focal)
-	[`ros:foxy-ros1-bridge`](#rosfoxy-ros1-bridge)
-	[`ros:foxy-ros1-bridge-focal`](#rosfoxy-ros1-bridge-focal)
-	[`ros:galactic`](#rosgalactic)
-	[`ros:galactic-ros-base`](#rosgalactic-ros-base)
-	[`ros:galactic-ros-base-focal`](#rosgalactic-ros-base-focal)
-	[`ros:galactic-ros-core`](#rosgalactic-ros-core)
-	[`ros:galactic-ros-core-focal`](#rosgalactic-ros-core-focal)
-	[`ros:galactic-ros1-bridge`](#rosgalactic-ros1-bridge)
-	[`ros:galactic-ros1-bridge-focal`](#rosgalactic-ros1-bridge-focal)
-	[`ros:latest`](#roslatest)
-	[`ros:melodic`](#rosmelodic)
-	[`ros:melodic-perception`](#rosmelodic-perception)
-	[`ros:melodic-perception-bionic`](#rosmelodic-perception-bionic)
-	[`ros:melodic-robot`](#rosmelodic-robot)
-	[`ros:melodic-robot-bionic`](#rosmelodic-robot-bionic)
-	[`ros:melodic-ros-base`](#rosmelodic-ros-base)
-	[`ros:melodic-ros-base-bionic`](#rosmelodic-ros-base-bionic)
-	[`ros:melodic-ros-core`](#rosmelodic-ros-core)
-	[`ros:melodic-ros-core-bionic`](#rosmelodic-ros-core-bionic)
-	[`ros:noetic`](#rosnoetic)
-	[`ros:noetic-perception`](#rosnoetic-perception)
-	[`ros:noetic-perception-buster`](#rosnoetic-perception-buster)
-	[`ros:noetic-perception-focal`](#rosnoetic-perception-focal)
-	[`ros:noetic-robot`](#rosnoetic-robot)
-	[`ros:noetic-robot-buster`](#rosnoetic-robot-buster)
-	[`ros:noetic-robot-focal`](#rosnoetic-robot-focal)
-	[`ros:noetic-ros-base`](#rosnoetic-ros-base)
-	[`ros:noetic-ros-base-buster`](#rosnoetic-ros-base-buster)
-	[`ros:noetic-ros-base-focal`](#rosnoetic-ros-base-focal)
-	[`ros:noetic-ros-core`](#rosnoetic-ros-core)
-	[`ros:noetic-ros-core-buster`](#rosnoetic-ros-core-buster)
-	[`ros:noetic-ros-core-focal`](#rosnoetic-ros-core-focal)
-	[`ros:rolling`](#rosrolling)
-	[`ros:rolling-ros-base`](#rosrolling-ros-base)
-	[`ros:rolling-ros-base-focal`](#rosrolling-ros-base-focal)
-	[`ros:rolling-ros-core`](#rosrolling-ros-core)
-	[`ros:rolling-ros-core-focal`](#rosrolling-ros-core-focal)
-	[`ros:rolling-ros1-bridge`](#rosrolling-ros1-bridge)
-	[`ros:rolling-ros1-bridge-focal`](#rosrolling-ros1-bridge-focal)

## `ros:foxy`

```console
$ docker pull ros@sha256:551bbab116cb41f010d73b4976f59bb4990d9543d07cf8a7b26dc3b1b758f07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy` - linux; amd64

```console
$ docker pull ros@sha256:c6c4dcdcdba4646d8a6bebd6448625ed80cb18d8f1cae85e21a55a7e3d7ffec2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236641898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df65e6ff4c8f4ed1107f086582df71878afcbeb8d71e39214959ca5517adda77`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV ROS_DISTRO=foxy
# Tue, 27 Jul 2021 01:03:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:03:15 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:03:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:03:15 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:04:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:04:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 01:04:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 27 Jul 2021 01:04:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6567e1e6579146c6323e3e1408e11008ac77c4d5c5ed8e5943332bc7254a56a5`  
		Last Modified: Tue, 27 Jul 2021 01:17:18 GMT  
		Size: 120.0 MB (119974774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88662ced653f598458e0c89695b0fb9e3e8bce9259f6efed11574a8f7ae220f5`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588ff9fb226bda0f04608743623449eccc27c7cc333932238b83bb7ec32398ea`  
		Last Modified: Tue, 27 Jul 2021 01:17:40 GMT  
		Size: 70.8 MB (70843719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a912ea800775dd8e48e78dac7555405832fcd4ad530eeae4cc976ba08ed32dbf`  
		Last Modified: Tue, 27 Jul 2021 01:17:30 GMT  
		Size: 238.5 KB (238478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b8c908ab26db0ef9598ff88bf38a1008a48fa6cc4f426e318321c589e254b4`  
		Last Modified: Tue, 27 Jul 2021 01:17:29 GMT  
		Size: 2.0 KB (2049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3ba81eeaf2f769cfb5f06e3b9de2651d04e9927d713613e7e5e7f86afbdba4`  
		Last Modified: Tue, 27 Jul 2021 01:17:32 GMT  
		Size: 10.3 MB (10282984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:669ca86db8856ea020734faa9aa88d4cab494d13c65095b86722918c92a3e66f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 MB (212759588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a0be06c48eb711e3e05a4dae51ed27feebd9df75cd7c64e2148ca2aee9ab19`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV ROS_DISTRO=foxy
# Tue, 31 Aug 2021 02:40:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:56 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:40:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:40:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:41:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:41:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:41:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 31 Aug 2021 02:41:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac2567afd7f21270eaf5dac9596df45b6dda0b77d64188744a7081a5f346b5`  
		Last Modified: Tue, 31 Aug 2021 02:55:58 GMT  
		Size: 104.2 MB (104162618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e0daf045c79605e6b79149e30817a2a6a12ee94bd746d4ddbf97b159b86d9f`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053652fdf77cf09c2d5f748e1392a941b0a2640722c2e70d661cb0f79ed668cf`  
		Last Modified: Tue, 31 Aug 2021 02:56:20 GMT  
		Size: 65.2 MB (65183560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aedc85ca67006659dbfc2b17452494645c1f0e417864446282ae6f592dc634e`  
		Last Modified: Tue, 31 Aug 2021 02:56:10 GMT  
		Size: 240.5 KB (240543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf81879f4a40b97c2359dafad0f780449e33d1663620a7c84e6edc1d195e3e4`  
		Last Modified: Tue, 31 Aug 2021 02:56:09 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68fc5fc59c2a35f0a91dba364f8820a1bdf634a40ffa0598d351cb20b4af65a`  
		Last Modified: Tue, 31 Aug 2021 02:56:11 GMT  
		Size: 9.3 MB (9298963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-base`

```console
$ docker pull ros@sha256:551bbab116cb41f010d73b4976f59bb4990d9543d07cf8a7b26dc3b1b758f07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:c6c4dcdcdba4646d8a6bebd6448625ed80cb18d8f1cae85e21a55a7e3d7ffec2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236641898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df65e6ff4c8f4ed1107f086582df71878afcbeb8d71e39214959ca5517adda77`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV ROS_DISTRO=foxy
# Tue, 27 Jul 2021 01:03:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:03:15 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:03:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:03:15 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:04:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:04:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 01:04:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 27 Jul 2021 01:04:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6567e1e6579146c6323e3e1408e11008ac77c4d5c5ed8e5943332bc7254a56a5`  
		Last Modified: Tue, 27 Jul 2021 01:17:18 GMT  
		Size: 120.0 MB (119974774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88662ced653f598458e0c89695b0fb9e3e8bce9259f6efed11574a8f7ae220f5`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588ff9fb226bda0f04608743623449eccc27c7cc333932238b83bb7ec32398ea`  
		Last Modified: Tue, 27 Jul 2021 01:17:40 GMT  
		Size: 70.8 MB (70843719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a912ea800775dd8e48e78dac7555405832fcd4ad530eeae4cc976ba08ed32dbf`  
		Last Modified: Tue, 27 Jul 2021 01:17:30 GMT  
		Size: 238.5 KB (238478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b8c908ab26db0ef9598ff88bf38a1008a48fa6cc4f426e318321c589e254b4`  
		Last Modified: Tue, 27 Jul 2021 01:17:29 GMT  
		Size: 2.0 KB (2049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3ba81eeaf2f769cfb5f06e3b9de2651d04e9927d713613e7e5e7f86afbdba4`  
		Last Modified: Tue, 27 Jul 2021 01:17:32 GMT  
		Size: 10.3 MB (10282984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:669ca86db8856ea020734faa9aa88d4cab494d13c65095b86722918c92a3e66f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 MB (212759588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a0be06c48eb711e3e05a4dae51ed27feebd9df75cd7c64e2148ca2aee9ab19`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV ROS_DISTRO=foxy
# Tue, 31 Aug 2021 02:40:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:56 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:40:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:40:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:41:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:41:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:41:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 31 Aug 2021 02:41:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac2567afd7f21270eaf5dac9596df45b6dda0b77d64188744a7081a5f346b5`  
		Last Modified: Tue, 31 Aug 2021 02:55:58 GMT  
		Size: 104.2 MB (104162618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e0daf045c79605e6b79149e30817a2a6a12ee94bd746d4ddbf97b159b86d9f`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053652fdf77cf09c2d5f748e1392a941b0a2640722c2e70d661cb0f79ed668cf`  
		Last Modified: Tue, 31 Aug 2021 02:56:20 GMT  
		Size: 65.2 MB (65183560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aedc85ca67006659dbfc2b17452494645c1f0e417864446282ae6f592dc634e`  
		Last Modified: Tue, 31 Aug 2021 02:56:10 GMT  
		Size: 240.5 KB (240543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf81879f4a40b97c2359dafad0f780449e33d1663620a7c84e6edc1d195e3e4`  
		Last Modified: Tue, 31 Aug 2021 02:56:09 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68fc5fc59c2a35f0a91dba364f8820a1bdf634a40ffa0598d351cb20b4af65a`  
		Last Modified: Tue, 31 Aug 2021 02:56:11 GMT  
		Size: 9.3 MB (9298963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-base-focal`

```console
$ docker pull ros@sha256:551bbab116cb41f010d73b4976f59bb4990d9543d07cf8a7b26dc3b1b758f07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:c6c4dcdcdba4646d8a6bebd6448625ed80cb18d8f1cae85e21a55a7e3d7ffec2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236641898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df65e6ff4c8f4ed1107f086582df71878afcbeb8d71e39214959ca5517adda77`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV ROS_DISTRO=foxy
# Tue, 27 Jul 2021 01:03:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:03:15 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:03:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:03:15 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:04:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:04:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 01:04:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 27 Jul 2021 01:04:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6567e1e6579146c6323e3e1408e11008ac77c4d5c5ed8e5943332bc7254a56a5`  
		Last Modified: Tue, 27 Jul 2021 01:17:18 GMT  
		Size: 120.0 MB (119974774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88662ced653f598458e0c89695b0fb9e3e8bce9259f6efed11574a8f7ae220f5`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588ff9fb226bda0f04608743623449eccc27c7cc333932238b83bb7ec32398ea`  
		Last Modified: Tue, 27 Jul 2021 01:17:40 GMT  
		Size: 70.8 MB (70843719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a912ea800775dd8e48e78dac7555405832fcd4ad530eeae4cc976ba08ed32dbf`  
		Last Modified: Tue, 27 Jul 2021 01:17:30 GMT  
		Size: 238.5 KB (238478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b8c908ab26db0ef9598ff88bf38a1008a48fa6cc4f426e318321c589e254b4`  
		Last Modified: Tue, 27 Jul 2021 01:17:29 GMT  
		Size: 2.0 KB (2049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3ba81eeaf2f769cfb5f06e3b9de2651d04e9927d713613e7e5e7f86afbdba4`  
		Last Modified: Tue, 27 Jul 2021 01:17:32 GMT  
		Size: 10.3 MB (10282984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:669ca86db8856ea020734faa9aa88d4cab494d13c65095b86722918c92a3e66f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 MB (212759588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a0be06c48eb711e3e05a4dae51ed27feebd9df75cd7c64e2148ca2aee9ab19`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV ROS_DISTRO=foxy
# Tue, 31 Aug 2021 02:40:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:56 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:40:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:40:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:41:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:41:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:41:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 31 Aug 2021 02:41:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac2567afd7f21270eaf5dac9596df45b6dda0b77d64188744a7081a5f346b5`  
		Last Modified: Tue, 31 Aug 2021 02:55:58 GMT  
		Size: 104.2 MB (104162618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e0daf045c79605e6b79149e30817a2a6a12ee94bd746d4ddbf97b159b86d9f`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053652fdf77cf09c2d5f748e1392a941b0a2640722c2e70d661cb0f79ed668cf`  
		Last Modified: Tue, 31 Aug 2021 02:56:20 GMT  
		Size: 65.2 MB (65183560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aedc85ca67006659dbfc2b17452494645c1f0e417864446282ae6f592dc634e`  
		Last Modified: Tue, 31 Aug 2021 02:56:10 GMT  
		Size: 240.5 KB (240543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf81879f4a40b97c2359dafad0f780449e33d1663620a7c84e6edc1d195e3e4`  
		Last Modified: Tue, 31 Aug 2021 02:56:09 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68fc5fc59c2a35f0a91dba364f8820a1bdf634a40ffa0598d351cb20b4af65a`  
		Last Modified: Tue, 31 Aug 2021 02:56:11 GMT  
		Size: 9.3 MB (9298963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-core`

```console
$ docker pull ros@sha256:5cefe4b0c192fa365b3e1c32013ca3d7e44f3e8273c38b357815ebf376221655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:683ba2918ce69e5a9601828f8f0391af5a2bcc2dca4343f9d25454e361453575
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155274668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b928b800f2e72749a36214430a363fdcd8e269b7956906b3a97a5728fc34af`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV ROS_DISTRO=foxy
# Tue, 27 Jul 2021 01:03:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:03:15 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:03:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:03:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6567e1e6579146c6323e3e1408e11008ac77c4d5c5ed8e5943332bc7254a56a5`  
		Last Modified: Tue, 27 Jul 2021 01:17:18 GMT  
		Size: 120.0 MB (119974774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88662ced653f598458e0c89695b0fb9e3e8bce9259f6efed11574a8f7ae220f5`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ec367fb389b69f8e074b7e4c1b21b55ca836cd1534a4a29e83262700423f1046
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (138034498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f9daa6840839c1a27652895ba54d31c0857b659c389247e6324fa232d1daa0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV ROS_DISTRO=foxy
# Tue, 31 Aug 2021 02:40:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:56 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:40:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:40:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac2567afd7f21270eaf5dac9596df45b6dda0b77d64188744a7081a5f346b5`  
		Last Modified: Tue, 31 Aug 2021 02:55:58 GMT  
		Size: 104.2 MB (104162618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e0daf045c79605e6b79149e30817a2a6a12ee94bd746d4ddbf97b159b86d9f`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-core-focal`

```console
$ docker pull ros@sha256:5cefe4b0c192fa365b3e1c32013ca3d7e44f3e8273c38b357815ebf376221655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:683ba2918ce69e5a9601828f8f0391af5a2bcc2dca4343f9d25454e361453575
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155274668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b928b800f2e72749a36214430a363fdcd8e269b7956906b3a97a5728fc34af`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV ROS_DISTRO=foxy
# Tue, 27 Jul 2021 01:03:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:03:15 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:03:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:03:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6567e1e6579146c6323e3e1408e11008ac77c4d5c5ed8e5943332bc7254a56a5`  
		Last Modified: Tue, 27 Jul 2021 01:17:18 GMT  
		Size: 120.0 MB (119974774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88662ced653f598458e0c89695b0fb9e3e8bce9259f6efed11574a8f7ae220f5`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ec367fb389b69f8e074b7e4c1b21b55ca836cd1534a4a29e83262700423f1046
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (138034498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f9daa6840839c1a27652895ba54d31c0857b659c389247e6324fa232d1daa0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV ROS_DISTRO=foxy
# Tue, 31 Aug 2021 02:40:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:56 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:40:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:40:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac2567afd7f21270eaf5dac9596df45b6dda0b77d64188744a7081a5f346b5`  
		Last Modified: Tue, 31 Aug 2021 02:55:58 GMT  
		Size: 104.2 MB (104162618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e0daf045c79605e6b79149e30817a2a6a12ee94bd746d4ddbf97b159b86d9f`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros1-bridge`

```console
$ docker pull ros@sha256:9536da4929ee4b0ffae8f14a5a1ea4e1a1dc13d146f1a376d7883a6c95169381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:ef32e4aab556e47f966d7f47f8a0be2b2a4fc87430d768aad7a8278d21fbf7ff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.5 MB (345507825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0de2bd00b710b309f04b3b8aece716e377b986ae69afa53efb7b861e4a96966`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV ROS_DISTRO=foxy
# Tue, 27 Jul 2021 01:03:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:03:15 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:03:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:03:15 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:04:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:04:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 01:04:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 27 Jul 2021 01:04:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:04:32 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 01:04:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:04:34 GMT
ENV ROS1_DISTRO=noetic
# Tue, 27 Jul 2021 01:04:34 GMT
ENV ROS2_DISTRO=foxy
# Tue, 27 Jul 2021 01:05:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.11-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:05:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:05:29 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6567e1e6579146c6323e3e1408e11008ac77c4d5c5ed8e5943332bc7254a56a5`  
		Last Modified: Tue, 27 Jul 2021 01:17:18 GMT  
		Size: 120.0 MB (119974774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88662ced653f598458e0c89695b0fb9e3e8bce9259f6efed11574a8f7ae220f5`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588ff9fb226bda0f04608743623449eccc27c7cc333932238b83bb7ec32398ea`  
		Last Modified: Tue, 27 Jul 2021 01:17:40 GMT  
		Size: 70.8 MB (70843719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a912ea800775dd8e48e78dac7555405832fcd4ad530eeae4cc976ba08ed32dbf`  
		Last Modified: Tue, 27 Jul 2021 01:17:30 GMT  
		Size: 238.5 KB (238478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b8c908ab26db0ef9598ff88bf38a1008a48fa6cc4f426e318321c589e254b4`  
		Last Modified: Tue, 27 Jul 2021 01:17:29 GMT  
		Size: 2.0 KB (2049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3ba81eeaf2f769cfb5f06e3b9de2651d04e9927d713613e7e5e7f86afbdba4`  
		Last Modified: Tue, 27 Jul 2021 01:17:32 GMT  
		Size: 10.3 MB (10282984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1506323a6748382badefb23bfb9e1426f36effd5b82d16d2694254e19f54c03d`  
		Last Modified: Tue, 27 Jul 2021 01:17:59 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94de0348dafb927ad69bfc28f49be82b04b67c489cbe28bbc61baca8fbd39aeb`  
		Last Modified: Tue, 27 Jul 2021 01:17:59 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b47f0b815bcd2eccc5fb521011a383e33f7df3c2e30dd4d21b5eff73327010`  
		Last Modified: Tue, 27 Jul 2021 01:18:14 GMT  
		Size: 76.1 MB (76130117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdf772cea424f27ffc6c8f44f4a54a1dc80fda4e2b8743d45cbf23f2de229f8`  
		Last Modified: Tue, 27 Jul 2021 01:18:05 GMT  
		Size: 32.7 MB (32735183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9353bf32a09ff870393a278312567b5a5dfcc62266e8569b44819c45946d61`  
		Last Modified: Tue, 27 Jul 2021 01:17:59 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c8524cea13cd0d60ab079d11f926b595139ae0f1b8a6ca8e78fc386fd4683ecc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314037710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23ba52270226f4808eb5db842151fb54102254f2f869045e283b3d00cba56c0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV ROS_DISTRO=foxy
# Tue, 31 Aug 2021 02:40:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:56 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:40:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:40:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:41:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:41:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:41:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 31 Aug 2021 02:41:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:41:52 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:42:02 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:42:02 GMT
ENV ROS1_DISTRO=noetic
# Tue, 31 Aug 2021 02:42:02 GMT
ENV ROS2_DISTRO=foxy
# Tue, 31 Aug 2021 02:42:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.11-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:42:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:42:43 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac2567afd7f21270eaf5dac9596df45b6dda0b77d64188744a7081a5f346b5`  
		Last Modified: Tue, 31 Aug 2021 02:55:58 GMT  
		Size: 104.2 MB (104162618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e0daf045c79605e6b79149e30817a2a6a12ee94bd746d4ddbf97b159b86d9f`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053652fdf77cf09c2d5f748e1392a941b0a2640722c2e70d661cb0f79ed668cf`  
		Last Modified: Tue, 31 Aug 2021 02:56:20 GMT  
		Size: 65.2 MB (65183560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aedc85ca67006659dbfc2b17452494645c1f0e417864446282ae6f592dc634e`  
		Last Modified: Tue, 31 Aug 2021 02:56:10 GMT  
		Size: 240.5 KB (240543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf81879f4a40b97c2359dafad0f780449e33d1663620a7c84e6edc1d195e3e4`  
		Last Modified: Tue, 31 Aug 2021 02:56:09 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68fc5fc59c2a35f0a91dba364f8820a1bdf634a40ffa0598d351cb20b4af65a`  
		Last Modified: Tue, 31 Aug 2021 02:56:11 GMT  
		Size: 9.3 MB (9298963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd3283cc3a3d0b05c08fbf8f9dd92a0d58882e3d3f4b30ad40605ca33f18330`  
		Last Modified: Tue, 31 Aug 2021 02:56:39 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3042d28ddb6bf62c8b0e1e54bc0d10a513a2f5c9b3a1f4202288198c324738d`  
		Last Modified: Tue, 31 Aug 2021 02:56:39 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c80802dfb985bc5e968ed325b0300ccc446bdd9de54b7af679333b9ebc11c74`  
		Last Modified: Tue, 31 Aug 2021 02:56:55 GMT  
		Size: 76.2 MB (76167513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d418353022c19184ddb5003057db95c611277d1f1bf4d789fab26eea7b08d5`  
		Last Modified: Tue, 31 Aug 2021 02:56:44 GMT  
		Size: 25.1 MB (25109980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1457cde4b44826bb5c7364ac964c0eea2aa3fb528fc1a5a935aec01b6be8bcf`  
		Last Modified: Tue, 31 Aug 2021 02:56:39 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:9536da4929ee4b0ffae8f14a5a1ea4e1a1dc13d146f1a376d7883a6c95169381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:ef32e4aab556e47f966d7f47f8a0be2b2a4fc87430d768aad7a8278d21fbf7ff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.5 MB (345507825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0de2bd00b710b309f04b3b8aece716e377b986ae69afa53efb7b861e4a96966`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV ROS_DISTRO=foxy
# Tue, 27 Jul 2021 01:03:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:03:15 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:03:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:03:15 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:04:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:04:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 01:04:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 27 Jul 2021 01:04:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:04:32 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 01:04:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:04:34 GMT
ENV ROS1_DISTRO=noetic
# Tue, 27 Jul 2021 01:04:34 GMT
ENV ROS2_DISTRO=foxy
# Tue, 27 Jul 2021 01:05:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.11-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:05:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:05:29 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6567e1e6579146c6323e3e1408e11008ac77c4d5c5ed8e5943332bc7254a56a5`  
		Last Modified: Tue, 27 Jul 2021 01:17:18 GMT  
		Size: 120.0 MB (119974774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88662ced653f598458e0c89695b0fb9e3e8bce9259f6efed11574a8f7ae220f5`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588ff9fb226bda0f04608743623449eccc27c7cc333932238b83bb7ec32398ea`  
		Last Modified: Tue, 27 Jul 2021 01:17:40 GMT  
		Size: 70.8 MB (70843719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a912ea800775dd8e48e78dac7555405832fcd4ad530eeae4cc976ba08ed32dbf`  
		Last Modified: Tue, 27 Jul 2021 01:17:30 GMT  
		Size: 238.5 KB (238478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b8c908ab26db0ef9598ff88bf38a1008a48fa6cc4f426e318321c589e254b4`  
		Last Modified: Tue, 27 Jul 2021 01:17:29 GMT  
		Size: 2.0 KB (2049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3ba81eeaf2f769cfb5f06e3b9de2651d04e9927d713613e7e5e7f86afbdba4`  
		Last Modified: Tue, 27 Jul 2021 01:17:32 GMT  
		Size: 10.3 MB (10282984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1506323a6748382badefb23bfb9e1426f36effd5b82d16d2694254e19f54c03d`  
		Last Modified: Tue, 27 Jul 2021 01:17:59 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94de0348dafb927ad69bfc28f49be82b04b67c489cbe28bbc61baca8fbd39aeb`  
		Last Modified: Tue, 27 Jul 2021 01:17:59 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b47f0b815bcd2eccc5fb521011a383e33f7df3c2e30dd4d21b5eff73327010`  
		Last Modified: Tue, 27 Jul 2021 01:18:14 GMT  
		Size: 76.1 MB (76130117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdf772cea424f27ffc6c8f44f4a54a1dc80fda4e2b8743d45cbf23f2de229f8`  
		Last Modified: Tue, 27 Jul 2021 01:18:05 GMT  
		Size: 32.7 MB (32735183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9353bf32a09ff870393a278312567b5a5dfcc62266e8569b44819c45946d61`  
		Last Modified: Tue, 27 Jul 2021 01:17:59 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c8524cea13cd0d60ab079d11f926b595139ae0f1b8a6ca8e78fc386fd4683ecc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314037710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23ba52270226f4808eb5db842151fb54102254f2f869045e283b3d00cba56c0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV ROS_DISTRO=foxy
# Tue, 31 Aug 2021 02:40:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:56 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:40:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:40:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:41:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:41:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:41:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 31 Aug 2021 02:41:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:41:52 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:42:02 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:42:02 GMT
ENV ROS1_DISTRO=noetic
# Tue, 31 Aug 2021 02:42:02 GMT
ENV ROS2_DISTRO=foxy
# Tue, 31 Aug 2021 02:42:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.11-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:42:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:42:43 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac2567afd7f21270eaf5dac9596df45b6dda0b77d64188744a7081a5f346b5`  
		Last Modified: Tue, 31 Aug 2021 02:55:58 GMT  
		Size: 104.2 MB (104162618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e0daf045c79605e6b79149e30817a2a6a12ee94bd746d4ddbf97b159b86d9f`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053652fdf77cf09c2d5f748e1392a941b0a2640722c2e70d661cb0f79ed668cf`  
		Last Modified: Tue, 31 Aug 2021 02:56:20 GMT  
		Size: 65.2 MB (65183560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aedc85ca67006659dbfc2b17452494645c1f0e417864446282ae6f592dc634e`  
		Last Modified: Tue, 31 Aug 2021 02:56:10 GMT  
		Size: 240.5 KB (240543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf81879f4a40b97c2359dafad0f780449e33d1663620a7c84e6edc1d195e3e4`  
		Last Modified: Tue, 31 Aug 2021 02:56:09 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68fc5fc59c2a35f0a91dba364f8820a1bdf634a40ffa0598d351cb20b4af65a`  
		Last Modified: Tue, 31 Aug 2021 02:56:11 GMT  
		Size: 9.3 MB (9298963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd3283cc3a3d0b05c08fbf8f9dd92a0d58882e3d3f4b30ad40605ca33f18330`  
		Last Modified: Tue, 31 Aug 2021 02:56:39 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3042d28ddb6bf62c8b0e1e54bc0d10a513a2f5c9b3a1f4202288198c324738d`  
		Last Modified: Tue, 31 Aug 2021 02:56:39 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c80802dfb985bc5e968ed325b0300ccc446bdd9de54b7af679333b9ebc11c74`  
		Last Modified: Tue, 31 Aug 2021 02:56:55 GMT  
		Size: 76.2 MB (76167513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d418353022c19184ddb5003057db95c611277d1f1bf4d789fab26eea7b08d5`  
		Last Modified: Tue, 31 Aug 2021 02:56:44 GMT  
		Size: 25.1 MB (25109980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1457cde4b44826bb5c7364ac964c0eea2aa3fb528fc1a5a935aec01b6be8bcf`  
		Last Modified: Tue, 31 Aug 2021 02:56:39 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic`

```console
$ docker pull ros@sha256:36f46d53f0818c897a9a6bf0fdc4e098a3d6328ee5fd96fd9fbd69f544cb33f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic` - linux; amd64

```console
$ docker pull ros@sha256:4d93293885527a8e099ba1d2e46b0f4540e78221490712adb30202e21c6278df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232069450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5776753f405d865e9853cfe70424e5cf92af3b3944c4c09533e41651a5aaaa4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:05:32 GMT
ENV ROS_DISTRO=galactic
# Tue, 27 Jul 2021 01:06:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:06:17 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:06:17 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:06:17 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:06:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:06:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 01:06:48 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 27 Jul 2021 01:07:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698085f1b967a89a6f46a3ab27fbf0926f76b483b0843140c750e906cdbce36e`  
		Last Modified: Tue, 27 Jul 2021 01:18:43 GMT  
		Size: 103.6 MB (103633085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66de36d29cf49a4bbc2b20c3f5795f7d9c972b6c03fbfef58203d93014aab22`  
		Last Modified: Tue, 27 Jul 2021 01:18:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71385bc5f93112c08888184a0254508d98eb9c547e40f70af98924d3c7f7b735`  
		Last Modified: Tue, 27 Jul 2021 01:19:05 GMT  
		Size: 70.8 MB (70797407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6f08ba387a09b78071f694d7eb0fb4774c732d8bbeba44462bd43acc75d78f`  
		Last Modified: Tue, 27 Jul 2021 01:18:55 GMT  
		Size: 241.2 KB (241230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7990cf09456775859f728e71494b2adcec01b46fdbcda5a418970af90f5e5056`  
		Last Modified: Tue, 27 Jul 2021 01:18:55 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23344c0439abccd2d4aff93d7e57f3697c56daad83902005a615a0e70e52a77c`  
		Last Modified: Tue, 27 Jul 2021 01:18:59 GMT  
		Size: 22.1 MB (22095808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1fc0a520864d1892da3074920d2c968809a3eb22cffe4422ff59d0939f9807d7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220730330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a173b0949bfc8ba51bf1cbbfb243961fc0f97897105d1579fc1bedeaae3c7002`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:42:53 GMT
ENV ROS_DISTRO=galactic
# Tue, 31 Aug 2021 02:43:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:43:33 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:43:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:43:33 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:44:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:44:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:44:10 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 31 Aug 2021 02:44:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d77fc4622ebe94f4dbfef84290640d2b0a8cb645e806937cae119da66e0a32c`  
		Last Modified: Tue, 31 Aug 2021 02:57:26 GMT  
		Size: 100.0 MB (100037845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a1ce4ccd8df8c236b714872e85748b5011a9c784f1308d3e8b7cde6d55cdcf`  
		Last Modified: Tue, 31 Aug 2021 02:57:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98f71bfc8c301186b7c6a5b38b04e91f5b5a52d664b2f8270051b08e762181c`  
		Last Modified: Tue, 31 Aug 2021 02:57:48 GMT  
		Size: 65.1 MB (65138271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44554f0d6a1dfdf9fb1da0b542b9e1bcbbecca7421118b2a705e78f5b956b609`  
		Last Modified: Tue, 31 Aug 2021 02:57:38 GMT  
		Size: 245.0 KB (245012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217cf8322ac9a1b82365a9710371636864d32637d22bd1d637b2bb97c4ddd306`  
		Last Modified: Tue, 31 Aug 2021 02:57:38 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120720b5aa2190a67c0c60941709cb411d04a7bc7e208f954115857ef0529410`  
		Last Modified: Tue, 31 Aug 2021 02:57:41 GMT  
		Size: 21.4 MB (21435306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-base`

```console
$ docker pull ros@sha256:36f46d53f0818c897a9a6bf0fdc4e098a3d6328ee5fd96fd9fbd69f544cb33f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:4d93293885527a8e099ba1d2e46b0f4540e78221490712adb30202e21c6278df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232069450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5776753f405d865e9853cfe70424e5cf92af3b3944c4c09533e41651a5aaaa4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:05:32 GMT
ENV ROS_DISTRO=galactic
# Tue, 27 Jul 2021 01:06:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:06:17 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:06:17 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:06:17 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:06:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:06:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 01:06:48 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 27 Jul 2021 01:07:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698085f1b967a89a6f46a3ab27fbf0926f76b483b0843140c750e906cdbce36e`  
		Last Modified: Tue, 27 Jul 2021 01:18:43 GMT  
		Size: 103.6 MB (103633085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66de36d29cf49a4bbc2b20c3f5795f7d9c972b6c03fbfef58203d93014aab22`  
		Last Modified: Tue, 27 Jul 2021 01:18:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71385bc5f93112c08888184a0254508d98eb9c547e40f70af98924d3c7f7b735`  
		Last Modified: Tue, 27 Jul 2021 01:19:05 GMT  
		Size: 70.8 MB (70797407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6f08ba387a09b78071f694d7eb0fb4774c732d8bbeba44462bd43acc75d78f`  
		Last Modified: Tue, 27 Jul 2021 01:18:55 GMT  
		Size: 241.2 KB (241230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7990cf09456775859f728e71494b2adcec01b46fdbcda5a418970af90f5e5056`  
		Last Modified: Tue, 27 Jul 2021 01:18:55 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23344c0439abccd2d4aff93d7e57f3697c56daad83902005a615a0e70e52a77c`  
		Last Modified: Tue, 27 Jul 2021 01:18:59 GMT  
		Size: 22.1 MB (22095808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1fc0a520864d1892da3074920d2c968809a3eb22cffe4422ff59d0939f9807d7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220730330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a173b0949bfc8ba51bf1cbbfb243961fc0f97897105d1579fc1bedeaae3c7002`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:42:53 GMT
ENV ROS_DISTRO=galactic
# Tue, 31 Aug 2021 02:43:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:43:33 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:43:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:43:33 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:44:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:44:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:44:10 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 31 Aug 2021 02:44:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d77fc4622ebe94f4dbfef84290640d2b0a8cb645e806937cae119da66e0a32c`  
		Last Modified: Tue, 31 Aug 2021 02:57:26 GMT  
		Size: 100.0 MB (100037845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a1ce4ccd8df8c236b714872e85748b5011a9c784f1308d3e8b7cde6d55cdcf`  
		Last Modified: Tue, 31 Aug 2021 02:57:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98f71bfc8c301186b7c6a5b38b04e91f5b5a52d664b2f8270051b08e762181c`  
		Last Modified: Tue, 31 Aug 2021 02:57:48 GMT  
		Size: 65.1 MB (65138271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44554f0d6a1dfdf9fb1da0b542b9e1bcbbecca7421118b2a705e78f5b956b609`  
		Last Modified: Tue, 31 Aug 2021 02:57:38 GMT  
		Size: 245.0 KB (245012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217cf8322ac9a1b82365a9710371636864d32637d22bd1d637b2bb97c4ddd306`  
		Last Modified: Tue, 31 Aug 2021 02:57:38 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120720b5aa2190a67c0c60941709cb411d04a7bc7e208f954115857ef0529410`  
		Last Modified: Tue, 31 Aug 2021 02:57:41 GMT  
		Size: 21.4 MB (21435306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-base-focal`

```console
$ docker pull ros@sha256:36f46d53f0818c897a9a6bf0fdc4e098a3d6328ee5fd96fd9fbd69f544cb33f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:4d93293885527a8e099ba1d2e46b0f4540e78221490712adb30202e21c6278df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232069450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5776753f405d865e9853cfe70424e5cf92af3b3944c4c09533e41651a5aaaa4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:05:32 GMT
ENV ROS_DISTRO=galactic
# Tue, 27 Jul 2021 01:06:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:06:17 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:06:17 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:06:17 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:06:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:06:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 01:06:48 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 27 Jul 2021 01:07:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698085f1b967a89a6f46a3ab27fbf0926f76b483b0843140c750e906cdbce36e`  
		Last Modified: Tue, 27 Jul 2021 01:18:43 GMT  
		Size: 103.6 MB (103633085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66de36d29cf49a4bbc2b20c3f5795f7d9c972b6c03fbfef58203d93014aab22`  
		Last Modified: Tue, 27 Jul 2021 01:18:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71385bc5f93112c08888184a0254508d98eb9c547e40f70af98924d3c7f7b735`  
		Last Modified: Tue, 27 Jul 2021 01:19:05 GMT  
		Size: 70.8 MB (70797407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6f08ba387a09b78071f694d7eb0fb4774c732d8bbeba44462bd43acc75d78f`  
		Last Modified: Tue, 27 Jul 2021 01:18:55 GMT  
		Size: 241.2 KB (241230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7990cf09456775859f728e71494b2adcec01b46fdbcda5a418970af90f5e5056`  
		Last Modified: Tue, 27 Jul 2021 01:18:55 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23344c0439abccd2d4aff93d7e57f3697c56daad83902005a615a0e70e52a77c`  
		Last Modified: Tue, 27 Jul 2021 01:18:59 GMT  
		Size: 22.1 MB (22095808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1fc0a520864d1892da3074920d2c968809a3eb22cffe4422ff59d0939f9807d7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220730330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a173b0949bfc8ba51bf1cbbfb243961fc0f97897105d1579fc1bedeaae3c7002`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:42:53 GMT
ENV ROS_DISTRO=galactic
# Tue, 31 Aug 2021 02:43:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:43:33 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:43:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:43:33 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:44:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:44:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:44:10 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 31 Aug 2021 02:44:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d77fc4622ebe94f4dbfef84290640d2b0a8cb645e806937cae119da66e0a32c`  
		Last Modified: Tue, 31 Aug 2021 02:57:26 GMT  
		Size: 100.0 MB (100037845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a1ce4ccd8df8c236b714872e85748b5011a9c784f1308d3e8b7cde6d55cdcf`  
		Last Modified: Tue, 31 Aug 2021 02:57:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98f71bfc8c301186b7c6a5b38b04e91f5b5a52d664b2f8270051b08e762181c`  
		Last Modified: Tue, 31 Aug 2021 02:57:48 GMT  
		Size: 65.1 MB (65138271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44554f0d6a1dfdf9fb1da0b542b9e1bcbbecca7421118b2a705e78f5b956b609`  
		Last Modified: Tue, 31 Aug 2021 02:57:38 GMT  
		Size: 245.0 KB (245012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217cf8322ac9a1b82365a9710371636864d32637d22bd1d637b2bb97c4ddd306`  
		Last Modified: Tue, 31 Aug 2021 02:57:38 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120720b5aa2190a67c0c60941709cb411d04a7bc7e208f954115857ef0529410`  
		Last Modified: Tue, 31 Aug 2021 02:57:41 GMT  
		Size: 21.4 MB (21435306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-core`

```console
$ docker pull ros@sha256:b24d7cb90852a1bfc52a14ea9a2999596a58e3d12bbf04c0b9ce6abd484fa2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:232f4e33bd2c038a0c3a6eb10ae85cf9f051e079f6cb6b82f0a0146962120770
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138932979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c8bff07074d08c5e567030f617963bfbafa60010f72fea266cca3224238726`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:05:32 GMT
ENV ROS_DISTRO=galactic
# Tue, 27 Jul 2021 01:06:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:06:17 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:06:17 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:06:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698085f1b967a89a6f46a3ab27fbf0926f76b483b0843140c750e906cdbce36e`  
		Last Modified: Tue, 27 Jul 2021 01:18:43 GMT  
		Size: 103.6 MB (103633085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66de36d29cf49a4bbc2b20c3f5795f7d9c972b6c03fbfef58203d93014aab22`  
		Last Modified: Tue, 27 Jul 2021 01:18:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c259a3d034d83af526b2dcb957a989fecb8bb7d74cc5f237754d946e2c5ecf13
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133909725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7945809677fd2da50bc1cd2c0807f85dc5ace5635ec2143153283b9c84fb63b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:42:53 GMT
ENV ROS_DISTRO=galactic
# Tue, 31 Aug 2021 02:43:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:43:33 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:43:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:43:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d77fc4622ebe94f4dbfef84290640d2b0a8cb645e806937cae119da66e0a32c`  
		Last Modified: Tue, 31 Aug 2021 02:57:26 GMT  
		Size: 100.0 MB (100037845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a1ce4ccd8df8c236b714872e85748b5011a9c784f1308d3e8b7cde6d55cdcf`  
		Last Modified: Tue, 31 Aug 2021 02:57:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-core-focal`

```console
$ docker pull ros@sha256:b24d7cb90852a1bfc52a14ea9a2999596a58e3d12bbf04c0b9ce6abd484fa2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:232f4e33bd2c038a0c3a6eb10ae85cf9f051e079f6cb6b82f0a0146962120770
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138932979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c8bff07074d08c5e567030f617963bfbafa60010f72fea266cca3224238726`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:05:32 GMT
ENV ROS_DISTRO=galactic
# Tue, 27 Jul 2021 01:06:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:06:17 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:06:17 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:06:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698085f1b967a89a6f46a3ab27fbf0926f76b483b0843140c750e906cdbce36e`  
		Last Modified: Tue, 27 Jul 2021 01:18:43 GMT  
		Size: 103.6 MB (103633085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66de36d29cf49a4bbc2b20c3f5795f7d9c972b6c03fbfef58203d93014aab22`  
		Last Modified: Tue, 27 Jul 2021 01:18:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c259a3d034d83af526b2dcb957a989fecb8bb7d74cc5f237754d946e2c5ecf13
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133909725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7945809677fd2da50bc1cd2c0807f85dc5ace5635ec2143153283b9c84fb63b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:42:53 GMT
ENV ROS_DISTRO=galactic
# Tue, 31 Aug 2021 02:43:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:43:33 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:43:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:43:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d77fc4622ebe94f4dbfef84290640d2b0a8cb645e806937cae119da66e0a32c`  
		Last Modified: Tue, 31 Aug 2021 02:57:26 GMT  
		Size: 100.0 MB (100037845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a1ce4ccd8df8c236b714872e85748b5011a9c784f1308d3e8b7cde6d55cdcf`  
		Last Modified: Tue, 31 Aug 2021 02:57:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros1-bridge`

```console
$ docker pull ros@sha256:e823c602de06494ad06a3b642b3599685bad58c8e45d71c1256fbbac95aa7aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:3cfba0166cb37b1a2e2b252102343ed7bd265bae34092826d2b39e0664275208
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.8 MB (326842374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb19318f478c5ad3deebb1767360a541c56af0014dd542003565bd5e3e24bf1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:05:32 GMT
ENV ROS_DISTRO=galactic
# Tue, 27 Jul 2021 01:06:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:06:17 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:06:17 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:06:17 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:06:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:06:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 01:06:48 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 27 Jul 2021 01:07:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:07:14 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 01:07:15 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:07:15 GMT
ENV ROS1_DISTRO=noetic
# Tue, 27 Jul 2021 01:07:16 GMT
ENV ROS2_DISTRO=galactic
# Tue, 27 Jul 2021 01:07:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.11-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:07:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:07:49 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698085f1b967a89a6f46a3ab27fbf0926f76b483b0843140c750e906cdbce36e`  
		Last Modified: Tue, 27 Jul 2021 01:18:43 GMT  
		Size: 103.6 MB (103633085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66de36d29cf49a4bbc2b20c3f5795f7d9c972b6c03fbfef58203d93014aab22`  
		Last Modified: Tue, 27 Jul 2021 01:18:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71385bc5f93112c08888184a0254508d98eb9c547e40f70af98924d3c7f7b735`  
		Last Modified: Tue, 27 Jul 2021 01:19:05 GMT  
		Size: 70.8 MB (70797407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6f08ba387a09b78071f694d7eb0fb4774c732d8bbeba44462bd43acc75d78f`  
		Last Modified: Tue, 27 Jul 2021 01:18:55 GMT  
		Size: 241.2 KB (241230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7990cf09456775859f728e71494b2adcec01b46fdbcda5a418970af90f5e5056`  
		Last Modified: Tue, 27 Jul 2021 01:18:55 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23344c0439abccd2d4aff93d7e57f3697c56daad83902005a615a0e70e52a77c`  
		Last Modified: Tue, 27 Jul 2021 01:18:59 GMT  
		Size: 22.1 MB (22095808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14520e7f4d5e7abaa150d713df486bd446780cf35343d659c964a116fb83314d`  
		Last Modified: Tue, 27 Jul 2021 01:19:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89be30453f2f44b3a020e5ec2bfe5b2c6da662ed820f295c10522d1fd3d163da`  
		Last Modified: Tue, 27 Jul 2021 01:19:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83f5e8e2ce60a31e2b6723160edad367d80a1dd8677d7e650af6cd43d84cb6a`  
		Last Modified: Tue, 27 Jul 2021 01:19:35 GMT  
		Size: 78.4 MB (78409624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901678866177d90b4b62b1fe5d39bc27b9c4485b64c290167252b5f8d99f76f9`  
		Last Modified: Tue, 27 Jul 2021 01:19:24 GMT  
		Size: 16.4 MB (16362675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b1b98982ff37b0d26a053f62a31f785d695504cc4b5e359ba3018868504af`  
		Last Modified: Tue, 27 Jul 2021 01:19:20 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ee3aaa53b5dd9b2f6c0676fdb499beb43d3aa6eb5e7def7a7594da50b85f135c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.0 MB (314996851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9498f260b5eed9c2e2bdae18ec2ac543e03c00e6e934a013f8e6b3f148abe78`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:42:53 GMT
ENV ROS_DISTRO=galactic
# Tue, 31 Aug 2021 02:43:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:43:33 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:43:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:43:33 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:44:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:44:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:44:10 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 31 Aug 2021 02:44:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:44:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:44:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:44:46 GMT
ENV ROS1_DISTRO=noetic
# Tue, 31 Aug 2021 02:44:46 GMT
ENV ROS2_DISTRO=galactic
# Tue, 31 Aug 2021 02:45:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.11-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:45:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:45:21 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d77fc4622ebe94f4dbfef84290640d2b0a8cb645e806937cae119da66e0a32c`  
		Last Modified: Tue, 31 Aug 2021 02:57:26 GMT  
		Size: 100.0 MB (100037845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a1ce4ccd8df8c236b714872e85748b5011a9c784f1308d3e8b7cde6d55cdcf`  
		Last Modified: Tue, 31 Aug 2021 02:57:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98f71bfc8c301186b7c6a5b38b04e91f5b5a52d664b2f8270051b08e762181c`  
		Last Modified: Tue, 31 Aug 2021 02:57:48 GMT  
		Size: 65.1 MB (65138271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44554f0d6a1dfdf9fb1da0b542b9e1bcbbecca7421118b2a705e78f5b956b609`  
		Last Modified: Tue, 31 Aug 2021 02:57:38 GMT  
		Size: 245.0 KB (245012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217cf8322ac9a1b82365a9710371636864d32637d22bd1d637b2bb97c4ddd306`  
		Last Modified: Tue, 31 Aug 2021 02:57:38 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120720b5aa2190a67c0c60941709cb411d04a7bc7e208f954115857ef0529410`  
		Last Modified: Tue, 31 Aug 2021 02:57:41 GMT  
		Size: 21.4 MB (21435306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000b79fc3753c17e268692b74af07168e20ef832f41c2b6d51aa4ebdc9b0b584`  
		Last Modified: Tue, 31 Aug 2021 02:58:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcfa3302fc9ef900d7b52b011d213d5500e493f37186bf49394b21ab8667ad9`  
		Last Modified: Tue, 31 Aug 2021 02:58:04 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267cbfb8468f5b8c83aa8a80301a114a9cfbf2fa9ceecbfbc4199761e9d3a022`  
		Last Modified: Tue, 31 Aug 2021 02:58:21 GMT  
		Size: 78.4 MB (78375726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d60cd931079f2558a9451c7b49abf36df676a1d533d65e6a646fe8b96549293`  
		Last Modified: Tue, 31 Aug 2021 02:58:07 GMT  
		Size: 15.9 MB (15890170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9e59276ccde1a327278f910f28b22a92d0e79cfa1b7b11a53e064f99baab37`  
		Last Modified: Tue, 31 Aug 2021 02:58:04 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros1-bridge-focal`

```console
$ docker pull ros@sha256:e823c602de06494ad06a3b642b3599685bad58c8e45d71c1256fbbac95aa7aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:3cfba0166cb37b1a2e2b252102343ed7bd265bae34092826d2b39e0664275208
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.8 MB (326842374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb19318f478c5ad3deebb1767360a541c56af0014dd542003565bd5e3e24bf1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:05:32 GMT
ENV ROS_DISTRO=galactic
# Tue, 27 Jul 2021 01:06:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:06:17 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:06:17 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:06:17 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:06:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:06:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 01:06:48 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 27 Jul 2021 01:07:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:07:14 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 01:07:15 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:07:15 GMT
ENV ROS1_DISTRO=noetic
# Tue, 27 Jul 2021 01:07:16 GMT
ENV ROS2_DISTRO=galactic
# Tue, 27 Jul 2021 01:07:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.11-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:07:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:07:49 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698085f1b967a89a6f46a3ab27fbf0926f76b483b0843140c750e906cdbce36e`  
		Last Modified: Tue, 27 Jul 2021 01:18:43 GMT  
		Size: 103.6 MB (103633085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66de36d29cf49a4bbc2b20c3f5795f7d9c972b6c03fbfef58203d93014aab22`  
		Last Modified: Tue, 27 Jul 2021 01:18:26 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71385bc5f93112c08888184a0254508d98eb9c547e40f70af98924d3c7f7b735`  
		Last Modified: Tue, 27 Jul 2021 01:19:05 GMT  
		Size: 70.8 MB (70797407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6f08ba387a09b78071f694d7eb0fb4774c732d8bbeba44462bd43acc75d78f`  
		Last Modified: Tue, 27 Jul 2021 01:18:55 GMT  
		Size: 241.2 KB (241230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7990cf09456775859f728e71494b2adcec01b46fdbcda5a418970af90f5e5056`  
		Last Modified: Tue, 27 Jul 2021 01:18:55 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23344c0439abccd2d4aff93d7e57f3697c56daad83902005a615a0e70e52a77c`  
		Last Modified: Tue, 27 Jul 2021 01:18:59 GMT  
		Size: 22.1 MB (22095808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14520e7f4d5e7abaa150d713df486bd446780cf35343d659c964a116fb83314d`  
		Last Modified: Tue, 27 Jul 2021 01:19:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89be30453f2f44b3a020e5ec2bfe5b2c6da662ed820f295c10522d1fd3d163da`  
		Last Modified: Tue, 27 Jul 2021 01:19:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83f5e8e2ce60a31e2b6723160edad367d80a1dd8677d7e650af6cd43d84cb6a`  
		Last Modified: Tue, 27 Jul 2021 01:19:35 GMT  
		Size: 78.4 MB (78409624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901678866177d90b4b62b1fe5d39bc27b9c4485b64c290167252b5f8d99f76f9`  
		Last Modified: Tue, 27 Jul 2021 01:19:24 GMT  
		Size: 16.4 MB (16362675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b1b98982ff37b0d26a053f62a31f785d695504cc4b5e359ba3018868504af`  
		Last Modified: Tue, 27 Jul 2021 01:19:20 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ee3aaa53b5dd9b2f6c0676fdb499beb43d3aa6eb5e7def7a7594da50b85f135c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.0 MB (314996851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9498f260b5eed9c2e2bdae18ec2ac543e03c00e6e934a013f8e6b3f148abe78`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:42:53 GMT
ENV ROS_DISTRO=galactic
# Tue, 31 Aug 2021 02:43:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:43:33 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:43:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:43:33 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:44:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:44:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:44:10 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 31 Aug 2021 02:44:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:44:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:44:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:44:46 GMT
ENV ROS1_DISTRO=noetic
# Tue, 31 Aug 2021 02:44:46 GMT
ENV ROS2_DISTRO=galactic
# Tue, 31 Aug 2021 02:45:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.11-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:45:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:45:21 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d77fc4622ebe94f4dbfef84290640d2b0a8cb645e806937cae119da66e0a32c`  
		Last Modified: Tue, 31 Aug 2021 02:57:26 GMT  
		Size: 100.0 MB (100037845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a1ce4ccd8df8c236b714872e85748b5011a9c784f1308d3e8b7cde6d55cdcf`  
		Last Modified: Tue, 31 Aug 2021 02:57:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98f71bfc8c301186b7c6a5b38b04e91f5b5a52d664b2f8270051b08e762181c`  
		Last Modified: Tue, 31 Aug 2021 02:57:48 GMT  
		Size: 65.1 MB (65138271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44554f0d6a1dfdf9fb1da0b542b9e1bcbbecca7421118b2a705e78f5b956b609`  
		Last Modified: Tue, 31 Aug 2021 02:57:38 GMT  
		Size: 245.0 KB (245012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217cf8322ac9a1b82365a9710371636864d32637d22bd1d637b2bb97c4ddd306`  
		Last Modified: Tue, 31 Aug 2021 02:57:38 GMT  
		Size: 2.0 KB (2016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120720b5aa2190a67c0c60941709cb411d04a7bc7e208f954115857ef0529410`  
		Last Modified: Tue, 31 Aug 2021 02:57:41 GMT  
		Size: 21.4 MB (21435306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000b79fc3753c17e268692b74af07168e20ef832f41c2b6d51aa4ebdc9b0b584`  
		Last Modified: Tue, 31 Aug 2021 02:58:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcfa3302fc9ef900d7b52b011d213d5500e493f37186bf49394b21ab8667ad9`  
		Last Modified: Tue, 31 Aug 2021 02:58:04 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267cbfb8468f5b8c83aa8a80301a114a9cfbf2fa9ceecbfbc4199761e9d3a022`  
		Last Modified: Tue, 31 Aug 2021 02:58:21 GMT  
		Size: 78.4 MB (78375726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d60cd931079f2558a9451c7b49abf36df676a1d533d65e6a646fe8b96549293`  
		Last Modified: Tue, 31 Aug 2021 02:58:07 GMT  
		Size: 15.9 MB (15890170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9e59276ccde1a327278f910f28b22a92d0e79cfa1b7b11a53e064f99baab37`  
		Last Modified: Tue, 31 Aug 2021 02:58:04 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:latest`

```console
$ docker pull ros@sha256:551bbab116cb41f010d73b4976f59bb4990d9543d07cf8a7b26dc3b1b758f07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:c6c4dcdcdba4646d8a6bebd6448625ed80cb18d8f1cae85e21a55a7e3d7ffec2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236641898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df65e6ff4c8f4ed1107f086582df71878afcbeb8d71e39214959ca5517adda77`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV ROS_DISTRO=foxy
# Tue, 27 Jul 2021 01:03:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:03:15 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:03:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:03:15 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:04:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:04:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 01:04:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 27 Jul 2021 01:04:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6567e1e6579146c6323e3e1408e11008ac77c4d5c5ed8e5943332bc7254a56a5`  
		Last Modified: Tue, 27 Jul 2021 01:17:18 GMT  
		Size: 120.0 MB (119974774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88662ced653f598458e0c89695b0fb9e3e8bce9259f6efed11574a8f7ae220f5`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588ff9fb226bda0f04608743623449eccc27c7cc333932238b83bb7ec32398ea`  
		Last Modified: Tue, 27 Jul 2021 01:17:40 GMT  
		Size: 70.8 MB (70843719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a912ea800775dd8e48e78dac7555405832fcd4ad530eeae4cc976ba08ed32dbf`  
		Last Modified: Tue, 27 Jul 2021 01:17:30 GMT  
		Size: 238.5 KB (238478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b8c908ab26db0ef9598ff88bf38a1008a48fa6cc4f426e318321c589e254b4`  
		Last Modified: Tue, 27 Jul 2021 01:17:29 GMT  
		Size: 2.0 KB (2049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3ba81eeaf2f769cfb5f06e3b9de2651d04e9927d713613e7e5e7f86afbdba4`  
		Last Modified: Tue, 27 Jul 2021 01:17:32 GMT  
		Size: 10.3 MB (10282984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:669ca86db8856ea020734faa9aa88d4cab494d13c65095b86722918c92a3e66f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.8 MB (212759588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a0be06c48eb711e3e05a4dae51ed27feebd9df75cd7c64e2148ca2aee9ab19`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV ROS_DISTRO=foxy
# Tue, 31 Aug 2021 02:40:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:56 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:40:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:40:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:41:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:41:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:41:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 31 Aug 2021 02:41:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cac2567afd7f21270eaf5dac9596df45b6dda0b77d64188744a7081a5f346b5`  
		Last Modified: Tue, 31 Aug 2021 02:55:58 GMT  
		Size: 104.2 MB (104162618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e0daf045c79605e6b79149e30817a2a6a12ee94bd746d4ddbf97b159b86d9f`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053652fdf77cf09c2d5f748e1392a941b0a2640722c2e70d661cb0f79ed668cf`  
		Last Modified: Tue, 31 Aug 2021 02:56:20 GMT  
		Size: 65.2 MB (65183560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aedc85ca67006659dbfc2b17452494645c1f0e417864446282ae6f592dc634e`  
		Last Modified: Tue, 31 Aug 2021 02:56:10 GMT  
		Size: 240.5 KB (240543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf81879f4a40b97c2359dafad0f780449e33d1663620a7c84e6edc1d195e3e4`  
		Last Modified: Tue, 31 Aug 2021 02:56:09 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68fc5fc59c2a35f0a91dba364f8820a1bdf634a40ffa0598d351cb20b4af65a`  
		Last Modified: Tue, 31 Aug 2021 02:56:11 GMT  
		Size: 9.3 MB (9298963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic`

```console
$ docker pull ros@sha256:976c369a0ebaac383ead1240e485fa3d2eb83647619112876b08cf7592173db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic` - linux; amd64

```console
$ docker pull ros@sha256:f9ab26ad9caf7c6025ff2669c4a4413746b68ea9ed05b3641829ccb515771e8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.4 MB (437364658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07711f635f57ed1907b716dba3ea6e751395f9e0e6d27350c4bb37860fac936`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:38:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:35:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 00:38:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:38:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:38:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:38:15 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:39:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:39:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 00:40:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1186553e47569a52e52d0ff6702d24c183760ccfa8f0865f5cd805b6a834f02a`  
		Last Modified: Tue, 27 Jul 2021 00:00:30 GMT  
		Size: 840.6 KB (840558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbd42adfa4f4468cc09d87fcaba98a160059fdee872c36809a69e43ab054efb`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 4.9 MB (4872150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e44ba6559363a0c0463b83b1977a52b1063833026aa6e9dddf178d444e003d`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccab66b30a6739dd0e587dc7eb7a3a05990bf99d4f6089491838f3bac0cfbdd`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f8627bbf4a2b81469316a6529e5a8c8bdd100a4ad64e0d474e973ec43f302`  
		Last Modified: Tue, 27 Jul 2021 01:11:51 GMT  
		Size: 259.4 MB (259445689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3fba9583601e046746fa9e5fb95242575e869b6747a7f9d937b202d9081bc`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75838d174816c0a4cd1517ea28102b2d7fdff541aa8d4229b56f30f29817ca86`  
		Last Modified: Tue, 27 Jul 2021 01:12:14 GMT  
		Size: 70.2 MB (70229942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4dde022f386e96e5a68cbc925d59be0ae93c493ce8f4915b24e88d8f8300035`  
		Last Modified: Tue, 27 Jul 2021 01:12:03 GMT  
		Size: 270.4 KB (270435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640152ffa6b1628c31822b6fed053f5978e7d41168ccdc646fca24e4869f1870`  
		Last Modified: Tue, 27 Jul 2021 01:12:18 GMT  
		Size: 75.0 MB (74994434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm variant v7

```console
$ docker pull ros@sha256:6339006da8aa9f01c5f140ff102a1281d7211f285c2079dd99bf3f9b115548f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385879574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9813875c3478474e0d8357aaaf54b39d326da4491c5e3329cc4ea7ef5bf40e5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:31 GMT
ADD file:93478fff12f14732647e59eaafbd2a694de2f3a162fdc6bb1270acc1c69edc5b in / 
# Mon, 26 Jul 2021 22:51:32 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:55:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 01:55:50 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:55:50 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 01:59:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:59:03 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 01:59:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:59:04 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:59:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:00:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 02:01:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5092371cc59fda70c1ace542259c1514fc023e571d50c900322f2a052531228`  
		Last Modified: Mon, 26 Jul 2021 22:55:43 GMT  
		Size: 22.3 MB (22306852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c6b394219d75466dd6176f09c02e5fe7400b0255c6d82480e7d35a0d34a8ee`  
		Last Modified: Tue, 27 Jul 2021 02:18:18 GMT  
		Size: 841.4 KB (841388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879567137a59e93bade6d5accbcd0176b192ccc85080022acea9edea54f9f6c1`  
		Last Modified: Tue, 27 Jul 2021 02:18:17 GMT  
		Size: 4.1 MB (4085785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7141a26daf78fc9f5e9d8cda14c17fb9be91fe6714168a8b33e5a379eeed3f8`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7addca390d668268cbed3008b2cb7707f27958f9f9bbb47a35a03159a18ea5ea`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95f8679d120ee66925b7105bdb869ae6de6c3cd59823868c707a5e768eeeb6b`  
		Last Modified: Tue, 27 Jul 2021 02:20:46 GMT  
		Size: 238.9 MB (238931369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49793c91e8a015ee752db63891347c7ba6811b6aa0837cf3d0715caadd94a942`  
		Last Modified: Tue, 27 Jul 2021 02:18:14 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488e4f135bc94ed38c27e20719c75a5e0a7159c305d1169046923b45458d5240`  
		Last Modified: Tue, 27 Jul 2021 02:21:29 GMT  
		Size: 54.7 MB (54695577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0296cffbb764eaba4174d14eb10d04dfaf32b3a2ee78b34e89246accb24e714`  
		Last Modified: Tue, 27 Jul 2021 02:21:00 GMT  
		Size: 270.4 KB (270436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f4c0cb893c1e65e83d2d1e4b4a23b5987c6936c3effd137151aa55f3bdb5a6`  
		Last Modified: Tue, 27 Jul 2021 02:21:49 GMT  
		Size: 64.7 MB (64745753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:faf38baa8dafbeaea844f6bd3bb0d45205efc80ba90c6e1e69f1a3304e1a3b77
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.9 MB (411938603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8454a0d9d6bf77e4866f7f50c0a5e9083fdd73d99d1b4e8b0af993e215257593`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:30:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:30:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:30:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:31:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:31:07 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:31:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:31:08 GMT
ENV ROS_DISTRO=melodic
# Tue, 31 Aug 2021 02:32:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:32:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Aug 2021 02:32:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:32:21 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:32:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:33:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:33:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8b614e7bd72e38096883e883a7f84bcf9757f4e2d5838723a9ca6e700f0990`  
		Last Modified: Tue, 31 Aug 2021 02:49:48 GMT  
		Size: 841.3 KB (841324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43656e04692247725d22bdcc170a41ec2540163104b7a54702efc8cf83c53312`  
		Last Modified: Tue, 31 Aug 2021 02:49:45 GMT  
		Size: 4.5 MB (4453736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f520100d01a5288e06132656cba43cb602edd010deab8f123a33a6c6e6f99a00`  
		Last Modified: Tue, 31 Aug 2021 02:49:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbba4eff4f186ba166cdbf23547d063084aed9a25ca5363ba642a1c04b93dfbf`  
		Last Modified: Tue, 31 Aug 2021 02:49:45 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e011fd406dfc5eb0a71d17f91cba4a1381fab3e32acc70c140333a6ef9e30f87`  
		Last Modified: Tue, 31 Aug 2021 02:50:30 GMT  
		Size: 252.4 MB (252358786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20b6a9fa48e98e1440b5a9863ff10b53a2fe506722cbcae9423e5101e6901ff`  
		Last Modified: Tue, 31 Aug 2021 02:49:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244d838c364dd2574092cdb2cc2e75b3c41c8c0b9b5b50320bcf25c169bafb7e`  
		Last Modified: Tue, 31 Aug 2021 02:50:52 GMT  
		Size: 63.1 MB (63058214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5701c5fbd70458258495752983482dd703fe5bc347a6884bdf2f6ea7f740b6`  
		Last Modified: Tue, 31 Aug 2021 02:50:42 GMT  
		Size: 271.6 KB (271587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99b1e4b90f000c0c1d02e622b100115401edc9d980f7d374a277b2cdb702041`  
		Last Modified: Tue, 31 Aug 2021 02:50:56 GMT  
		Size: 67.2 MB (67221944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-perception`

```console
$ docker pull ros@sha256:f36c60882efdb144143ab9d3ef5a70f91bd9102447272cfbfbed07888d14aa6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-perception` - linux; amd64

```console
$ docker pull ros@sha256:516907559ba16c6625cad9746a8347c807ccb17ae3418a84894b240066f629eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.5 MB (742484508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49c556e58f4297dda608e3de45be487be949cba84e99b0b7c6a2a5a74f9a153`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:38:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:35:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 00:38:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:38:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:38:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:38:15 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:39:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:39:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 00:40:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1186553e47569a52e52d0ff6702d24c183760ccfa8f0865f5cd805b6a834f02a`  
		Last Modified: Tue, 27 Jul 2021 00:00:30 GMT  
		Size: 840.6 KB (840558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbd42adfa4f4468cc09d87fcaba98a160059fdee872c36809a69e43ab054efb`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 4.9 MB (4872150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e44ba6559363a0c0463b83b1977a52b1063833026aa6e9dddf178d444e003d`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccab66b30a6739dd0e587dc7eb7a3a05990bf99d4f6089491838f3bac0cfbdd`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f8627bbf4a2b81469316a6529e5a8c8bdd100a4ad64e0d474e973ec43f302`  
		Last Modified: Tue, 27 Jul 2021 01:11:51 GMT  
		Size: 259.4 MB (259445689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3fba9583601e046746fa9e5fb95242575e869b6747a7f9d937b202d9081bc`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75838d174816c0a4cd1517ea28102b2d7fdff541aa8d4229b56f30f29817ca86`  
		Last Modified: Tue, 27 Jul 2021 01:12:14 GMT  
		Size: 70.2 MB (70229942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4dde022f386e96e5a68cbc925d59be0ae93c493ce8f4915b24e88d8f8300035`  
		Last Modified: Tue, 27 Jul 2021 01:12:03 GMT  
		Size: 270.4 KB (270435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640152ffa6b1628c31822b6fed053f5978e7d41168ccdc646fca24e4869f1870`  
		Last Modified: Tue, 27 Jul 2021 01:12:18 GMT  
		Size: 75.0 MB (74994434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6babfc3c4e4d20e1f53e5fb0c1116097706546750ec7abc06b6f4fb8705b9c85`  
		Last Modified: Tue, 27 Jul 2021 01:13:38 GMT  
		Size: 305.1 MB (305119850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:10fd0dbc09abe923ce8d42ae5042cd13bff0e1d72eb835681c884f54d599e98c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **645.8 MB (645757906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf68020a039da037c8aeb6cd545bb4eb7c8e33dfc3677d94db76c7f2fdb58ae7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:31 GMT
ADD file:93478fff12f14732647e59eaafbd2a694de2f3a162fdc6bb1270acc1c69edc5b in / 
# Mon, 26 Jul 2021 22:51:32 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:55:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 01:55:50 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:55:50 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 01:59:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:59:03 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 01:59:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:59:04 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:59:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:00:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 02:01:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:05:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5092371cc59fda70c1ace542259c1514fc023e571d50c900322f2a052531228`  
		Last Modified: Mon, 26 Jul 2021 22:55:43 GMT  
		Size: 22.3 MB (22306852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c6b394219d75466dd6176f09c02e5fe7400b0255c6d82480e7d35a0d34a8ee`  
		Last Modified: Tue, 27 Jul 2021 02:18:18 GMT  
		Size: 841.4 KB (841388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879567137a59e93bade6d5accbcd0176b192ccc85080022acea9edea54f9f6c1`  
		Last Modified: Tue, 27 Jul 2021 02:18:17 GMT  
		Size: 4.1 MB (4085785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7141a26daf78fc9f5e9d8cda14c17fb9be91fe6714168a8b33e5a379eeed3f8`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7addca390d668268cbed3008b2cb7707f27958f9f9bbb47a35a03159a18ea5ea`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95f8679d120ee66925b7105bdb869ae6de6c3cd59823868c707a5e768eeeb6b`  
		Last Modified: Tue, 27 Jul 2021 02:20:46 GMT  
		Size: 238.9 MB (238931369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49793c91e8a015ee752db63891347c7ba6811b6aa0837cf3d0715caadd94a942`  
		Last Modified: Tue, 27 Jul 2021 02:18:14 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488e4f135bc94ed38c27e20719c75a5e0a7159c305d1169046923b45458d5240`  
		Last Modified: Tue, 27 Jul 2021 02:21:29 GMT  
		Size: 54.7 MB (54695577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0296cffbb764eaba4174d14eb10d04dfaf32b3a2ee78b34e89246accb24e714`  
		Last Modified: Tue, 27 Jul 2021 02:21:00 GMT  
		Size: 270.4 KB (270436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f4c0cb893c1e65e83d2d1e4b4a23b5987c6936c3effd137151aa55f3bdb5a6`  
		Last Modified: Tue, 27 Jul 2021 02:21:49 GMT  
		Size: 64.7 MB (64745753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e0922fb4aff190d3e807b024491145e6553e86cd576b6c12027240d8460c3c`  
		Last Modified: Tue, 27 Jul 2021 02:25:12 GMT  
		Size: 259.9 MB (259878332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:077b221c40c28022dc8ba4762cc98302e4cd29124801e7c66d2ca3bf56daa631
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.4 MB (703402368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504e883f0b6b31ac6c97c0ded2f7becb65320f90b88e953b114a22f111339cf5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:30:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:30:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:30:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:31:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:31:07 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:31:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:31:08 GMT
ENV ROS_DISTRO=melodic
# Tue, 31 Aug 2021 02:32:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:32:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Aug 2021 02:32:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:32:21 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:32:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:33:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:33:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8b614e7bd72e38096883e883a7f84bcf9757f4e2d5838723a9ca6e700f0990`  
		Last Modified: Tue, 31 Aug 2021 02:49:48 GMT  
		Size: 841.3 KB (841324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43656e04692247725d22bdcc170a41ec2540163104b7a54702efc8cf83c53312`  
		Last Modified: Tue, 31 Aug 2021 02:49:45 GMT  
		Size: 4.5 MB (4453736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f520100d01a5288e06132656cba43cb602edd010deab8f123a33a6c6e6f99a00`  
		Last Modified: Tue, 31 Aug 2021 02:49:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbba4eff4f186ba166cdbf23547d063084aed9a25ca5363ba642a1c04b93dfbf`  
		Last Modified: Tue, 31 Aug 2021 02:49:45 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e011fd406dfc5eb0a71d17f91cba4a1381fab3e32acc70c140333a6ef9e30f87`  
		Last Modified: Tue, 31 Aug 2021 02:50:30 GMT  
		Size: 252.4 MB (252358786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20b6a9fa48e98e1440b5a9863ff10b53a2fe506722cbcae9423e5101e6901ff`  
		Last Modified: Tue, 31 Aug 2021 02:49:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244d838c364dd2574092cdb2cc2e75b3c41c8c0b9b5b50320bcf25c169bafb7e`  
		Last Modified: Tue, 31 Aug 2021 02:50:52 GMT  
		Size: 63.1 MB (63058214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5701c5fbd70458258495752983482dd703fe5bc347a6884bdf2f6ea7f740b6`  
		Last Modified: Tue, 31 Aug 2021 02:50:42 GMT  
		Size: 271.6 KB (271587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99b1e4b90f000c0c1d02e622b100115401edc9d980f7d374a277b2cdb702041`  
		Last Modified: Tue, 31 Aug 2021 02:50:56 GMT  
		Size: 67.2 MB (67221944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9b5764f768a4d0bf7dcd32665a915a46d0ca482b711ea7fecfe3a8b801b280`  
		Last Modified: Tue, 31 Aug 2021 02:52:19 GMT  
		Size: 291.5 MB (291463765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-perception-bionic`

```console
$ docker pull ros@sha256:f36c60882efdb144143ab9d3ef5a70f91bd9102447272cfbfbed07888d14aa6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-perception-bionic` - linux; amd64

```console
$ docker pull ros@sha256:516907559ba16c6625cad9746a8347c807ccb17ae3418a84894b240066f629eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.5 MB (742484508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49c556e58f4297dda608e3de45be487be949cba84e99b0b7c6a2a5a74f9a153`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:38:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:35:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 00:38:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:38:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:38:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:38:15 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:39:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:39:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 00:40:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1186553e47569a52e52d0ff6702d24c183760ccfa8f0865f5cd805b6a834f02a`  
		Last Modified: Tue, 27 Jul 2021 00:00:30 GMT  
		Size: 840.6 KB (840558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbd42adfa4f4468cc09d87fcaba98a160059fdee872c36809a69e43ab054efb`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 4.9 MB (4872150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e44ba6559363a0c0463b83b1977a52b1063833026aa6e9dddf178d444e003d`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccab66b30a6739dd0e587dc7eb7a3a05990bf99d4f6089491838f3bac0cfbdd`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f8627bbf4a2b81469316a6529e5a8c8bdd100a4ad64e0d474e973ec43f302`  
		Last Modified: Tue, 27 Jul 2021 01:11:51 GMT  
		Size: 259.4 MB (259445689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3fba9583601e046746fa9e5fb95242575e869b6747a7f9d937b202d9081bc`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75838d174816c0a4cd1517ea28102b2d7fdff541aa8d4229b56f30f29817ca86`  
		Last Modified: Tue, 27 Jul 2021 01:12:14 GMT  
		Size: 70.2 MB (70229942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4dde022f386e96e5a68cbc925d59be0ae93c493ce8f4915b24e88d8f8300035`  
		Last Modified: Tue, 27 Jul 2021 01:12:03 GMT  
		Size: 270.4 KB (270435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640152ffa6b1628c31822b6fed053f5978e7d41168ccdc646fca24e4869f1870`  
		Last Modified: Tue, 27 Jul 2021 01:12:18 GMT  
		Size: 75.0 MB (74994434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6babfc3c4e4d20e1f53e5fb0c1116097706546750ec7abc06b6f4fb8705b9c85`  
		Last Modified: Tue, 27 Jul 2021 01:13:38 GMT  
		Size: 305.1 MB (305119850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:10fd0dbc09abe923ce8d42ae5042cd13bff0e1d72eb835681c884f54d599e98c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **645.8 MB (645757906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf68020a039da037c8aeb6cd545bb4eb7c8e33dfc3677d94db76c7f2fdb58ae7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:31 GMT
ADD file:93478fff12f14732647e59eaafbd2a694de2f3a162fdc6bb1270acc1c69edc5b in / 
# Mon, 26 Jul 2021 22:51:32 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:55:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 01:55:50 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:55:50 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 01:59:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:59:03 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 01:59:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:59:04 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:59:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:00:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 02:01:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:05:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5092371cc59fda70c1ace542259c1514fc023e571d50c900322f2a052531228`  
		Last Modified: Mon, 26 Jul 2021 22:55:43 GMT  
		Size: 22.3 MB (22306852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c6b394219d75466dd6176f09c02e5fe7400b0255c6d82480e7d35a0d34a8ee`  
		Last Modified: Tue, 27 Jul 2021 02:18:18 GMT  
		Size: 841.4 KB (841388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879567137a59e93bade6d5accbcd0176b192ccc85080022acea9edea54f9f6c1`  
		Last Modified: Tue, 27 Jul 2021 02:18:17 GMT  
		Size: 4.1 MB (4085785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7141a26daf78fc9f5e9d8cda14c17fb9be91fe6714168a8b33e5a379eeed3f8`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7addca390d668268cbed3008b2cb7707f27958f9f9bbb47a35a03159a18ea5ea`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95f8679d120ee66925b7105bdb869ae6de6c3cd59823868c707a5e768eeeb6b`  
		Last Modified: Tue, 27 Jul 2021 02:20:46 GMT  
		Size: 238.9 MB (238931369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49793c91e8a015ee752db63891347c7ba6811b6aa0837cf3d0715caadd94a942`  
		Last Modified: Tue, 27 Jul 2021 02:18:14 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488e4f135bc94ed38c27e20719c75a5e0a7159c305d1169046923b45458d5240`  
		Last Modified: Tue, 27 Jul 2021 02:21:29 GMT  
		Size: 54.7 MB (54695577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0296cffbb764eaba4174d14eb10d04dfaf32b3a2ee78b34e89246accb24e714`  
		Last Modified: Tue, 27 Jul 2021 02:21:00 GMT  
		Size: 270.4 KB (270436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f4c0cb893c1e65e83d2d1e4b4a23b5987c6936c3effd137151aa55f3bdb5a6`  
		Last Modified: Tue, 27 Jul 2021 02:21:49 GMT  
		Size: 64.7 MB (64745753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e0922fb4aff190d3e807b024491145e6553e86cd576b6c12027240d8460c3c`  
		Last Modified: Tue, 27 Jul 2021 02:25:12 GMT  
		Size: 259.9 MB (259878332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:077b221c40c28022dc8ba4762cc98302e4cd29124801e7c66d2ca3bf56daa631
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.4 MB (703402368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504e883f0b6b31ac6c97c0ded2f7becb65320f90b88e953b114a22f111339cf5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:30:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:30:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:30:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:31:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:31:07 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:31:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:31:08 GMT
ENV ROS_DISTRO=melodic
# Tue, 31 Aug 2021 02:32:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:32:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Aug 2021 02:32:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:32:21 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:32:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:33:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:33:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8b614e7bd72e38096883e883a7f84bcf9757f4e2d5838723a9ca6e700f0990`  
		Last Modified: Tue, 31 Aug 2021 02:49:48 GMT  
		Size: 841.3 KB (841324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43656e04692247725d22bdcc170a41ec2540163104b7a54702efc8cf83c53312`  
		Last Modified: Tue, 31 Aug 2021 02:49:45 GMT  
		Size: 4.5 MB (4453736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f520100d01a5288e06132656cba43cb602edd010deab8f123a33a6c6e6f99a00`  
		Last Modified: Tue, 31 Aug 2021 02:49:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbba4eff4f186ba166cdbf23547d063084aed9a25ca5363ba642a1c04b93dfbf`  
		Last Modified: Tue, 31 Aug 2021 02:49:45 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e011fd406dfc5eb0a71d17f91cba4a1381fab3e32acc70c140333a6ef9e30f87`  
		Last Modified: Tue, 31 Aug 2021 02:50:30 GMT  
		Size: 252.4 MB (252358786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20b6a9fa48e98e1440b5a9863ff10b53a2fe506722cbcae9423e5101e6901ff`  
		Last Modified: Tue, 31 Aug 2021 02:49:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244d838c364dd2574092cdb2cc2e75b3c41c8c0b9b5b50320bcf25c169bafb7e`  
		Last Modified: Tue, 31 Aug 2021 02:50:52 GMT  
		Size: 63.1 MB (63058214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5701c5fbd70458258495752983482dd703fe5bc347a6884bdf2f6ea7f740b6`  
		Last Modified: Tue, 31 Aug 2021 02:50:42 GMT  
		Size: 271.6 KB (271587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99b1e4b90f000c0c1d02e622b100115401edc9d980f7d374a277b2cdb702041`  
		Last Modified: Tue, 31 Aug 2021 02:50:56 GMT  
		Size: 67.2 MB (67221944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9b5764f768a4d0bf7dcd32665a915a46d0ca482b711ea7fecfe3a8b801b280`  
		Last Modified: Tue, 31 Aug 2021 02:52:19 GMT  
		Size: 291.5 MB (291463765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-robot`

```console
$ docker pull ros@sha256:11b2b459a097efca63d9b0fcc16013836941050442e52e211ff898a469a16b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot` - linux; amd64

```console
$ docker pull ros@sha256:c006321b47e47cf84b4c8bdf2c7eaddf2125080769e0038e1ce867507433273a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.4 MB (448441915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac37ed9cee6d46118984bf85d40fb6e2569cfe8f6e2e0c8d7dda02d35f91dd4b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:38:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:35:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 00:38:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:38:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:38:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:38:15 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:39:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:39:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 00:40:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:41:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1186553e47569a52e52d0ff6702d24c183760ccfa8f0865f5cd805b6a834f02a`  
		Last Modified: Tue, 27 Jul 2021 00:00:30 GMT  
		Size: 840.6 KB (840558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbd42adfa4f4468cc09d87fcaba98a160059fdee872c36809a69e43ab054efb`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 4.9 MB (4872150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e44ba6559363a0c0463b83b1977a52b1063833026aa6e9dddf178d444e003d`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccab66b30a6739dd0e587dc7eb7a3a05990bf99d4f6089491838f3bac0cfbdd`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f8627bbf4a2b81469316a6529e5a8c8bdd100a4ad64e0d474e973ec43f302`  
		Last Modified: Tue, 27 Jul 2021 01:11:51 GMT  
		Size: 259.4 MB (259445689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3fba9583601e046746fa9e5fb95242575e869b6747a7f9d937b202d9081bc`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75838d174816c0a4cd1517ea28102b2d7fdff541aa8d4229b56f30f29817ca86`  
		Last Modified: Tue, 27 Jul 2021 01:12:14 GMT  
		Size: 70.2 MB (70229942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4dde022f386e96e5a68cbc925d59be0ae93c493ce8f4915b24e88d8f8300035`  
		Last Modified: Tue, 27 Jul 2021 01:12:03 GMT  
		Size: 270.4 KB (270435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640152ffa6b1628c31822b6fed053f5978e7d41168ccdc646fca24e4869f1870`  
		Last Modified: Tue, 27 Jul 2021 01:12:18 GMT  
		Size: 75.0 MB (74994434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55eed9add0cfd575614a9c9c18845491df98558313d952c8c14fbe6419939423`  
		Last Modified: Tue, 27 Jul 2021 01:12:35 GMT  
		Size: 11.1 MB (11077257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:039b40aa8f2b991d341921a46f3d029c5ec3f746cdbd54dcf890c49ef4cef301
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.0 MB (396000038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23834d4bdbcb9fad85a5824bd8664267bdbd7ae601c602d0e8742d5c38fab3d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:31 GMT
ADD file:93478fff12f14732647e59eaafbd2a694de2f3a162fdc6bb1270acc1c69edc5b in / 
# Mon, 26 Jul 2021 22:51:32 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:55:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 01:55:50 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:55:50 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 01:59:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:59:03 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 01:59:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:59:04 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:59:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:00:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 02:01:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:02:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5092371cc59fda70c1ace542259c1514fc023e571d50c900322f2a052531228`  
		Last Modified: Mon, 26 Jul 2021 22:55:43 GMT  
		Size: 22.3 MB (22306852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c6b394219d75466dd6176f09c02e5fe7400b0255c6d82480e7d35a0d34a8ee`  
		Last Modified: Tue, 27 Jul 2021 02:18:18 GMT  
		Size: 841.4 KB (841388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879567137a59e93bade6d5accbcd0176b192ccc85080022acea9edea54f9f6c1`  
		Last Modified: Tue, 27 Jul 2021 02:18:17 GMT  
		Size: 4.1 MB (4085785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7141a26daf78fc9f5e9d8cda14c17fb9be91fe6714168a8b33e5a379eeed3f8`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7addca390d668268cbed3008b2cb7707f27958f9f9bbb47a35a03159a18ea5ea`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95f8679d120ee66925b7105bdb869ae6de6c3cd59823868c707a5e768eeeb6b`  
		Last Modified: Tue, 27 Jul 2021 02:20:46 GMT  
		Size: 238.9 MB (238931369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49793c91e8a015ee752db63891347c7ba6811b6aa0837cf3d0715caadd94a942`  
		Last Modified: Tue, 27 Jul 2021 02:18:14 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488e4f135bc94ed38c27e20719c75a5e0a7159c305d1169046923b45458d5240`  
		Last Modified: Tue, 27 Jul 2021 02:21:29 GMT  
		Size: 54.7 MB (54695577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0296cffbb764eaba4174d14eb10d04dfaf32b3a2ee78b34e89246accb24e714`  
		Last Modified: Tue, 27 Jul 2021 02:21:00 GMT  
		Size: 270.4 KB (270436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f4c0cb893c1e65e83d2d1e4b4a23b5987c6936c3effd137151aa55f3bdb5a6`  
		Last Modified: Tue, 27 Jul 2021 02:21:49 GMT  
		Size: 64.7 MB (64745753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6dba6abf33f0661b634dc6452efbb426f401b8a7552592a3d87c980195ced29`  
		Last Modified: Tue, 27 Jul 2021 02:22:15 GMT  
		Size: 10.1 MB (10120464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cd16546ed9798fd7ab5fcbd0a4f7cc58f7f1977878758a84e35d6cfb7ffd5a3a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.7 MB (422670769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a229ea78af2e9060b93cde25354ae75401235568a5547bcb6a39c3bdfc06fa3e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:30:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:30:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:30:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:31:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:31:07 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:31:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:31:08 GMT
ENV ROS_DISTRO=melodic
# Tue, 31 Aug 2021 02:32:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:32:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Aug 2021 02:32:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:32:21 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:32:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:33:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:33:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:33:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8b614e7bd72e38096883e883a7f84bcf9757f4e2d5838723a9ca6e700f0990`  
		Last Modified: Tue, 31 Aug 2021 02:49:48 GMT  
		Size: 841.3 KB (841324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43656e04692247725d22bdcc170a41ec2540163104b7a54702efc8cf83c53312`  
		Last Modified: Tue, 31 Aug 2021 02:49:45 GMT  
		Size: 4.5 MB (4453736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f520100d01a5288e06132656cba43cb602edd010deab8f123a33a6c6e6f99a00`  
		Last Modified: Tue, 31 Aug 2021 02:49:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbba4eff4f186ba166cdbf23547d063084aed9a25ca5363ba642a1c04b93dfbf`  
		Last Modified: Tue, 31 Aug 2021 02:49:45 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e011fd406dfc5eb0a71d17f91cba4a1381fab3e32acc70c140333a6ef9e30f87`  
		Last Modified: Tue, 31 Aug 2021 02:50:30 GMT  
		Size: 252.4 MB (252358786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20b6a9fa48e98e1440b5a9863ff10b53a2fe506722cbcae9423e5101e6901ff`  
		Last Modified: Tue, 31 Aug 2021 02:49:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244d838c364dd2574092cdb2cc2e75b3c41c8c0b9b5b50320bcf25c169bafb7e`  
		Last Modified: Tue, 31 Aug 2021 02:50:52 GMT  
		Size: 63.1 MB (63058214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5701c5fbd70458258495752983482dd703fe5bc347a6884bdf2f6ea7f740b6`  
		Last Modified: Tue, 31 Aug 2021 02:50:42 GMT  
		Size: 271.6 KB (271587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99b1e4b90f000c0c1d02e622b100115401edc9d980f7d374a277b2cdb702041`  
		Last Modified: Tue, 31 Aug 2021 02:50:56 GMT  
		Size: 67.2 MB (67221944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0030851addd2f9077149c79370d4e8792fb86d2d5d8a8a75678645d09ec47f`  
		Last Modified: Tue, 31 Aug 2021 02:51:14 GMT  
		Size: 10.7 MB (10732166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-robot-bionic`

```console
$ docker pull ros@sha256:11b2b459a097efca63d9b0fcc16013836941050442e52e211ff898a469a16b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot-bionic` - linux; amd64

```console
$ docker pull ros@sha256:c006321b47e47cf84b4c8bdf2c7eaddf2125080769e0038e1ce867507433273a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.4 MB (448441915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac37ed9cee6d46118984bf85d40fb6e2569cfe8f6e2e0c8d7dda02d35f91dd4b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:38:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:35:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 00:38:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:38:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:38:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:38:15 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:39:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:39:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 00:40:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:41:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1186553e47569a52e52d0ff6702d24c183760ccfa8f0865f5cd805b6a834f02a`  
		Last Modified: Tue, 27 Jul 2021 00:00:30 GMT  
		Size: 840.6 KB (840558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbd42adfa4f4468cc09d87fcaba98a160059fdee872c36809a69e43ab054efb`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 4.9 MB (4872150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e44ba6559363a0c0463b83b1977a52b1063833026aa6e9dddf178d444e003d`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccab66b30a6739dd0e587dc7eb7a3a05990bf99d4f6089491838f3bac0cfbdd`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f8627bbf4a2b81469316a6529e5a8c8bdd100a4ad64e0d474e973ec43f302`  
		Last Modified: Tue, 27 Jul 2021 01:11:51 GMT  
		Size: 259.4 MB (259445689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3fba9583601e046746fa9e5fb95242575e869b6747a7f9d937b202d9081bc`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75838d174816c0a4cd1517ea28102b2d7fdff541aa8d4229b56f30f29817ca86`  
		Last Modified: Tue, 27 Jul 2021 01:12:14 GMT  
		Size: 70.2 MB (70229942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4dde022f386e96e5a68cbc925d59be0ae93c493ce8f4915b24e88d8f8300035`  
		Last Modified: Tue, 27 Jul 2021 01:12:03 GMT  
		Size: 270.4 KB (270435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640152ffa6b1628c31822b6fed053f5978e7d41168ccdc646fca24e4869f1870`  
		Last Modified: Tue, 27 Jul 2021 01:12:18 GMT  
		Size: 75.0 MB (74994434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55eed9add0cfd575614a9c9c18845491df98558313d952c8c14fbe6419939423`  
		Last Modified: Tue, 27 Jul 2021 01:12:35 GMT  
		Size: 11.1 MB (11077257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:039b40aa8f2b991d341921a46f3d029c5ec3f746cdbd54dcf890c49ef4cef301
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.0 MB (396000038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23834d4bdbcb9fad85a5824bd8664267bdbd7ae601c602d0e8742d5c38fab3d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:31 GMT
ADD file:93478fff12f14732647e59eaafbd2a694de2f3a162fdc6bb1270acc1c69edc5b in / 
# Mon, 26 Jul 2021 22:51:32 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:55:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 01:55:50 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:55:50 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 01:59:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:59:03 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 01:59:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:59:04 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:59:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:00:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 02:01:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:02:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5092371cc59fda70c1ace542259c1514fc023e571d50c900322f2a052531228`  
		Last Modified: Mon, 26 Jul 2021 22:55:43 GMT  
		Size: 22.3 MB (22306852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c6b394219d75466dd6176f09c02e5fe7400b0255c6d82480e7d35a0d34a8ee`  
		Last Modified: Tue, 27 Jul 2021 02:18:18 GMT  
		Size: 841.4 KB (841388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879567137a59e93bade6d5accbcd0176b192ccc85080022acea9edea54f9f6c1`  
		Last Modified: Tue, 27 Jul 2021 02:18:17 GMT  
		Size: 4.1 MB (4085785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7141a26daf78fc9f5e9d8cda14c17fb9be91fe6714168a8b33e5a379eeed3f8`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7addca390d668268cbed3008b2cb7707f27958f9f9bbb47a35a03159a18ea5ea`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95f8679d120ee66925b7105bdb869ae6de6c3cd59823868c707a5e768eeeb6b`  
		Last Modified: Tue, 27 Jul 2021 02:20:46 GMT  
		Size: 238.9 MB (238931369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49793c91e8a015ee752db63891347c7ba6811b6aa0837cf3d0715caadd94a942`  
		Last Modified: Tue, 27 Jul 2021 02:18:14 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488e4f135bc94ed38c27e20719c75a5e0a7159c305d1169046923b45458d5240`  
		Last Modified: Tue, 27 Jul 2021 02:21:29 GMT  
		Size: 54.7 MB (54695577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0296cffbb764eaba4174d14eb10d04dfaf32b3a2ee78b34e89246accb24e714`  
		Last Modified: Tue, 27 Jul 2021 02:21:00 GMT  
		Size: 270.4 KB (270436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f4c0cb893c1e65e83d2d1e4b4a23b5987c6936c3effd137151aa55f3bdb5a6`  
		Last Modified: Tue, 27 Jul 2021 02:21:49 GMT  
		Size: 64.7 MB (64745753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6dba6abf33f0661b634dc6452efbb426f401b8a7552592a3d87c980195ced29`  
		Last Modified: Tue, 27 Jul 2021 02:22:15 GMT  
		Size: 10.1 MB (10120464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cd16546ed9798fd7ab5fcbd0a4f7cc58f7f1977878758a84e35d6cfb7ffd5a3a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.7 MB (422670769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a229ea78af2e9060b93cde25354ae75401235568a5547bcb6a39c3bdfc06fa3e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:30:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:30:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:30:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:31:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:31:07 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:31:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:31:08 GMT
ENV ROS_DISTRO=melodic
# Tue, 31 Aug 2021 02:32:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:32:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Aug 2021 02:32:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:32:21 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:32:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:33:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:33:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:33:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8b614e7bd72e38096883e883a7f84bcf9757f4e2d5838723a9ca6e700f0990`  
		Last Modified: Tue, 31 Aug 2021 02:49:48 GMT  
		Size: 841.3 KB (841324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43656e04692247725d22bdcc170a41ec2540163104b7a54702efc8cf83c53312`  
		Last Modified: Tue, 31 Aug 2021 02:49:45 GMT  
		Size: 4.5 MB (4453736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f520100d01a5288e06132656cba43cb602edd010deab8f123a33a6c6e6f99a00`  
		Last Modified: Tue, 31 Aug 2021 02:49:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbba4eff4f186ba166cdbf23547d063084aed9a25ca5363ba642a1c04b93dfbf`  
		Last Modified: Tue, 31 Aug 2021 02:49:45 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e011fd406dfc5eb0a71d17f91cba4a1381fab3e32acc70c140333a6ef9e30f87`  
		Last Modified: Tue, 31 Aug 2021 02:50:30 GMT  
		Size: 252.4 MB (252358786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20b6a9fa48e98e1440b5a9863ff10b53a2fe506722cbcae9423e5101e6901ff`  
		Last Modified: Tue, 31 Aug 2021 02:49:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244d838c364dd2574092cdb2cc2e75b3c41c8c0b9b5b50320bcf25c169bafb7e`  
		Last Modified: Tue, 31 Aug 2021 02:50:52 GMT  
		Size: 63.1 MB (63058214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5701c5fbd70458258495752983482dd703fe5bc347a6884bdf2f6ea7f740b6`  
		Last Modified: Tue, 31 Aug 2021 02:50:42 GMT  
		Size: 271.6 KB (271587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99b1e4b90f000c0c1d02e622b100115401edc9d980f7d374a277b2cdb702041`  
		Last Modified: Tue, 31 Aug 2021 02:50:56 GMT  
		Size: 67.2 MB (67221944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0030851addd2f9077149c79370d4e8792fb86d2d5d8a8a75678645d09ec47f`  
		Last Modified: Tue, 31 Aug 2021 02:51:14 GMT  
		Size: 10.7 MB (10732166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-base`

```console
$ docker pull ros@sha256:976c369a0ebaac383ead1240e485fa3d2eb83647619112876b08cf7592173db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:f9ab26ad9caf7c6025ff2669c4a4413746b68ea9ed05b3641829ccb515771e8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.4 MB (437364658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07711f635f57ed1907b716dba3ea6e751395f9e0e6d27350c4bb37860fac936`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:38:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:35:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 00:38:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:38:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:38:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:38:15 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:39:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:39:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 00:40:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1186553e47569a52e52d0ff6702d24c183760ccfa8f0865f5cd805b6a834f02a`  
		Last Modified: Tue, 27 Jul 2021 00:00:30 GMT  
		Size: 840.6 KB (840558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbd42adfa4f4468cc09d87fcaba98a160059fdee872c36809a69e43ab054efb`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 4.9 MB (4872150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e44ba6559363a0c0463b83b1977a52b1063833026aa6e9dddf178d444e003d`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccab66b30a6739dd0e587dc7eb7a3a05990bf99d4f6089491838f3bac0cfbdd`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f8627bbf4a2b81469316a6529e5a8c8bdd100a4ad64e0d474e973ec43f302`  
		Last Modified: Tue, 27 Jul 2021 01:11:51 GMT  
		Size: 259.4 MB (259445689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3fba9583601e046746fa9e5fb95242575e869b6747a7f9d937b202d9081bc`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75838d174816c0a4cd1517ea28102b2d7fdff541aa8d4229b56f30f29817ca86`  
		Last Modified: Tue, 27 Jul 2021 01:12:14 GMT  
		Size: 70.2 MB (70229942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4dde022f386e96e5a68cbc925d59be0ae93c493ce8f4915b24e88d8f8300035`  
		Last Modified: Tue, 27 Jul 2021 01:12:03 GMT  
		Size: 270.4 KB (270435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640152ffa6b1628c31822b6fed053f5978e7d41168ccdc646fca24e4869f1870`  
		Last Modified: Tue, 27 Jul 2021 01:12:18 GMT  
		Size: 75.0 MB (74994434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:6339006da8aa9f01c5f140ff102a1281d7211f285c2079dd99bf3f9b115548f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385879574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9813875c3478474e0d8357aaaf54b39d326da4491c5e3329cc4ea7ef5bf40e5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:31 GMT
ADD file:93478fff12f14732647e59eaafbd2a694de2f3a162fdc6bb1270acc1c69edc5b in / 
# Mon, 26 Jul 2021 22:51:32 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:55:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 01:55:50 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:55:50 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 01:59:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:59:03 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 01:59:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:59:04 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:59:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:00:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 02:01:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5092371cc59fda70c1ace542259c1514fc023e571d50c900322f2a052531228`  
		Last Modified: Mon, 26 Jul 2021 22:55:43 GMT  
		Size: 22.3 MB (22306852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c6b394219d75466dd6176f09c02e5fe7400b0255c6d82480e7d35a0d34a8ee`  
		Last Modified: Tue, 27 Jul 2021 02:18:18 GMT  
		Size: 841.4 KB (841388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879567137a59e93bade6d5accbcd0176b192ccc85080022acea9edea54f9f6c1`  
		Last Modified: Tue, 27 Jul 2021 02:18:17 GMT  
		Size: 4.1 MB (4085785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7141a26daf78fc9f5e9d8cda14c17fb9be91fe6714168a8b33e5a379eeed3f8`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7addca390d668268cbed3008b2cb7707f27958f9f9bbb47a35a03159a18ea5ea`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95f8679d120ee66925b7105bdb869ae6de6c3cd59823868c707a5e768eeeb6b`  
		Last Modified: Tue, 27 Jul 2021 02:20:46 GMT  
		Size: 238.9 MB (238931369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49793c91e8a015ee752db63891347c7ba6811b6aa0837cf3d0715caadd94a942`  
		Last Modified: Tue, 27 Jul 2021 02:18:14 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488e4f135bc94ed38c27e20719c75a5e0a7159c305d1169046923b45458d5240`  
		Last Modified: Tue, 27 Jul 2021 02:21:29 GMT  
		Size: 54.7 MB (54695577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0296cffbb764eaba4174d14eb10d04dfaf32b3a2ee78b34e89246accb24e714`  
		Last Modified: Tue, 27 Jul 2021 02:21:00 GMT  
		Size: 270.4 KB (270436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f4c0cb893c1e65e83d2d1e4b4a23b5987c6936c3effd137151aa55f3bdb5a6`  
		Last Modified: Tue, 27 Jul 2021 02:21:49 GMT  
		Size: 64.7 MB (64745753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:faf38baa8dafbeaea844f6bd3bb0d45205efc80ba90c6e1e69f1a3304e1a3b77
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.9 MB (411938603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8454a0d9d6bf77e4866f7f50c0a5e9083fdd73d99d1b4e8b0af993e215257593`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:30:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:30:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:30:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:31:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:31:07 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:31:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:31:08 GMT
ENV ROS_DISTRO=melodic
# Tue, 31 Aug 2021 02:32:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:32:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Aug 2021 02:32:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:32:21 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:32:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:33:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:33:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8b614e7bd72e38096883e883a7f84bcf9757f4e2d5838723a9ca6e700f0990`  
		Last Modified: Tue, 31 Aug 2021 02:49:48 GMT  
		Size: 841.3 KB (841324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43656e04692247725d22bdcc170a41ec2540163104b7a54702efc8cf83c53312`  
		Last Modified: Tue, 31 Aug 2021 02:49:45 GMT  
		Size: 4.5 MB (4453736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f520100d01a5288e06132656cba43cb602edd010deab8f123a33a6c6e6f99a00`  
		Last Modified: Tue, 31 Aug 2021 02:49:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbba4eff4f186ba166cdbf23547d063084aed9a25ca5363ba642a1c04b93dfbf`  
		Last Modified: Tue, 31 Aug 2021 02:49:45 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e011fd406dfc5eb0a71d17f91cba4a1381fab3e32acc70c140333a6ef9e30f87`  
		Last Modified: Tue, 31 Aug 2021 02:50:30 GMT  
		Size: 252.4 MB (252358786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20b6a9fa48e98e1440b5a9863ff10b53a2fe506722cbcae9423e5101e6901ff`  
		Last Modified: Tue, 31 Aug 2021 02:49:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244d838c364dd2574092cdb2cc2e75b3c41c8c0b9b5b50320bcf25c169bafb7e`  
		Last Modified: Tue, 31 Aug 2021 02:50:52 GMT  
		Size: 63.1 MB (63058214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5701c5fbd70458258495752983482dd703fe5bc347a6884bdf2f6ea7f740b6`  
		Last Modified: Tue, 31 Aug 2021 02:50:42 GMT  
		Size: 271.6 KB (271587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99b1e4b90f000c0c1d02e622b100115401edc9d980f7d374a277b2cdb702041`  
		Last Modified: Tue, 31 Aug 2021 02:50:56 GMT  
		Size: 67.2 MB (67221944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-base-bionic`

```console
$ docker pull ros@sha256:976c369a0ebaac383ead1240e485fa3d2eb83647619112876b08cf7592173db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base-bionic` - linux; amd64

```console
$ docker pull ros@sha256:f9ab26ad9caf7c6025ff2669c4a4413746b68ea9ed05b3641829ccb515771e8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.4 MB (437364658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07711f635f57ed1907b716dba3ea6e751395f9e0e6d27350c4bb37860fac936`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:38:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:35:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 00:38:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:38:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:38:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:38:15 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:39:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:39:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 00:40:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1186553e47569a52e52d0ff6702d24c183760ccfa8f0865f5cd805b6a834f02a`  
		Last Modified: Tue, 27 Jul 2021 00:00:30 GMT  
		Size: 840.6 KB (840558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbd42adfa4f4468cc09d87fcaba98a160059fdee872c36809a69e43ab054efb`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 4.9 MB (4872150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e44ba6559363a0c0463b83b1977a52b1063833026aa6e9dddf178d444e003d`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccab66b30a6739dd0e587dc7eb7a3a05990bf99d4f6089491838f3bac0cfbdd`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f8627bbf4a2b81469316a6529e5a8c8bdd100a4ad64e0d474e973ec43f302`  
		Last Modified: Tue, 27 Jul 2021 01:11:51 GMT  
		Size: 259.4 MB (259445689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3fba9583601e046746fa9e5fb95242575e869b6747a7f9d937b202d9081bc`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75838d174816c0a4cd1517ea28102b2d7fdff541aa8d4229b56f30f29817ca86`  
		Last Modified: Tue, 27 Jul 2021 01:12:14 GMT  
		Size: 70.2 MB (70229942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4dde022f386e96e5a68cbc925d59be0ae93c493ce8f4915b24e88d8f8300035`  
		Last Modified: Tue, 27 Jul 2021 01:12:03 GMT  
		Size: 270.4 KB (270435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640152ffa6b1628c31822b6fed053f5978e7d41168ccdc646fca24e4869f1870`  
		Last Modified: Tue, 27 Jul 2021 01:12:18 GMT  
		Size: 75.0 MB (74994434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:6339006da8aa9f01c5f140ff102a1281d7211f285c2079dd99bf3f9b115548f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385879574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9813875c3478474e0d8357aaaf54b39d326da4491c5e3329cc4ea7ef5bf40e5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:31 GMT
ADD file:93478fff12f14732647e59eaafbd2a694de2f3a162fdc6bb1270acc1c69edc5b in / 
# Mon, 26 Jul 2021 22:51:32 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:55:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 01:55:50 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:55:50 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 01:59:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:59:03 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 01:59:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:59:04 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:59:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:00:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 02:01:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5092371cc59fda70c1ace542259c1514fc023e571d50c900322f2a052531228`  
		Last Modified: Mon, 26 Jul 2021 22:55:43 GMT  
		Size: 22.3 MB (22306852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c6b394219d75466dd6176f09c02e5fe7400b0255c6d82480e7d35a0d34a8ee`  
		Last Modified: Tue, 27 Jul 2021 02:18:18 GMT  
		Size: 841.4 KB (841388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879567137a59e93bade6d5accbcd0176b192ccc85080022acea9edea54f9f6c1`  
		Last Modified: Tue, 27 Jul 2021 02:18:17 GMT  
		Size: 4.1 MB (4085785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7141a26daf78fc9f5e9d8cda14c17fb9be91fe6714168a8b33e5a379eeed3f8`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7addca390d668268cbed3008b2cb7707f27958f9f9bbb47a35a03159a18ea5ea`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95f8679d120ee66925b7105bdb869ae6de6c3cd59823868c707a5e768eeeb6b`  
		Last Modified: Tue, 27 Jul 2021 02:20:46 GMT  
		Size: 238.9 MB (238931369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49793c91e8a015ee752db63891347c7ba6811b6aa0837cf3d0715caadd94a942`  
		Last Modified: Tue, 27 Jul 2021 02:18:14 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488e4f135bc94ed38c27e20719c75a5e0a7159c305d1169046923b45458d5240`  
		Last Modified: Tue, 27 Jul 2021 02:21:29 GMT  
		Size: 54.7 MB (54695577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0296cffbb764eaba4174d14eb10d04dfaf32b3a2ee78b34e89246accb24e714`  
		Last Modified: Tue, 27 Jul 2021 02:21:00 GMT  
		Size: 270.4 KB (270436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f4c0cb893c1e65e83d2d1e4b4a23b5987c6936c3effd137151aa55f3bdb5a6`  
		Last Modified: Tue, 27 Jul 2021 02:21:49 GMT  
		Size: 64.7 MB (64745753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:faf38baa8dafbeaea844f6bd3bb0d45205efc80ba90c6e1e69f1a3304e1a3b77
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.9 MB (411938603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8454a0d9d6bf77e4866f7f50c0a5e9083fdd73d99d1b4e8b0af993e215257593`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:30:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:30:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:30:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:31:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:31:07 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:31:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:31:08 GMT
ENV ROS_DISTRO=melodic
# Tue, 31 Aug 2021 02:32:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:32:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Aug 2021 02:32:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:32:21 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:32:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:33:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:33:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8b614e7bd72e38096883e883a7f84bcf9757f4e2d5838723a9ca6e700f0990`  
		Last Modified: Tue, 31 Aug 2021 02:49:48 GMT  
		Size: 841.3 KB (841324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43656e04692247725d22bdcc170a41ec2540163104b7a54702efc8cf83c53312`  
		Last Modified: Tue, 31 Aug 2021 02:49:45 GMT  
		Size: 4.5 MB (4453736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f520100d01a5288e06132656cba43cb602edd010deab8f123a33a6c6e6f99a00`  
		Last Modified: Tue, 31 Aug 2021 02:49:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbba4eff4f186ba166cdbf23547d063084aed9a25ca5363ba642a1c04b93dfbf`  
		Last Modified: Tue, 31 Aug 2021 02:49:45 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e011fd406dfc5eb0a71d17f91cba4a1381fab3e32acc70c140333a6ef9e30f87`  
		Last Modified: Tue, 31 Aug 2021 02:50:30 GMT  
		Size: 252.4 MB (252358786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20b6a9fa48e98e1440b5a9863ff10b53a2fe506722cbcae9423e5101e6901ff`  
		Last Modified: Tue, 31 Aug 2021 02:49:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244d838c364dd2574092cdb2cc2e75b3c41c8c0b9b5b50320bcf25c169bafb7e`  
		Last Modified: Tue, 31 Aug 2021 02:50:52 GMT  
		Size: 63.1 MB (63058214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5701c5fbd70458258495752983482dd703fe5bc347a6884bdf2f6ea7f740b6`  
		Last Modified: Tue, 31 Aug 2021 02:50:42 GMT  
		Size: 271.6 KB (271587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99b1e4b90f000c0c1d02e622b100115401edc9d980f7d374a277b2cdb702041`  
		Last Modified: Tue, 31 Aug 2021 02:50:56 GMT  
		Size: 67.2 MB (67221944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-core`

```console
$ docker pull ros@sha256:61ec2e6ca3c265c4c386236cd53d996e64bb78b5d98b99edbd3333155f93f06c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:75a3bb07c9b6265827bf559fcc633d660776bb8f408b6dc4c3901f8d48a7fc3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291869847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947363507d39ea6611167fc1c338d12ef5b49ba0a2a5cc6274d9860949f1d3a8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:38:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:35:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 00:38:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:38:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:38:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:38:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1186553e47569a52e52d0ff6702d24c183760ccfa8f0865f5cd805b6a834f02a`  
		Last Modified: Tue, 27 Jul 2021 00:00:30 GMT  
		Size: 840.6 KB (840558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbd42adfa4f4468cc09d87fcaba98a160059fdee872c36809a69e43ab054efb`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 4.9 MB (4872150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e44ba6559363a0c0463b83b1977a52b1063833026aa6e9dddf178d444e003d`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccab66b30a6739dd0e587dc7eb7a3a05990bf99d4f6089491838f3bac0cfbdd`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f8627bbf4a2b81469316a6529e5a8c8bdd100a4ad64e0d474e973ec43f302`  
		Last Modified: Tue, 27 Jul 2021 01:11:51 GMT  
		Size: 259.4 MB (259445689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3fba9583601e046746fa9e5fb95242575e869b6747a7f9d937b202d9081bc`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:bbd128c88179834dd78f67e2f697f122e407e77a4a2f0e86dc2873ff0deca7f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266167808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71b21d55415e370ea0f2efce7f099343d10317d448c608d9927230700632df0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:31 GMT
ADD file:93478fff12f14732647e59eaafbd2a694de2f3a162fdc6bb1270acc1c69edc5b in / 
# Mon, 26 Jul 2021 22:51:32 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:55:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 01:55:50 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:55:50 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 01:59:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:59:03 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 01:59:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:59:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d5092371cc59fda70c1ace542259c1514fc023e571d50c900322f2a052531228`  
		Last Modified: Mon, 26 Jul 2021 22:55:43 GMT  
		Size: 22.3 MB (22306852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c6b394219d75466dd6176f09c02e5fe7400b0255c6d82480e7d35a0d34a8ee`  
		Last Modified: Tue, 27 Jul 2021 02:18:18 GMT  
		Size: 841.4 KB (841388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879567137a59e93bade6d5accbcd0176b192ccc85080022acea9edea54f9f6c1`  
		Last Modified: Tue, 27 Jul 2021 02:18:17 GMT  
		Size: 4.1 MB (4085785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7141a26daf78fc9f5e9d8cda14c17fb9be91fe6714168a8b33e5a379eeed3f8`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7addca390d668268cbed3008b2cb7707f27958f9f9bbb47a35a03159a18ea5ea`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95f8679d120ee66925b7105bdb869ae6de6c3cd59823868c707a5e768eeeb6b`  
		Last Modified: Tue, 27 Jul 2021 02:20:46 GMT  
		Size: 238.9 MB (238931369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49793c91e8a015ee752db63891347c7ba6811b6aa0837cf3d0715caadd94a942`  
		Last Modified: Tue, 27 Jul 2021 02:18:14 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8558b06cba0b0fe5b01aa01eb86def7df91430b506aa3dfdb92f009424071a34
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 MB (281386858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d265980b900e789c6ab4768716d4add45868e8d5ddde032b8882870373f5041`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:30:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:30:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:30:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:31:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:31:07 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:31:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:31:08 GMT
ENV ROS_DISTRO=melodic
# Tue, 31 Aug 2021 02:32:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:32:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Aug 2021 02:32:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:32:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8b614e7bd72e38096883e883a7f84bcf9757f4e2d5838723a9ca6e700f0990`  
		Last Modified: Tue, 31 Aug 2021 02:49:48 GMT  
		Size: 841.3 KB (841324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43656e04692247725d22bdcc170a41ec2540163104b7a54702efc8cf83c53312`  
		Last Modified: Tue, 31 Aug 2021 02:49:45 GMT  
		Size: 4.5 MB (4453736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f520100d01a5288e06132656cba43cb602edd010deab8f123a33a6c6e6f99a00`  
		Last Modified: Tue, 31 Aug 2021 02:49:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbba4eff4f186ba166cdbf23547d063084aed9a25ca5363ba642a1c04b93dfbf`  
		Last Modified: Tue, 31 Aug 2021 02:49:45 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e011fd406dfc5eb0a71d17f91cba4a1381fab3e32acc70c140333a6ef9e30f87`  
		Last Modified: Tue, 31 Aug 2021 02:50:30 GMT  
		Size: 252.4 MB (252358786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20b6a9fa48e98e1440b5a9863ff10b53a2fe506722cbcae9423e5101e6901ff`  
		Last Modified: Tue, 31 Aug 2021 02:49:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-core-bionic`

```console
$ docker pull ros@sha256:61ec2e6ca3c265c4c386236cd53d996e64bb78b5d98b99edbd3333155f93f06c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:75a3bb07c9b6265827bf559fcc633d660776bb8f408b6dc4c3901f8d48a7fc3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291869847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947363507d39ea6611167fc1c338d12ef5b49ba0a2a5cc6274d9860949f1d3a8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:38:16 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:35:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:35:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:35:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 00:38:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:38:14 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:38:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:38:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1186553e47569a52e52d0ff6702d24c183760ccfa8f0865f5cd805b6a834f02a`  
		Last Modified: Tue, 27 Jul 2021 00:00:30 GMT  
		Size: 840.6 KB (840558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbd42adfa4f4468cc09d87fcaba98a160059fdee872c36809a69e43ab054efb`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 4.9 MB (4872150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e44ba6559363a0c0463b83b1977a52b1063833026aa6e9dddf178d444e003d`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccab66b30a6739dd0e587dc7eb7a3a05990bf99d4f6089491838f3bac0cfbdd`  
		Last Modified: Tue, 27 Jul 2021 01:11:08 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f8627bbf4a2b81469316a6529e5a8c8bdd100a4ad64e0d474e973ec43f302`  
		Last Modified: Tue, 27 Jul 2021 01:11:51 GMT  
		Size: 259.4 MB (259445689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3fba9583601e046746fa9e5fb95242575e869b6747a7f9d937b202d9081bc`  
		Last Modified: Tue, 27 Jul 2021 01:11:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:bbd128c88179834dd78f67e2f697f122e407e77a4a2f0e86dc2873ff0deca7f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266167808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71b21d55415e370ea0f2efce7f099343d10317d448c608d9927230700632df0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:31 GMT
ADD file:93478fff12f14732647e59eaafbd2a694de2f3a162fdc6bb1270acc1c69edc5b in / 
# Mon, 26 Jul 2021 22:51:32 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:55:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:55:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 01:55:50 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:55:50 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:55:51 GMT
ENV ROS_DISTRO=melodic
# Tue, 27 Jul 2021 01:59:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:59:03 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 01:59:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:59:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d5092371cc59fda70c1ace542259c1514fc023e571d50c900322f2a052531228`  
		Last Modified: Mon, 26 Jul 2021 22:55:43 GMT  
		Size: 22.3 MB (22306852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c6b394219d75466dd6176f09c02e5fe7400b0255c6d82480e7d35a0d34a8ee`  
		Last Modified: Tue, 27 Jul 2021 02:18:18 GMT  
		Size: 841.4 KB (841388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879567137a59e93bade6d5accbcd0176b192ccc85080022acea9edea54f9f6c1`  
		Last Modified: Tue, 27 Jul 2021 02:18:17 GMT  
		Size: 4.1 MB (4085785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7141a26daf78fc9f5e9d8cda14c17fb9be91fe6714168a8b33e5a379eeed3f8`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7addca390d668268cbed3008b2cb7707f27958f9f9bbb47a35a03159a18ea5ea`  
		Last Modified: Tue, 27 Jul 2021 02:18:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95f8679d120ee66925b7105bdb869ae6de6c3cd59823868c707a5e768eeeb6b`  
		Last Modified: Tue, 27 Jul 2021 02:20:46 GMT  
		Size: 238.9 MB (238931369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49793c91e8a015ee752db63891347c7ba6811b6aa0837cf3d0715caadd94a942`  
		Last Modified: Tue, 27 Jul 2021 02:18:14 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8558b06cba0b0fe5b01aa01eb86def7df91430b506aa3dfdb92f009424071a34
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 MB (281386858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d265980b900e789c6ab4768716d4add45868e8d5ddde032b8882870373f5041`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:30:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:30:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:30:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:31:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:31:07 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:31:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:31:08 GMT
ENV ROS_DISTRO=melodic
# Tue, 31 Aug 2021 02:32:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:32:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Aug 2021 02:32:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:32:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8b614e7bd72e38096883e883a7f84bcf9757f4e2d5838723a9ca6e700f0990`  
		Last Modified: Tue, 31 Aug 2021 02:49:48 GMT  
		Size: 841.3 KB (841324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43656e04692247725d22bdcc170a41ec2540163104b7a54702efc8cf83c53312`  
		Last Modified: Tue, 31 Aug 2021 02:49:45 GMT  
		Size: 4.5 MB (4453736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f520100d01a5288e06132656cba43cb602edd010deab8f123a33a6c6e6f99a00`  
		Last Modified: Tue, 31 Aug 2021 02:49:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbba4eff4f186ba166cdbf23547d063084aed9a25ca5363ba642a1c04b93dfbf`  
		Last Modified: Tue, 31 Aug 2021 02:49:45 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e011fd406dfc5eb0a71d17f91cba4a1381fab3e32acc70c140333a6ef9e30f87`  
		Last Modified: Tue, 31 Aug 2021 02:50:30 GMT  
		Size: 252.4 MB (252358786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20b6a9fa48e98e1440b5a9863ff10b53a2fe506722cbcae9423e5101e6901ff`  
		Last Modified: Tue, 31 Aug 2021 02:49:44 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic`

```console
$ docker pull ros@sha256:5dec8c8b4eb625d344bff02477b70b08c3cdd1b593e60918d1c46d1c619a96ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:42187c1172c16383c3115f69296874cf789b49f8139799c02b4e541da27c5244
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339178352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426daddb2147136e833c0d5562c86f62a3be0b266a24c08482c3c12b919aae8b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:48:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:48:27 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:48:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:48:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jul 2021 00:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:50:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:50:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:50:51 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:51:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:51:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 00:52:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2997acb5dc01c0a5dcc159471aea13a7b87074a11df83667b1f8b108602e7dda`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5853e486374821ccfc40d07b68affecdc12e88f4ff7e8be0d58d904d3f525d5a`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e9cabb7a6a3ae445854e8bda4e4762b3d7ab26b3191ab8a006360c8dd0689f`  
		Last Modified: Tue, 27 Jul 2021 01:14:29 GMT  
		Size: 176.7 MB (176702826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c5a6e61679ad83770b86fc37c72db8d318a69a8d5dcac2d00db8bf86b0e9fc`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b972074e1773fd5c4e1a932d55b75a2a2850d2e1ffced2c52e961b49f75d22`  
		Last Modified: Tue, 27 Jul 2021 01:14:49 GMT  
		Size: 47.3 MB (47259266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eccfe2edcc7482e1d5dc3b436b2197ed3020befcbc53e9f4f4e18c3a46497772`  
		Last Modified: Tue, 27 Jul 2021 01:14:40 GMT  
		Size: 313.4 KB (313417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c855981c165d5abfeb9c7d6a5bbfd8616a913a3674a8e23f9f4f9e6efd7fe627`  
		Last Modified: Tue, 27 Jul 2021 01:14:54 GMT  
		Size: 79.6 MB (79602950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:611a526bca19877d1fbfdd8dd84b9b1c3991b9157f4910b1951704df716fa316
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284623996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7d588f8655d95e5f10227e22b94f2c5d45b6fa733577a24393b2cc9c5acfb1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:51 GMT
ADD file:dec1b30555f66d79050762dc2b6c8e55dc130245f3bd1af94d77f1e1e6aa3ccb in / 
# Mon, 26 Jul 2021 22:51:52 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:06:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 02:06:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 02:06:30 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 02:06:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 02:06:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jul 2021 02:08:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 02:08:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 02:08:54 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:09:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:09:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 02:10:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84f015b4bc25868153a5ad10fafccf4b87d5e230c6346262a972324d9846c3cb`  
		Last Modified: Mon, 26 Jul 2021 22:56:13 GMT  
		Size: 24.1 MB (24064238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3707933348ed35dee73fe666615c4468caff6e2006136da4acd92e3cc985216d`  
		Last Modified: Tue, 27 Jul 2021 02:25:29 GMT  
		Size: 1.2 MB (1183472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf3da2af0d31416b9fa8b8d6cdca9940f2b02f0114144b0dd45896609465550`  
		Last Modified: Tue, 27 Jul 2021 02:25:28 GMT  
		Size: 4.7 MB (4676474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894df612b4be55234c3870d52402c8e0f8d862a70d921469dabd90fce65dd19b`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b69804f2417b467f0d90f227007b6ad0784998510b3059db7781646c4d9d7b0`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5140583e1bb4ff168122d517efa0932ee6c515d4c64167423b2c65c7f945120`  
		Last Modified: Tue, 27 Jul 2021 02:27:32 GMT  
		Size: 157.2 MB (157210837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b14c8f11163b8fb56261a038b46a4424d6e04e8de12d91373885b3374fedd6`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c215fdc8101cc4022455bc40043758167955d643398391a07fb8f274a8b4b2`  
		Last Modified: Tue, 27 Jul 2021 02:28:05 GMT  
		Size: 36.7 MB (36691203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a81c5b7e4065976c7abc3018689ba1a166dbebe6f84d05c97525d8b823e4d38`  
		Last Modified: Tue, 27 Jul 2021 02:27:45 GMT  
		Size: 313.4 KB (313420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095184adef319323695c597ab15710f2f39440c2e9d62ffbd0a61ac2a230cc0c`  
		Last Modified: Tue, 27 Jul 2021 02:28:28 GMT  
		Size: 60.5 MB (60481937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9144b1da59a7cbc4746c2b6d093ac1eca8bcf8d666cac4144360a3d80b039310
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318831283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567450cbc68db666b5ef210466a9e445ae7b35344fe9ab9fbd6102a41e9b5700`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:39 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:35:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:35:49 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:35:49 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:35:49 GMT
ENV ROS_DISTRO=noetic
# Tue, 31 Aug 2021 02:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:36:38 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Aug 2021 02:36:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:36:38 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:37:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:37:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:37:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e6b11a7bb7f78e22996a184b764b32e64f3f4ef7d41dc571d55d606cc1a6ac`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aada428d5fc8dcbd529a9a5a2d09d46e75fde1b0cad9c895dfe9e81109657ee1`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca561674e29ba9be5ab00aa2dc9f3cf19a9b9c521d7e84bebdb5c285317079a`  
		Last Modified: Tue, 31 Aug 2021 02:53:09 GMT  
		Size: 171.1 MB (171148029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dee245aab371139d97caaba068958d119f132acdb5c08cec9c17f2c9db9c6ce`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785f6e4808b7908f861bce0cbf08dedf895e579a5474fd9fab133bcc56f92549`  
		Last Modified: Tue, 31 Aug 2021 02:53:29 GMT  
		Size: 41.5 MB (41520808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b50ac425df80624b0f3931e6c262c69b4b1e63d9bb4966fdb4b22e4ceb822e2`  
		Last Modified: Tue, 31 Aug 2021 02:53:21 GMT  
		Size: 317.8 KB (317842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08dccd1599a0df6b5e1eca72b82a800e27f6062c6d12cbaab8fdcf7bb3117962`  
		Last Modified: Tue, 31 Aug 2021 02:53:34 GMT  
		Size: 72.0 MB (71972726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:6c65319449487feafe7fcb424c661df116b5565566695917b667598babbbd761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:26f10371a9feb831aaab0f337e007879cf2001ab060c1de3291a28cb06ce2b3a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.2 MB (838191492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5835c71f748dc1ca333528fbad856c0d030269b829e193d158db34fd104ff52e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:48:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:48:27 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:48:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:48:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jul 2021 00:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:50:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:50:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:50:51 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:51:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:51:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 00:52:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:01:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2997acb5dc01c0a5dcc159471aea13a7b87074a11df83667b1f8b108602e7dda`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5853e486374821ccfc40d07b68affecdc12e88f4ff7e8be0d58d904d3f525d5a`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e9cabb7a6a3ae445854e8bda4e4762b3d7ab26b3191ab8a006360c8dd0689f`  
		Last Modified: Tue, 27 Jul 2021 01:14:29 GMT  
		Size: 176.7 MB (176702826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c5a6e61679ad83770b86fc37c72db8d318a69a8d5dcac2d00db8bf86b0e9fc`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b972074e1773fd5c4e1a932d55b75a2a2850d2e1ffced2c52e961b49f75d22`  
		Last Modified: Tue, 27 Jul 2021 01:14:49 GMT  
		Size: 47.3 MB (47259266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eccfe2edcc7482e1d5dc3b436b2197ed3020befcbc53e9f4f4e18c3a46497772`  
		Last Modified: Tue, 27 Jul 2021 01:14:40 GMT  
		Size: 313.4 KB (313417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c855981c165d5abfeb9c7d6a5bbfd8616a913a3674a8e23f9f4f9e6efd7fe627`  
		Last Modified: Tue, 27 Jul 2021 01:14:54 GMT  
		Size: 79.6 MB (79602950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ae84aba4fac5673ddc385e0d102d1420378f500119d4cdb9e8c2d45d1da053`  
		Last Modified: Tue, 27 Jul 2021 01:16:43 GMT  
		Size: 499.0 MB (499013140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:8c8eaf9b8c1a8021a91e252e878cc9e4dc0e827adbdc334b59859afd385789f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **727.9 MB (727868158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3d22869639ec3542d9a7c46d53c44fc952f1b9872a3e0d11d711b1a68e57a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:51 GMT
ADD file:dec1b30555f66d79050762dc2b6c8e55dc130245f3bd1af94d77f1e1e6aa3ccb in / 
# Mon, 26 Jul 2021 22:51:52 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:06:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 02:06:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 02:06:30 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 02:06:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 02:06:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jul 2021 02:08:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 02:08:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 02:08:54 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:09:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:09:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 02:10:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:16:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84f015b4bc25868153a5ad10fafccf4b87d5e230c6346262a972324d9846c3cb`  
		Last Modified: Mon, 26 Jul 2021 22:56:13 GMT  
		Size: 24.1 MB (24064238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3707933348ed35dee73fe666615c4468caff6e2006136da4acd92e3cc985216d`  
		Last Modified: Tue, 27 Jul 2021 02:25:29 GMT  
		Size: 1.2 MB (1183472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf3da2af0d31416b9fa8b8d6cdca9940f2b02f0114144b0dd45896609465550`  
		Last Modified: Tue, 27 Jul 2021 02:25:28 GMT  
		Size: 4.7 MB (4676474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894df612b4be55234c3870d52402c8e0f8d862a70d921469dabd90fce65dd19b`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b69804f2417b467f0d90f227007b6ad0784998510b3059db7781646c4d9d7b0`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5140583e1bb4ff168122d517efa0932ee6c515d4c64167423b2c65c7f945120`  
		Last Modified: Tue, 27 Jul 2021 02:27:32 GMT  
		Size: 157.2 MB (157210837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b14c8f11163b8fb56261a038b46a4424d6e04e8de12d91373885b3374fedd6`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c215fdc8101cc4022455bc40043758167955d643398391a07fb8f274a8b4b2`  
		Last Modified: Tue, 27 Jul 2021 02:28:05 GMT  
		Size: 36.7 MB (36691203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a81c5b7e4065976c7abc3018689ba1a166dbebe6f84d05c97525d8b823e4d38`  
		Last Modified: Tue, 27 Jul 2021 02:27:45 GMT  
		Size: 313.4 KB (313420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095184adef319323695c597ab15710f2f39440c2e9d62ffbd0a61ac2a230cc0c`  
		Last Modified: Tue, 27 Jul 2021 02:28:28 GMT  
		Size: 60.5 MB (60481937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853f747b06bd9dbd06fef00ef1ffeba03276c0e8b456e243008dd30e0fdc5887`  
		Last Modified: Tue, 27 Jul 2021 02:33:41 GMT  
		Size: 443.2 MB (443244162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:78cc89e14e3a8e59a88f8843fd284b27ba8c94ffc993b9b54218ec8b5d3c0173
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **790.9 MB (790931348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6860a9d9d5f78146fef318e473ef718697431dbddbfda597f4d0f30025d7f49d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:39 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:35:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:35:49 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:35:49 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:35:49 GMT
ENV ROS_DISTRO=noetic
# Tue, 31 Aug 2021 02:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:36:38 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Aug 2021 02:36:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:36:38 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:37:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:37:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:37:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:39:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e6b11a7bb7f78e22996a184b764b32e64f3f4ef7d41dc571d55d606cc1a6ac`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aada428d5fc8dcbd529a9a5a2d09d46e75fde1b0cad9c895dfe9e81109657ee1`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca561674e29ba9be5ab00aa2dc9f3cf19a9b9c521d7e84bebdb5c285317079a`  
		Last Modified: Tue, 31 Aug 2021 02:53:09 GMT  
		Size: 171.1 MB (171148029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dee245aab371139d97caaba068958d119f132acdb5c08cec9c17f2c9db9c6ce`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785f6e4808b7908f861bce0cbf08dedf895e579a5474fd9fab133bcc56f92549`  
		Last Modified: Tue, 31 Aug 2021 02:53:29 GMT  
		Size: 41.5 MB (41520808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b50ac425df80624b0f3931e6c262c69b4b1e63d9bb4966fdb4b22e4ceb822e2`  
		Last Modified: Tue, 31 Aug 2021 02:53:21 GMT  
		Size: 317.8 KB (317842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08dccd1599a0df6b5e1eca72b82a800e27f6062c6d12cbaab8fdcf7bb3117962`  
		Last Modified: Tue, 31 Aug 2021 02:53:34 GMT  
		Size: 72.0 MB (71972726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3ef8c38235c8c6ae3688876b8bcc0e9d6553d110e1210573b9b1216603b0f8`  
		Last Modified: Tue, 31 Aug 2021 02:55:21 GMT  
		Size: 472.1 MB (472100065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-buster`

```console
$ docker pull ros@sha256:52f9e9bf4654bd70cab5fa729e4736db7ab299687f885f07cf06b979b7976e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-perception-buster` - linux; amd64

```console
$ docker pull ros@sha256:08388a8f291a61bafc049a98bafc9c2ef2a7a58f3909cc90d67b98a1f7bb45b9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **968.0 MB (968013134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a3b0467f6eb0d92bf3c16db06cb5a90993e6b1ef764947e6d64b4b3079627a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:54:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:54:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 17 Aug 2021 14:54:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 17 Aug 2021 14:54:12 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 14:54:12 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Aug 2021 14:54:12 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Aug 2021 14:55:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:55:18 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 17 Aug 2021 14:55:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Aug 2021 14:55:18 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:55:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:56:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 17 Aug 2021 14:56:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 15:00:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6a25b8c075beb4891f7c9088956d2a452f32036d8126e37217b5b62fd7024c`  
		Last Modified: Tue, 17 Aug 2021 15:02:09 GMT  
		Size: 10.9 MB (10891952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e00b43ac20734a706cb03369661415e15f6856a48275dcd4fe7744b0bde5d23`  
		Last Modified: Tue, 17 Aug 2021 15:02:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b19825ce46253a4664a6e606382250ba22ec8d0e1d13516be7d225efcca57f`  
		Last Modified: Tue, 17 Aug 2021 15:02:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034eef40d3fabaea23b5d4473263a3a6ab8cd3545504c1ba16818b3b90152d1f`  
		Last Modified: Tue, 17 Aug 2021 15:02:50 GMT  
		Size: 239.1 MB (239050839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ae7d371ba1fee4f46bf91b9a18289de1dd3472eb2c3b8458f8ff2df5825c78`  
		Last Modified: Tue, 17 Aug 2021 15:02:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b4384fc4992e164b0946674e8bf7905f6037fbe56d20552b0a9f981e0b23df`  
		Last Modified: Tue, 17 Aug 2021 15:03:21 GMT  
		Size: 86.6 MB (86566411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6466d96361536da7163da2fbe6e4e5267a768c30f1f04480d818c767e0ef32`  
		Last Modified: Tue, 17 Aug 2021 15:02:59 GMT  
		Size: 310.1 KB (310086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43da0dad1381eb1948df8e9a05518d305a6b3a7df20eb1f0b82edb2a00bee76b`  
		Last Modified: Tue, 17 Aug 2021 15:03:19 GMT  
		Size: 76.0 MB (75975146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b682f5f1680f2c4ec265e9f6da30a3f02e3e8782fbb3f6ced55263d693845a`  
		Last Modified: Tue, 17 Aug 2021 15:05:05 GMT  
		Size: 504.8 MB (504780085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:80c222e67d0165628296171890545c1ce5142b993e96c8d56d5d13c08a75dc29
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **884.8 MB (884788088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9313f1dfa329f985bc41257c8c9628e684c8a7357e520918d3373f8c9232e83`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:16 GMT
ADD file:9e7d801ba29c50f7388cf80395faef75e0b4db056e16d1117293539bda895467 in / 
# Tue, 17 Aug 2021 01:46:16 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:48:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:48:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 17 Aug 2021 11:48:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 17 Aug 2021 11:48:59 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 11:48:59 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Aug 2021 11:49:00 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Aug 2021 11:49:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:49:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 17 Aug 2021 11:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Aug 2021 11:49:54 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:50:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:50:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 17 Aug 2021 11:50:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:53:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b721438f56fc7c4bf10a9f9ac58d22b52d97c50353a44f531fb5b7a70314e642`  
		Last Modified: Tue, 17 Aug 2021 01:53:52 GMT  
		Size: 49.2 MB (49222362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21602f601a18ce34c8a479ae1d7bac4442282478925664d6f67ad1d2b34e020`  
		Last Modified: Tue, 17 Aug 2021 11:56:11 GMT  
		Size: 10.9 MB (10883354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630d4e557cfdbdf3a855acc0ae4cb3c204ac63ae1dd071cd42e608dcb0645c2d`  
		Last Modified: Tue, 17 Aug 2021 11:56:09 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f24119c6422825783e8ee727d9b12a12c7cb5605e9b6e883b5101a388b450a`  
		Last Modified: Tue, 17 Aug 2021 11:56:09 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd82c4517707ac42892fd33d02b10b53c8eb41cf05683d381df617056c035fd`  
		Last Modified: Tue, 17 Aug 2021 11:56:42 GMT  
		Size: 184.2 MB (184236324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5bbd42e097110d8576baa6d6d16c7a91e608fad20f3b7978c7e0e99f4ee7df`  
		Last Modified: Tue, 17 Aug 2021 11:56:09 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf124f136abb277ab2e63f14af6802ccc288e34cc0c43a7d62f7c42717f23e3`  
		Last Modified: Tue, 17 Aug 2021 11:57:03 GMT  
		Size: 84.4 MB (84358116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6515efab5054193f9a8defd851ec9536c17950ae722b38778b4bd6aef481e9`  
		Last Modified: Tue, 17 Aug 2021 11:56:51 GMT  
		Size: 310.1 KB (310090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa915bc3d0bc2ea62806da8704257a5df824c41fa8997831b5de9ac482cca14`  
		Last Modified: Tue, 17 Aug 2021 11:57:03 GMT  
		Size: 74.1 MB (74087852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8ca443554ff1e63ad39ca3a88974d297e3128e3fa0f11c10d900b45a58daac`  
		Last Modified: Tue, 17 Aug 2021 11:58:36 GMT  
		Size: 481.7 MB (481687577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:6c65319449487feafe7fcb424c661df116b5565566695917b667598babbbd761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:26f10371a9feb831aaab0f337e007879cf2001ab060c1de3291a28cb06ce2b3a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.2 MB (838191492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5835c71f748dc1ca333528fbad856c0d030269b829e193d158db34fd104ff52e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:48:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:48:27 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:48:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:48:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jul 2021 00:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:50:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:50:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:50:51 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:51:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:51:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 00:52:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:01:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2997acb5dc01c0a5dcc159471aea13a7b87074a11df83667b1f8b108602e7dda`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5853e486374821ccfc40d07b68affecdc12e88f4ff7e8be0d58d904d3f525d5a`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e9cabb7a6a3ae445854e8bda4e4762b3d7ab26b3191ab8a006360c8dd0689f`  
		Last Modified: Tue, 27 Jul 2021 01:14:29 GMT  
		Size: 176.7 MB (176702826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c5a6e61679ad83770b86fc37c72db8d318a69a8d5dcac2d00db8bf86b0e9fc`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b972074e1773fd5c4e1a932d55b75a2a2850d2e1ffced2c52e961b49f75d22`  
		Last Modified: Tue, 27 Jul 2021 01:14:49 GMT  
		Size: 47.3 MB (47259266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eccfe2edcc7482e1d5dc3b436b2197ed3020befcbc53e9f4f4e18c3a46497772`  
		Last Modified: Tue, 27 Jul 2021 01:14:40 GMT  
		Size: 313.4 KB (313417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c855981c165d5abfeb9c7d6a5bbfd8616a913a3674a8e23f9f4f9e6efd7fe627`  
		Last Modified: Tue, 27 Jul 2021 01:14:54 GMT  
		Size: 79.6 MB (79602950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ae84aba4fac5673ddc385e0d102d1420378f500119d4cdb9e8c2d45d1da053`  
		Last Modified: Tue, 27 Jul 2021 01:16:43 GMT  
		Size: 499.0 MB (499013140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:8c8eaf9b8c1a8021a91e252e878cc9e4dc0e827adbdc334b59859afd385789f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **727.9 MB (727868158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3d22869639ec3542d9a7c46d53c44fc952f1b9872a3e0d11d711b1a68e57a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:51 GMT
ADD file:dec1b30555f66d79050762dc2b6c8e55dc130245f3bd1af94d77f1e1e6aa3ccb in / 
# Mon, 26 Jul 2021 22:51:52 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:06:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 02:06:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 02:06:30 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 02:06:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 02:06:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jul 2021 02:08:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 02:08:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 02:08:54 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:09:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:09:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 02:10:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:16:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84f015b4bc25868153a5ad10fafccf4b87d5e230c6346262a972324d9846c3cb`  
		Last Modified: Mon, 26 Jul 2021 22:56:13 GMT  
		Size: 24.1 MB (24064238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3707933348ed35dee73fe666615c4468caff6e2006136da4acd92e3cc985216d`  
		Last Modified: Tue, 27 Jul 2021 02:25:29 GMT  
		Size: 1.2 MB (1183472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf3da2af0d31416b9fa8b8d6cdca9940f2b02f0114144b0dd45896609465550`  
		Last Modified: Tue, 27 Jul 2021 02:25:28 GMT  
		Size: 4.7 MB (4676474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894df612b4be55234c3870d52402c8e0f8d862a70d921469dabd90fce65dd19b`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b69804f2417b467f0d90f227007b6ad0784998510b3059db7781646c4d9d7b0`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5140583e1bb4ff168122d517efa0932ee6c515d4c64167423b2c65c7f945120`  
		Last Modified: Tue, 27 Jul 2021 02:27:32 GMT  
		Size: 157.2 MB (157210837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b14c8f11163b8fb56261a038b46a4424d6e04e8de12d91373885b3374fedd6`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c215fdc8101cc4022455bc40043758167955d643398391a07fb8f274a8b4b2`  
		Last Modified: Tue, 27 Jul 2021 02:28:05 GMT  
		Size: 36.7 MB (36691203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a81c5b7e4065976c7abc3018689ba1a166dbebe6f84d05c97525d8b823e4d38`  
		Last Modified: Tue, 27 Jul 2021 02:27:45 GMT  
		Size: 313.4 KB (313420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095184adef319323695c597ab15710f2f39440c2e9d62ffbd0a61ac2a230cc0c`  
		Last Modified: Tue, 27 Jul 2021 02:28:28 GMT  
		Size: 60.5 MB (60481937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853f747b06bd9dbd06fef00ef1ffeba03276c0e8b456e243008dd30e0fdc5887`  
		Last Modified: Tue, 27 Jul 2021 02:33:41 GMT  
		Size: 443.2 MB (443244162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:78cc89e14e3a8e59a88f8843fd284b27ba8c94ffc993b9b54218ec8b5d3c0173
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **790.9 MB (790931348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6860a9d9d5f78146fef318e473ef718697431dbddbfda597f4d0f30025d7f49d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:39 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:35:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:35:49 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:35:49 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:35:49 GMT
ENV ROS_DISTRO=noetic
# Tue, 31 Aug 2021 02:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:36:38 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Aug 2021 02:36:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:36:38 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:37:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:37:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:37:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:39:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e6b11a7bb7f78e22996a184b764b32e64f3f4ef7d41dc571d55d606cc1a6ac`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aada428d5fc8dcbd529a9a5a2d09d46e75fde1b0cad9c895dfe9e81109657ee1`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca561674e29ba9be5ab00aa2dc9f3cf19a9b9c521d7e84bebdb5c285317079a`  
		Last Modified: Tue, 31 Aug 2021 02:53:09 GMT  
		Size: 171.1 MB (171148029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dee245aab371139d97caaba068958d119f132acdb5c08cec9c17f2c9db9c6ce`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785f6e4808b7908f861bce0cbf08dedf895e579a5474fd9fab133bcc56f92549`  
		Last Modified: Tue, 31 Aug 2021 02:53:29 GMT  
		Size: 41.5 MB (41520808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b50ac425df80624b0f3931e6c262c69b4b1e63d9bb4966fdb4b22e4ceb822e2`  
		Last Modified: Tue, 31 Aug 2021 02:53:21 GMT  
		Size: 317.8 KB (317842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08dccd1599a0df6b5e1eca72b82a800e27f6062c6d12cbaab8fdcf7bb3117962`  
		Last Modified: Tue, 31 Aug 2021 02:53:34 GMT  
		Size: 72.0 MB (71972726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3ef8c38235c8c6ae3688876b8bcc0e9d6553d110e1210573b9b1216603b0f8`  
		Last Modified: Tue, 31 Aug 2021 02:55:21 GMT  
		Size: 472.1 MB (472100065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:f6c7ddf2fcac2ce39b58db6378da71695d19a5dd0d4836d8ab0b951d08040204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:c8af0dded98fb671ba69c484aeca30af7fbbd5f9b6d22336982e2c32822e1341
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.9 MB (354915755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd21d28f34bd9d2dfe85aacd05d13ddf63490765d2557a24c8fd0ce03a8a384a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:48:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:48:27 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:48:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:48:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jul 2021 00:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:50:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:50:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:50:51 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:51:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:51:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 00:52:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:53:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2997acb5dc01c0a5dcc159471aea13a7b87074a11df83667b1f8b108602e7dda`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5853e486374821ccfc40d07b68affecdc12e88f4ff7e8be0d58d904d3f525d5a`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e9cabb7a6a3ae445854e8bda4e4762b3d7ab26b3191ab8a006360c8dd0689f`  
		Last Modified: Tue, 27 Jul 2021 01:14:29 GMT  
		Size: 176.7 MB (176702826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c5a6e61679ad83770b86fc37c72db8d318a69a8d5dcac2d00db8bf86b0e9fc`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b972074e1773fd5c4e1a932d55b75a2a2850d2e1ffced2c52e961b49f75d22`  
		Last Modified: Tue, 27 Jul 2021 01:14:49 GMT  
		Size: 47.3 MB (47259266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eccfe2edcc7482e1d5dc3b436b2197ed3020befcbc53e9f4f4e18c3a46497772`  
		Last Modified: Tue, 27 Jul 2021 01:14:40 GMT  
		Size: 313.4 KB (313417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c855981c165d5abfeb9c7d6a5bbfd8616a913a3674a8e23f9f4f9e6efd7fe627`  
		Last Modified: Tue, 27 Jul 2021 01:14:54 GMT  
		Size: 79.6 MB (79602950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caed4353fbe38855f36fb5376060099dca87d8674318e8a911b9943f6e574423`  
		Last Modified: Tue, 27 Jul 2021 01:15:12 GMT  
		Size: 15.7 MB (15737403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:9433435e54c4ccf5d734dd4be8e5492fecafb890743ad963d5ba5151c2beb583
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298584275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51362dde9245e1d744f33b498603a195f3e0cf834395a7eb3acaf9d4c003980b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:51 GMT
ADD file:dec1b30555f66d79050762dc2b6c8e55dc130245f3bd1af94d77f1e1e6aa3ccb in / 
# Mon, 26 Jul 2021 22:51:52 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:06:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 02:06:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 02:06:30 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 02:06:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 02:06:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jul 2021 02:08:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 02:08:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 02:08:54 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:09:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:09:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 02:10:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:11:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84f015b4bc25868153a5ad10fafccf4b87d5e230c6346262a972324d9846c3cb`  
		Last Modified: Mon, 26 Jul 2021 22:56:13 GMT  
		Size: 24.1 MB (24064238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3707933348ed35dee73fe666615c4468caff6e2006136da4acd92e3cc985216d`  
		Last Modified: Tue, 27 Jul 2021 02:25:29 GMT  
		Size: 1.2 MB (1183472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf3da2af0d31416b9fa8b8d6cdca9940f2b02f0114144b0dd45896609465550`  
		Last Modified: Tue, 27 Jul 2021 02:25:28 GMT  
		Size: 4.7 MB (4676474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894df612b4be55234c3870d52402c8e0f8d862a70d921469dabd90fce65dd19b`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b69804f2417b467f0d90f227007b6ad0784998510b3059db7781646c4d9d7b0`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5140583e1bb4ff168122d517efa0932ee6c515d4c64167423b2c65c7f945120`  
		Last Modified: Tue, 27 Jul 2021 02:27:32 GMT  
		Size: 157.2 MB (157210837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b14c8f11163b8fb56261a038b46a4424d6e04e8de12d91373885b3374fedd6`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c215fdc8101cc4022455bc40043758167955d643398391a07fb8f274a8b4b2`  
		Last Modified: Tue, 27 Jul 2021 02:28:05 GMT  
		Size: 36.7 MB (36691203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a81c5b7e4065976c7abc3018689ba1a166dbebe6f84d05c97525d8b823e4d38`  
		Last Modified: Tue, 27 Jul 2021 02:27:45 GMT  
		Size: 313.4 KB (313420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095184adef319323695c597ab15710f2f39440c2e9d62ffbd0a61ac2a230cc0c`  
		Last Modified: Tue, 27 Jul 2021 02:28:28 GMT  
		Size: 60.5 MB (60481937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597531626f0d53d0a21f11d7ee2c6247efdaec8f4b239b813e51d780e664e40a`  
		Last Modified: Tue, 27 Jul 2021 02:28:54 GMT  
		Size: 14.0 MB (13960279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:813c723e4931c7bc2b491ff59b754734528ac64a56206c13070ce100f80c02c7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.2 MB (334182491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556b85d27db401b75771b5630a345b9baeda4f9a57e31ec8fecfb220e8118c51`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:39 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:35:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:35:49 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:35:49 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:35:49 GMT
ENV ROS_DISTRO=noetic
# Tue, 31 Aug 2021 02:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:36:38 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Aug 2021 02:36:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:36:38 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:37:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:37:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:37:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:37:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e6b11a7bb7f78e22996a184b764b32e64f3f4ef7d41dc571d55d606cc1a6ac`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aada428d5fc8dcbd529a9a5a2d09d46e75fde1b0cad9c895dfe9e81109657ee1`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca561674e29ba9be5ab00aa2dc9f3cf19a9b9c521d7e84bebdb5c285317079a`  
		Last Modified: Tue, 31 Aug 2021 02:53:09 GMT  
		Size: 171.1 MB (171148029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dee245aab371139d97caaba068958d119f132acdb5c08cec9c17f2c9db9c6ce`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785f6e4808b7908f861bce0cbf08dedf895e579a5474fd9fab133bcc56f92549`  
		Last Modified: Tue, 31 Aug 2021 02:53:29 GMT  
		Size: 41.5 MB (41520808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b50ac425df80624b0f3931e6c262c69b4b1e63d9bb4966fdb4b22e4ceb822e2`  
		Last Modified: Tue, 31 Aug 2021 02:53:21 GMT  
		Size: 317.8 KB (317842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08dccd1599a0df6b5e1eca72b82a800e27f6062c6d12cbaab8fdcf7bb3117962`  
		Last Modified: Tue, 31 Aug 2021 02:53:34 GMT  
		Size: 72.0 MB (71972726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd467d085e57203717ff7b95b64f46886f5f7b435e84511c89031efc644aa911`  
		Last Modified: Tue, 31 Aug 2021 02:53:53 GMT  
		Size: 15.4 MB (15351208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:fd9e03a878cadcb365ccb236cd47c36dc1a19ce4105becedd4e9418dc8d1ca1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:8fc740c4c663c10544f1c6fcbe0d9ed232d15725bc41d4b4ee256a5cc193f534
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.5 MB (484451700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca0c9f7c246ad81ee27739eb65046725966c9334246e9e1571884a8cf33cdf6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:54:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:54:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 17 Aug 2021 14:54:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 17 Aug 2021 14:54:12 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 14:54:12 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Aug 2021 14:54:12 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Aug 2021 14:55:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:55:18 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 17 Aug 2021 14:55:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Aug 2021 14:55:18 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:55:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:56:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 17 Aug 2021 14:56:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6a25b8c075beb4891f7c9088956d2a452f32036d8126e37217b5b62fd7024c`  
		Last Modified: Tue, 17 Aug 2021 15:02:09 GMT  
		Size: 10.9 MB (10891952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e00b43ac20734a706cb03369661415e15f6856a48275dcd4fe7744b0bde5d23`  
		Last Modified: Tue, 17 Aug 2021 15:02:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b19825ce46253a4664a6e606382250ba22ec8d0e1d13516be7d225efcca57f`  
		Last Modified: Tue, 17 Aug 2021 15:02:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034eef40d3fabaea23b5d4473263a3a6ab8cd3545504c1ba16818b3b90152d1f`  
		Last Modified: Tue, 17 Aug 2021 15:02:50 GMT  
		Size: 239.1 MB (239050839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ae7d371ba1fee4f46bf91b9a18289de1dd3472eb2c3b8458f8ff2df5825c78`  
		Last Modified: Tue, 17 Aug 2021 15:02:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b4384fc4992e164b0946674e8bf7905f6037fbe56d20552b0a9f981e0b23df`  
		Last Modified: Tue, 17 Aug 2021 15:03:21 GMT  
		Size: 86.6 MB (86566411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6466d96361536da7163da2fbe6e4e5267a768c30f1f04480d818c767e0ef32`  
		Last Modified: Tue, 17 Aug 2021 15:02:59 GMT  
		Size: 310.1 KB (310086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43da0dad1381eb1948df8e9a05518d305a6b3a7df20eb1f0b82edb2a00bee76b`  
		Last Modified: Tue, 17 Aug 2021 15:03:19 GMT  
		Size: 76.0 MB (75975146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb420023d0d4981e7e1c712cf7670854d7160f6cd251076d6fa94d822b18cef2`  
		Last Modified: Tue, 17 Aug 2021 15:03:35 GMT  
		Size: 21.2 MB (21218651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a71321e849437464740dadf3a7d92ba33aa9cd325313096b2092348fc5582503
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.0 MB (423996486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1339d6e7c2ba9eca967117d5d0a6a8b425002eb4c8f7803111013392eb2e9f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:16 GMT
ADD file:9e7d801ba29c50f7388cf80395faef75e0b4db056e16d1117293539bda895467 in / 
# Tue, 17 Aug 2021 01:46:16 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:48:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:48:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 17 Aug 2021 11:48:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 17 Aug 2021 11:48:59 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 11:48:59 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Aug 2021 11:49:00 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Aug 2021 11:49:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:49:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 17 Aug 2021 11:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Aug 2021 11:49:54 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:50:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:50:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 17 Aug 2021 11:50:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:51:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b721438f56fc7c4bf10a9f9ac58d22b52d97c50353a44f531fb5b7a70314e642`  
		Last Modified: Tue, 17 Aug 2021 01:53:52 GMT  
		Size: 49.2 MB (49222362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21602f601a18ce34c8a479ae1d7bac4442282478925664d6f67ad1d2b34e020`  
		Last Modified: Tue, 17 Aug 2021 11:56:11 GMT  
		Size: 10.9 MB (10883354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630d4e557cfdbdf3a855acc0ae4cb3c204ac63ae1dd071cd42e608dcb0645c2d`  
		Last Modified: Tue, 17 Aug 2021 11:56:09 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f24119c6422825783e8ee727d9b12a12c7cb5605e9b6e883b5101a388b450a`  
		Last Modified: Tue, 17 Aug 2021 11:56:09 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd82c4517707ac42892fd33d02b10b53c8eb41cf05683d381df617056c035fd`  
		Last Modified: Tue, 17 Aug 2021 11:56:42 GMT  
		Size: 184.2 MB (184236324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5bbd42e097110d8576baa6d6d16c7a91e608fad20f3b7978c7e0e99f4ee7df`  
		Last Modified: Tue, 17 Aug 2021 11:56:09 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf124f136abb277ab2e63f14af6802ccc288e34cc0c43a7d62f7c42717f23e3`  
		Last Modified: Tue, 17 Aug 2021 11:57:03 GMT  
		Size: 84.4 MB (84358116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6515efab5054193f9a8defd851ec9536c17950ae722b38778b4bd6aef481e9`  
		Last Modified: Tue, 17 Aug 2021 11:56:51 GMT  
		Size: 310.1 KB (310090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa915bc3d0bc2ea62806da8704257a5df824c41fa8997831b5de9ac482cca14`  
		Last Modified: Tue, 17 Aug 2021 11:57:03 GMT  
		Size: 74.1 MB (74087852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f1b5f110e2990823b69a716c68ef7506a92319e4d3c59c1991db59244653d1`  
		Last Modified: Tue, 17 Aug 2021 11:57:14 GMT  
		Size: 20.9 MB (20895975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:f6c7ddf2fcac2ce39b58db6378da71695d19a5dd0d4836d8ab0b951d08040204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:c8af0dded98fb671ba69c484aeca30af7fbbd5f9b6d22336982e2c32822e1341
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.9 MB (354915755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd21d28f34bd9d2dfe85aacd05d13ddf63490765d2557a24c8fd0ce03a8a384a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:48:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:48:27 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:48:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:48:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jul 2021 00:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:50:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:50:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:50:51 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:51:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:51:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 00:52:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:53:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2997acb5dc01c0a5dcc159471aea13a7b87074a11df83667b1f8b108602e7dda`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5853e486374821ccfc40d07b68affecdc12e88f4ff7e8be0d58d904d3f525d5a`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e9cabb7a6a3ae445854e8bda4e4762b3d7ab26b3191ab8a006360c8dd0689f`  
		Last Modified: Tue, 27 Jul 2021 01:14:29 GMT  
		Size: 176.7 MB (176702826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c5a6e61679ad83770b86fc37c72db8d318a69a8d5dcac2d00db8bf86b0e9fc`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b972074e1773fd5c4e1a932d55b75a2a2850d2e1ffced2c52e961b49f75d22`  
		Last Modified: Tue, 27 Jul 2021 01:14:49 GMT  
		Size: 47.3 MB (47259266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eccfe2edcc7482e1d5dc3b436b2197ed3020befcbc53e9f4f4e18c3a46497772`  
		Last Modified: Tue, 27 Jul 2021 01:14:40 GMT  
		Size: 313.4 KB (313417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c855981c165d5abfeb9c7d6a5bbfd8616a913a3674a8e23f9f4f9e6efd7fe627`  
		Last Modified: Tue, 27 Jul 2021 01:14:54 GMT  
		Size: 79.6 MB (79602950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caed4353fbe38855f36fb5376060099dca87d8674318e8a911b9943f6e574423`  
		Last Modified: Tue, 27 Jul 2021 01:15:12 GMT  
		Size: 15.7 MB (15737403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:9433435e54c4ccf5d734dd4be8e5492fecafb890743ad963d5ba5151c2beb583
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298584275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51362dde9245e1d744f33b498603a195f3e0cf834395a7eb3acaf9d4c003980b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:51 GMT
ADD file:dec1b30555f66d79050762dc2b6c8e55dc130245f3bd1af94d77f1e1e6aa3ccb in / 
# Mon, 26 Jul 2021 22:51:52 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:06:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 02:06:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 02:06:30 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 02:06:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 02:06:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jul 2021 02:08:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 02:08:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 02:08:54 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:09:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:09:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 02:10:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:11:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84f015b4bc25868153a5ad10fafccf4b87d5e230c6346262a972324d9846c3cb`  
		Last Modified: Mon, 26 Jul 2021 22:56:13 GMT  
		Size: 24.1 MB (24064238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3707933348ed35dee73fe666615c4468caff6e2006136da4acd92e3cc985216d`  
		Last Modified: Tue, 27 Jul 2021 02:25:29 GMT  
		Size: 1.2 MB (1183472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf3da2af0d31416b9fa8b8d6cdca9940f2b02f0114144b0dd45896609465550`  
		Last Modified: Tue, 27 Jul 2021 02:25:28 GMT  
		Size: 4.7 MB (4676474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894df612b4be55234c3870d52402c8e0f8d862a70d921469dabd90fce65dd19b`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b69804f2417b467f0d90f227007b6ad0784998510b3059db7781646c4d9d7b0`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5140583e1bb4ff168122d517efa0932ee6c515d4c64167423b2c65c7f945120`  
		Last Modified: Tue, 27 Jul 2021 02:27:32 GMT  
		Size: 157.2 MB (157210837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b14c8f11163b8fb56261a038b46a4424d6e04e8de12d91373885b3374fedd6`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c215fdc8101cc4022455bc40043758167955d643398391a07fb8f274a8b4b2`  
		Last Modified: Tue, 27 Jul 2021 02:28:05 GMT  
		Size: 36.7 MB (36691203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a81c5b7e4065976c7abc3018689ba1a166dbebe6f84d05c97525d8b823e4d38`  
		Last Modified: Tue, 27 Jul 2021 02:27:45 GMT  
		Size: 313.4 KB (313420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095184adef319323695c597ab15710f2f39440c2e9d62ffbd0a61ac2a230cc0c`  
		Last Modified: Tue, 27 Jul 2021 02:28:28 GMT  
		Size: 60.5 MB (60481937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597531626f0d53d0a21f11d7ee2c6247efdaec8f4b239b813e51d780e664e40a`  
		Last Modified: Tue, 27 Jul 2021 02:28:54 GMT  
		Size: 14.0 MB (13960279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:813c723e4931c7bc2b491ff59b754734528ac64a56206c13070ce100f80c02c7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.2 MB (334182491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556b85d27db401b75771b5630a345b9baeda4f9a57e31ec8fecfb220e8118c51`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:39 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:35:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:35:49 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:35:49 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:35:49 GMT
ENV ROS_DISTRO=noetic
# Tue, 31 Aug 2021 02:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:36:38 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Aug 2021 02:36:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:36:38 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:37:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:37:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:37:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:37:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e6b11a7bb7f78e22996a184b764b32e64f3f4ef7d41dc571d55d606cc1a6ac`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aada428d5fc8dcbd529a9a5a2d09d46e75fde1b0cad9c895dfe9e81109657ee1`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca561674e29ba9be5ab00aa2dc9f3cf19a9b9c521d7e84bebdb5c285317079a`  
		Last Modified: Tue, 31 Aug 2021 02:53:09 GMT  
		Size: 171.1 MB (171148029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dee245aab371139d97caaba068958d119f132acdb5c08cec9c17f2c9db9c6ce`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785f6e4808b7908f861bce0cbf08dedf895e579a5474fd9fab133bcc56f92549`  
		Last Modified: Tue, 31 Aug 2021 02:53:29 GMT  
		Size: 41.5 MB (41520808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b50ac425df80624b0f3931e6c262c69b4b1e63d9bb4966fdb4b22e4ceb822e2`  
		Last Modified: Tue, 31 Aug 2021 02:53:21 GMT  
		Size: 317.8 KB (317842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08dccd1599a0df6b5e1eca72b82a800e27f6062c6d12cbaab8fdcf7bb3117962`  
		Last Modified: Tue, 31 Aug 2021 02:53:34 GMT  
		Size: 72.0 MB (71972726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd467d085e57203717ff7b95b64f46886f5f7b435e84511c89031efc644aa911`  
		Last Modified: Tue, 31 Aug 2021 02:53:53 GMT  
		Size: 15.4 MB (15351208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:5dec8c8b4eb625d344bff02477b70b08c3cdd1b593e60918d1c46d1c619a96ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:42187c1172c16383c3115f69296874cf789b49f8139799c02b4e541da27c5244
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339178352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426daddb2147136e833c0d5562c86f62a3be0b266a24c08482c3c12b919aae8b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:48:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:48:27 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:48:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:48:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jul 2021 00:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:50:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:50:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:50:51 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:51:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:51:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 00:52:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2997acb5dc01c0a5dcc159471aea13a7b87074a11df83667b1f8b108602e7dda`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5853e486374821ccfc40d07b68affecdc12e88f4ff7e8be0d58d904d3f525d5a`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e9cabb7a6a3ae445854e8bda4e4762b3d7ab26b3191ab8a006360c8dd0689f`  
		Last Modified: Tue, 27 Jul 2021 01:14:29 GMT  
		Size: 176.7 MB (176702826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c5a6e61679ad83770b86fc37c72db8d318a69a8d5dcac2d00db8bf86b0e9fc`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b972074e1773fd5c4e1a932d55b75a2a2850d2e1ffced2c52e961b49f75d22`  
		Last Modified: Tue, 27 Jul 2021 01:14:49 GMT  
		Size: 47.3 MB (47259266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eccfe2edcc7482e1d5dc3b436b2197ed3020befcbc53e9f4f4e18c3a46497772`  
		Last Modified: Tue, 27 Jul 2021 01:14:40 GMT  
		Size: 313.4 KB (313417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c855981c165d5abfeb9c7d6a5bbfd8616a913a3674a8e23f9f4f9e6efd7fe627`  
		Last Modified: Tue, 27 Jul 2021 01:14:54 GMT  
		Size: 79.6 MB (79602950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:611a526bca19877d1fbfdd8dd84b9b1c3991b9157f4910b1951704df716fa316
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284623996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7d588f8655d95e5f10227e22b94f2c5d45b6fa733577a24393b2cc9c5acfb1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:51 GMT
ADD file:dec1b30555f66d79050762dc2b6c8e55dc130245f3bd1af94d77f1e1e6aa3ccb in / 
# Mon, 26 Jul 2021 22:51:52 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:06:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 02:06:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 02:06:30 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 02:06:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 02:06:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jul 2021 02:08:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 02:08:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 02:08:54 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:09:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:09:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 02:10:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84f015b4bc25868153a5ad10fafccf4b87d5e230c6346262a972324d9846c3cb`  
		Last Modified: Mon, 26 Jul 2021 22:56:13 GMT  
		Size: 24.1 MB (24064238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3707933348ed35dee73fe666615c4468caff6e2006136da4acd92e3cc985216d`  
		Last Modified: Tue, 27 Jul 2021 02:25:29 GMT  
		Size: 1.2 MB (1183472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf3da2af0d31416b9fa8b8d6cdca9940f2b02f0114144b0dd45896609465550`  
		Last Modified: Tue, 27 Jul 2021 02:25:28 GMT  
		Size: 4.7 MB (4676474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894df612b4be55234c3870d52402c8e0f8d862a70d921469dabd90fce65dd19b`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b69804f2417b467f0d90f227007b6ad0784998510b3059db7781646c4d9d7b0`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5140583e1bb4ff168122d517efa0932ee6c515d4c64167423b2c65c7f945120`  
		Last Modified: Tue, 27 Jul 2021 02:27:32 GMT  
		Size: 157.2 MB (157210837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b14c8f11163b8fb56261a038b46a4424d6e04e8de12d91373885b3374fedd6`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c215fdc8101cc4022455bc40043758167955d643398391a07fb8f274a8b4b2`  
		Last Modified: Tue, 27 Jul 2021 02:28:05 GMT  
		Size: 36.7 MB (36691203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a81c5b7e4065976c7abc3018689ba1a166dbebe6f84d05c97525d8b823e4d38`  
		Last Modified: Tue, 27 Jul 2021 02:27:45 GMT  
		Size: 313.4 KB (313420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095184adef319323695c597ab15710f2f39440c2e9d62ffbd0a61ac2a230cc0c`  
		Last Modified: Tue, 27 Jul 2021 02:28:28 GMT  
		Size: 60.5 MB (60481937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9144b1da59a7cbc4746c2b6d093ac1eca8bcf8d666cac4144360a3d80b039310
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318831283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567450cbc68db666b5ef210466a9e445ae7b35344fe9ab9fbd6102a41e9b5700`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:39 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:35:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:35:49 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:35:49 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:35:49 GMT
ENV ROS_DISTRO=noetic
# Tue, 31 Aug 2021 02:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:36:38 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Aug 2021 02:36:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:36:38 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:37:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:37:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:37:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e6b11a7bb7f78e22996a184b764b32e64f3f4ef7d41dc571d55d606cc1a6ac`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aada428d5fc8dcbd529a9a5a2d09d46e75fde1b0cad9c895dfe9e81109657ee1`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca561674e29ba9be5ab00aa2dc9f3cf19a9b9c521d7e84bebdb5c285317079a`  
		Last Modified: Tue, 31 Aug 2021 02:53:09 GMT  
		Size: 171.1 MB (171148029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dee245aab371139d97caaba068958d119f132acdb5c08cec9c17f2c9db9c6ce`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785f6e4808b7908f861bce0cbf08dedf895e579a5474fd9fab133bcc56f92549`  
		Last Modified: Tue, 31 Aug 2021 02:53:29 GMT  
		Size: 41.5 MB (41520808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b50ac425df80624b0f3931e6c262c69b4b1e63d9bb4966fdb4b22e4ceb822e2`  
		Last Modified: Tue, 31 Aug 2021 02:53:21 GMT  
		Size: 317.8 KB (317842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08dccd1599a0df6b5e1eca72b82a800e27f6062c6d12cbaab8fdcf7bb3117962`  
		Last Modified: Tue, 31 Aug 2021 02:53:34 GMT  
		Size: 72.0 MB (71972726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:1ede5a1c4cc2e4f58e1584d4ddc67b3f557ab9a7e1c26e80416e50ba9e055910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:90d57bbd4866380ad8d03a8d9442a8c476aafaf933950a491d513e90c41442f1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.2 MB (463233049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d80fa568e8b606cab686e55d3a879a85c0de337ff0c5f9abc9987416b5c6ec4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:54:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:54:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 17 Aug 2021 14:54:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 17 Aug 2021 14:54:12 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 14:54:12 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Aug 2021 14:54:12 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Aug 2021 14:55:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:55:18 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 17 Aug 2021 14:55:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Aug 2021 14:55:18 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:55:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:56:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 17 Aug 2021 14:56:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6a25b8c075beb4891f7c9088956d2a452f32036d8126e37217b5b62fd7024c`  
		Last Modified: Tue, 17 Aug 2021 15:02:09 GMT  
		Size: 10.9 MB (10891952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e00b43ac20734a706cb03369661415e15f6856a48275dcd4fe7744b0bde5d23`  
		Last Modified: Tue, 17 Aug 2021 15:02:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b19825ce46253a4664a6e606382250ba22ec8d0e1d13516be7d225efcca57f`  
		Last Modified: Tue, 17 Aug 2021 15:02:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034eef40d3fabaea23b5d4473263a3a6ab8cd3545504c1ba16818b3b90152d1f`  
		Last Modified: Tue, 17 Aug 2021 15:02:50 GMT  
		Size: 239.1 MB (239050839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ae7d371ba1fee4f46bf91b9a18289de1dd3472eb2c3b8458f8ff2df5825c78`  
		Last Modified: Tue, 17 Aug 2021 15:02:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b4384fc4992e164b0946674e8bf7905f6037fbe56d20552b0a9f981e0b23df`  
		Last Modified: Tue, 17 Aug 2021 15:03:21 GMT  
		Size: 86.6 MB (86566411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6466d96361536da7163da2fbe6e4e5267a768c30f1f04480d818c767e0ef32`  
		Last Modified: Tue, 17 Aug 2021 15:02:59 GMT  
		Size: 310.1 KB (310086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43da0dad1381eb1948df8e9a05518d305a6b3a7df20eb1f0b82edb2a00bee76b`  
		Last Modified: Tue, 17 Aug 2021 15:03:19 GMT  
		Size: 76.0 MB (75975146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a082ab94d8f9a2d34787226bfb46ba3cfb97bb8f6ce73f6d7fe1b49f34da4f20
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.1 MB (403100511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24888980eb73078603a8d2bf0a573fd83f79dcfa00bd30e7dc6acb44a44897c5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:16 GMT
ADD file:9e7d801ba29c50f7388cf80395faef75e0b4db056e16d1117293539bda895467 in / 
# Tue, 17 Aug 2021 01:46:16 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:48:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:48:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 17 Aug 2021 11:48:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 17 Aug 2021 11:48:59 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 11:48:59 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Aug 2021 11:49:00 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Aug 2021 11:49:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:49:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 17 Aug 2021 11:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Aug 2021 11:49:54 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:50:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:50:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 17 Aug 2021 11:50:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b721438f56fc7c4bf10a9f9ac58d22b52d97c50353a44f531fb5b7a70314e642`  
		Last Modified: Tue, 17 Aug 2021 01:53:52 GMT  
		Size: 49.2 MB (49222362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21602f601a18ce34c8a479ae1d7bac4442282478925664d6f67ad1d2b34e020`  
		Last Modified: Tue, 17 Aug 2021 11:56:11 GMT  
		Size: 10.9 MB (10883354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630d4e557cfdbdf3a855acc0ae4cb3c204ac63ae1dd071cd42e608dcb0645c2d`  
		Last Modified: Tue, 17 Aug 2021 11:56:09 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f24119c6422825783e8ee727d9b12a12c7cb5605e9b6e883b5101a388b450a`  
		Last Modified: Tue, 17 Aug 2021 11:56:09 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd82c4517707ac42892fd33d02b10b53c8eb41cf05683d381df617056c035fd`  
		Last Modified: Tue, 17 Aug 2021 11:56:42 GMT  
		Size: 184.2 MB (184236324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5bbd42e097110d8576baa6d6d16c7a91e608fad20f3b7978c7e0e99f4ee7df`  
		Last Modified: Tue, 17 Aug 2021 11:56:09 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf124f136abb277ab2e63f14af6802ccc288e34cc0c43a7d62f7c42717f23e3`  
		Last Modified: Tue, 17 Aug 2021 11:57:03 GMT  
		Size: 84.4 MB (84358116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6515efab5054193f9a8defd851ec9536c17950ae722b38778b4bd6aef481e9`  
		Last Modified: Tue, 17 Aug 2021 11:56:51 GMT  
		Size: 310.1 KB (310090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa915bc3d0bc2ea62806da8704257a5df824c41fa8997831b5de9ac482cca14`  
		Last Modified: Tue, 17 Aug 2021 11:57:03 GMT  
		Size: 74.1 MB (74087852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:5dec8c8b4eb625d344bff02477b70b08c3cdd1b593e60918d1c46d1c619a96ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:42187c1172c16383c3115f69296874cf789b49f8139799c02b4e541da27c5244
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339178352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426daddb2147136e833c0d5562c86f62a3be0b266a24c08482c3c12b919aae8b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:48:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:48:27 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:48:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:48:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jul 2021 00:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:50:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:50:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:50:51 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:51:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:51:14 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 00:52:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2997acb5dc01c0a5dcc159471aea13a7b87074a11df83667b1f8b108602e7dda`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5853e486374821ccfc40d07b68affecdc12e88f4ff7e8be0d58d904d3f525d5a`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e9cabb7a6a3ae445854e8bda4e4762b3d7ab26b3191ab8a006360c8dd0689f`  
		Last Modified: Tue, 27 Jul 2021 01:14:29 GMT  
		Size: 176.7 MB (176702826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c5a6e61679ad83770b86fc37c72db8d318a69a8d5dcac2d00db8bf86b0e9fc`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b972074e1773fd5c4e1a932d55b75a2a2850d2e1ffced2c52e961b49f75d22`  
		Last Modified: Tue, 27 Jul 2021 01:14:49 GMT  
		Size: 47.3 MB (47259266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eccfe2edcc7482e1d5dc3b436b2197ed3020befcbc53e9f4f4e18c3a46497772`  
		Last Modified: Tue, 27 Jul 2021 01:14:40 GMT  
		Size: 313.4 KB (313417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c855981c165d5abfeb9c7d6a5bbfd8616a913a3674a8e23f9f4f9e6efd7fe627`  
		Last Modified: Tue, 27 Jul 2021 01:14:54 GMT  
		Size: 79.6 MB (79602950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:611a526bca19877d1fbfdd8dd84b9b1c3991b9157f4910b1951704df716fa316
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284623996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7d588f8655d95e5f10227e22b94f2c5d45b6fa733577a24393b2cc9c5acfb1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:51 GMT
ADD file:dec1b30555f66d79050762dc2b6c8e55dc130245f3bd1af94d77f1e1e6aa3ccb in / 
# Mon, 26 Jul 2021 22:51:52 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:06:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 02:06:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 02:06:30 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 02:06:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 02:06:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jul 2021 02:08:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 02:08:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 02:08:54 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:09:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:09:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 02:10:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84f015b4bc25868153a5ad10fafccf4b87d5e230c6346262a972324d9846c3cb`  
		Last Modified: Mon, 26 Jul 2021 22:56:13 GMT  
		Size: 24.1 MB (24064238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3707933348ed35dee73fe666615c4468caff6e2006136da4acd92e3cc985216d`  
		Last Modified: Tue, 27 Jul 2021 02:25:29 GMT  
		Size: 1.2 MB (1183472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf3da2af0d31416b9fa8b8d6cdca9940f2b02f0114144b0dd45896609465550`  
		Last Modified: Tue, 27 Jul 2021 02:25:28 GMT  
		Size: 4.7 MB (4676474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894df612b4be55234c3870d52402c8e0f8d862a70d921469dabd90fce65dd19b`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b69804f2417b467f0d90f227007b6ad0784998510b3059db7781646c4d9d7b0`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5140583e1bb4ff168122d517efa0932ee6c515d4c64167423b2c65c7f945120`  
		Last Modified: Tue, 27 Jul 2021 02:27:32 GMT  
		Size: 157.2 MB (157210837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b14c8f11163b8fb56261a038b46a4424d6e04e8de12d91373885b3374fedd6`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c215fdc8101cc4022455bc40043758167955d643398391a07fb8f274a8b4b2`  
		Last Modified: Tue, 27 Jul 2021 02:28:05 GMT  
		Size: 36.7 MB (36691203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a81c5b7e4065976c7abc3018689ba1a166dbebe6f84d05c97525d8b823e4d38`  
		Last Modified: Tue, 27 Jul 2021 02:27:45 GMT  
		Size: 313.4 KB (313420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095184adef319323695c597ab15710f2f39440c2e9d62ffbd0a61ac2a230cc0c`  
		Last Modified: Tue, 27 Jul 2021 02:28:28 GMT  
		Size: 60.5 MB (60481937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9144b1da59a7cbc4746c2b6d093ac1eca8bcf8d666cac4144360a3d80b039310
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318831283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567450cbc68db666b5ef210466a9e445ae7b35344fe9ab9fbd6102a41e9b5700`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:39 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:35:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:35:49 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:35:49 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:35:49 GMT
ENV ROS_DISTRO=noetic
# Tue, 31 Aug 2021 02:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:36:38 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Aug 2021 02:36:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:36:38 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:37:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:37:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:37:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e6b11a7bb7f78e22996a184b764b32e64f3f4ef7d41dc571d55d606cc1a6ac`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aada428d5fc8dcbd529a9a5a2d09d46e75fde1b0cad9c895dfe9e81109657ee1`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca561674e29ba9be5ab00aa2dc9f3cf19a9b9c521d7e84bebdb5c285317079a`  
		Last Modified: Tue, 31 Aug 2021 02:53:09 GMT  
		Size: 171.1 MB (171148029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dee245aab371139d97caaba068958d119f132acdb5c08cec9c17f2c9db9c6ce`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785f6e4808b7908f861bce0cbf08dedf895e579a5474fd9fab133bcc56f92549`  
		Last Modified: Tue, 31 Aug 2021 02:53:29 GMT  
		Size: 41.5 MB (41520808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b50ac425df80624b0f3931e6c262c69b4b1e63d9bb4966fdb4b22e4ceb822e2`  
		Last Modified: Tue, 31 Aug 2021 02:53:21 GMT  
		Size: 317.8 KB (317842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08dccd1599a0df6b5e1eca72b82a800e27f6062c6d12cbaab8fdcf7bb3117962`  
		Last Modified: Tue, 31 Aug 2021 02:53:34 GMT  
		Size: 72.0 MB (71972726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:a55fe4f80d2d640ba5076f4ebefa7261a03cee81b56a6dbe23b4ee917c441e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:518d9f49f3956bf92607be0c47a8dbf00d0c567dbb919c607b611e3bcf8c8912
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212002719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b1740831ef859270de7fd9091d58dda92142f7d3f71df422fb26d0376da185`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:48:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:48:27 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:48:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:48:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jul 2021 00:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:50:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:50:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:50:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2997acb5dc01c0a5dcc159471aea13a7b87074a11df83667b1f8b108602e7dda`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5853e486374821ccfc40d07b68affecdc12e88f4ff7e8be0d58d904d3f525d5a`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e9cabb7a6a3ae445854e8bda4e4762b3d7ab26b3191ab8a006360c8dd0689f`  
		Last Modified: Tue, 27 Jul 2021 01:14:29 GMT  
		Size: 176.7 MB (176702826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c5a6e61679ad83770b86fc37c72db8d318a69a8d5dcac2d00db8bf86b0e9fc`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:45f08fb5b042970e1b561d9b3940fdabc46b34958678536c54a07e17c3a253cf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187137436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a223e481044d9ab0a67a6bad021ae42bd8957c52c4a9357dd2632e569d1594c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:51 GMT
ADD file:dec1b30555f66d79050762dc2b6c8e55dc130245f3bd1af94d77f1e1e6aa3ccb in / 
# Mon, 26 Jul 2021 22:51:52 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:06:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 02:06:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 02:06:30 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 02:06:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 02:06:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jul 2021 02:08:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 02:08:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 02:08:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:84f015b4bc25868153a5ad10fafccf4b87d5e230c6346262a972324d9846c3cb`  
		Last Modified: Mon, 26 Jul 2021 22:56:13 GMT  
		Size: 24.1 MB (24064238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3707933348ed35dee73fe666615c4468caff6e2006136da4acd92e3cc985216d`  
		Last Modified: Tue, 27 Jul 2021 02:25:29 GMT  
		Size: 1.2 MB (1183472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf3da2af0d31416b9fa8b8d6cdca9940f2b02f0114144b0dd45896609465550`  
		Last Modified: Tue, 27 Jul 2021 02:25:28 GMT  
		Size: 4.7 MB (4676474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894df612b4be55234c3870d52402c8e0f8d862a70d921469dabd90fce65dd19b`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b69804f2417b467f0d90f227007b6ad0784998510b3059db7781646c4d9d7b0`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5140583e1bb4ff168122d517efa0932ee6c515d4c64167423b2c65c7f945120`  
		Last Modified: Tue, 27 Jul 2021 02:27:32 GMT  
		Size: 157.2 MB (157210837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b14c8f11163b8fb56261a038b46a4424d6e04e8de12d91373885b3374fedd6`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0850657732dfecab0ff6a2487789883727010fd14e57aab8feba116caffa3f0c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (205019907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2fa84d33513e91015a1e0d0c9234245e7312f5a4a3414516fed5a343fda6c0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:39 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:35:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:35:49 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:35:49 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:35:49 GMT
ENV ROS_DISTRO=noetic
# Tue, 31 Aug 2021 02:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:36:38 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Aug 2021 02:36:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:36:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e6b11a7bb7f78e22996a184b764b32e64f3f4ef7d41dc571d55d606cc1a6ac`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aada428d5fc8dcbd529a9a5a2d09d46e75fde1b0cad9c895dfe9e81109657ee1`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca561674e29ba9be5ab00aa2dc9f3cf19a9b9c521d7e84bebdb5c285317079a`  
		Last Modified: Tue, 31 Aug 2021 02:53:09 GMT  
		Size: 171.1 MB (171148029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dee245aab371139d97caaba068958d119f132acdb5c08cec9c17f2c9db9c6ce`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:6e3a5b219f3a4a0e75256ba574886e178d4a9b35b4247877e3732193f2cf56a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:01366ef13d56050834f595349bc90ab8ae4359b56eedba140cfcb80ef2a36263
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300381406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303e70ddcefe851421ed225be4fec71d1d962061c0b5bb14d1228dd5544eca97`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:52 GMT
ADD file:b9e6354f7b545096b6cb6072a50de0dffa2232f22d1972a4679f46a7e6394cae in / 
# Tue, 17 Aug 2021 01:23:53 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 14:54:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:54:08 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 17 Aug 2021 14:54:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 17 Aug 2021 14:54:12 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 14:54:12 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Aug 2021 14:54:12 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Aug 2021 14:55:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 14:55:18 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 17 Aug 2021 14:55:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Aug 2021 14:55:18 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1cfaf5c6f756207bc4607d40ddd440bd2bfa7ab455b2c3015ccf56d85cd1377b`  
		Last Modified: Tue, 17 Aug 2021 01:29:55 GMT  
		Size: 50.4 MB (50436201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6a25b8c075beb4891f7c9088956d2a452f32036d8126e37217b5b62fd7024c`  
		Last Modified: Tue, 17 Aug 2021 15:02:09 GMT  
		Size: 10.9 MB (10891952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e00b43ac20734a706cb03369661415e15f6856a48275dcd4fe7744b0bde5d23`  
		Last Modified: Tue, 17 Aug 2021 15:02:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b19825ce46253a4664a6e606382250ba22ec8d0e1d13516be7d225efcca57f`  
		Last Modified: Tue, 17 Aug 2021 15:02:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034eef40d3fabaea23b5d4473263a3a6ab8cd3545504c1ba16818b3b90152d1f`  
		Last Modified: Tue, 17 Aug 2021 15:02:50 GMT  
		Size: 239.1 MB (239050839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ae7d371ba1fee4f46bf91b9a18289de1dd3472eb2c3b8458f8ff2df5825c78`  
		Last Modified: Tue, 17 Aug 2021 15:02:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fea064eda565638082f2e8760091f3fda497b0dd13579bbf933c410c8cf59381
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244344453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d1c6cce066e55bcf52b0af531c51e0602c93303ea9c98a7c580faaca63978f3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:16 GMT
ADD file:9e7d801ba29c50f7388cf80395faef75e0b4db056e16d1117293539bda895467 in / 
# Tue, 17 Aug 2021 01:46:16 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:48:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:48:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 17 Aug 2021 11:48:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 17 Aug 2021 11:48:59 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 11:48:59 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Aug 2021 11:49:00 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Aug 2021 11:49:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:49:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 17 Aug 2021 11:49:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Aug 2021 11:49:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b721438f56fc7c4bf10a9f9ac58d22b52d97c50353a44f531fb5b7a70314e642`  
		Last Modified: Tue, 17 Aug 2021 01:53:52 GMT  
		Size: 49.2 MB (49222362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21602f601a18ce34c8a479ae1d7bac4442282478925664d6f67ad1d2b34e020`  
		Last Modified: Tue, 17 Aug 2021 11:56:11 GMT  
		Size: 10.9 MB (10883354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630d4e557cfdbdf3a855acc0ae4cb3c204ac63ae1dd071cd42e608dcb0645c2d`  
		Last Modified: Tue, 17 Aug 2021 11:56:09 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f24119c6422825783e8ee727d9b12a12c7cb5605e9b6e883b5101a388b450a`  
		Last Modified: Tue, 17 Aug 2021 11:56:09 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd82c4517707ac42892fd33d02b10b53c8eb41cf05683d381df617056c035fd`  
		Last Modified: Tue, 17 Aug 2021 11:56:42 GMT  
		Size: 184.2 MB (184236324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5bbd42e097110d8576baa6d6d16c7a91e608fad20f3b7978c7e0e99f4ee7df`  
		Last Modified: Tue, 17 Aug 2021 11:56:09 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:a55fe4f80d2d640ba5076f4ebefa7261a03cee81b56a6dbe23b4ee917c441e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:518d9f49f3956bf92607be0c47a8dbf00d0c567dbb919c607b611e3bcf8c8912
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212002719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b1740831ef859270de7fd9091d58dda92142f7d3f71df422fb26d0376da185`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 00:48:27 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 00:48:27 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 00:48:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 00:48:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jul 2021 00:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:50:51 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 00:50:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 00:50:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2997acb5dc01c0a5dcc159471aea13a7b87074a11df83667b1f8b108602e7dda`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5853e486374821ccfc40d07b68affecdc12e88f4ff7e8be0d58d904d3f525d5a`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e9cabb7a6a3ae445854e8bda4e4762b3d7ab26b3191ab8a006360c8dd0689f`  
		Last Modified: Tue, 27 Jul 2021 01:14:29 GMT  
		Size: 176.7 MB (176702826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c5a6e61679ad83770b86fc37c72db8d318a69a8d5dcac2d00db8bf86b0e9fc`  
		Last Modified: Tue, 27 Jul 2021 01:13:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:45f08fb5b042970e1b561d9b3940fdabc46b34958678536c54a07e17c3a253cf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187137436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a223e481044d9ab0a67a6bad021ae42bd8957c52c4a9357dd2632e569d1594c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 22:51:51 GMT
ADD file:dec1b30555f66d79050762dc2b6c8e55dc130245f3bd1af94d77f1e1e6aa3ccb in / 
# Mon, 26 Jul 2021 22:51:52 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:06:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 02:06:29 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 02:06:30 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 02:06:30 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 02:06:31 GMT
ENV ROS_DISTRO=noetic
# Tue, 27 Jul 2021 02:08:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:53 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 27 Jul 2021 02:08:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 02:08:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:84f015b4bc25868153a5ad10fafccf4b87d5e230c6346262a972324d9846c3cb`  
		Last Modified: Mon, 26 Jul 2021 22:56:13 GMT  
		Size: 24.1 MB (24064238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3707933348ed35dee73fe666615c4468caff6e2006136da4acd92e3cc985216d`  
		Last Modified: Tue, 27 Jul 2021 02:25:29 GMT  
		Size: 1.2 MB (1183472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf3da2af0d31416b9fa8b8d6cdca9940f2b02f0114144b0dd45896609465550`  
		Last Modified: Tue, 27 Jul 2021 02:25:28 GMT  
		Size: 4.7 MB (4676474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894df612b4be55234c3870d52402c8e0f8d862a70d921469dabd90fce65dd19b`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b69804f2417b467f0d90f227007b6ad0784998510b3059db7781646c4d9d7b0`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5140583e1bb4ff168122d517efa0932ee6c515d4c64167423b2c65c7f945120`  
		Last Modified: Tue, 27 Jul 2021 02:27:32 GMT  
		Size: 157.2 MB (157210837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b14c8f11163b8fb56261a038b46a4424d6e04e8de12d91373885b3374fedd6`  
		Last Modified: Tue, 27 Jul 2021 02:25:26 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0850657732dfecab0ff6a2487789883727010fd14e57aab8feba116caffa3f0c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (205019907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2fa84d33513e91015a1e0d0c9234245e7312f5a4a3414516fed5a343fda6c0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:39 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:35:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:35:49 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:35:49 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:35:49 GMT
ENV ROS_DISTRO=noetic
# Tue, 31 Aug 2021 02:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:36:38 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Tue, 31 Aug 2021 02:36:38 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:36:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e6b11a7bb7f78e22996a184b764b32e64f3f4ef7d41dc571d55d606cc1a6ac`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aada428d5fc8dcbd529a9a5a2d09d46e75fde1b0cad9c895dfe9e81109657ee1`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca561674e29ba9be5ab00aa2dc9f3cf19a9b9c521d7e84bebdb5c285317079a`  
		Last Modified: Tue, 31 Aug 2021 02:53:09 GMT  
		Size: 171.1 MB (171148029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dee245aab371139d97caaba068958d119f132acdb5c08cec9c17f2c9db9c6ce`  
		Last Modified: Tue, 31 Aug 2021 02:52:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling`

```console
$ docker pull ros@sha256:e3f5b74ecccd504f8d69c9fa31a6fc9c2a8a1cadcb3809d07ff3995b46846e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:343d66d45a2db6917dcf8f2e9e0ecbb0dff0ebe4a10500330d92bd0199c6a8bc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232538721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31047f12e16b5886c3a18ae5a9c86ecb487730e1f4d402d208ec8ba461027409`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:07:55 GMT
ENV ROS_DISTRO=rolling
# Tue, 27 Jul 2021 01:08:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:08:39 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:08:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:08:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:09:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:09:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 01:09:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 27 Jul 2021 01:09:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8928ebb6fc76f821cd15ef57553baa7177425b57b45dca1dc55d1fa7ac567a99`  
		Last Modified: Tue, 27 Jul 2021 01:20:05 GMT  
		Size: 104.0 MB (104037402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87230aa31aac601bd98ed495d1da57881931ef6ba2fd088208ff7edcc11a6645`  
		Last Modified: Tue, 27 Jul 2021 01:19:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ecfae6e660eea869e3a4f0b50e02e1f4d59061ecd4f0183ae66f147a79b142`  
		Last Modified: Tue, 27 Jul 2021 01:20:31 GMT  
		Size: 70.8 MB (70796958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9dc0d5adb890f7b8a3773d5280d5a49fc76acb26a178acc8625286d67ffb48`  
		Last Modified: Tue, 27 Jul 2021 01:20:21 GMT  
		Size: 239.9 KB (239910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72269352c197138327479f8993a3f63c4d1e1f551153f8892c4b0e0655b7cda`  
		Last Modified: Tue, 27 Jul 2021 01:20:20 GMT  
		Size: 2.0 KB (2029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164c9e6f758bbce1c98b1b54d6df1e86f651ececc09089ad70ff299c3251599b`  
		Last Modified: Tue, 27 Jul 2021 01:20:24 GMT  
		Size: 22.2 MB (22162528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:068d654eb81e37f10f8b7d2652a176acb72aa68be74703ba8aafd790601b4af2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.3 MB (221316964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02d60688898aa225f7ab6565faaf26af8515852e06e50b584ae6ba7a2a6283c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:45:28 GMT
ENV ROS_DISTRO=rolling
# Tue, 31 Aug 2021 02:46:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:09 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:46:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:46:09 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:46:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:46:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 31 Aug 2021 02:47:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b5c1e17fbe503ccf8bebc08da06f5478b90f03326ea7cc016d9e73507f10ce`  
		Last Modified: Tue, 31 Aug 2021 02:58:52 GMT  
		Size: 100.5 MB (100535790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45400d8e0bf75fe9e077d037d3f7b0e895432f5540ae74445ce40f4b797111a7`  
		Last Modified: Tue, 31 Aug 2021 02:58:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1497a728946ec991c8b236b4101cde77517a464c2b22ebc0c2853c613f8edc`  
		Last Modified: Tue, 31 Aug 2021 02:59:15 GMT  
		Size: 65.1 MB (65137816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cb14f8cc4408bc999a0012920c6670355132f9cd04cfa6f3632da05868c24b`  
		Last Modified: Tue, 31 Aug 2021 02:59:04 GMT  
		Size: 243.4 KB (243377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a36f33083ce43a2fe6e2a6de6c0ef97f01bfded87f9bb0c50615c85cb4e312`  
		Last Modified: Tue, 31 Aug 2021 02:59:04 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177b7dcdd13b2c3e4ae37d2c849c4d4f5288ac23426c57d481e802f7cc6d6d96`  
		Last Modified: Tue, 31 Aug 2021 02:59:07 GMT  
		Size: 21.5 MB (21526088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:e3f5b74ecccd504f8d69c9fa31a6fc9c2a8a1cadcb3809d07ff3995b46846e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:343d66d45a2db6917dcf8f2e9e0ecbb0dff0ebe4a10500330d92bd0199c6a8bc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232538721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31047f12e16b5886c3a18ae5a9c86ecb487730e1f4d402d208ec8ba461027409`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:07:55 GMT
ENV ROS_DISTRO=rolling
# Tue, 27 Jul 2021 01:08:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:08:39 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:08:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:08:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:09:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:09:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 01:09:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 27 Jul 2021 01:09:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8928ebb6fc76f821cd15ef57553baa7177425b57b45dca1dc55d1fa7ac567a99`  
		Last Modified: Tue, 27 Jul 2021 01:20:05 GMT  
		Size: 104.0 MB (104037402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87230aa31aac601bd98ed495d1da57881931ef6ba2fd088208ff7edcc11a6645`  
		Last Modified: Tue, 27 Jul 2021 01:19:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ecfae6e660eea869e3a4f0b50e02e1f4d59061ecd4f0183ae66f147a79b142`  
		Last Modified: Tue, 27 Jul 2021 01:20:31 GMT  
		Size: 70.8 MB (70796958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9dc0d5adb890f7b8a3773d5280d5a49fc76acb26a178acc8625286d67ffb48`  
		Last Modified: Tue, 27 Jul 2021 01:20:21 GMT  
		Size: 239.9 KB (239910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72269352c197138327479f8993a3f63c4d1e1f551153f8892c4b0e0655b7cda`  
		Last Modified: Tue, 27 Jul 2021 01:20:20 GMT  
		Size: 2.0 KB (2029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164c9e6f758bbce1c98b1b54d6df1e86f651ececc09089ad70ff299c3251599b`  
		Last Modified: Tue, 27 Jul 2021 01:20:24 GMT  
		Size: 22.2 MB (22162528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:068d654eb81e37f10f8b7d2652a176acb72aa68be74703ba8aafd790601b4af2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.3 MB (221316964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02d60688898aa225f7ab6565faaf26af8515852e06e50b584ae6ba7a2a6283c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:45:28 GMT
ENV ROS_DISTRO=rolling
# Tue, 31 Aug 2021 02:46:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:09 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:46:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:46:09 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:46:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:46:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 31 Aug 2021 02:47:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b5c1e17fbe503ccf8bebc08da06f5478b90f03326ea7cc016d9e73507f10ce`  
		Last Modified: Tue, 31 Aug 2021 02:58:52 GMT  
		Size: 100.5 MB (100535790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45400d8e0bf75fe9e077d037d3f7b0e895432f5540ae74445ce40f4b797111a7`  
		Last Modified: Tue, 31 Aug 2021 02:58:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1497a728946ec991c8b236b4101cde77517a464c2b22ebc0c2853c613f8edc`  
		Last Modified: Tue, 31 Aug 2021 02:59:15 GMT  
		Size: 65.1 MB (65137816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cb14f8cc4408bc999a0012920c6670355132f9cd04cfa6f3632da05868c24b`  
		Last Modified: Tue, 31 Aug 2021 02:59:04 GMT  
		Size: 243.4 KB (243377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a36f33083ce43a2fe6e2a6de6c0ef97f01bfded87f9bb0c50615c85cb4e312`  
		Last Modified: Tue, 31 Aug 2021 02:59:04 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177b7dcdd13b2c3e4ae37d2c849c4d4f5288ac23426c57d481e802f7cc6d6d96`  
		Last Modified: Tue, 31 Aug 2021 02:59:07 GMT  
		Size: 21.5 MB (21526088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base-focal`

```console
$ docker pull ros@sha256:e3f5b74ecccd504f8d69c9fa31a6fc9c2a8a1cadcb3809d07ff3995b46846e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:343d66d45a2db6917dcf8f2e9e0ecbb0dff0ebe4a10500330d92bd0199c6a8bc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232538721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31047f12e16b5886c3a18ae5a9c86ecb487730e1f4d402d208ec8ba461027409`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:07:55 GMT
ENV ROS_DISTRO=rolling
# Tue, 27 Jul 2021 01:08:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:08:39 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:08:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:08:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:09:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:09:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 01:09:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 27 Jul 2021 01:09:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8928ebb6fc76f821cd15ef57553baa7177425b57b45dca1dc55d1fa7ac567a99`  
		Last Modified: Tue, 27 Jul 2021 01:20:05 GMT  
		Size: 104.0 MB (104037402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87230aa31aac601bd98ed495d1da57881931ef6ba2fd088208ff7edcc11a6645`  
		Last Modified: Tue, 27 Jul 2021 01:19:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ecfae6e660eea869e3a4f0b50e02e1f4d59061ecd4f0183ae66f147a79b142`  
		Last Modified: Tue, 27 Jul 2021 01:20:31 GMT  
		Size: 70.8 MB (70796958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9dc0d5adb890f7b8a3773d5280d5a49fc76acb26a178acc8625286d67ffb48`  
		Last Modified: Tue, 27 Jul 2021 01:20:21 GMT  
		Size: 239.9 KB (239910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72269352c197138327479f8993a3f63c4d1e1f551153f8892c4b0e0655b7cda`  
		Last Modified: Tue, 27 Jul 2021 01:20:20 GMT  
		Size: 2.0 KB (2029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164c9e6f758bbce1c98b1b54d6df1e86f651ececc09089ad70ff299c3251599b`  
		Last Modified: Tue, 27 Jul 2021 01:20:24 GMT  
		Size: 22.2 MB (22162528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:068d654eb81e37f10f8b7d2652a176acb72aa68be74703ba8aafd790601b4af2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.3 MB (221316964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02d60688898aa225f7ab6565faaf26af8515852e06e50b584ae6ba7a2a6283c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:45:28 GMT
ENV ROS_DISTRO=rolling
# Tue, 31 Aug 2021 02:46:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:09 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:46:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:46:09 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:46:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:46:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 31 Aug 2021 02:47:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b5c1e17fbe503ccf8bebc08da06f5478b90f03326ea7cc016d9e73507f10ce`  
		Last Modified: Tue, 31 Aug 2021 02:58:52 GMT  
		Size: 100.5 MB (100535790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45400d8e0bf75fe9e077d037d3f7b0e895432f5540ae74445ce40f4b797111a7`  
		Last Modified: Tue, 31 Aug 2021 02:58:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1497a728946ec991c8b236b4101cde77517a464c2b22ebc0c2853c613f8edc`  
		Last Modified: Tue, 31 Aug 2021 02:59:15 GMT  
		Size: 65.1 MB (65137816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cb14f8cc4408bc999a0012920c6670355132f9cd04cfa6f3632da05868c24b`  
		Last Modified: Tue, 31 Aug 2021 02:59:04 GMT  
		Size: 243.4 KB (243377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a36f33083ce43a2fe6e2a6de6c0ef97f01bfded87f9bb0c50615c85cb4e312`  
		Last Modified: Tue, 31 Aug 2021 02:59:04 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177b7dcdd13b2c3e4ae37d2c849c4d4f5288ac23426c57d481e802f7cc6d6d96`  
		Last Modified: Tue, 31 Aug 2021 02:59:07 GMT  
		Size: 21.5 MB (21526088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:3718d3843639a4a9ae35af5e855914009f63bd24dbc98792df9a837186caabcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:c2f8c1fbe1b3dc3d98c532d7797036db90c409e648e473cc21cfba41bb97c834
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139337296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddaef19d5f6bebf29770911fea7c2a2377a782d34649acf780095cc1ce3b1f9c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:07:55 GMT
ENV ROS_DISTRO=rolling
# Tue, 27 Jul 2021 01:08:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:08:39 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:08:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:08:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8928ebb6fc76f821cd15ef57553baa7177425b57b45dca1dc55d1fa7ac567a99`  
		Last Modified: Tue, 27 Jul 2021 01:20:05 GMT  
		Size: 104.0 MB (104037402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87230aa31aac601bd98ed495d1da57881931ef6ba2fd088208ff7edcc11a6645`  
		Last Modified: Tue, 27 Jul 2021 01:19:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a5eab13bc07244a3f6f9423bad6a6fca3edc2f1e702d1dd3e7b29fd2056f77dd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134407670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8987ce0ec633d4f9d1f08bd4f31f12ffe62f8d01d0837f087b17e0a37b8d9b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:45:28 GMT
ENV ROS_DISTRO=rolling
# Tue, 31 Aug 2021 02:46:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:09 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:46:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:46:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b5c1e17fbe503ccf8bebc08da06f5478b90f03326ea7cc016d9e73507f10ce`  
		Last Modified: Tue, 31 Aug 2021 02:58:52 GMT  
		Size: 100.5 MB (100535790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45400d8e0bf75fe9e077d037d3f7b0e895432f5540ae74445ce40f4b797111a7`  
		Last Modified: Tue, 31 Aug 2021 02:58:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core-focal`

```console
$ docker pull ros@sha256:3718d3843639a4a9ae35af5e855914009f63bd24dbc98792df9a837186caabcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:c2f8c1fbe1b3dc3d98c532d7797036db90c409e648e473cc21cfba41bb97c834
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139337296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddaef19d5f6bebf29770911fea7c2a2377a782d34649acf780095cc1ce3b1f9c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:07:55 GMT
ENV ROS_DISTRO=rolling
# Tue, 27 Jul 2021 01:08:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:08:39 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:08:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:08:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8928ebb6fc76f821cd15ef57553baa7177425b57b45dca1dc55d1fa7ac567a99`  
		Last Modified: Tue, 27 Jul 2021 01:20:05 GMT  
		Size: 104.0 MB (104037402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87230aa31aac601bd98ed495d1da57881931ef6ba2fd088208ff7edcc11a6645`  
		Last Modified: Tue, 27 Jul 2021 01:19:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a5eab13bc07244a3f6f9423bad6a6fca3edc2f1e702d1dd3e7b29fd2056f77dd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134407670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8987ce0ec633d4f9d1f08bd4f31f12ffe62f8d01d0837f087b17e0a37b8d9b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:45:28 GMT
ENV ROS_DISTRO=rolling
# Tue, 31 Aug 2021 02:46:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:09 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:46:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:46:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b5c1e17fbe503ccf8bebc08da06f5478b90f03326ea7cc016d9e73507f10ce`  
		Last Modified: Tue, 31 Aug 2021 02:58:52 GMT  
		Size: 100.5 MB (100535790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45400d8e0bf75fe9e077d037d3f7b0e895432f5540ae74445ce40f4b797111a7`  
		Last Modified: Tue, 31 Aug 2021 02:58:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros1-bridge`

```console
$ docker pull ros@sha256:a72a2f1227f6295bf83307db5846bdc861eeb81637c05b5e3686a13df683adbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:1010c208fe8e29be8d29f89a94e4480db5e11bd7bf1ef56833c75836a1aaec65
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.1 MB (326094672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc57847edd472970365b429cdc9c8523700c4221eea7538d91b88d77be7f2d0b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:07:55 GMT
ENV ROS_DISTRO=rolling
# Tue, 27 Jul 2021 01:08:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:08:39 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:08:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:08:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:09:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:09:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 01:09:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 27 Jul 2021 01:09:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:09:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 01:09:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:09:39 GMT
ENV ROS1_DISTRO=noetic
# Tue, 27 Jul 2021 01:09:39 GMT
ENV ROS2_DISTRO=rolling
# Tue, 27 Jul 2021 01:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.11-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 21 Aug 2021 01:45:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros1-bridge=0.10.1-1*     ros-rolling-demo-nodes-cpp=0.16.0-1*     ros-rolling-demo-nodes-py=0.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 21 Aug 2021 01:45:32 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8928ebb6fc76f821cd15ef57553baa7177425b57b45dca1dc55d1fa7ac567a99`  
		Last Modified: Tue, 27 Jul 2021 01:20:05 GMT  
		Size: 104.0 MB (104037402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87230aa31aac601bd98ed495d1da57881931ef6ba2fd088208ff7edcc11a6645`  
		Last Modified: Tue, 27 Jul 2021 01:19:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ecfae6e660eea869e3a4f0b50e02e1f4d59061ecd4f0183ae66f147a79b142`  
		Last Modified: Tue, 27 Jul 2021 01:20:31 GMT  
		Size: 70.8 MB (70796958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9dc0d5adb890f7b8a3773d5280d5a49fc76acb26a178acc8625286d67ffb48`  
		Last Modified: Tue, 27 Jul 2021 01:20:21 GMT  
		Size: 239.9 KB (239910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72269352c197138327479f8993a3f63c4d1e1f551153f8892c4b0e0655b7cda`  
		Last Modified: Tue, 27 Jul 2021 01:20:20 GMT  
		Size: 2.0 KB (2029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164c9e6f758bbce1c98b1b54d6df1e86f651ececc09089ad70ff299c3251599b`  
		Last Modified: Tue, 27 Jul 2021 01:20:24 GMT  
		Size: 22.2 MB (22162528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b7e5b68d937de167626e1fbf8f8aa89e0b98f223f92214e751b6bc93ac02ae`  
		Last Modified: Tue, 27 Jul 2021 01:20:46 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae277910ca8875daebb4c39ac8f951db856449b3de053bc5fd2b5823c5ee57b6`  
		Last Modified: Tue, 27 Jul 2021 01:20:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f022dbe32fe832b14ad9e12583044b8108dcef7b9a90ffdbe21c579aa88700df`  
		Last Modified: Tue, 27 Jul 2021 01:21:00 GMT  
		Size: 78.4 MB (78413507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b07ce364cacb668c0b096aebdd66bc5439729cf0a322bb564205b6c403aaade`  
		Last Modified: Sat, 21 Aug 2021 01:46:43 GMT  
		Size: 15.1 MB (15141817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238a62a5e0a9e729b7a703eed6e39398d0da9bf3d0381499c8aa2df0452f4d40`  
		Last Modified: Sat, 21 Aug 2021 01:46:40 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:68468ac2b592b84dfaf20f49bb60edc59b0afa216eb47435803f5b68171cc498
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314397076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c88b7492ee1a3327220ba723459be0df41a8a1c4cfa1997003ca073e08b325e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:45:28 GMT
ENV ROS_DISTRO=rolling
# Tue, 31 Aug 2021 02:46:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:09 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:46:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:46:09 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:46:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:46:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 31 Aug 2021 02:47:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:47:11 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:47:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:47:18 GMT
ENV ROS1_DISTRO=noetic
# Tue, 31 Aug 2021 02:47:18 GMT
ENV ROS2_DISTRO=rolling
# Tue, 31 Aug 2021 02:47:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.11-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:47:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros1-bridge=0.10.1-1*     ros-rolling-demo-nodes-cpp=0.16.0-1*     ros-rolling-demo-nodes-py=0.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:47:53 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b5c1e17fbe503ccf8bebc08da06f5478b90f03326ea7cc016d9e73507f10ce`  
		Last Modified: Tue, 31 Aug 2021 02:58:52 GMT  
		Size: 100.5 MB (100535790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45400d8e0bf75fe9e077d037d3f7b0e895432f5540ae74445ce40f4b797111a7`  
		Last Modified: Tue, 31 Aug 2021 02:58:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1497a728946ec991c8b236b4101cde77517a464c2b22ebc0c2853c613f8edc`  
		Last Modified: Tue, 31 Aug 2021 02:59:15 GMT  
		Size: 65.1 MB (65137816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cb14f8cc4408bc999a0012920c6670355132f9cd04cfa6f3632da05868c24b`  
		Last Modified: Tue, 31 Aug 2021 02:59:04 GMT  
		Size: 243.4 KB (243377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a36f33083ce43a2fe6e2a6de6c0ef97f01bfded87f9bb0c50615c85cb4e312`  
		Last Modified: Tue, 31 Aug 2021 02:59:04 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177b7dcdd13b2c3e4ae37d2c849c4d4f5288ac23426c57d481e802f7cc6d6d96`  
		Last Modified: Tue, 31 Aug 2021 02:59:07 GMT  
		Size: 21.5 MB (21526088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bda22c832442974a0ad5794123fbb4e6221cdb2bc0453dae21d103dbfec86f5`  
		Last Modified: Tue, 31 Aug 2021 02:59:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82725bf8c13207af80944626bf8589affa0081f57afc0ac9909f1593c083bef8`  
		Last Modified: Tue, 31 Aug 2021 02:59:31 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d686b241380f7b3f8cfa70ef4d17a3aa23b8aa004ed5a0b058f2ef1297a313`  
		Last Modified: Tue, 31 Aug 2021 02:59:47 GMT  
		Size: 78.4 MB (78374994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4acdaad577df7d049bf04dedb300fb427799c94a4b55e063a1b5127c5e31d45`  
		Last Modified: Tue, 31 Aug 2021 02:59:34 GMT  
		Size: 14.7 MB (14704492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7e46de183de8b86fe1c86ff9b994c58a22b11e9a8d9327c1f58b6bcc729ec7`  
		Last Modified: Tue, 31 Aug 2021 02:59:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros1-bridge-focal`

```console
$ docker pull ros@sha256:a72a2f1227f6295bf83307db5846bdc861eeb81637c05b5e3686a13df683adbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:1010c208fe8e29be8d29f89a94e4480db5e11bd7bf1ef56833c75836a1aaec65
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.1 MB (326094672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc57847edd472970365b429cdc9c8523700c4221eea7538d91b88d77be7f2d0b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:48:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:48:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:02:06 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 27 Jul 2021 01:02:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jul 2021 01:02:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 27 Jul 2021 01:07:55 GMT
ENV ROS_DISTRO=rolling
# Tue, 27 Jul 2021 01:08:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:08:39 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 27 Jul 2021 01:08:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 27 Jul 2021 01:08:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:09:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:09:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 27 Jul 2021 01:09:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 27 Jul 2021 01:09:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:09:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 27 Jul 2021 01:09:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 27 Jul 2021 01:09:39 GMT
ENV ROS1_DISTRO=noetic
# Tue, 27 Jul 2021 01:09:39 GMT
ENV ROS2_DISTRO=rolling
# Tue, 27 Jul 2021 01:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.11-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 21 Aug 2021 01:45:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros1-bridge=0.10.1-1*     ros-rolling-demo-nodes-cpp=0.16.0-1*     ros-rolling-demo-nodes-py=0.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 21 Aug 2021 01:45:32 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec889c2abce161c5ac65f816c63d528f9b38633bcdcb93759283fd6bd28064`  
		Last Modified: Tue, 27 Jul 2021 00:03:14 GMT  
		Size: 1.2 MB (1182475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39deaaa7423e6ef1165a73155147eae3a10e676ec72379e083d81881a0aed170`  
		Last Modified: Tue, 27 Jul 2021 01:13:51 GMT  
		Size: 5.5 MB (5547062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09dd913f1251e30dc9e89af3583ddb796558251c0aa59b8fccabd59fc11ed0`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4b7162625d29326104f879225ff200e77afe83b35bca9f42e7e26f4894ce2`  
		Last Modified: Tue, 27 Jul 2021 01:16:58 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8928ebb6fc76f821cd15ef57553baa7177425b57b45dca1dc55d1fa7ac567a99`  
		Last Modified: Tue, 27 Jul 2021 01:20:05 GMT  
		Size: 104.0 MB (104037402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87230aa31aac601bd98ed495d1da57881931ef6ba2fd088208ff7edcc11a6645`  
		Last Modified: Tue, 27 Jul 2021 01:19:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ecfae6e660eea869e3a4f0b50e02e1f4d59061ecd4f0183ae66f147a79b142`  
		Last Modified: Tue, 27 Jul 2021 01:20:31 GMT  
		Size: 70.8 MB (70796958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9dc0d5adb890f7b8a3773d5280d5a49fc76acb26a178acc8625286d67ffb48`  
		Last Modified: Tue, 27 Jul 2021 01:20:21 GMT  
		Size: 239.9 KB (239910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72269352c197138327479f8993a3f63c4d1e1f551153f8892c4b0e0655b7cda`  
		Last Modified: Tue, 27 Jul 2021 01:20:20 GMT  
		Size: 2.0 KB (2029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164c9e6f758bbce1c98b1b54d6df1e86f651ececc09089ad70ff299c3251599b`  
		Last Modified: Tue, 27 Jul 2021 01:20:24 GMT  
		Size: 22.2 MB (22162528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b7e5b68d937de167626e1fbf8f8aa89e0b98f223f92214e751b6bc93ac02ae`  
		Last Modified: Tue, 27 Jul 2021 01:20:46 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae277910ca8875daebb4c39ac8f951db856449b3de053bc5fd2b5823c5ee57b6`  
		Last Modified: Tue, 27 Jul 2021 01:20:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f022dbe32fe832b14ad9e12583044b8108dcef7b9a90ffdbe21c579aa88700df`  
		Last Modified: Tue, 27 Jul 2021 01:21:00 GMT  
		Size: 78.4 MB (78413507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b07ce364cacb668c0b096aebdd66bc5439729cf0a322bb564205b6c403aaade`  
		Last Modified: Sat, 21 Aug 2021 01:46:43 GMT  
		Size: 15.1 MB (15141817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238a62a5e0a9e729b7a703eed6e39398d0da9bf3d0381499c8aa2df0452f4d40`  
		Last Modified: Sat, 21 Aug 2021 01:46:40 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:68468ac2b592b84dfaf20f49bb60edc59b0afa216eb47435803f5b68171cc498
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314397076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c88b7492ee1a3327220ba723459be0df41a8a1c4cfa1997003ca073e08b325e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:35:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:35:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:40:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 31 Aug 2021 02:40:14 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LANG=C.UTF-8
# Tue, 31 Aug 2021 02:40:15 GMT
ENV LC_ALL=C.UTF-8
# Tue, 31 Aug 2021 02:45:28 GMT
ENV ROS_DISTRO=rolling
# Tue, 31 Aug 2021 02:46:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:09 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 31 Aug 2021 02:46:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 31 Aug 2021 02:46:09 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:46:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 31 Aug 2021 02:46:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 31 Aug 2021 02:47:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:47:11 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 31 Aug 2021 02:47:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 31 Aug 2021 02:47:18 GMT
ENV ROS1_DISTRO=noetic
# Tue, 31 Aug 2021 02:47:18 GMT
ENV ROS2_DISTRO=rolling
# Tue, 31 Aug 2021 02:47:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.11-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:47:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros1-bridge=0.10.1-1*     ros-rolling-demo-nodes-cpp=0.16.0-1*     ros-rolling-demo-nodes-py=0.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:47:53 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869ca97320a7af4e9ce7c382543a1b04a7005c70779507cbb85ace89adde42e`  
		Last Modified: Tue, 31 Aug 2021 02:52:34 GMT  
		Size: 1.2 MB (1183579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7b498b8e70b033b401f685710eb46ada1aab199891dfe061488eb0ba40831`  
		Last Modified: Tue, 31 Aug 2021 02:52:32 GMT  
		Size: 5.5 MB (5512786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e16b4767757045ca5abd59a845a7b7cbc2916b1d1a63d930661eec9fc232b`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e90d25ecd370ffb201a02739df5a10f437fb2d2c95060875411cf40d5d0e12`  
		Last Modified: Tue, 31 Aug 2021 02:55:39 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b5c1e17fbe503ccf8bebc08da06f5478b90f03326ea7cc016d9e73507f10ce`  
		Last Modified: Tue, 31 Aug 2021 02:58:52 GMT  
		Size: 100.5 MB (100535790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45400d8e0bf75fe9e077d037d3f7b0e895432f5540ae74445ce40f4b797111a7`  
		Last Modified: Tue, 31 Aug 2021 02:58:34 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1497a728946ec991c8b236b4101cde77517a464c2b22ebc0c2853c613f8edc`  
		Last Modified: Tue, 31 Aug 2021 02:59:15 GMT  
		Size: 65.1 MB (65137816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cb14f8cc4408bc999a0012920c6670355132f9cd04cfa6f3632da05868c24b`  
		Last Modified: Tue, 31 Aug 2021 02:59:04 GMT  
		Size: 243.4 KB (243377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a36f33083ce43a2fe6e2a6de6c0ef97f01bfded87f9bb0c50615c85cb4e312`  
		Last Modified: Tue, 31 Aug 2021 02:59:04 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177b7dcdd13b2c3e4ae37d2c849c4d4f5288ac23426c57d481e802f7cc6d6d96`  
		Last Modified: Tue, 31 Aug 2021 02:59:07 GMT  
		Size: 21.5 MB (21526088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bda22c832442974a0ad5794123fbb4e6221cdb2bc0453dae21d103dbfec86f5`  
		Last Modified: Tue, 31 Aug 2021 02:59:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82725bf8c13207af80944626bf8589affa0081f57afc0ac9909f1593c083bef8`  
		Last Modified: Tue, 31 Aug 2021 02:59:31 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d686b241380f7b3f8cfa70ef4d17a3aa23b8aa004ed5a0b058f2ef1297a313`  
		Last Modified: Tue, 31 Aug 2021 02:59:47 GMT  
		Size: 78.4 MB (78374994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4acdaad577df7d049bf04dedb300fb427799c94a4b55e063a1b5127c5e31d45`  
		Last Modified: Tue, 31 Aug 2021 02:59:34 GMT  
		Size: 14.7 MB (14704492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7e46de183de8b86fe1c86ff9b994c58a22b11e9a8d9327c1f58b6bcc729ec7`  
		Last Modified: Tue, 31 Aug 2021 02:59:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
