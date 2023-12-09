## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:d359fc7f639d08350fcaddaa5837fa425802ffc1f024325f92c97334713c53e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:c2a0d0fcebd3f5e78300f8425d7e8f1c91d7db08a90cd4fcbed5bcb6577a7503
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.4 MB (840383915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46ef436c990ec1421b31bc1daa1ffd3c2526bde135fd6c6d38bb305d857cd8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Nov 2023 05:17:39 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:17:41 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Tue, 28 Nov 2023 05:17:41 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 02:08:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:04:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:11:15 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 09 Dec 2023 03:11:16 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 09 Dec 2023 03:11:16 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:11:16 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:11:16 GMT
ENV ROS_DISTRO=noetic
# Sat, 09 Dec 2023 03:15:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:15:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 09 Dec 2023 03:15:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:15:39 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:16:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:16:50 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 03:19:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:26:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:30ecab32a3b65c6ec04c63a65b90e627b49d1297d8793896ed50b656377d8a06`  
		Last Modified: Tue, 28 Nov 2023 10:11:56 GMT  
		Size: 28.6 MB (28584029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc1327734170da8c4ae4171fb4248189d0691d6b4a3f01b09239c3e34688651`  
		Last Modified: Sat, 02 Dec 2023 02:20:57 GMT  
		Size: 1.2 MB (1198788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77125e61032dbbcd43c015fe756de97b5661bdbbf4f5219588148f651ae900c1`  
		Last Modified: Sat, 02 Dec 2023 05:59:34 GMT  
		Size: 5.6 MB (5553989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854fa492c1515b2e14c4cf7d8f5424731e04a784ac4198639ecb30eeeb9a45e7`  
		Last Modified: Sat, 09 Dec 2023 04:39:04 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616ec384d8f7cf53f7ba2888d486c48c73d604a06f119c7fa3ba0bd4cb841f8d`  
		Last Modified: Sat, 09 Dec 2023 04:39:04 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cc12c912dc40206f622e17afe3ff5a803c260f093b2466364bae4fe6a95d5c`  
		Last Modified: Sat, 09 Dec 2023 04:39:43 GMT  
		Size: 182.1 MB (182116941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d021d342bec51fb4da1489b7487a3812b65a7bbf181e146c141645e7d0e1b0`  
		Last Modified: Sat, 09 Dec 2023 04:39:04 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9592f69eba9dc46e306b2b1459505c1eb8f5015b1aea82de715342e69c33ee`  
		Last Modified: Sat, 09 Dec 2023 04:39:59 GMT  
		Size: 50.9 MB (50940645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c711d4ea13dcbc5cc87616e104c035ae2c60e07f52feedcb37ce7cbcbcf9e65`  
		Last Modified: Sat, 09 Dec 2023 04:39:51 GMT  
		Size: 311.1 KB (311126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8195e0b4c07a8eef4ca13b215659a423fe4335ae341e31a63c6120e0b25786`  
		Last Modified: Sat, 09 Dec 2023 04:40:04 GMT  
		Size: 79.6 MB (79616526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7030bdfa345700fb940ff892dc187979d1579245f2be16898d4819662c2342c`  
		Last Modified: Sat, 09 Dec 2023 04:41:49 GMT  
		Size: 492.1 MB (492059464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:6ea67e0679ee2d06f2b8a9e4ade6422fd36e1e0be364f0a322eeff87a12179f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.6 MB (730643992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f12c07b33c73621f78576b87a1d9645b2d43934f940a5ab149180a8763bb24`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Nov 2023 05:27:44 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:27:51 GMT
ADD file:043af50602b163e71a05aa02ec03cbbb2659582ffeea29004c4477939cf448e0 in / 
# Tue, 28 Nov 2023 05:27:52 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 07:01:10 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:01:16 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:10:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 09 Dec 2023 03:10:51 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 09 Dec 2023 03:10:51 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:10:51 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:10:51 GMT
ENV ROS_DISTRO=noetic
# Sat, 09 Dec 2023 03:14:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:14:08 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 09 Dec 2023 03:14:08 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:14:08 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:14:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:14:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 03:16:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:25:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e2f879bfa159449422063ff666ac028f07b2d0d0240c9d1beecd2171ce0eac6b`  
		Last Modified: Wed, 29 Nov 2023 17:47:28 GMT  
		Size: 24.6 MB (24600167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d98a07bfa7aac27f091bf0d7219b9f7fde1d8aaaef4867256e199e71b299f1`  
		Last Modified: Sat, 02 Dec 2023 07:13:58 GMT  
		Size: 1.2 MB (1198794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3b1f005911cb4959d07abd5ac0987c950ecd363f9b62c9ee6a67f9c4207207`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 4.7 MB (4679365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b4ad3e9f7a76a574eff31f3c99b34d2bd8cb10c7824c647f41a00b79f39dd5`  
		Last Modified: Sat, 09 Dec 2023 03:41:30 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbe6af4a8c022ccb57c16535ef593b4c79b9ca695dd7aeaf6f69a19ab781773`  
		Last Modified: Sat, 09 Dec 2023 03:41:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42d68ab1ec2d1b1b63caf10beb32b17f38d9fe6704d50773ce6826b08175b8e`  
		Last Modified: Sat, 09 Dec 2023 03:42:11 GMT  
		Size: 161.8 MB (161838616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ab032d2adcd87e21c9ff3ba7750d9572871da1e94529ef0cf3510d64a64e46`  
		Last Modified: Sat, 09 Dec 2023 03:41:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aeafc85acb474de9ab8e053a87c67ccd59678e963228b0cafb152cb081fab60`  
		Last Modified: Sat, 09 Dec 2023 03:42:26 GMT  
		Size: 40.5 MB (40503680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901ab58517d47769e4c4a076daaf24c2d3e6aed481047e9ddb1e0450b6f41f7e`  
		Last Modified: Sat, 09 Dec 2023 03:42:20 GMT  
		Size: 311.1 KB (311122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886424a6f57b5809cb590e17f25aca0679c09b480ccf619f1a608e9a206e700a`  
		Last Modified: Sat, 09 Dec 2023 03:42:31 GMT  
		Size: 60.5 MB (60499558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21343f915524ffd69021f032f0327816225bd9d6170f2e5ae5ea5137f74336ef`  
		Last Modified: Sat, 09 Dec 2023 03:44:06 GMT  
		Size: 437.0 MB (437010283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:060d4ab2aee82f8df5712f3f8a44a0867b2e1626dd1b0c2b598f18eda060ce66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **789.7 MB (789725461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7d9458507fe087e6e6a46b3e5fa4a3785b3288d18c0bceba93a48e2ab6250f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Nov 2023 05:25:16 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:25:16 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:25:23 GMT
ADD file:f80c582e6edb1f05fc0cefc201be3c47d4b4c6ceb20889c434c9fdef0291cbbf in / 
# Tue, 28 Nov 2023 05:25:23 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:21:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:21:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:37:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 09 Dec 2023 02:37:28 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 09 Dec 2023 02:37:28 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 02:37:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 02:37:28 GMT
ENV ROS_DISTRO=noetic
# Sat, 09 Dec 2023 02:40:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:40:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 09 Dec 2023 02:40:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 02:40:42 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 02:41:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:41:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 02:42:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 02:51:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5d2acf9ee7cfde47b6ce997317767b8fa9bf8d93b8297016db9e093d06aa913d`  
		Last Modified: Wed, 29 Nov 2023 17:47:09 GMT  
		Size: 27.2 MB (27203865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2aa78ed8ad18394d7ae521e83b2810fec9fbb7d95aa074d794bb43e6e2bbfb`  
		Last Modified: Sat, 02 Dec 2023 06:56:12 GMT  
		Size: 1.2 MB (1198781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f106a95fef578814e019c4ac69f1cf32b15d5f85da2729a7ab2487c5d3505d`  
		Last Modified: Sat, 02 Dec 2023 06:56:11 GMT  
		Size: 5.5 MB (5532202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde5587588684db83e0c22fb5d4979df124ea1cb18322ace2e4c3ea5c96b6367`  
		Last Modified: Sat, 09 Dec 2023 03:55:53 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9c5b1b69c1b0400c6d51e9b08a29868443a22bc46ce96467a1b6fd75f9aa2c`  
		Last Modified: Sat, 09 Dec 2023 03:55:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c0f3f95aca8df1ff165733b239844d0700cbd97842b1699375b9137cd0075e`  
		Last Modified: Sat, 09 Dec 2023 03:56:30 GMT  
		Size: 175.6 MB (175614595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648bea585de95bdc098b0f496d2c461fc072dda803fe1be92b970893fd65443c`  
		Last Modified: Sat, 09 Dec 2023 03:55:53 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f261b12e1911ed6acc0c610902189f69372d1dbce997eb8ff1ede6dbf9e5ae21`  
		Last Modified: Sat, 09 Dec 2023 03:56:45 GMT  
		Size: 45.2 MB (45206492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92f89f65bd6464334de4ab44489a72c7bb00a4e5286a829f25300f62f3b1f25`  
		Last Modified: Sat, 09 Dec 2023 03:56:39 GMT  
		Size: 311.1 KB (311125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814329a852addc5f898a88b8ca07e7f891f15ddafaa210e9558da08b2bdc5e91`  
		Last Modified: Sat, 09 Dec 2023 03:56:48 GMT  
		Size: 72.0 MB (71972547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b451059359bf1ff30b83aab3d4235ca6bd1b90a82ea53503e434ae19ac6f37`  
		Last Modified: Sat, 09 Dec 2023 03:58:12 GMT  
		Size: 462.7 MB (462683445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
