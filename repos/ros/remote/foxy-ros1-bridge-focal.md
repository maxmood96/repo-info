## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:1eac0797ab9b5c85378d7bbdf17d4db3199b7f437b001c17ccbbe5ded7c0ad00
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
$ docker pull ros@sha256:d597d5e7c208683e0f65b765d88df852a350ac74f749753a26335733657316bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314030519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72880d992a4585224fda3bda11e0f3afe8f4491229781d73bd198496f292b92f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:03:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:03:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:08:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Mon, 26 Jul 2021 23:08:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Mon, 26 Jul 2021 23:08:17 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 23:08:17 GMT
ENV LC_ALL=C.UTF-8
# Mon, 26 Jul 2021 23:08:17 GMT
ENV ROS_DISTRO=foxy
# Mon, 26 Jul 2021 23:08:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:09:00 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Mon, 26 Jul 2021 23:09:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 26 Jul 2021 23:09:00 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 23:09:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:09:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 26 Jul 2021 23:09:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Mon, 26 Jul 2021 23:09:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:09:52 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Mon, 26 Jul 2021 23:09:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Mon, 26 Jul 2021 23:09:53 GMT
ENV ROS1_DISTRO=noetic
# Mon, 26 Jul 2021 23:09:53 GMT
ENV ROS2_DISTRO=foxy
# Mon, 26 Jul 2021 23:10:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.11-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:10:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 23:10:36 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47ae118bf19cf825ac83647c1d65d099e24417c73620e6553806e36aa26d8c5`  
		Last Modified: Mon, 26 Jul 2021 23:20:22 GMT  
		Size: 1.2 MB (1183453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74becffb9ea2d3b903303692f91a3abc607df25339bd7464db56343eefb622e`  
		Last Modified: Mon, 26 Jul 2021 23:20:20 GMT  
		Size: 5.5 MB (5512652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8145ea28ffd9b0942ba98116cde1e498e4572f6c665186683366584a32a0a9c0`  
		Last Modified: Mon, 26 Jul 2021 23:23:38 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb0e59f8a1856416b541915263ab8419535ec407203cdedec71cee7983a4f28`  
		Last Modified: Mon, 26 Jul 2021 23:23:37 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99638d27524b744be6c72b148745cecbd30fce62732e56202509249a739f015`  
		Last Modified: Mon, 26 Jul 2021 23:24:01 GMT  
		Size: 104.2 MB (104166106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0795de1605d5236fe906b0103be795fd0d5906337ac8e1219ab8680fc286d6cc`  
		Last Modified: Mon, 26 Jul 2021 23:23:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9212adaf308df7200d272b55747b777ee4c3f69fd8c33ed43a8cff46b456bcc`  
		Last Modified: Mon, 26 Jul 2021 23:24:25 GMT  
		Size: 65.2 MB (65183893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31858964d3495f929c4fbd43404976dce2b87c812a4a25b1a0c2c83dd29fddd`  
		Last Modified: Mon, 26 Jul 2021 23:24:14 GMT  
		Size: 238.5 KB (238481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c120cd143733715303fadf97c47bb4fc1cb0590feeb076c32ccfe7258ac90b`  
		Last Modified: Mon, 26 Jul 2021 23:24:14 GMT  
		Size: 2.0 KB (2048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28758a874a9f9821a0fabd399ffae95818ddd755930e5b479087a3bd9b77b272`  
		Last Modified: Mon, 26 Jul 2021 23:24:16 GMT  
		Size: 9.3 MB (9298707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56248d6b9a01933af094d8757699870aa609465d4792cfd4e0336e2c7e26161a`  
		Last Modified: Mon, 26 Jul 2021 23:24:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1a54c8d0b154ce4292783bb78ca5f06e3b98159d11a7c15f87c7f371031021`  
		Last Modified: Mon, 26 Jul 2021 23:24:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd615e8d8979e0faeed49833a47290b5855be669fd01bcacb56a7412c847bf52`  
		Last Modified: Mon, 26 Jul 2021 23:25:09 GMT  
		Size: 76.2 MB (76162720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191d6e1650f37b0d617071d14fbfffac08300c16ab3d0bd4b79239545bac4a29`  
		Last Modified: Mon, 26 Jul 2021 23:24:51 GMT  
		Size: 25.1 MB (25109167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529f4006067a03d7813622e41f0d355ebfc4a95c87751a77c4ecd33a9824c42a`  
		Last Modified: Mon, 26 Jul 2021 23:24:47 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
