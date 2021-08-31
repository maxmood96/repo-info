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
