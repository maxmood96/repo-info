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
$ docker pull ros@sha256:00d5355a13ddb300eab3eff6dd8287ddd000f11c203efd3ac2f1aa22b009b459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:05b3e7f3c895c60e9469c91d0271976ecd7055b5ae1eb6cb9d0ecc0e9b4dbf09
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263545173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47cf82a0a3b25e52463e4179c42af1efd18c4d9ae620a0df573d8e673f75aba1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV ROS_DISTRO=humble
# Wed, 06 Mar 2024 04:40:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:40:28 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:40:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:40:28 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:41:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:41:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:42:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c808dc8041d8a08e842df47732a8a08f550dd01f260447bb4f7d07cd5c9a1cd`  
		Last Modified: Wed, 06 Mar 2024 05:00:46 GMT  
		Size: 106.5 MB (106474978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fe6ecab2306edbc241045147aabc2f3c32a7b958e13590a65d0de0ab8bcefa`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b4f32e4504417ca1e106aa1bfda41d44c9cdc4f0aec4ae1fc8d26593debc6c`  
		Last Modified: Wed, 06 Mar 2024 05:01:07 GMT  
		Size: 98.1 MB (98138476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0775ae3bc65d52e84e7136bdb7663bf1e1c0ec3b416b29d953d41c3759b464ba`  
		Last Modified: Wed, 06 Mar 2024 05:00:54 GMT  
		Size: 331.1 KB (331145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268e8e2f7cd13633d7af262b5ace2a4d9bb67e72a22c9c2edb09675f9cb55270`  
		Last Modified: Wed, 06 Mar 2024 05:00:54 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4339e166fc83d67a3d7b94d17e59c0859e045120689720637aada3df371c7f`  
		Last Modified: Wed, 06 Mar 2024 05:00:57 GMT  
		Size: 23.1 MB (23101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d620458704bfe1d2fd2f87073427bc7486c0c6e2b04fccd256de8e53c870a7ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256152936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6f17c2aa477132e1d5386bc8a583fd9e168935a9456624321a5670c9d58e14`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV ROS_DISTRO=humble
# Wed, 06 Mar 2024 04:25:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:25:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:25:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:25:02 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:26:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:26:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:26:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3eb2e67a0ee0642539e9d0fa629f2696ed7e1bf68d5718f0f0d34a541a9afaa`  
		Last Modified: Wed, 06 Mar 2024 04:46:59 GMT  
		Size: 104.2 MB (104195832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12122adf1664bd4b96bc0459e52dd0d65a90e0569bd8452f4e4bfaa693611e22`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf21c988284258171de1e605ee3f1700216eba121998c9adbfc92831666888b`  
		Last Modified: Wed, 06 Mar 2024 04:47:20 GMT  
		Size: 95.7 MB (95685185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25894b282822606f5b2e64d41cea219409ba94a685ae8860acf9c924dcfedbcc`  
		Last Modified: Wed, 06 Mar 2024 04:47:08 GMT  
		Size: 331.1 KB (331148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9edf1c5d6eb51cde5a703b4b0d5f2c69eb275ae5ef4e1ff4f7fea5a0f58b81a`  
		Last Modified: Wed, 06 Mar 2024 04:47:08 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa2e80e8cab55dd73c4158423e5d52e5bebfdab597b2e0473f63f2837200b5`  
		Last Modified: Wed, 06 Mar 2024 04:47:12 GMT  
		Size: 22.5 MB (22519781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception`

```console
$ docker pull ros@sha256:3482eb1935679cbab8a5ee3ce39717f47fc059c78e1396a05fff9ea2e318edbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:003e1e3317712290cd01dc9bd9fd82b818364c65cec9e5ebc9cd8dcce2b3d8b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.0 MB (954973770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5ba6579ed64e22f32f5431e93a359fa351c0c4eb8fdcda71c467936ac57f84`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV ROS_DISTRO=humble
# Wed, 06 Mar 2024 04:40:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:40:28 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:40:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:40:28 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:41:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:41:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:42:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:49:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c808dc8041d8a08e842df47732a8a08f550dd01f260447bb4f7d07cd5c9a1cd`  
		Last Modified: Wed, 06 Mar 2024 05:00:46 GMT  
		Size: 106.5 MB (106474978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fe6ecab2306edbc241045147aabc2f3c32a7b958e13590a65d0de0ab8bcefa`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b4f32e4504417ca1e106aa1bfda41d44c9cdc4f0aec4ae1fc8d26593debc6c`  
		Last Modified: Wed, 06 Mar 2024 05:01:07 GMT  
		Size: 98.1 MB (98138476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0775ae3bc65d52e84e7136bdb7663bf1e1c0ec3b416b29d953d41c3759b464ba`  
		Last Modified: Wed, 06 Mar 2024 05:00:54 GMT  
		Size: 331.1 KB (331145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268e8e2f7cd13633d7af262b5ace2a4d9bb67e72a22c9c2edb09675f9cb55270`  
		Last Modified: Wed, 06 Mar 2024 05:00:54 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4339e166fc83d67a3d7b94d17e59c0859e045120689720637aada3df371c7f`  
		Last Modified: Wed, 06 Mar 2024 05:00:57 GMT  
		Size: 23.1 MB (23101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806162a5fd15e7a42ac6999515d695c71a16db09c2f5c844c1912e2bde0f3794`  
		Last Modified: Wed, 06 Mar 2024 05:02:50 GMT  
		Size: 691.4 MB (691428597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:18f05b82978b803530614f9058bde6ffa0832f21388debf30c2186d9944c0c63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.5 MB (915483555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e3f9ffbcbaba6d52cfb1b5fded7919d6934c36a165d99a5c2a0cb04f0fec9d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV ROS_DISTRO=humble
# Wed, 06 Mar 2024 04:25:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:25:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:25:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:25:02 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:26:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:26:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:26:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:36:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3eb2e67a0ee0642539e9d0fa629f2696ed7e1bf68d5718f0f0d34a541a9afaa`  
		Last Modified: Wed, 06 Mar 2024 04:46:59 GMT  
		Size: 104.2 MB (104195832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12122adf1664bd4b96bc0459e52dd0d65a90e0569bd8452f4e4bfaa693611e22`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf21c988284258171de1e605ee3f1700216eba121998c9adbfc92831666888b`  
		Last Modified: Wed, 06 Mar 2024 04:47:20 GMT  
		Size: 95.7 MB (95685185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25894b282822606f5b2e64d41cea219409ba94a685ae8860acf9c924dcfedbcc`  
		Last Modified: Wed, 06 Mar 2024 04:47:08 GMT  
		Size: 331.1 KB (331148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9edf1c5d6eb51cde5a703b4b0d5f2c69eb275ae5ef4e1ff4f7fea5a0f58b81a`  
		Last Modified: Wed, 06 Mar 2024 04:47:08 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa2e80e8cab55dd73c4158423e5d52e5bebfdab597b2e0473f63f2837200b5`  
		Last Modified: Wed, 06 Mar 2024 04:47:12 GMT  
		Size: 22.5 MB (22519781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259355afc7e3ff3447c79f64c5231f6d04ebd851e7cc2441326a59e3a72c71df`  
		Last Modified: Wed, 06 Mar 2024 04:48:57 GMT  
		Size: 659.3 MB (659330619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:3482eb1935679cbab8a5ee3ce39717f47fc059c78e1396a05fff9ea2e318edbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:003e1e3317712290cd01dc9bd9fd82b818364c65cec9e5ebc9cd8dcce2b3d8b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.0 MB (954973770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5ba6579ed64e22f32f5431e93a359fa351c0c4eb8fdcda71c467936ac57f84`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV ROS_DISTRO=humble
# Wed, 06 Mar 2024 04:40:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:40:28 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:40:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:40:28 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:41:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:41:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:42:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:49:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c808dc8041d8a08e842df47732a8a08f550dd01f260447bb4f7d07cd5c9a1cd`  
		Last Modified: Wed, 06 Mar 2024 05:00:46 GMT  
		Size: 106.5 MB (106474978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fe6ecab2306edbc241045147aabc2f3c32a7b958e13590a65d0de0ab8bcefa`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b4f32e4504417ca1e106aa1bfda41d44c9cdc4f0aec4ae1fc8d26593debc6c`  
		Last Modified: Wed, 06 Mar 2024 05:01:07 GMT  
		Size: 98.1 MB (98138476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0775ae3bc65d52e84e7136bdb7663bf1e1c0ec3b416b29d953d41c3759b464ba`  
		Last Modified: Wed, 06 Mar 2024 05:00:54 GMT  
		Size: 331.1 KB (331145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268e8e2f7cd13633d7af262b5ace2a4d9bb67e72a22c9c2edb09675f9cb55270`  
		Last Modified: Wed, 06 Mar 2024 05:00:54 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4339e166fc83d67a3d7b94d17e59c0859e045120689720637aada3df371c7f`  
		Last Modified: Wed, 06 Mar 2024 05:00:57 GMT  
		Size: 23.1 MB (23101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806162a5fd15e7a42ac6999515d695c71a16db09c2f5c844c1912e2bde0f3794`  
		Last Modified: Wed, 06 Mar 2024 05:02:50 GMT  
		Size: 691.4 MB (691428597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:18f05b82978b803530614f9058bde6ffa0832f21388debf30c2186d9944c0c63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.5 MB (915483555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e3f9ffbcbaba6d52cfb1b5fded7919d6934c36a165d99a5c2a0cb04f0fec9d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV ROS_DISTRO=humble
# Wed, 06 Mar 2024 04:25:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:25:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:25:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:25:02 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:26:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:26:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:26:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:36:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3eb2e67a0ee0642539e9d0fa629f2696ed7e1bf68d5718f0f0d34a541a9afaa`  
		Last Modified: Wed, 06 Mar 2024 04:46:59 GMT  
		Size: 104.2 MB (104195832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12122adf1664bd4b96bc0459e52dd0d65a90e0569bd8452f4e4bfaa693611e22`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf21c988284258171de1e605ee3f1700216eba121998c9adbfc92831666888b`  
		Last Modified: Wed, 06 Mar 2024 04:47:20 GMT  
		Size: 95.7 MB (95685185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25894b282822606f5b2e64d41cea219409ba94a685ae8860acf9c924dcfedbcc`  
		Last Modified: Wed, 06 Mar 2024 04:47:08 GMT  
		Size: 331.1 KB (331148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9edf1c5d6eb51cde5a703b4b0d5f2c69eb275ae5ef4e1ff4f7fea5a0f58b81a`  
		Last Modified: Wed, 06 Mar 2024 04:47:08 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa2e80e8cab55dd73c4158423e5d52e5bebfdab597b2e0473f63f2837200b5`  
		Last Modified: Wed, 06 Mar 2024 04:47:12 GMT  
		Size: 22.5 MB (22519781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259355afc7e3ff3447c79f64c5231f6d04ebd851e7cc2441326a59e3a72c71df`  
		Last Modified: Wed, 06 Mar 2024 04:48:57 GMT  
		Size: 659.3 MB (659330619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:00d5355a13ddb300eab3eff6dd8287ddd000f11c203efd3ac2f1aa22b009b459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:05b3e7f3c895c60e9469c91d0271976ecd7055b5ae1eb6cb9d0ecc0e9b4dbf09
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263545173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47cf82a0a3b25e52463e4179c42af1efd18c4d9ae620a0df573d8e673f75aba1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV ROS_DISTRO=humble
# Wed, 06 Mar 2024 04:40:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:40:28 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:40:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:40:28 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:41:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:41:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:42:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c808dc8041d8a08e842df47732a8a08f550dd01f260447bb4f7d07cd5c9a1cd`  
		Last Modified: Wed, 06 Mar 2024 05:00:46 GMT  
		Size: 106.5 MB (106474978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fe6ecab2306edbc241045147aabc2f3c32a7b958e13590a65d0de0ab8bcefa`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b4f32e4504417ca1e106aa1bfda41d44c9cdc4f0aec4ae1fc8d26593debc6c`  
		Last Modified: Wed, 06 Mar 2024 05:01:07 GMT  
		Size: 98.1 MB (98138476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0775ae3bc65d52e84e7136bdb7663bf1e1c0ec3b416b29d953d41c3759b464ba`  
		Last Modified: Wed, 06 Mar 2024 05:00:54 GMT  
		Size: 331.1 KB (331145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268e8e2f7cd13633d7af262b5ace2a4d9bb67e72a22c9c2edb09675f9cb55270`  
		Last Modified: Wed, 06 Mar 2024 05:00:54 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4339e166fc83d67a3d7b94d17e59c0859e045120689720637aada3df371c7f`  
		Last Modified: Wed, 06 Mar 2024 05:00:57 GMT  
		Size: 23.1 MB (23101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d620458704bfe1d2fd2f87073427bc7486c0c6e2b04fccd256de8e53c870a7ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256152936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6f17c2aa477132e1d5386bc8a583fd9e168935a9456624321a5670c9d58e14`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV ROS_DISTRO=humble
# Wed, 06 Mar 2024 04:25:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:25:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:25:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:25:02 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:26:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:26:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:26:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3eb2e67a0ee0642539e9d0fa629f2696ed7e1bf68d5718f0f0d34a541a9afaa`  
		Last Modified: Wed, 06 Mar 2024 04:46:59 GMT  
		Size: 104.2 MB (104195832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12122adf1664bd4b96bc0459e52dd0d65a90e0569bd8452f4e4bfaa693611e22`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf21c988284258171de1e605ee3f1700216eba121998c9adbfc92831666888b`  
		Last Modified: Wed, 06 Mar 2024 04:47:20 GMT  
		Size: 95.7 MB (95685185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25894b282822606f5b2e64d41cea219409ba94a685ae8860acf9c924dcfedbcc`  
		Last Modified: Wed, 06 Mar 2024 04:47:08 GMT  
		Size: 331.1 KB (331148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9edf1c5d6eb51cde5a703b4b0d5f2c69eb275ae5ef4e1ff4f7fea5a0f58b81a`  
		Last Modified: Wed, 06 Mar 2024 04:47:08 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa2e80e8cab55dd73c4158423e5d52e5bebfdab597b2e0473f63f2837200b5`  
		Last Modified: Wed, 06 Mar 2024 04:47:12 GMT  
		Size: 22.5 MB (22519781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:00d5355a13ddb300eab3eff6dd8287ddd000f11c203efd3ac2f1aa22b009b459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:05b3e7f3c895c60e9469c91d0271976ecd7055b5ae1eb6cb9d0ecc0e9b4dbf09
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263545173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47cf82a0a3b25e52463e4179c42af1efd18c4d9ae620a0df573d8e673f75aba1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV ROS_DISTRO=humble
# Wed, 06 Mar 2024 04:40:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:40:28 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:40:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:40:28 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:41:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:41:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:42:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c808dc8041d8a08e842df47732a8a08f550dd01f260447bb4f7d07cd5c9a1cd`  
		Last Modified: Wed, 06 Mar 2024 05:00:46 GMT  
		Size: 106.5 MB (106474978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fe6ecab2306edbc241045147aabc2f3c32a7b958e13590a65d0de0ab8bcefa`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b4f32e4504417ca1e106aa1bfda41d44c9cdc4f0aec4ae1fc8d26593debc6c`  
		Last Modified: Wed, 06 Mar 2024 05:01:07 GMT  
		Size: 98.1 MB (98138476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0775ae3bc65d52e84e7136bdb7663bf1e1c0ec3b416b29d953d41c3759b464ba`  
		Last Modified: Wed, 06 Mar 2024 05:00:54 GMT  
		Size: 331.1 KB (331145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268e8e2f7cd13633d7af262b5ace2a4d9bb67e72a22c9c2edb09675f9cb55270`  
		Last Modified: Wed, 06 Mar 2024 05:00:54 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4339e166fc83d67a3d7b94d17e59c0859e045120689720637aada3df371c7f`  
		Last Modified: Wed, 06 Mar 2024 05:00:57 GMT  
		Size: 23.1 MB (23101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d620458704bfe1d2fd2f87073427bc7486c0c6e2b04fccd256de8e53c870a7ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256152936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6f17c2aa477132e1d5386bc8a583fd9e168935a9456624321a5670c9d58e14`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV ROS_DISTRO=humble
# Wed, 06 Mar 2024 04:25:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:25:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:25:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:25:02 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:26:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:26:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:26:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3eb2e67a0ee0642539e9d0fa629f2696ed7e1bf68d5718f0f0d34a541a9afaa`  
		Last Modified: Wed, 06 Mar 2024 04:46:59 GMT  
		Size: 104.2 MB (104195832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12122adf1664bd4b96bc0459e52dd0d65a90e0569bd8452f4e4bfaa693611e22`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf21c988284258171de1e605ee3f1700216eba121998c9adbfc92831666888b`  
		Last Modified: Wed, 06 Mar 2024 04:47:20 GMT  
		Size: 95.7 MB (95685185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25894b282822606f5b2e64d41cea219409ba94a685ae8860acf9c924dcfedbcc`  
		Last Modified: Wed, 06 Mar 2024 04:47:08 GMT  
		Size: 331.1 KB (331148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9edf1c5d6eb51cde5a703b4b0d5f2c69eb275ae5ef4e1ff4f7fea5a0f58b81a`  
		Last Modified: Wed, 06 Mar 2024 04:47:08 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa2e80e8cab55dd73c4158423e5d52e5bebfdab597b2e0473f63f2837200b5`  
		Last Modified: Wed, 06 Mar 2024 04:47:12 GMT  
		Size: 22.5 MB (22519781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:8b0b337db341c4e17baaa0945ad0b519d83b7036a80ee771b455272a4beb2af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:01e30aa5f55d88fbb0f579b7da90a80a1332fbd6ac938d607ac652468c0ce8b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141972051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d2f84ce30cd421c2c0fe110672717ef0cb8ef68f521a33b1a823f2a835df42`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV ROS_DISTRO=humble
# Wed, 06 Mar 2024 04:40:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:40:28 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:40:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:40:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c808dc8041d8a08e842df47732a8a08f550dd01f260447bb4f7d07cd5c9a1cd`  
		Last Modified: Wed, 06 Mar 2024 05:00:46 GMT  
		Size: 106.5 MB (106474978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fe6ecab2306edbc241045147aabc2f3c32a7b958e13590a65d0de0ab8bcefa`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0beab3ef3ab5f56e6340dd7db8726ee60c240083361625a9131e40587cb26b3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137614324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a7f54e1e84b6456e674c6735445bd0b9f0926c0933c4f7ab3bcf660cda9d00`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV ROS_DISTRO=humble
# Wed, 06 Mar 2024 04:25:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:25:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:25:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:25:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3eb2e67a0ee0642539e9d0fa629f2696ed7e1bf68d5718f0f0d34a541a9afaa`  
		Last Modified: Wed, 06 Mar 2024 04:46:59 GMT  
		Size: 104.2 MB (104195832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12122adf1664bd4b96bc0459e52dd0d65a90e0569bd8452f4e4bfaa693611e22`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:8b0b337db341c4e17baaa0945ad0b519d83b7036a80ee771b455272a4beb2af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:01e30aa5f55d88fbb0f579b7da90a80a1332fbd6ac938d607ac652468c0ce8b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141972051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d2f84ce30cd421c2c0fe110672717ef0cb8ef68f521a33b1a823f2a835df42`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV ROS_DISTRO=humble
# Wed, 06 Mar 2024 04:40:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:40:28 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:40:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:40:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c808dc8041d8a08e842df47732a8a08f550dd01f260447bb4f7d07cd5c9a1cd`  
		Last Modified: Wed, 06 Mar 2024 05:00:46 GMT  
		Size: 106.5 MB (106474978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fe6ecab2306edbc241045147aabc2f3c32a7b958e13590a65d0de0ab8bcefa`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0beab3ef3ab5f56e6340dd7db8726ee60c240083361625a9131e40587cb26b3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137614324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a7f54e1e84b6456e674c6735445bd0b9f0926c0933c4f7ab3bcf660cda9d00`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV ROS_DISTRO=humble
# Wed, 06 Mar 2024 04:25:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:25:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:25:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:25:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3eb2e67a0ee0642539e9d0fa629f2696ed7e1bf68d5718f0f0d34a541a9afaa`  
		Last Modified: Wed, 06 Mar 2024 04:46:59 GMT  
		Size: 104.2 MB (104195832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12122adf1664bd4b96bc0459e52dd0d65a90e0569bd8452f4e4bfaa693611e22`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron`

```console
$ docker pull ros@sha256:962fa2ff74ce609a2cd1d9fb866502ab3b4bbe3b81af52194325eb9135b80cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron` - linux; amd64

```console
$ docker pull ros@sha256:6dd9fb81134cfe4696e09d9c9541e6d41b7853cda69080633391d763e1fca0b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268925574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22184b5715a73536fbcb27573f171783290bd710be1691a893de06c129898bad`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:50:10 GMT
ENV ROS_DISTRO=iron
# Wed, 06 Mar 2024 04:50:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:50:59 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:50:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:51:00 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:51:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:51:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:51:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:51:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e8e3ea014906f3a7c3e83d63e916e71430408df8cc6ca0b1b428cb5a7f7456`  
		Last Modified: Wed, 06 Mar 2024 05:03:20 GMT  
		Size: 124.2 MB (124224432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a7cc6de96d628a75624552fc6df79665be5f96ede7dd447f5eecddd16adcf7`  
		Last Modified: Wed, 06 Mar 2024 05:03:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3167aa37ba92964ce15c83d9bb0f226b86fc57041d959a84f2bd786e535449aa`  
		Last Modified: Wed, 06 Mar 2024 05:03:39 GMT  
		Size: 85.2 MB (85170647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdfa9a57e3781d78cdc781adb91610b842cf34ccc7992e17a29fe285e982bda`  
		Last Modified: Wed, 06 Mar 2024 05:03:29 GMT  
		Size: 297.8 KB (297817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0094ff430353f6440554ec0e0d7480ebec80674101740bba21cfe36d577343`  
		Last Modified: Wed, 06 Mar 2024 05:03:29 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732d2239bae29d1d76b8e33286d5c267501ed50825666af9b379391a898eec3f`  
		Last Modified: Wed, 06 Mar 2024 05:03:32 GMT  
		Size: 23.7 MB (23733119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8fa53945e1f892ec8132dc28885848ebf49d62de9c209a7a3c698d7d5eb714ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261399957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9511ef962573abab8adb8f5c2535e7c0b6226cd663392be971e30512d9290d0d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:36:56 GMT
ENV ROS_DISTRO=iron
# Wed, 06 Mar 2024 04:37:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:37:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:37:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:37:43 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:38:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:38:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:38:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94163e2e56dff6bcf8394dcf0c51e0c1e05f7d35905bf61f7868375517678a69`  
		Last Modified: Wed, 06 Mar 2024 04:49:30 GMT  
		Size: 121.7 MB (121715975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1a09d4269a9877c1e165e1c2c52b60e6d81faf469d4acea17a4e625b2e046b`  
		Last Modified: Wed, 06 Mar 2024 04:49:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21979e52cf569da9d1ca16c13ba7cadf068e3d0af36e6864cb518352191009e0`  
		Last Modified: Wed, 06 Mar 2024 04:49:48 GMT  
		Size: 82.8 MB (82844860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc557ba7379579a08b2dabcc6bb9a358d34de5a1d4ab4a6dbcd905a4ccf7a93`  
		Last Modified: Wed, 06 Mar 2024 04:49:40 GMT  
		Size: 297.8 KB (297812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167f55e60982941a94e2c52ee255fbcc15677fea931cc30658f05bf3410dbbdb`  
		Last Modified: Wed, 06 Mar 2024 04:49:39 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788e377e2a2bd9912a433ca23ee48613e4122b8d7a2035c06f344264f4fb431e`  
		Last Modified: Wed, 06 Mar 2024 04:49:44 GMT  
		Size: 23.1 MB (23120349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-perception`

```console
$ docker pull ros@sha256:6d4c312735e5f4469539cb6c50810bcbf0c23bd0e27d95b58a78e39418938c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception` - linux; amd64

```console
$ docker pull ros@sha256:b6a6a52637f8d9ac4f904c12ef0e93928f9351cef800c5b2315e04e1180f56d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.0 MB (961036360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38f3a452363adc740d5bdfb88b42cbc5e115dabc558366326b0eec17f481589`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:50:10 GMT
ENV ROS_DISTRO=iron
# Wed, 06 Mar 2024 04:50:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:50:59 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:50:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:51:00 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:51:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:51:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:51:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:51:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:53:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e8e3ea014906f3a7c3e83d63e916e71430408df8cc6ca0b1b428cb5a7f7456`  
		Last Modified: Wed, 06 Mar 2024 05:03:20 GMT  
		Size: 124.2 MB (124224432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a7cc6de96d628a75624552fc6df79665be5f96ede7dd447f5eecddd16adcf7`  
		Last Modified: Wed, 06 Mar 2024 05:03:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3167aa37ba92964ce15c83d9bb0f226b86fc57041d959a84f2bd786e535449aa`  
		Last Modified: Wed, 06 Mar 2024 05:03:39 GMT  
		Size: 85.2 MB (85170647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdfa9a57e3781d78cdc781adb91610b842cf34ccc7992e17a29fe285e982bda`  
		Last Modified: Wed, 06 Mar 2024 05:03:29 GMT  
		Size: 297.8 KB (297817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0094ff430353f6440554ec0e0d7480ebec80674101740bba21cfe36d577343`  
		Last Modified: Wed, 06 Mar 2024 05:03:29 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732d2239bae29d1d76b8e33286d5c267501ed50825666af9b379391a898eec3f`  
		Last Modified: Wed, 06 Mar 2024 05:03:32 GMT  
		Size: 23.7 MB (23733119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdde8c028c5e38ba7a068ef4cda7f20689881262dd4863277928484387336a72`  
		Last Modified: Wed, 06 Mar 2024 05:05:20 GMT  
		Size: 692.1 MB (692110786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:803c6b37f3f112e82710655cd3a6f79cb85813a7c3046904838f3fb6c615f512
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.4 MB (921380281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b3178948fa4ca03d8a1b384db7edb7dd01358586f0a8e8be8173edeb34a8a1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:36:56 GMT
ENV ROS_DISTRO=iron
# Wed, 06 Mar 2024 04:37:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:37:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:37:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:37:43 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:38:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:38:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:38:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:40:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94163e2e56dff6bcf8394dcf0c51e0c1e05f7d35905bf61f7868375517678a69`  
		Last Modified: Wed, 06 Mar 2024 04:49:30 GMT  
		Size: 121.7 MB (121715975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1a09d4269a9877c1e165e1c2c52b60e6d81faf469d4acea17a4e625b2e046b`  
		Last Modified: Wed, 06 Mar 2024 04:49:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21979e52cf569da9d1ca16c13ba7cadf068e3d0af36e6864cb518352191009e0`  
		Last Modified: Wed, 06 Mar 2024 04:49:48 GMT  
		Size: 82.8 MB (82844860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc557ba7379579a08b2dabcc6bb9a358d34de5a1d4ab4a6dbcd905a4ccf7a93`  
		Last Modified: Wed, 06 Mar 2024 04:49:40 GMT  
		Size: 297.8 KB (297812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167f55e60982941a94e2c52ee255fbcc15677fea931cc30658f05bf3410dbbdb`  
		Last Modified: Wed, 06 Mar 2024 04:49:39 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788e377e2a2bd9912a433ca23ee48613e4122b8d7a2035c06f344264f4fb431e`  
		Last Modified: Wed, 06 Mar 2024 04:49:44 GMT  
		Size: 23.1 MB (23120349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455b74d6e1d02327440ff477bfc01055959e998528524842c2e46833135c16e6`  
		Last Modified: Wed, 06 Mar 2024 04:51:26 GMT  
		Size: 660.0 MB (659980324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:6d4c312735e5f4469539cb6c50810bcbf0c23bd0e27d95b58a78e39418938c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:b6a6a52637f8d9ac4f904c12ef0e93928f9351cef800c5b2315e04e1180f56d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.0 MB (961036360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38f3a452363adc740d5bdfb88b42cbc5e115dabc558366326b0eec17f481589`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:50:10 GMT
ENV ROS_DISTRO=iron
# Wed, 06 Mar 2024 04:50:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:50:59 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:50:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:51:00 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:51:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:51:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:51:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:51:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:53:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e8e3ea014906f3a7c3e83d63e916e71430408df8cc6ca0b1b428cb5a7f7456`  
		Last Modified: Wed, 06 Mar 2024 05:03:20 GMT  
		Size: 124.2 MB (124224432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a7cc6de96d628a75624552fc6df79665be5f96ede7dd447f5eecddd16adcf7`  
		Last Modified: Wed, 06 Mar 2024 05:03:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3167aa37ba92964ce15c83d9bb0f226b86fc57041d959a84f2bd786e535449aa`  
		Last Modified: Wed, 06 Mar 2024 05:03:39 GMT  
		Size: 85.2 MB (85170647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdfa9a57e3781d78cdc781adb91610b842cf34ccc7992e17a29fe285e982bda`  
		Last Modified: Wed, 06 Mar 2024 05:03:29 GMT  
		Size: 297.8 KB (297817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0094ff430353f6440554ec0e0d7480ebec80674101740bba21cfe36d577343`  
		Last Modified: Wed, 06 Mar 2024 05:03:29 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732d2239bae29d1d76b8e33286d5c267501ed50825666af9b379391a898eec3f`  
		Last Modified: Wed, 06 Mar 2024 05:03:32 GMT  
		Size: 23.7 MB (23733119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdde8c028c5e38ba7a068ef4cda7f20689881262dd4863277928484387336a72`  
		Last Modified: Wed, 06 Mar 2024 05:05:20 GMT  
		Size: 692.1 MB (692110786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:803c6b37f3f112e82710655cd3a6f79cb85813a7c3046904838f3fb6c615f512
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.4 MB (921380281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b3178948fa4ca03d8a1b384db7edb7dd01358586f0a8e8be8173edeb34a8a1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:36:56 GMT
ENV ROS_DISTRO=iron
# Wed, 06 Mar 2024 04:37:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:37:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:37:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:37:43 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:38:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:38:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:38:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:40:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94163e2e56dff6bcf8394dcf0c51e0c1e05f7d35905bf61f7868375517678a69`  
		Last Modified: Wed, 06 Mar 2024 04:49:30 GMT  
		Size: 121.7 MB (121715975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1a09d4269a9877c1e165e1c2c52b60e6d81faf469d4acea17a4e625b2e046b`  
		Last Modified: Wed, 06 Mar 2024 04:49:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21979e52cf569da9d1ca16c13ba7cadf068e3d0af36e6864cb518352191009e0`  
		Last Modified: Wed, 06 Mar 2024 04:49:48 GMT  
		Size: 82.8 MB (82844860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc557ba7379579a08b2dabcc6bb9a358d34de5a1d4ab4a6dbcd905a4ccf7a93`  
		Last Modified: Wed, 06 Mar 2024 04:49:40 GMT  
		Size: 297.8 KB (297812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167f55e60982941a94e2c52ee255fbcc15677fea931cc30658f05bf3410dbbdb`  
		Last Modified: Wed, 06 Mar 2024 04:49:39 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788e377e2a2bd9912a433ca23ee48613e4122b8d7a2035c06f344264f4fb431e`  
		Last Modified: Wed, 06 Mar 2024 04:49:44 GMT  
		Size: 23.1 MB (23120349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455b74d6e1d02327440ff477bfc01055959e998528524842c2e46833135c16e6`  
		Last Modified: Wed, 06 Mar 2024 04:51:26 GMT  
		Size: 660.0 MB (659980324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-base`

```console
$ docker pull ros@sha256:962fa2ff74ce609a2cd1d9fb866502ab3b4bbe3b81af52194325eb9135b80cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:6dd9fb81134cfe4696e09d9c9541e6d41b7853cda69080633391d763e1fca0b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268925574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22184b5715a73536fbcb27573f171783290bd710be1691a893de06c129898bad`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:50:10 GMT
ENV ROS_DISTRO=iron
# Wed, 06 Mar 2024 04:50:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:50:59 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:50:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:51:00 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:51:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:51:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:51:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:51:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e8e3ea014906f3a7c3e83d63e916e71430408df8cc6ca0b1b428cb5a7f7456`  
		Last Modified: Wed, 06 Mar 2024 05:03:20 GMT  
		Size: 124.2 MB (124224432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a7cc6de96d628a75624552fc6df79665be5f96ede7dd447f5eecddd16adcf7`  
		Last Modified: Wed, 06 Mar 2024 05:03:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3167aa37ba92964ce15c83d9bb0f226b86fc57041d959a84f2bd786e535449aa`  
		Last Modified: Wed, 06 Mar 2024 05:03:39 GMT  
		Size: 85.2 MB (85170647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdfa9a57e3781d78cdc781adb91610b842cf34ccc7992e17a29fe285e982bda`  
		Last Modified: Wed, 06 Mar 2024 05:03:29 GMT  
		Size: 297.8 KB (297817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0094ff430353f6440554ec0e0d7480ebec80674101740bba21cfe36d577343`  
		Last Modified: Wed, 06 Mar 2024 05:03:29 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732d2239bae29d1d76b8e33286d5c267501ed50825666af9b379391a898eec3f`  
		Last Modified: Wed, 06 Mar 2024 05:03:32 GMT  
		Size: 23.7 MB (23733119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8fa53945e1f892ec8132dc28885848ebf49d62de9c209a7a3c698d7d5eb714ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261399957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9511ef962573abab8adb8f5c2535e7c0b6226cd663392be971e30512d9290d0d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:36:56 GMT
ENV ROS_DISTRO=iron
# Wed, 06 Mar 2024 04:37:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:37:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:37:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:37:43 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:38:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:38:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:38:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94163e2e56dff6bcf8394dcf0c51e0c1e05f7d35905bf61f7868375517678a69`  
		Last Modified: Wed, 06 Mar 2024 04:49:30 GMT  
		Size: 121.7 MB (121715975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1a09d4269a9877c1e165e1c2c52b60e6d81faf469d4acea17a4e625b2e046b`  
		Last Modified: Wed, 06 Mar 2024 04:49:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21979e52cf569da9d1ca16c13ba7cadf068e3d0af36e6864cb518352191009e0`  
		Last Modified: Wed, 06 Mar 2024 04:49:48 GMT  
		Size: 82.8 MB (82844860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc557ba7379579a08b2dabcc6bb9a358d34de5a1d4ab4a6dbcd905a4ccf7a93`  
		Last Modified: Wed, 06 Mar 2024 04:49:40 GMT  
		Size: 297.8 KB (297812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167f55e60982941a94e2c52ee255fbcc15677fea931cc30658f05bf3410dbbdb`  
		Last Modified: Wed, 06 Mar 2024 04:49:39 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788e377e2a2bd9912a433ca23ee48613e4122b8d7a2035c06f344264f4fb431e`  
		Last Modified: Wed, 06 Mar 2024 04:49:44 GMT  
		Size: 23.1 MB (23120349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:962fa2ff74ce609a2cd1d9fb866502ab3b4bbe3b81af52194325eb9135b80cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:6dd9fb81134cfe4696e09d9c9541e6d41b7853cda69080633391d763e1fca0b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268925574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22184b5715a73536fbcb27573f171783290bd710be1691a893de06c129898bad`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:50:10 GMT
ENV ROS_DISTRO=iron
# Wed, 06 Mar 2024 04:50:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:50:59 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:50:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:51:00 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:51:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:51:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:51:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:51:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e8e3ea014906f3a7c3e83d63e916e71430408df8cc6ca0b1b428cb5a7f7456`  
		Last Modified: Wed, 06 Mar 2024 05:03:20 GMT  
		Size: 124.2 MB (124224432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a7cc6de96d628a75624552fc6df79665be5f96ede7dd447f5eecddd16adcf7`  
		Last Modified: Wed, 06 Mar 2024 05:03:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3167aa37ba92964ce15c83d9bb0f226b86fc57041d959a84f2bd786e535449aa`  
		Last Modified: Wed, 06 Mar 2024 05:03:39 GMT  
		Size: 85.2 MB (85170647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdfa9a57e3781d78cdc781adb91610b842cf34ccc7992e17a29fe285e982bda`  
		Last Modified: Wed, 06 Mar 2024 05:03:29 GMT  
		Size: 297.8 KB (297817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0094ff430353f6440554ec0e0d7480ebec80674101740bba21cfe36d577343`  
		Last Modified: Wed, 06 Mar 2024 05:03:29 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732d2239bae29d1d76b8e33286d5c267501ed50825666af9b379391a898eec3f`  
		Last Modified: Wed, 06 Mar 2024 05:03:32 GMT  
		Size: 23.7 MB (23733119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8fa53945e1f892ec8132dc28885848ebf49d62de9c209a7a3c698d7d5eb714ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261399957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9511ef962573abab8adb8f5c2535e7c0b6226cd663392be971e30512d9290d0d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:36:56 GMT
ENV ROS_DISTRO=iron
# Wed, 06 Mar 2024 04:37:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:37:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:37:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:37:43 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:38:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:38:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:38:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94163e2e56dff6bcf8394dcf0c51e0c1e05f7d35905bf61f7868375517678a69`  
		Last Modified: Wed, 06 Mar 2024 04:49:30 GMT  
		Size: 121.7 MB (121715975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1a09d4269a9877c1e165e1c2c52b60e6d81faf469d4acea17a4e625b2e046b`  
		Last Modified: Wed, 06 Mar 2024 04:49:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21979e52cf569da9d1ca16c13ba7cadf068e3d0af36e6864cb518352191009e0`  
		Last Modified: Wed, 06 Mar 2024 04:49:48 GMT  
		Size: 82.8 MB (82844860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc557ba7379579a08b2dabcc6bb9a358d34de5a1d4ab4a6dbcd905a4ccf7a93`  
		Last Modified: Wed, 06 Mar 2024 04:49:40 GMT  
		Size: 297.8 KB (297812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167f55e60982941a94e2c52ee255fbcc15677fea931cc30658f05bf3410dbbdb`  
		Last Modified: Wed, 06 Mar 2024 04:49:39 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788e377e2a2bd9912a433ca23ee48613e4122b8d7a2035c06f344264f4fb431e`  
		Last Modified: Wed, 06 Mar 2024 04:49:44 GMT  
		Size: 23.1 MB (23120349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:c370c6c60a41262f443d08938ba73af46d985a56f44584cb2fe84b18656edf5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:f75b68e82aaecb885455f6ae890200a529639200942e6900c73f89e55fde9e83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159721505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e45bbed2800b1f74abcf89b3acb8acc1bd8f2506003217a97196114c336961`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:50:10 GMT
ENV ROS_DISTRO=iron
# Wed, 06 Mar 2024 04:50:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:50:59 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:50:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:51:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e8e3ea014906f3a7c3e83d63e916e71430408df8cc6ca0b1b428cb5a7f7456`  
		Last Modified: Wed, 06 Mar 2024 05:03:20 GMT  
		Size: 124.2 MB (124224432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a7cc6de96d628a75624552fc6df79665be5f96ede7dd447f5eecddd16adcf7`  
		Last Modified: Wed, 06 Mar 2024 05:03:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:267dea038d7fced087c3edbde4d9219feb2a8038553c0dae0d860e4d1bb9aeef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155134466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc292c361dfaa504db2e83de554e13b6c3e19bfa63dc10e806388997594c064`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:36:56 GMT
ENV ROS_DISTRO=iron
# Wed, 06 Mar 2024 04:37:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:37:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:37:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:37:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94163e2e56dff6bcf8394dcf0c51e0c1e05f7d35905bf61f7868375517678a69`  
		Last Modified: Wed, 06 Mar 2024 04:49:30 GMT  
		Size: 121.7 MB (121715975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1a09d4269a9877c1e165e1c2c52b60e6d81faf469d4acea17a4e625b2e046b`  
		Last Modified: Wed, 06 Mar 2024 04:49:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-core-jammy`

```console
$ docker pull ros@sha256:c370c6c60a41262f443d08938ba73af46d985a56f44584cb2fe84b18656edf5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:f75b68e82aaecb885455f6ae890200a529639200942e6900c73f89e55fde9e83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159721505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e45bbed2800b1f74abcf89b3acb8acc1bd8f2506003217a97196114c336961`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:50:10 GMT
ENV ROS_DISTRO=iron
# Wed, 06 Mar 2024 04:50:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:50:59 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:50:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:51:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e8e3ea014906f3a7c3e83d63e916e71430408df8cc6ca0b1b428cb5a7f7456`  
		Last Modified: Wed, 06 Mar 2024 05:03:20 GMT  
		Size: 124.2 MB (124224432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a7cc6de96d628a75624552fc6df79665be5f96ede7dd447f5eecddd16adcf7`  
		Last Modified: Wed, 06 Mar 2024 05:03:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:267dea038d7fced087c3edbde4d9219feb2a8038553c0dae0d860e4d1bb9aeef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155134466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc292c361dfaa504db2e83de554e13b6c3e19bfa63dc10e806388997594c064`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:36:56 GMT
ENV ROS_DISTRO=iron
# Wed, 06 Mar 2024 04:37:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:37:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:37:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:37:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94163e2e56dff6bcf8394dcf0c51e0c1e05f7d35905bf61f7868375517678a69`  
		Last Modified: Wed, 06 Mar 2024 04:49:30 GMT  
		Size: 121.7 MB (121715975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1a09d4269a9877c1e165e1c2c52b60e6d81faf469d4acea17a4e625b2e046b`  
		Last Modified: Wed, 06 Mar 2024 04:49:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:latest`

```console
$ docker pull ros@sha256:00d5355a13ddb300eab3eff6dd8287ddd000f11c203efd3ac2f1aa22b009b459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:05b3e7f3c895c60e9469c91d0271976ecd7055b5ae1eb6cb9d0ecc0e9b4dbf09
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263545173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47cf82a0a3b25e52463e4179c42af1efd18c4d9ae620a0df573d8e673f75aba1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV ROS_DISTRO=humble
# Wed, 06 Mar 2024 04:40:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:40:28 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:40:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:40:28 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:41:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:41:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:42:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c808dc8041d8a08e842df47732a8a08f550dd01f260447bb4f7d07cd5c9a1cd`  
		Last Modified: Wed, 06 Mar 2024 05:00:46 GMT  
		Size: 106.5 MB (106474978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fe6ecab2306edbc241045147aabc2f3c32a7b958e13590a65d0de0ab8bcefa`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b4f32e4504417ca1e106aa1bfda41d44c9cdc4f0aec4ae1fc8d26593debc6c`  
		Last Modified: Wed, 06 Mar 2024 05:01:07 GMT  
		Size: 98.1 MB (98138476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0775ae3bc65d52e84e7136bdb7663bf1e1c0ec3b416b29d953d41c3759b464ba`  
		Last Modified: Wed, 06 Mar 2024 05:00:54 GMT  
		Size: 331.1 KB (331145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268e8e2f7cd13633d7af262b5ace2a4d9bb67e72a22c9c2edb09675f9cb55270`  
		Last Modified: Wed, 06 Mar 2024 05:00:54 GMT  
		Size: 2.5 KB (2500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4339e166fc83d67a3d7b94d17e59c0859e045120689720637aada3df371c7f`  
		Last Modified: Wed, 06 Mar 2024 05:00:57 GMT  
		Size: 23.1 MB (23101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d620458704bfe1d2fd2f87073427bc7486c0c6e2b04fccd256de8e53c870a7ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256152936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6f17c2aa477132e1d5386bc8a583fd9e168935a9456624321a5670c9d58e14`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV ROS_DISTRO=humble
# Wed, 06 Mar 2024 04:25:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:25:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:25:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:25:02 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:26:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:26:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:26:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3eb2e67a0ee0642539e9d0fa629f2696ed7e1bf68d5718f0f0d34a541a9afaa`  
		Last Modified: Wed, 06 Mar 2024 04:46:59 GMT  
		Size: 104.2 MB (104195832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12122adf1664bd4b96bc0459e52dd0d65a90e0569bd8452f4e4bfaa693611e22`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf21c988284258171de1e605ee3f1700216eba121998c9adbfc92831666888b`  
		Last Modified: Wed, 06 Mar 2024 04:47:20 GMT  
		Size: 95.7 MB (95685185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25894b282822606f5b2e64d41cea219409ba94a685ae8860acf9c924dcfedbcc`  
		Last Modified: Wed, 06 Mar 2024 04:47:08 GMT  
		Size: 331.1 KB (331148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9edf1c5d6eb51cde5a703b4b0d5f2c69eb275ae5ef4e1ff4f7fea5a0f58b81a`  
		Last Modified: Wed, 06 Mar 2024 04:47:08 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa2e80e8cab55dd73c4158423e5d52e5bebfdab597b2e0473f63f2837200b5`  
		Last Modified: Wed, 06 Mar 2024 04:47:12 GMT  
		Size: 22.5 MB (22519781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic`

```console
$ docker pull ros@sha256:052f161fe3c356f7e9a6b84a786635efcea992af12d638c202b593af04de8c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:0079c89a0b83b2a9bc8df635ba6e417cc70341fdc28b58b6107b8ee115aff90b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264727097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d27c296d320dd5e72294985860d6b8aee0e24e7e447e49c53b5b6d1a336f285`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:18:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:19:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:31:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:31:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 04:31:17 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:31:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:31:17 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 04:32:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:32:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 04:32:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:32:39 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:33:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:33:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:33:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b717a9d4ad213e59d73577a626c9c9093b2e6bf2dd493fc3fee4c33f9db601`  
		Last Modified: Wed, 06 Mar 2024 04:27:10 GMT  
		Size: 1.2 MB (1198476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f5ecd5001c5e4c5758fef666edcd4e26272b0cfecf06a567b8ad6584e6eabb`  
		Last Modified: Wed, 06 Mar 2024 04:27:08 GMT  
		Size: 5.6 MB (5553760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e87f945a5b1504b35e47df2fa6a203a1450bace36c3431c267361ae8ff84923`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c85c9351d67b117f6445876b30cb2a165a86b20103f9256f257a13974eee0e6`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5048c3edf0e27dbeab1cd05a3ad923ca803ea5b1489d6a0811eeb392549d3272`  
		Last Modified: Wed, 06 Mar 2024 04:58:22 GMT  
		Size: 177.0 MB (176998267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6dd23d624167f78a9fcbc142d6f13ff19d0598456e12c4c6048d541f6726f7`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e54e59330e9a8f9d250b062121a852c8a375d755bca20b39794ea2bd92f3e78`  
		Last Modified: Wed, 06 Mar 2024 04:58:38 GMT  
		Size: 50.9 MB (50942039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ddf4fbb020496e4eaaf355a6cd2a24b481295beffeb19738591d417c3c51a9`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 317.1 KB (317112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11354471cad5084e7d4a54163b6875984b80aae53f1b22226e60250b6f14b465`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 1.1 MB (1130634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:962f66ef1fb5e89c2defb0d9292396bc824c07d73b993906c6dd3dcacbe4edee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229837192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81aebcf2c59e23191c160390b401ff59cf5857e2eb0507ee07d0e010919d3d86`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:27:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:28:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:28:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 02:28:22 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 02:28:22 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 02:28:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 02:28:23 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 02:31:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:31:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 02:32:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 02:32:00 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 02:32:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:32:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 02:33:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a57ab8f3f909fb2a530a207c0b93b306ab27641c9c91ca7906af7d1eb85594c3`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 24.6 MB (24601340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa9329034da92c594d47e3dace53a9ceff3cbeffa063b398a0d6255e08c1ed8`  
		Last Modified: Wed, 06 Mar 2024 02:45:16 GMT  
		Size: 1.2 MB (1198533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28b7f93477437a2a60ecdc7208404196973f7489c9fbb4704c58d401443db90`  
		Last Modified: Wed, 06 Mar 2024 02:45:13 GMT  
		Size: 4.7 MB (4679331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456a7f559bad5c045a80841a7b566f694cf537d0b919d83634aa980087d81c4c`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef809d2cd923bd111a9311e0912e4f8006c77cf10b170e268441d064a962046`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a0d81a0257ef7784cc06c5b65d2ba804e66fa7593392ae04f04a64a4cad67c`  
		Last Modified: Wed, 06 Mar 2024 02:45:54 GMT  
		Size: 157.5 MB (157471632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0af84a8ac32154d956f99bd2ff4dc677f612db38d7e41b50ce908386d2fdb68`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b832bc149615378810f4a9fe40729770ad9dba7a7c228e62d356c50099736428`  
		Last Modified: Wed, 06 Mar 2024 02:46:09 GMT  
		Size: 40.5 MB (40505317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefdce4a2b8116db5f3f6152d30787df0a9c52fded830a5320b2269895938171`  
		Last Modified: Wed, 06 Mar 2024 02:46:03 GMT  
		Size: 317.1 KB (317110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e455f7807a21a05976ec00cb49130c7b2d93e058e90a6d16d04dbc3aa81696`  
		Last Modified: Wed, 06 Mar 2024 02:46:03 GMT  
		Size: 1.1 MB (1061437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b6ef817d5656642cbe1ee562a8a8375855b2e88c231f5ad95dcfb5d1e8837fc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251978011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bea440a091d3e9b7efec94ad5662096ef0a1363dcb32ff70504dddfb04738a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:30 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:10:30 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 04:10:30 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:10:30 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:10:30 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 04:12:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:12:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 04:12:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:12:42 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:12:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:13:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:13:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79dec5d4c4cd04e1e0085fdbe98bf2ecf754da7fe38a4cecb6c07bc9455520e9`  
		Last Modified: Wed, 06 Mar 2024 04:44:09 GMT  
		Size: 1.2 MB (1198548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f06f20f5ca5422d55808ff5eeea0324d21312c719c44cf7782e1d0a00db2a4`  
		Last Modified: Wed, 06 Mar 2024 04:44:08 GMT  
		Size: 5.5 MB (5532073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f2e3537c72de5ae529b44b0b0f1a0d17d3a4ba5e285f7c3a51fde2c93b95dc`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c1b7297f025d37b4fc703b337051c633da9de7f426f7d5f1b812e95f276e09`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a49a29ad0e0140da135daa347b774207b84e124d9cc64016207e77aaf40c3f7`  
		Last Modified: Wed, 06 Mar 2024 04:44:41 GMT  
		Size: 171.4 MB (171401255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93185f06229eeeafb914e15cd877669230a929a660d09bbaef30e423a05fcc82`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c690c1ca3d85a61d8f3e87d84817be0932b2873f0785d6d61d64d3f54a7137`  
		Last Modified: Wed, 06 Mar 2024 04:44:55 GMT  
		Size: 45.2 MB (45207349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de39e35aab238ae9a046045f0be90350874ce4e999a82a14fa6b1ae0e3616cab`  
		Last Modified: Wed, 06 Mar 2024 04:44:50 GMT  
		Size: 317.1 KB (317112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b89ab41d60352f77ccd8e2a2d80710850509070284e9dc6792a405b578dc1b`  
		Last Modified: Wed, 06 Mar 2024 04:44:50 GMT  
		Size: 1.1 MB (1114895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:2ea2d2daf28a4be8cf8138792d50526a587e82da0d0a9950b1efdceda7a4fc1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:24d68148eea081dd8b8ddabea91dbaeefbaa259433a585789dcaff46325f7114
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.2 MB (835219651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b83a16ebf4c9d7b2f2dc882e36fa18644f75fcc35d0d0fa5f09ebfbfb4f7ef3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:18:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:19:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:31:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:31:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 04:31:17 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:31:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:31:17 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 04:32:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:32:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 04:32:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:32:39 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:33:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:33:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:33:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b717a9d4ad213e59d73577a626c9c9093b2e6bf2dd493fc3fee4c33f9db601`  
		Last Modified: Wed, 06 Mar 2024 04:27:10 GMT  
		Size: 1.2 MB (1198476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f5ecd5001c5e4c5758fef666edcd4e26272b0cfecf06a567b8ad6584e6eabb`  
		Last Modified: Wed, 06 Mar 2024 04:27:08 GMT  
		Size: 5.6 MB (5553760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e87f945a5b1504b35e47df2fa6a203a1450bace36c3431c267361ae8ff84923`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c85c9351d67b117f6445876b30cb2a165a86b20103f9256f257a13974eee0e6`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5048c3edf0e27dbeab1cd05a3ad923ca803ea5b1489d6a0811eeb392549d3272`  
		Last Modified: Wed, 06 Mar 2024 04:58:22 GMT  
		Size: 177.0 MB (176998267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6dd23d624167f78a9fcbc142d6f13ff19d0598456e12c4c6048d541f6726f7`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e54e59330e9a8f9d250b062121a852c8a375d755bca20b39794ea2bd92f3e78`  
		Last Modified: Wed, 06 Mar 2024 04:58:38 GMT  
		Size: 50.9 MB (50942039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ddf4fbb020496e4eaaf355a6cd2a24b481295beffeb19738591d417c3c51a9`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 317.1 KB (317112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11354471cad5084e7d4a54163b6875984b80aae53f1b22226e60250b6f14b465`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 1.1 MB (1130634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5255159392436789f89a4054e639b6e1707c49e38e1f1a92f713cc3c07d774d6`  
		Last Modified: Wed, 06 Mar 2024 05:00:21 GMT  
		Size: 570.5 MB (570492554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:9ce23ca0160e6c8103116c5b8cb64e9675feecd931a6a5471d7aac119c6d3cb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.2 MB (726218440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db7e317d856dff1ba8cb75151e6ca692cd462fc1e64f572d0c748fa0666bee0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:27:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:28:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:28:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 02:28:22 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 02:28:22 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 02:28:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 02:28:23 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 02:31:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:31:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 02:32:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 02:32:00 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 02:32:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:32:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 02:33:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:44:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a57ab8f3f909fb2a530a207c0b93b306ab27641c9c91ca7906af7d1eb85594c3`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 24.6 MB (24601340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa9329034da92c594d47e3dace53a9ceff3cbeffa063b398a0d6255e08c1ed8`  
		Last Modified: Wed, 06 Mar 2024 02:45:16 GMT  
		Size: 1.2 MB (1198533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28b7f93477437a2a60ecdc7208404196973f7489c9fbb4704c58d401443db90`  
		Last Modified: Wed, 06 Mar 2024 02:45:13 GMT  
		Size: 4.7 MB (4679331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456a7f559bad5c045a80841a7b566f694cf537d0b919d83634aa980087d81c4c`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef809d2cd923bd111a9311e0912e4f8006c77cf10b170e268441d064a962046`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a0d81a0257ef7784cc06c5b65d2ba804e66fa7593392ae04f04a64a4cad67c`  
		Last Modified: Wed, 06 Mar 2024 02:45:54 GMT  
		Size: 157.5 MB (157471632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0af84a8ac32154d956f99bd2ff4dc677f612db38d7e41b50ce908386d2fdb68`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b832bc149615378810f4a9fe40729770ad9dba7a7c228e62d356c50099736428`  
		Last Modified: Wed, 06 Mar 2024 02:46:09 GMT  
		Size: 40.5 MB (40505317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefdce4a2b8116db5f3f6152d30787df0a9c52fded830a5320b2269895938171`  
		Last Modified: Wed, 06 Mar 2024 02:46:03 GMT  
		Size: 317.1 KB (317110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e455f7807a21a05976ec00cb49130c7b2d93e058e90a6d16d04dbc3aa81696`  
		Last Modified: Wed, 06 Mar 2024 02:46:03 GMT  
		Size: 1.1 MB (1061437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8d30e0606ce27fd291d8167034e47a6d2aa920bbe64f21eae76d07174e76e0`  
		Last Modified: Wed, 06 Mar 2024 02:47:57 GMT  
		Size: 496.4 MB (496381248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a36bb43bec3718d7b6b9438fcb6383400204b811d7cee6c1f1bcae434d92f455
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.5 MB (785467683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f53d8d7f193ecf16fe38aaa4eb475165ff1697ea44b6b61a1347144149fc66`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:30 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:10:30 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 04:10:30 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:10:30 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:10:30 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 04:12:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:12:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 04:12:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:12:42 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:12:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:13:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:13:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:22:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79dec5d4c4cd04e1e0085fdbe98bf2ecf754da7fe38a4cecb6c07bc9455520e9`  
		Last Modified: Wed, 06 Mar 2024 04:44:09 GMT  
		Size: 1.2 MB (1198548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f06f20f5ca5422d55808ff5eeea0324d21312c719c44cf7782e1d0a00db2a4`  
		Last Modified: Wed, 06 Mar 2024 04:44:08 GMT  
		Size: 5.5 MB (5532073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f2e3537c72de5ae529b44b0b0f1a0d17d3a4ba5e285f7c3a51fde2c93b95dc`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c1b7297f025d37b4fc703b337051c633da9de7f426f7d5f1b812e95f276e09`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a49a29ad0e0140da135daa347b774207b84e124d9cc64016207e77aaf40c3f7`  
		Last Modified: Wed, 06 Mar 2024 04:44:41 GMT  
		Size: 171.4 MB (171401255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93185f06229eeeafb914e15cd877669230a929a660d09bbaef30e423a05fcc82`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c690c1ca3d85a61d8f3e87d84817be0932b2873f0785d6d61d64d3f54a7137`  
		Last Modified: Wed, 06 Mar 2024 04:44:55 GMT  
		Size: 45.2 MB (45207349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de39e35aab238ae9a046045f0be90350874ce4e999a82a14fa6b1ae0e3616cab`  
		Last Modified: Wed, 06 Mar 2024 04:44:50 GMT  
		Size: 317.1 KB (317112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b89ab41d60352f77ccd8e2a2d80710850509070284e9dc6792a405b578dc1b`  
		Last Modified: Wed, 06 Mar 2024 04:44:50 GMT  
		Size: 1.1 MB (1114895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9d2daa20df3657295834721a85f09970bfe42b9cd4f9c163963124f230597e`  
		Last Modified: Wed, 06 Mar 2024 04:46:29 GMT  
		Size: 533.5 MB (533489672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:2ea2d2daf28a4be8cf8138792d50526a587e82da0d0a9950b1efdceda7a4fc1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:24d68148eea081dd8b8ddabea91dbaeefbaa259433a585789dcaff46325f7114
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.2 MB (835219651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b83a16ebf4c9d7b2f2dc882e36fa18644f75fcc35d0d0fa5f09ebfbfb4f7ef3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:18:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:19:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:31:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:31:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 04:31:17 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:31:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:31:17 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 04:32:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:32:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 04:32:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:32:39 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:33:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:33:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:33:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b717a9d4ad213e59d73577a626c9c9093b2e6bf2dd493fc3fee4c33f9db601`  
		Last Modified: Wed, 06 Mar 2024 04:27:10 GMT  
		Size: 1.2 MB (1198476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f5ecd5001c5e4c5758fef666edcd4e26272b0cfecf06a567b8ad6584e6eabb`  
		Last Modified: Wed, 06 Mar 2024 04:27:08 GMT  
		Size: 5.6 MB (5553760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e87f945a5b1504b35e47df2fa6a203a1450bace36c3431c267361ae8ff84923`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c85c9351d67b117f6445876b30cb2a165a86b20103f9256f257a13974eee0e6`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5048c3edf0e27dbeab1cd05a3ad923ca803ea5b1489d6a0811eeb392549d3272`  
		Last Modified: Wed, 06 Mar 2024 04:58:22 GMT  
		Size: 177.0 MB (176998267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6dd23d624167f78a9fcbc142d6f13ff19d0598456e12c4c6048d541f6726f7`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e54e59330e9a8f9d250b062121a852c8a375d755bca20b39794ea2bd92f3e78`  
		Last Modified: Wed, 06 Mar 2024 04:58:38 GMT  
		Size: 50.9 MB (50942039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ddf4fbb020496e4eaaf355a6cd2a24b481295beffeb19738591d417c3c51a9`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 317.1 KB (317112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11354471cad5084e7d4a54163b6875984b80aae53f1b22226e60250b6f14b465`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 1.1 MB (1130634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5255159392436789f89a4054e639b6e1707c49e38e1f1a92f713cc3c07d774d6`  
		Last Modified: Wed, 06 Mar 2024 05:00:21 GMT  
		Size: 570.5 MB (570492554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:9ce23ca0160e6c8103116c5b8cb64e9675feecd931a6a5471d7aac119c6d3cb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.2 MB (726218440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db7e317d856dff1ba8cb75151e6ca692cd462fc1e64f572d0c748fa0666bee0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:27:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:28:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:28:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 02:28:22 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 02:28:22 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 02:28:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 02:28:23 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 02:31:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:31:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 02:32:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 02:32:00 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 02:32:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:32:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 02:33:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:44:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a57ab8f3f909fb2a530a207c0b93b306ab27641c9c91ca7906af7d1eb85594c3`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 24.6 MB (24601340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa9329034da92c594d47e3dace53a9ceff3cbeffa063b398a0d6255e08c1ed8`  
		Last Modified: Wed, 06 Mar 2024 02:45:16 GMT  
		Size: 1.2 MB (1198533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28b7f93477437a2a60ecdc7208404196973f7489c9fbb4704c58d401443db90`  
		Last Modified: Wed, 06 Mar 2024 02:45:13 GMT  
		Size: 4.7 MB (4679331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456a7f559bad5c045a80841a7b566f694cf537d0b919d83634aa980087d81c4c`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef809d2cd923bd111a9311e0912e4f8006c77cf10b170e268441d064a962046`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a0d81a0257ef7784cc06c5b65d2ba804e66fa7593392ae04f04a64a4cad67c`  
		Last Modified: Wed, 06 Mar 2024 02:45:54 GMT  
		Size: 157.5 MB (157471632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0af84a8ac32154d956f99bd2ff4dc677f612db38d7e41b50ce908386d2fdb68`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b832bc149615378810f4a9fe40729770ad9dba7a7c228e62d356c50099736428`  
		Last Modified: Wed, 06 Mar 2024 02:46:09 GMT  
		Size: 40.5 MB (40505317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefdce4a2b8116db5f3f6152d30787df0a9c52fded830a5320b2269895938171`  
		Last Modified: Wed, 06 Mar 2024 02:46:03 GMT  
		Size: 317.1 KB (317110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e455f7807a21a05976ec00cb49130c7b2d93e058e90a6d16d04dbc3aa81696`  
		Last Modified: Wed, 06 Mar 2024 02:46:03 GMT  
		Size: 1.1 MB (1061437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8d30e0606ce27fd291d8167034e47a6d2aa920bbe64f21eae76d07174e76e0`  
		Last Modified: Wed, 06 Mar 2024 02:47:57 GMT  
		Size: 496.4 MB (496381248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a36bb43bec3718d7b6b9438fcb6383400204b811d7cee6c1f1bcae434d92f455
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.5 MB (785467683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f53d8d7f193ecf16fe38aaa4eb475165ff1697ea44b6b61a1347144149fc66`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:30 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:10:30 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 04:10:30 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:10:30 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:10:30 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 04:12:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:12:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 04:12:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:12:42 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:12:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:13:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:13:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:22:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79dec5d4c4cd04e1e0085fdbe98bf2ecf754da7fe38a4cecb6c07bc9455520e9`  
		Last Modified: Wed, 06 Mar 2024 04:44:09 GMT  
		Size: 1.2 MB (1198548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f06f20f5ca5422d55808ff5eeea0324d21312c719c44cf7782e1d0a00db2a4`  
		Last Modified: Wed, 06 Mar 2024 04:44:08 GMT  
		Size: 5.5 MB (5532073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f2e3537c72de5ae529b44b0b0f1a0d17d3a4ba5e285f7c3a51fde2c93b95dc`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c1b7297f025d37b4fc703b337051c633da9de7f426f7d5f1b812e95f276e09`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a49a29ad0e0140da135daa347b774207b84e124d9cc64016207e77aaf40c3f7`  
		Last Modified: Wed, 06 Mar 2024 04:44:41 GMT  
		Size: 171.4 MB (171401255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93185f06229eeeafb914e15cd877669230a929a660d09bbaef30e423a05fcc82`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c690c1ca3d85a61d8f3e87d84817be0932b2873f0785d6d61d64d3f54a7137`  
		Last Modified: Wed, 06 Mar 2024 04:44:55 GMT  
		Size: 45.2 MB (45207349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de39e35aab238ae9a046045f0be90350874ce4e999a82a14fa6b1ae0e3616cab`  
		Last Modified: Wed, 06 Mar 2024 04:44:50 GMT  
		Size: 317.1 KB (317112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b89ab41d60352f77ccd8e2a2d80710850509070284e9dc6792a405b578dc1b`  
		Last Modified: Wed, 06 Mar 2024 04:44:50 GMT  
		Size: 1.1 MB (1114895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9d2daa20df3657295834721a85f09970bfe42b9cd4f9c163963124f230597e`  
		Last Modified: Wed, 06 Mar 2024 04:46:29 GMT  
		Size: 533.5 MB (533489672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:8fcd1714ac4cf42129b8f356e5fa086ed7079c1f5f26354ae5503bd45cf179c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:24e67104fe28b94af01dce4f6f004365e262f9b905fdca76c5bbeb2d42cae5a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.7 MB (281655534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09cd3d5f4978b8c20a7042bf6f26a2af4471cd37a1d62fbe187e7abb1c40626`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:18:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:19:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:31:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:31:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 04:31:17 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:31:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:31:17 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 04:32:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:32:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 04:32:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:32:39 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:33:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:33:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:33:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:34:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b717a9d4ad213e59d73577a626c9c9093b2e6bf2dd493fc3fee4c33f9db601`  
		Last Modified: Wed, 06 Mar 2024 04:27:10 GMT  
		Size: 1.2 MB (1198476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f5ecd5001c5e4c5758fef666edcd4e26272b0cfecf06a567b8ad6584e6eabb`  
		Last Modified: Wed, 06 Mar 2024 04:27:08 GMT  
		Size: 5.6 MB (5553760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e87f945a5b1504b35e47df2fa6a203a1450bace36c3431c267361ae8ff84923`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c85c9351d67b117f6445876b30cb2a165a86b20103f9256f257a13974eee0e6`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5048c3edf0e27dbeab1cd05a3ad923ca803ea5b1489d6a0811eeb392549d3272`  
		Last Modified: Wed, 06 Mar 2024 04:58:22 GMT  
		Size: 177.0 MB (176998267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6dd23d624167f78a9fcbc142d6f13ff19d0598456e12c4c6048d541f6726f7`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e54e59330e9a8f9d250b062121a852c8a375d755bca20b39794ea2bd92f3e78`  
		Last Modified: Wed, 06 Mar 2024 04:58:38 GMT  
		Size: 50.9 MB (50942039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ddf4fbb020496e4eaaf355a6cd2a24b481295beffeb19738591d417c3c51a9`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 317.1 KB (317112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11354471cad5084e7d4a54163b6875984b80aae53f1b22226e60250b6f14b465`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 1.1 MB (1130634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29869988c179364bef5cd7800a92a966ac038f145e150129225e9e01511b1aa3`  
		Last Modified: Wed, 06 Mar 2024 04:58:51 GMT  
		Size: 16.9 MB (16928437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:84bd53d5fb99d4af793fdb438025a5293c40577a9c35b649028d23ad074093b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244865979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f539360876ae7855a57fbe88db9cee075f0ea4d2f08f9aab475a20a8568e1b0b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:27:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:28:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:28:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 02:28:22 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 02:28:22 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 02:28:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 02:28:23 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 02:31:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:31:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 02:32:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 02:32:00 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 02:32:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:32:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 02:33:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:34:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a57ab8f3f909fb2a530a207c0b93b306ab27641c9c91ca7906af7d1eb85594c3`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 24.6 MB (24601340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa9329034da92c594d47e3dace53a9ceff3cbeffa063b398a0d6255e08c1ed8`  
		Last Modified: Wed, 06 Mar 2024 02:45:16 GMT  
		Size: 1.2 MB (1198533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28b7f93477437a2a60ecdc7208404196973f7489c9fbb4704c58d401443db90`  
		Last Modified: Wed, 06 Mar 2024 02:45:13 GMT  
		Size: 4.7 MB (4679331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456a7f559bad5c045a80841a7b566f694cf537d0b919d83634aa980087d81c4c`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef809d2cd923bd111a9311e0912e4f8006c77cf10b170e268441d064a962046`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a0d81a0257ef7784cc06c5b65d2ba804e66fa7593392ae04f04a64a4cad67c`  
		Last Modified: Wed, 06 Mar 2024 02:45:54 GMT  
		Size: 157.5 MB (157471632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0af84a8ac32154d956f99bd2ff4dc677f612db38d7e41b50ce908386d2fdb68`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b832bc149615378810f4a9fe40729770ad9dba7a7c228e62d356c50099736428`  
		Last Modified: Wed, 06 Mar 2024 02:46:09 GMT  
		Size: 40.5 MB (40505317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefdce4a2b8116db5f3f6152d30787df0a9c52fded830a5320b2269895938171`  
		Last Modified: Wed, 06 Mar 2024 02:46:03 GMT  
		Size: 317.1 KB (317110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e455f7807a21a05976ec00cb49130c7b2d93e058e90a6d16d04dbc3aa81696`  
		Last Modified: Wed, 06 Mar 2024 02:46:03 GMT  
		Size: 1.1 MB (1061437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6abed4124b592bb43be293c9c3b4f53f88c163fa07aa2aa13d873949466a8d4`  
		Last Modified: Wed, 06 Mar 2024 02:46:24 GMT  
		Size: 15.0 MB (15028787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9d21581a4c9a36b29b4bbd159fcd57589005862e2b4f962d52b2bbc0f22b0f1b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268508378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27561b05b5f6469d5b8b84f0c3164f85adec4f71373132a153213dad3ee9ce11`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:30 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:10:30 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 04:10:30 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:10:30 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:10:30 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 04:12:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:12:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 04:12:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:12:42 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:12:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:13:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:13:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:13:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79dec5d4c4cd04e1e0085fdbe98bf2ecf754da7fe38a4cecb6c07bc9455520e9`  
		Last Modified: Wed, 06 Mar 2024 04:44:09 GMT  
		Size: 1.2 MB (1198548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f06f20f5ca5422d55808ff5eeea0324d21312c719c44cf7782e1d0a00db2a4`  
		Last Modified: Wed, 06 Mar 2024 04:44:08 GMT  
		Size: 5.5 MB (5532073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f2e3537c72de5ae529b44b0b0f1a0d17d3a4ba5e285f7c3a51fde2c93b95dc`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c1b7297f025d37b4fc703b337051c633da9de7f426f7d5f1b812e95f276e09`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a49a29ad0e0140da135daa347b774207b84e124d9cc64016207e77aaf40c3f7`  
		Last Modified: Wed, 06 Mar 2024 04:44:41 GMT  
		Size: 171.4 MB (171401255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93185f06229eeeafb914e15cd877669230a929a660d09bbaef30e423a05fcc82`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c690c1ca3d85a61d8f3e87d84817be0932b2873f0785d6d61d64d3f54a7137`  
		Last Modified: Wed, 06 Mar 2024 04:44:55 GMT  
		Size: 45.2 MB (45207349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de39e35aab238ae9a046045f0be90350874ce4e999a82a14fa6b1ae0e3616cab`  
		Last Modified: Wed, 06 Mar 2024 04:44:50 GMT  
		Size: 317.1 KB (317112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b89ab41d60352f77ccd8e2a2d80710850509070284e9dc6792a405b578dc1b`  
		Last Modified: Wed, 06 Mar 2024 04:44:50 GMT  
		Size: 1.1 MB (1114895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c495fc356f7e15796cb114a32593102554752b1fe13b4c748a2391d7e9b20a32`  
		Last Modified: Wed, 06 Mar 2024 04:45:10 GMT  
		Size: 16.5 MB (16530367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:8fcd1714ac4cf42129b8f356e5fa086ed7079c1f5f26354ae5503bd45cf179c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:24e67104fe28b94af01dce4f6f004365e262f9b905fdca76c5bbeb2d42cae5a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.7 MB (281655534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09cd3d5f4978b8c20a7042bf6f26a2af4471cd37a1d62fbe187e7abb1c40626`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:18:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:19:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:31:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:31:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 04:31:17 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:31:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:31:17 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 04:32:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:32:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 04:32:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:32:39 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:33:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:33:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:33:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:34:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b717a9d4ad213e59d73577a626c9c9093b2e6bf2dd493fc3fee4c33f9db601`  
		Last Modified: Wed, 06 Mar 2024 04:27:10 GMT  
		Size: 1.2 MB (1198476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f5ecd5001c5e4c5758fef666edcd4e26272b0cfecf06a567b8ad6584e6eabb`  
		Last Modified: Wed, 06 Mar 2024 04:27:08 GMT  
		Size: 5.6 MB (5553760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e87f945a5b1504b35e47df2fa6a203a1450bace36c3431c267361ae8ff84923`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c85c9351d67b117f6445876b30cb2a165a86b20103f9256f257a13974eee0e6`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5048c3edf0e27dbeab1cd05a3ad923ca803ea5b1489d6a0811eeb392549d3272`  
		Last Modified: Wed, 06 Mar 2024 04:58:22 GMT  
		Size: 177.0 MB (176998267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6dd23d624167f78a9fcbc142d6f13ff19d0598456e12c4c6048d541f6726f7`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e54e59330e9a8f9d250b062121a852c8a375d755bca20b39794ea2bd92f3e78`  
		Last Modified: Wed, 06 Mar 2024 04:58:38 GMT  
		Size: 50.9 MB (50942039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ddf4fbb020496e4eaaf355a6cd2a24b481295beffeb19738591d417c3c51a9`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 317.1 KB (317112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11354471cad5084e7d4a54163b6875984b80aae53f1b22226e60250b6f14b465`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 1.1 MB (1130634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29869988c179364bef5cd7800a92a966ac038f145e150129225e9e01511b1aa3`  
		Last Modified: Wed, 06 Mar 2024 04:58:51 GMT  
		Size: 16.9 MB (16928437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:84bd53d5fb99d4af793fdb438025a5293c40577a9c35b649028d23ad074093b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244865979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f539360876ae7855a57fbe88db9cee075f0ea4d2f08f9aab475a20a8568e1b0b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:27:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:28:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:28:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 02:28:22 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 02:28:22 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 02:28:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 02:28:23 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 02:31:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:31:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 02:32:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 02:32:00 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 02:32:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:32:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 02:33:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:34:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a57ab8f3f909fb2a530a207c0b93b306ab27641c9c91ca7906af7d1eb85594c3`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 24.6 MB (24601340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa9329034da92c594d47e3dace53a9ceff3cbeffa063b398a0d6255e08c1ed8`  
		Last Modified: Wed, 06 Mar 2024 02:45:16 GMT  
		Size: 1.2 MB (1198533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28b7f93477437a2a60ecdc7208404196973f7489c9fbb4704c58d401443db90`  
		Last Modified: Wed, 06 Mar 2024 02:45:13 GMT  
		Size: 4.7 MB (4679331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456a7f559bad5c045a80841a7b566f694cf537d0b919d83634aa980087d81c4c`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef809d2cd923bd111a9311e0912e4f8006c77cf10b170e268441d064a962046`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a0d81a0257ef7784cc06c5b65d2ba804e66fa7593392ae04f04a64a4cad67c`  
		Last Modified: Wed, 06 Mar 2024 02:45:54 GMT  
		Size: 157.5 MB (157471632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0af84a8ac32154d956f99bd2ff4dc677f612db38d7e41b50ce908386d2fdb68`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b832bc149615378810f4a9fe40729770ad9dba7a7c228e62d356c50099736428`  
		Last Modified: Wed, 06 Mar 2024 02:46:09 GMT  
		Size: 40.5 MB (40505317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefdce4a2b8116db5f3f6152d30787df0a9c52fded830a5320b2269895938171`  
		Last Modified: Wed, 06 Mar 2024 02:46:03 GMT  
		Size: 317.1 KB (317110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e455f7807a21a05976ec00cb49130c7b2d93e058e90a6d16d04dbc3aa81696`  
		Last Modified: Wed, 06 Mar 2024 02:46:03 GMT  
		Size: 1.1 MB (1061437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6abed4124b592bb43be293c9c3b4f53f88c163fa07aa2aa13d873949466a8d4`  
		Last Modified: Wed, 06 Mar 2024 02:46:24 GMT  
		Size: 15.0 MB (15028787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9d21581a4c9a36b29b4bbd159fcd57589005862e2b4f962d52b2bbc0f22b0f1b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268508378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27561b05b5f6469d5b8b84f0c3164f85adec4f71373132a153213dad3ee9ce11`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:30 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:10:30 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 04:10:30 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:10:30 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:10:30 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 04:12:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:12:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 04:12:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:12:42 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:12:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:13:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:13:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:13:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79dec5d4c4cd04e1e0085fdbe98bf2ecf754da7fe38a4cecb6c07bc9455520e9`  
		Last Modified: Wed, 06 Mar 2024 04:44:09 GMT  
		Size: 1.2 MB (1198548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f06f20f5ca5422d55808ff5eeea0324d21312c719c44cf7782e1d0a00db2a4`  
		Last Modified: Wed, 06 Mar 2024 04:44:08 GMT  
		Size: 5.5 MB (5532073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f2e3537c72de5ae529b44b0b0f1a0d17d3a4ba5e285f7c3a51fde2c93b95dc`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c1b7297f025d37b4fc703b337051c633da9de7f426f7d5f1b812e95f276e09`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a49a29ad0e0140da135daa347b774207b84e124d9cc64016207e77aaf40c3f7`  
		Last Modified: Wed, 06 Mar 2024 04:44:41 GMT  
		Size: 171.4 MB (171401255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93185f06229eeeafb914e15cd877669230a929a660d09bbaef30e423a05fcc82`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c690c1ca3d85a61d8f3e87d84817be0932b2873f0785d6d61d64d3f54a7137`  
		Last Modified: Wed, 06 Mar 2024 04:44:55 GMT  
		Size: 45.2 MB (45207349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de39e35aab238ae9a046045f0be90350874ce4e999a82a14fa6b1ae0e3616cab`  
		Last Modified: Wed, 06 Mar 2024 04:44:50 GMT  
		Size: 317.1 KB (317112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b89ab41d60352f77ccd8e2a2d80710850509070284e9dc6792a405b578dc1b`  
		Last Modified: Wed, 06 Mar 2024 04:44:50 GMT  
		Size: 1.1 MB (1114895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c495fc356f7e15796cb114a32593102554752b1fe13b4c748a2391d7e9b20a32`  
		Last Modified: Wed, 06 Mar 2024 04:45:10 GMT  
		Size: 16.5 MB (16530367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:052f161fe3c356f7e9a6b84a786635efcea992af12d638c202b593af04de8c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:0079c89a0b83b2a9bc8df635ba6e417cc70341fdc28b58b6107b8ee115aff90b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264727097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d27c296d320dd5e72294985860d6b8aee0e24e7e447e49c53b5b6d1a336f285`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:18:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:19:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:31:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:31:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 04:31:17 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:31:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:31:17 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 04:32:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:32:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 04:32:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:32:39 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:33:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:33:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:33:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b717a9d4ad213e59d73577a626c9c9093b2e6bf2dd493fc3fee4c33f9db601`  
		Last Modified: Wed, 06 Mar 2024 04:27:10 GMT  
		Size: 1.2 MB (1198476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f5ecd5001c5e4c5758fef666edcd4e26272b0cfecf06a567b8ad6584e6eabb`  
		Last Modified: Wed, 06 Mar 2024 04:27:08 GMT  
		Size: 5.6 MB (5553760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e87f945a5b1504b35e47df2fa6a203a1450bace36c3431c267361ae8ff84923`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c85c9351d67b117f6445876b30cb2a165a86b20103f9256f257a13974eee0e6`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5048c3edf0e27dbeab1cd05a3ad923ca803ea5b1489d6a0811eeb392549d3272`  
		Last Modified: Wed, 06 Mar 2024 04:58:22 GMT  
		Size: 177.0 MB (176998267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6dd23d624167f78a9fcbc142d6f13ff19d0598456e12c4c6048d541f6726f7`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e54e59330e9a8f9d250b062121a852c8a375d755bca20b39794ea2bd92f3e78`  
		Last Modified: Wed, 06 Mar 2024 04:58:38 GMT  
		Size: 50.9 MB (50942039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ddf4fbb020496e4eaaf355a6cd2a24b481295beffeb19738591d417c3c51a9`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 317.1 KB (317112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11354471cad5084e7d4a54163b6875984b80aae53f1b22226e60250b6f14b465`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 1.1 MB (1130634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:962f66ef1fb5e89c2defb0d9292396bc824c07d73b993906c6dd3dcacbe4edee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229837192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81aebcf2c59e23191c160390b401ff59cf5857e2eb0507ee07d0e010919d3d86`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:27:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:28:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:28:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 02:28:22 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 02:28:22 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 02:28:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 02:28:23 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 02:31:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:31:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 02:32:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 02:32:00 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 02:32:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:32:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 02:33:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a57ab8f3f909fb2a530a207c0b93b306ab27641c9c91ca7906af7d1eb85594c3`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 24.6 MB (24601340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa9329034da92c594d47e3dace53a9ceff3cbeffa063b398a0d6255e08c1ed8`  
		Last Modified: Wed, 06 Mar 2024 02:45:16 GMT  
		Size: 1.2 MB (1198533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28b7f93477437a2a60ecdc7208404196973f7489c9fbb4704c58d401443db90`  
		Last Modified: Wed, 06 Mar 2024 02:45:13 GMT  
		Size: 4.7 MB (4679331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456a7f559bad5c045a80841a7b566f694cf537d0b919d83634aa980087d81c4c`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef809d2cd923bd111a9311e0912e4f8006c77cf10b170e268441d064a962046`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a0d81a0257ef7784cc06c5b65d2ba804e66fa7593392ae04f04a64a4cad67c`  
		Last Modified: Wed, 06 Mar 2024 02:45:54 GMT  
		Size: 157.5 MB (157471632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0af84a8ac32154d956f99bd2ff4dc677f612db38d7e41b50ce908386d2fdb68`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b832bc149615378810f4a9fe40729770ad9dba7a7c228e62d356c50099736428`  
		Last Modified: Wed, 06 Mar 2024 02:46:09 GMT  
		Size: 40.5 MB (40505317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefdce4a2b8116db5f3f6152d30787df0a9c52fded830a5320b2269895938171`  
		Last Modified: Wed, 06 Mar 2024 02:46:03 GMT  
		Size: 317.1 KB (317110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e455f7807a21a05976ec00cb49130c7b2d93e058e90a6d16d04dbc3aa81696`  
		Last Modified: Wed, 06 Mar 2024 02:46:03 GMT  
		Size: 1.1 MB (1061437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b6ef817d5656642cbe1ee562a8a8375855b2e88c231f5ad95dcfb5d1e8837fc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251978011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bea440a091d3e9b7efec94ad5662096ef0a1363dcb32ff70504dddfb04738a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:30 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:10:30 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 04:10:30 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:10:30 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:10:30 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 04:12:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:12:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 04:12:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:12:42 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:12:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:13:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:13:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79dec5d4c4cd04e1e0085fdbe98bf2ecf754da7fe38a4cecb6c07bc9455520e9`  
		Last Modified: Wed, 06 Mar 2024 04:44:09 GMT  
		Size: 1.2 MB (1198548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f06f20f5ca5422d55808ff5eeea0324d21312c719c44cf7782e1d0a00db2a4`  
		Last Modified: Wed, 06 Mar 2024 04:44:08 GMT  
		Size: 5.5 MB (5532073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f2e3537c72de5ae529b44b0b0f1a0d17d3a4ba5e285f7c3a51fde2c93b95dc`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c1b7297f025d37b4fc703b337051c633da9de7f426f7d5f1b812e95f276e09`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a49a29ad0e0140da135daa347b774207b84e124d9cc64016207e77aaf40c3f7`  
		Last Modified: Wed, 06 Mar 2024 04:44:41 GMT  
		Size: 171.4 MB (171401255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93185f06229eeeafb914e15cd877669230a929a660d09bbaef30e423a05fcc82`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c690c1ca3d85a61d8f3e87d84817be0932b2873f0785d6d61d64d3f54a7137`  
		Last Modified: Wed, 06 Mar 2024 04:44:55 GMT  
		Size: 45.2 MB (45207349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de39e35aab238ae9a046045f0be90350874ce4e999a82a14fa6b1ae0e3616cab`  
		Last Modified: Wed, 06 Mar 2024 04:44:50 GMT  
		Size: 317.1 KB (317112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b89ab41d60352f77ccd8e2a2d80710850509070284e9dc6792a405b578dc1b`  
		Last Modified: Wed, 06 Mar 2024 04:44:50 GMT  
		Size: 1.1 MB (1114895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:052f161fe3c356f7e9a6b84a786635efcea992af12d638c202b593af04de8c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:0079c89a0b83b2a9bc8df635ba6e417cc70341fdc28b58b6107b8ee115aff90b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264727097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d27c296d320dd5e72294985860d6b8aee0e24e7e447e49c53b5b6d1a336f285`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:18:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:19:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:31:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:31:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 04:31:17 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:31:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:31:17 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 04:32:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:32:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 04:32:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:32:39 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:33:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:33:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:33:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b717a9d4ad213e59d73577a626c9c9093b2e6bf2dd493fc3fee4c33f9db601`  
		Last Modified: Wed, 06 Mar 2024 04:27:10 GMT  
		Size: 1.2 MB (1198476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f5ecd5001c5e4c5758fef666edcd4e26272b0cfecf06a567b8ad6584e6eabb`  
		Last Modified: Wed, 06 Mar 2024 04:27:08 GMT  
		Size: 5.6 MB (5553760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e87f945a5b1504b35e47df2fa6a203a1450bace36c3431c267361ae8ff84923`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c85c9351d67b117f6445876b30cb2a165a86b20103f9256f257a13974eee0e6`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5048c3edf0e27dbeab1cd05a3ad923ca803ea5b1489d6a0811eeb392549d3272`  
		Last Modified: Wed, 06 Mar 2024 04:58:22 GMT  
		Size: 177.0 MB (176998267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6dd23d624167f78a9fcbc142d6f13ff19d0598456e12c4c6048d541f6726f7`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e54e59330e9a8f9d250b062121a852c8a375d755bca20b39794ea2bd92f3e78`  
		Last Modified: Wed, 06 Mar 2024 04:58:38 GMT  
		Size: 50.9 MB (50942039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ddf4fbb020496e4eaaf355a6cd2a24b481295beffeb19738591d417c3c51a9`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 317.1 KB (317112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11354471cad5084e7d4a54163b6875984b80aae53f1b22226e60250b6f14b465`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 1.1 MB (1130634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:962f66ef1fb5e89c2defb0d9292396bc824c07d73b993906c6dd3dcacbe4edee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229837192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81aebcf2c59e23191c160390b401ff59cf5857e2eb0507ee07d0e010919d3d86`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:27:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:28:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:28:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 02:28:22 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 02:28:22 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 02:28:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 02:28:23 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 02:31:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:31:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 02:32:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 02:32:00 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 02:32:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:32:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 02:33:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a57ab8f3f909fb2a530a207c0b93b306ab27641c9c91ca7906af7d1eb85594c3`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 24.6 MB (24601340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa9329034da92c594d47e3dace53a9ceff3cbeffa063b398a0d6255e08c1ed8`  
		Last Modified: Wed, 06 Mar 2024 02:45:16 GMT  
		Size: 1.2 MB (1198533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28b7f93477437a2a60ecdc7208404196973f7489c9fbb4704c58d401443db90`  
		Last Modified: Wed, 06 Mar 2024 02:45:13 GMT  
		Size: 4.7 MB (4679331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456a7f559bad5c045a80841a7b566f694cf537d0b919d83634aa980087d81c4c`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef809d2cd923bd111a9311e0912e4f8006c77cf10b170e268441d064a962046`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a0d81a0257ef7784cc06c5b65d2ba804e66fa7593392ae04f04a64a4cad67c`  
		Last Modified: Wed, 06 Mar 2024 02:45:54 GMT  
		Size: 157.5 MB (157471632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0af84a8ac32154d956f99bd2ff4dc677f612db38d7e41b50ce908386d2fdb68`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b832bc149615378810f4a9fe40729770ad9dba7a7c228e62d356c50099736428`  
		Last Modified: Wed, 06 Mar 2024 02:46:09 GMT  
		Size: 40.5 MB (40505317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefdce4a2b8116db5f3f6152d30787df0a9c52fded830a5320b2269895938171`  
		Last Modified: Wed, 06 Mar 2024 02:46:03 GMT  
		Size: 317.1 KB (317110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e455f7807a21a05976ec00cb49130c7b2d93e058e90a6d16d04dbc3aa81696`  
		Last Modified: Wed, 06 Mar 2024 02:46:03 GMT  
		Size: 1.1 MB (1061437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b6ef817d5656642cbe1ee562a8a8375855b2e88c231f5ad95dcfb5d1e8837fc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251978011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bea440a091d3e9b7efec94ad5662096ef0a1363dcb32ff70504dddfb04738a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:30 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:10:30 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 04:10:30 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:10:30 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:10:30 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 04:12:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:12:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 04:12:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:12:42 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:12:59 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:13:04 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:13:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79dec5d4c4cd04e1e0085fdbe98bf2ecf754da7fe38a4cecb6c07bc9455520e9`  
		Last Modified: Wed, 06 Mar 2024 04:44:09 GMT  
		Size: 1.2 MB (1198548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f06f20f5ca5422d55808ff5eeea0324d21312c719c44cf7782e1d0a00db2a4`  
		Last Modified: Wed, 06 Mar 2024 04:44:08 GMT  
		Size: 5.5 MB (5532073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f2e3537c72de5ae529b44b0b0f1a0d17d3a4ba5e285f7c3a51fde2c93b95dc`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c1b7297f025d37b4fc703b337051c633da9de7f426f7d5f1b812e95f276e09`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a49a29ad0e0140da135daa347b774207b84e124d9cc64016207e77aaf40c3f7`  
		Last Modified: Wed, 06 Mar 2024 04:44:41 GMT  
		Size: 171.4 MB (171401255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93185f06229eeeafb914e15cd877669230a929a660d09bbaef30e423a05fcc82`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c690c1ca3d85a61d8f3e87d84817be0932b2873f0785d6d61d64d3f54a7137`  
		Last Modified: Wed, 06 Mar 2024 04:44:55 GMT  
		Size: 45.2 MB (45207349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de39e35aab238ae9a046045f0be90350874ce4e999a82a14fa6b1ae0e3616cab`  
		Last Modified: Wed, 06 Mar 2024 04:44:50 GMT  
		Size: 317.1 KB (317112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b89ab41d60352f77ccd8e2a2d80710850509070284e9dc6792a405b578dc1b`  
		Last Modified: Wed, 06 Mar 2024 04:44:50 GMT  
		Size: 1.1 MB (1114895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:ba9c7efeba9d068ae4f32d4d10b463ee4e1d889482739c3ad1bef5ce87c3a360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:3d8309bcbc1866b9f648261f1083b315dc7e027be665caacf4dba5deba8981c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212337312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4433647c87593add14b75b17c1df6952cf57ede1b3fc1a1d62927c5c3300e88e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:18:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:19:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:31:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:31:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 04:31:17 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:31:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:31:17 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 04:32:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:32:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 04:32:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:32:39 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b717a9d4ad213e59d73577a626c9c9093b2e6bf2dd493fc3fee4c33f9db601`  
		Last Modified: Wed, 06 Mar 2024 04:27:10 GMT  
		Size: 1.2 MB (1198476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f5ecd5001c5e4c5758fef666edcd4e26272b0cfecf06a567b8ad6584e6eabb`  
		Last Modified: Wed, 06 Mar 2024 04:27:08 GMT  
		Size: 5.6 MB (5553760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e87f945a5b1504b35e47df2fa6a203a1450bace36c3431c267361ae8ff84923`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c85c9351d67b117f6445876b30cb2a165a86b20103f9256f257a13974eee0e6`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5048c3edf0e27dbeab1cd05a3ad923ca803ea5b1489d6a0811eeb392549d3272`  
		Last Modified: Wed, 06 Mar 2024 04:58:22 GMT  
		Size: 177.0 MB (176998267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6dd23d624167f78a9fcbc142d6f13ff19d0598456e12c4c6048d541f6726f7`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:9c805f96e59bfa706f4dc457766221f5eb8362657f06475e0fbb0c3a5698a206
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187953328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c4484900c4fbaac43927ec35f52e49452c8cae4c23adf28ab78460f898e8f5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:27:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:28:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:28:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 02:28:22 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 02:28:22 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 02:28:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 02:28:23 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 02:31:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:31:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 02:32:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 02:32:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a57ab8f3f909fb2a530a207c0b93b306ab27641c9c91ca7906af7d1eb85594c3`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 24.6 MB (24601340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa9329034da92c594d47e3dace53a9ceff3cbeffa063b398a0d6255e08c1ed8`  
		Last Modified: Wed, 06 Mar 2024 02:45:16 GMT  
		Size: 1.2 MB (1198533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28b7f93477437a2a60ecdc7208404196973f7489c9fbb4704c58d401443db90`  
		Last Modified: Wed, 06 Mar 2024 02:45:13 GMT  
		Size: 4.7 MB (4679331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456a7f559bad5c045a80841a7b566f694cf537d0b919d83634aa980087d81c4c`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef809d2cd923bd111a9311e0912e4f8006c77cf10b170e268441d064a962046`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a0d81a0257ef7784cc06c5b65d2ba804e66fa7593392ae04f04a64a4cad67c`  
		Last Modified: Wed, 06 Mar 2024 02:45:54 GMT  
		Size: 157.5 MB (157471632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0af84a8ac32154d956f99bd2ff4dc677f612db38d7e41b50ce908386d2fdb68`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e595a95536e614013da0eefaf9312c846e14db0448831c3673bfaf716fef40f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205338655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63dc6cbf2be3a541bcb3be985de27cb7e28e1ed71388f9cbc3b8228e96c83c92`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:30 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:10:30 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 04:10:30 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:10:30 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:10:30 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 04:12:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:12:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 04:12:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:12:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79dec5d4c4cd04e1e0085fdbe98bf2ecf754da7fe38a4cecb6c07bc9455520e9`  
		Last Modified: Wed, 06 Mar 2024 04:44:09 GMT  
		Size: 1.2 MB (1198548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f06f20f5ca5422d55808ff5eeea0324d21312c719c44cf7782e1d0a00db2a4`  
		Last Modified: Wed, 06 Mar 2024 04:44:08 GMT  
		Size: 5.5 MB (5532073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f2e3537c72de5ae529b44b0b0f1a0d17d3a4ba5e285f7c3a51fde2c93b95dc`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c1b7297f025d37b4fc703b337051c633da9de7f426f7d5f1b812e95f276e09`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a49a29ad0e0140da135daa347b774207b84e124d9cc64016207e77aaf40c3f7`  
		Last Modified: Wed, 06 Mar 2024 04:44:41 GMT  
		Size: 171.4 MB (171401255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93185f06229eeeafb914e15cd877669230a929a660d09bbaef30e423a05fcc82`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:ba9c7efeba9d068ae4f32d4d10b463ee4e1d889482739c3ad1bef5ce87c3a360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:3d8309bcbc1866b9f648261f1083b315dc7e027be665caacf4dba5deba8981c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212337312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4433647c87593add14b75b17c1df6952cf57ede1b3fc1a1d62927c5c3300e88e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:18:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:19:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:31:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:31:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 04:31:17 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:31:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:31:17 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 04:32:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:32:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 04:32:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:32:39 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b717a9d4ad213e59d73577a626c9c9093b2e6bf2dd493fc3fee4c33f9db601`  
		Last Modified: Wed, 06 Mar 2024 04:27:10 GMT  
		Size: 1.2 MB (1198476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f5ecd5001c5e4c5758fef666edcd4e26272b0cfecf06a567b8ad6584e6eabb`  
		Last Modified: Wed, 06 Mar 2024 04:27:08 GMT  
		Size: 5.6 MB (5553760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e87f945a5b1504b35e47df2fa6a203a1450bace36c3431c267361ae8ff84923`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c85c9351d67b117f6445876b30cb2a165a86b20103f9256f257a13974eee0e6`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5048c3edf0e27dbeab1cd05a3ad923ca803ea5b1489d6a0811eeb392549d3272`  
		Last Modified: Wed, 06 Mar 2024 04:58:22 GMT  
		Size: 177.0 MB (176998267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6dd23d624167f78a9fcbc142d6f13ff19d0598456e12c4c6048d541f6726f7`  
		Last Modified: Wed, 06 Mar 2024 04:57:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:9c805f96e59bfa706f4dc457766221f5eb8362657f06475e0fbb0c3a5698a206
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187953328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c4484900c4fbaac43927ec35f52e49452c8cae4c23adf28ab78460f898e8f5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:13:06 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:13:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:13:06 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:13:14 GMT
ADD file:66096c88a70dfe9ed5e8eb12f0baffb429f0baba39540262b8339b6de267a8bc in / 
# Fri, 16 Feb 2024 19:13:15 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:27:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:28:17 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:28:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 02:28:22 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 02:28:22 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 02:28:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 02:28:23 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 02:31:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:31:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 02:32:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 02:32:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a57ab8f3f909fb2a530a207c0b93b306ab27641c9c91ca7906af7d1eb85594c3`  
		Last Modified: Wed, 06 Mar 2024 02:22:43 GMT  
		Size: 24.6 MB (24601340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa9329034da92c594d47e3dace53a9ceff3cbeffa063b398a0d6255e08c1ed8`  
		Last Modified: Wed, 06 Mar 2024 02:45:16 GMT  
		Size: 1.2 MB (1198533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28b7f93477437a2a60ecdc7208404196973f7489c9fbb4704c58d401443db90`  
		Last Modified: Wed, 06 Mar 2024 02:45:13 GMT  
		Size: 4.7 MB (4679331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456a7f559bad5c045a80841a7b566f694cf537d0b919d83634aa980087d81c4c`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef809d2cd923bd111a9311e0912e4f8006c77cf10b170e268441d064a962046`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a0d81a0257ef7784cc06c5b65d2ba804e66fa7593392ae04f04a64a4cad67c`  
		Last Modified: Wed, 06 Mar 2024 02:45:54 GMT  
		Size: 157.5 MB (157471632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0af84a8ac32154d956f99bd2ff4dc677f612db38d7e41b50ce908386d2fdb68`  
		Last Modified: Wed, 06 Mar 2024 02:45:12 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e595a95536e614013da0eefaf9312c846e14db0448831c3673bfaf716fef40f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205338655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63dc6cbf2be3a541bcb3be985de27cb7e28e1ed71388f9cbc3b8228e96c83c92`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:28 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:10:30 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:10:30 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 06 Mar 2024 04:10:30 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:10:30 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:10:30 GMT
ENV ROS_DISTRO=noetic
# Wed, 06 Mar 2024 04:12:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:12:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 06 Mar 2024 04:12:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:12:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79dec5d4c4cd04e1e0085fdbe98bf2ecf754da7fe38a4cecb6c07bc9455520e9`  
		Last Modified: Wed, 06 Mar 2024 04:44:09 GMT  
		Size: 1.2 MB (1198548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f06f20f5ca5422d55808ff5eeea0324d21312c719c44cf7782e1d0a00db2a4`  
		Last Modified: Wed, 06 Mar 2024 04:44:08 GMT  
		Size: 5.5 MB (5532073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f2e3537c72de5ae529b44b0b0f1a0d17d3a4ba5e285f7c3a51fde2c93b95dc`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c1b7297f025d37b4fc703b337051c633da9de7f426f7d5f1b812e95f276e09`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a49a29ad0e0140da135daa347b774207b84e124d9cc64016207e77aaf40c3f7`  
		Last Modified: Wed, 06 Mar 2024 04:44:41 GMT  
		Size: 171.4 MB (171401255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93185f06229eeeafb914e15cd877669230a929a660d09bbaef30e423a05fcc82`  
		Last Modified: Wed, 06 Mar 2024 04:44:07 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling`

```console
$ docker pull ros@sha256:c2c2aeebbb5d70f19a4048f0af2f67d6dee0e4d8c6953befa9110d318d74d66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:d046a3886c25da1f8ae4cefdb7b9ba8bcd0cddfa63e2ef2a2953c765b104f2b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268882673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6da1abec4d859f5b99ebdfe3ca5b94ddcd9fbe4f6f7d31c8f82ed05bad71fcd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:53:52 GMT
ENV ROS_DISTRO=rolling
# Wed, 06 Mar 2024 04:54:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:54:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:54:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:54:41 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:55:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:55:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:55:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:55:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d93a44684bbcbc78e29bcab36972dab63fec251f48a63ecfb1ae10ba3a9f52`  
		Last Modified: Wed, 06 Mar 2024 05:05:50 GMT  
		Size: 124.2 MB (124186646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c637203e66d84fab8aecbd4017a80ec1df09a80ac25baabf93d3f3efc6e0de`  
		Last Modified: Wed, 06 Mar 2024 05:05:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a62c6bde6154e7e639110732d0e02b1597e021b7ed2e5b8cbab535864d229`  
		Last Modified: Wed, 06 Mar 2024 05:06:09 GMT  
		Size: 85.2 MB (85172575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883023cf75c1b70893791cf326ab499c79b45dfa1bc41e071adf317e28ff3456`  
		Last Modified: Wed, 06 Mar 2024 05:05:59 GMT  
		Size: 290.6 KB (290622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5715a399e9f1fd1e8b661a50fa09979ac4222215dbcb929371a02008556f9c72`  
		Last Modified: Wed, 06 Mar 2024 05:05:59 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f86a7442663e4519b8449c3f90284d8ed0263610cdda9a745c751c3635b7861`  
		Last Modified: Wed, 06 Mar 2024 05:06:03 GMT  
		Size: 23.7 MB (23733286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:000b81e6da49e1f0256da726cc181f63fc32a0f78e39a324f0fe102d0ca46b58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261285551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cadf267e725c3e714572c03a376080374c097e2dc8c0ce3bbc0284bcede79b44`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:40:26 GMT
ENV ROS_DISTRO=rolling
# Wed, 06 Mar 2024 04:41:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:07 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:41:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:41:07 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:41:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:41:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:41:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e9f987cc75510f54eba22ea4c1450f3139c22b93a5eeb8bcae0d809c4cd265`  
		Last Modified: Wed, 06 Mar 2024 04:51:59 GMT  
		Size: 121.6 MB (121624541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b18819c6978fced567e004c8375f87c123872f5cd215d40d4b80847f0a0800f`  
		Last Modified: Wed, 06 Mar 2024 04:51:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22617ce11378da240c6c3c2d18629fda2e590c45b400e949a44d573d6a253b6`  
		Last Modified: Wed, 06 Mar 2024 04:52:18 GMT  
		Size: 82.8 MB (82847601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ff893af2fe38cffe84ae31fb677aee96349177f954359202fd1afcdf4369a9`  
		Last Modified: Wed, 06 Mar 2024 04:52:09 GMT  
		Size: 290.6 KB (290613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f60849007555690da1a453d4d2f31d579c5d33baa9b38ffa06965f26253d68`  
		Last Modified: Wed, 06 Mar 2024 04:52:08 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c14bdb55b7e2e569bf3e0be77e1de5a0c4a81597776cd6bada36fe0a393dd18`  
		Last Modified: Wed, 06 Mar 2024 04:52:13 GMT  
		Size: 23.1 MB (23101809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:8097da973717c35a774e58f8aa169f03760114016bfa2f3c4f79b891500eb1ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:5fac66c19929d142d2176dd535977765b27e738c42e2febb43969dbf93bf2524
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.3 MB (961268645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006d231fdb3ec2b3f943f31ddb2aea9c0d1883997835017485d6bad8f6199e5f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:53:52 GMT
ENV ROS_DISTRO=rolling
# Wed, 06 Mar 2024 04:54:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:54:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:54:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:54:41 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:55:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:55:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:55:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:55:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:57:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d93a44684bbcbc78e29bcab36972dab63fec251f48a63ecfb1ae10ba3a9f52`  
		Last Modified: Wed, 06 Mar 2024 05:05:50 GMT  
		Size: 124.2 MB (124186646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c637203e66d84fab8aecbd4017a80ec1df09a80ac25baabf93d3f3efc6e0de`  
		Last Modified: Wed, 06 Mar 2024 05:05:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a62c6bde6154e7e639110732d0e02b1597e021b7ed2e5b8cbab535864d229`  
		Last Modified: Wed, 06 Mar 2024 05:06:09 GMT  
		Size: 85.2 MB (85172575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883023cf75c1b70893791cf326ab499c79b45dfa1bc41e071adf317e28ff3456`  
		Last Modified: Wed, 06 Mar 2024 05:05:59 GMT  
		Size: 290.6 KB (290622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5715a399e9f1fd1e8b661a50fa09979ac4222215dbcb929371a02008556f9c72`  
		Last Modified: Wed, 06 Mar 2024 05:05:59 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f86a7442663e4519b8449c3f90284d8ed0263610cdda9a745c751c3635b7861`  
		Last Modified: Wed, 06 Mar 2024 05:06:03 GMT  
		Size: 23.7 MB (23733286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4d01715d234fe44d0693ab803d3e6252ccd9c68935903ba91856c409135c36`  
		Last Modified: Wed, 06 Mar 2024 05:07:51 GMT  
		Size: 692.4 MB (692385972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4259d9b103503475428d4989db5e3e204a5ed983f858367c7f7d2a5546ec9677
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.5 MB (921511052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04faf749378f7d3c487285ab57195a30d81fb923b7ffa5c69912330704323541`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:40:26 GMT
ENV ROS_DISTRO=rolling
# Wed, 06 Mar 2024 04:41:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:07 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:41:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:41:07 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:41:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:41:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:41:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:43:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e9f987cc75510f54eba22ea4c1450f3139c22b93a5eeb8bcae0d809c4cd265`  
		Last Modified: Wed, 06 Mar 2024 04:51:59 GMT  
		Size: 121.6 MB (121624541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b18819c6978fced567e004c8375f87c123872f5cd215d40d4b80847f0a0800f`  
		Last Modified: Wed, 06 Mar 2024 04:51:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22617ce11378da240c6c3c2d18629fda2e590c45b400e949a44d573d6a253b6`  
		Last Modified: Wed, 06 Mar 2024 04:52:18 GMT  
		Size: 82.8 MB (82847601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ff893af2fe38cffe84ae31fb677aee96349177f954359202fd1afcdf4369a9`  
		Last Modified: Wed, 06 Mar 2024 04:52:09 GMT  
		Size: 290.6 KB (290613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f60849007555690da1a453d4d2f31d579c5d33baa9b38ffa06965f26253d68`  
		Last Modified: Wed, 06 Mar 2024 04:52:08 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c14bdb55b7e2e569bf3e0be77e1de5a0c4a81597776cd6bada36fe0a393dd18`  
		Last Modified: Wed, 06 Mar 2024 04:52:13 GMT  
		Size: 23.1 MB (23101809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c6ab0121874393f8ac4aa565f897b4fdb4b5b30e2d98fc102a4e7140944e6e`  
		Last Modified: Wed, 06 Mar 2024 04:53:52 GMT  
		Size: 660.2 MB (660225501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception-jammy`

```console
$ docker pull ros@sha256:8097da973717c35a774e58f8aa169f03760114016bfa2f3c4f79b891500eb1ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:5fac66c19929d142d2176dd535977765b27e738c42e2febb43969dbf93bf2524
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.3 MB (961268645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006d231fdb3ec2b3f943f31ddb2aea9c0d1883997835017485d6bad8f6199e5f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:53:52 GMT
ENV ROS_DISTRO=rolling
# Wed, 06 Mar 2024 04:54:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:54:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:54:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:54:41 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:55:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:55:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:55:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:55:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:57:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d93a44684bbcbc78e29bcab36972dab63fec251f48a63ecfb1ae10ba3a9f52`  
		Last Modified: Wed, 06 Mar 2024 05:05:50 GMT  
		Size: 124.2 MB (124186646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c637203e66d84fab8aecbd4017a80ec1df09a80ac25baabf93d3f3efc6e0de`  
		Last Modified: Wed, 06 Mar 2024 05:05:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a62c6bde6154e7e639110732d0e02b1597e021b7ed2e5b8cbab535864d229`  
		Last Modified: Wed, 06 Mar 2024 05:06:09 GMT  
		Size: 85.2 MB (85172575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883023cf75c1b70893791cf326ab499c79b45dfa1bc41e071adf317e28ff3456`  
		Last Modified: Wed, 06 Mar 2024 05:05:59 GMT  
		Size: 290.6 KB (290622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5715a399e9f1fd1e8b661a50fa09979ac4222215dbcb929371a02008556f9c72`  
		Last Modified: Wed, 06 Mar 2024 05:05:59 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f86a7442663e4519b8449c3f90284d8ed0263610cdda9a745c751c3635b7861`  
		Last Modified: Wed, 06 Mar 2024 05:06:03 GMT  
		Size: 23.7 MB (23733286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4d01715d234fe44d0693ab803d3e6252ccd9c68935903ba91856c409135c36`  
		Last Modified: Wed, 06 Mar 2024 05:07:51 GMT  
		Size: 692.4 MB (692385972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4259d9b103503475428d4989db5e3e204a5ed983f858367c7f7d2a5546ec9677
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.5 MB (921511052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04faf749378f7d3c487285ab57195a30d81fb923b7ffa5c69912330704323541`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:40:26 GMT
ENV ROS_DISTRO=rolling
# Wed, 06 Mar 2024 04:41:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:07 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:41:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:41:07 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:41:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:41:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:41:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:43:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e9f987cc75510f54eba22ea4c1450f3139c22b93a5eeb8bcae0d809c4cd265`  
		Last Modified: Wed, 06 Mar 2024 04:51:59 GMT  
		Size: 121.6 MB (121624541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b18819c6978fced567e004c8375f87c123872f5cd215d40d4b80847f0a0800f`  
		Last Modified: Wed, 06 Mar 2024 04:51:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22617ce11378da240c6c3c2d18629fda2e590c45b400e949a44d573d6a253b6`  
		Last Modified: Wed, 06 Mar 2024 04:52:18 GMT  
		Size: 82.8 MB (82847601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ff893af2fe38cffe84ae31fb677aee96349177f954359202fd1afcdf4369a9`  
		Last Modified: Wed, 06 Mar 2024 04:52:09 GMT  
		Size: 290.6 KB (290613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f60849007555690da1a453d4d2f31d579c5d33baa9b38ffa06965f26253d68`  
		Last Modified: Wed, 06 Mar 2024 04:52:08 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c14bdb55b7e2e569bf3e0be77e1de5a0c4a81597776cd6bada36fe0a393dd18`  
		Last Modified: Wed, 06 Mar 2024 04:52:13 GMT  
		Size: 23.1 MB (23101809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c6ab0121874393f8ac4aa565f897b4fdb4b5b30e2d98fc102a4e7140944e6e`  
		Last Modified: Wed, 06 Mar 2024 04:53:52 GMT  
		Size: 660.2 MB (660225501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:c2c2aeebbb5d70f19a4048f0af2f67d6dee0e4d8c6953befa9110d318d74d66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:d046a3886c25da1f8ae4cefdb7b9ba8bcd0cddfa63e2ef2a2953c765b104f2b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268882673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6da1abec4d859f5b99ebdfe3ca5b94ddcd9fbe4f6f7d31c8f82ed05bad71fcd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:53:52 GMT
ENV ROS_DISTRO=rolling
# Wed, 06 Mar 2024 04:54:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:54:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:54:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:54:41 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:55:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:55:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:55:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:55:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d93a44684bbcbc78e29bcab36972dab63fec251f48a63ecfb1ae10ba3a9f52`  
		Last Modified: Wed, 06 Mar 2024 05:05:50 GMT  
		Size: 124.2 MB (124186646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c637203e66d84fab8aecbd4017a80ec1df09a80ac25baabf93d3f3efc6e0de`  
		Last Modified: Wed, 06 Mar 2024 05:05:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a62c6bde6154e7e639110732d0e02b1597e021b7ed2e5b8cbab535864d229`  
		Last Modified: Wed, 06 Mar 2024 05:06:09 GMT  
		Size: 85.2 MB (85172575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883023cf75c1b70893791cf326ab499c79b45dfa1bc41e071adf317e28ff3456`  
		Last Modified: Wed, 06 Mar 2024 05:05:59 GMT  
		Size: 290.6 KB (290622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5715a399e9f1fd1e8b661a50fa09979ac4222215dbcb929371a02008556f9c72`  
		Last Modified: Wed, 06 Mar 2024 05:05:59 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f86a7442663e4519b8449c3f90284d8ed0263610cdda9a745c751c3635b7861`  
		Last Modified: Wed, 06 Mar 2024 05:06:03 GMT  
		Size: 23.7 MB (23733286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:000b81e6da49e1f0256da726cc181f63fc32a0f78e39a324f0fe102d0ca46b58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261285551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cadf267e725c3e714572c03a376080374c097e2dc8c0ce3bbc0284bcede79b44`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:40:26 GMT
ENV ROS_DISTRO=rolling
# Wed, 06 Mar 2024 04:41:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:07 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:41:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:41:07 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:41:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:41:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:41:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e9f987cc75510f54eba22ea4c1450f3139c22b93a5eeb8bcae0d809c4cd265`  
		Last Modified: Wed, 06 Mar 2024 04:51:59 GMT  
		Size: 121.6 MB (121624541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b18819c6978fced567e004c8375f87c123872f5cd215d40d4b80847f0a0800f`  
		Last Modified: Wed, 06 Mar 2024 04:51:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22617ce11378da240c6c3c2d18629fda2e590c45b400e949a44d573d6a253b6`  
		Last Modified: Wed, 06 Mar 2024 04:52:18 GMT  
		Size: 82.8 MB (82847601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ff893af2fe38cffe84ae31fb677aee96349177f954359202fd1afcdf4369a9`  
		Last Modified: Wed, 06 Mar 2024 04:52:09 GMT  
		Size: 290.6 KB (290613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f60849007555690da1a453d4d2f31d579c5d33baa9b38ffa06965f26253d68`  
		Last Modified: Wed, 06 Mar 2024 04:52:08 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c14bdb55b7e2e569bf3e0be77e1de5a0c4a81597776cd6bada36fe0a393dd18`  
		Last Modified: Wed, 06 Mar 2024 04:52:13 GMT  
		Size: 23.1 MB (23101809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base-jammy`

```console
$ docker pull ros@sha256:c2c2aeebbb5d70f19a4048f0af2f67d6dee0e4d8c6953befa9110d318d74d66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:d046a3886c25da1f8ae4cefdb7b9ba8bcd0cddfa63e2ef2a2953c765b104f2b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268882673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6da1abec4d859f5b99ebdfe3ca5b94ddcd9fbe4f6f7d31c8f82ed05bad71fcd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:53:52 GMT
ENV ROS_DISTRO=rolling
# Wed, 06 Mar 2024 04:54:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:54:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:54:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:54:41 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:55:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:55:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:55:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:55:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d93a44684bbcbc78e29bcab36972dab63fec251f48a63ecfb1ae10ba3a9f52`  
		Last Modified: Wed, 06 Mar 2024 05:05:50 GMT  
		Size: 124.2 MB (124186646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c637203e66d84fab8aecbd4017a80ec1df09a80ac25baabf93d3f3efc6e0de`  
		Last Modified: Wed, 06 Mar 2024 05:05:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a62c6bde6154e7e639110732d0e02b1597e021b7ed2e5b8cbab535864d229`  
		Last Modified: Wed, 06 Mar 2024 05:06:09 GMT  
		Size: 85.2 MB (85172575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883023cf75c1b70893791cf326ab499c79b45dfa1bc41e071adf317e28ff3456`  
		Last Modified: Wed, 06 Mar 2024 05:05:59 GMT  
		Size: 290.6 KB (290622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5715a399e9f1fd1e8b661a50fa09979ac4222215dbcb929371a02008556f9c72`  
		Last Modified: Wed, 06 Mar 2024 05:05:59 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f86a7442663e4519b8449c3f90284d8ed0263610cdda9a745c751c3635b7861`  
		Last Modified: Wed, 06 Mar 2024 05:06:03 GMT  
		Size: 23.7 MB (23733286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:000b81e6da49e1f0256da726cc181f63fc32a0f78e39a324f0fe102d0ca46b58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261285551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cadf267e725c3e714572c03a376080374c097e2dc8c0ce3bbc0284bcede79b44`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:40:26 GMT
ENV ROS_DISTRO=rolling
# Wed, 06 Mar 2024 04:41:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:07 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:41:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:41:07 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 04:41:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 06 Mar 2024 04:41:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 06 Mar 2024 04:41:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e9f987cc75510f54eba22ea4c1450f3139c22b93a5eeb8bcae0d809c4cd265`  
		Last Modified: Wed, 06 Mar 2024 04:51:59 GMT  
		Size: 121.6 MB (121624541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b18819c6978fced567e004c8375f87c123872f5cd215d40d4b80847f0a0800f`  
		Last Modified: Wed, 06 Mar 2024 04:51:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22617ce11378da240c6c3c2d18629fda2e590c45b400e949a44d573d6a253b6`  
		Last Modified: Wed, 06 Mar 2024 04:52:18 GMT  
		Size: 82.8 MB (82847601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ff893af2fe38cffe84ae31fb677aee96349177f954359202fd1afcdf4369a9`  
		Last Modified: Wed, 06 Mar 2024 04:52:09 GMT  
		Size: 290.6 KB (290613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f60849007555690da1a453d4d2f31d579c5d33baa9b38ffa06965f26253d68`  
		Last Modified: Wed, 06 Mar 2024 04:52:08 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c14bdb55b7e2e569bf3e0be77e1de5a0c4a81597776cd6bada36fe0a393dd18`  
		Last Modified: Wed, 06 Mar 2024 04:52:13 GMT  
		Size: 23.1 MB (23101809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:570426983cdb163f2d153a2ef30c1baa3146836d177827d935f76d664d5b2646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:c0a01b8e7d9f303a7e8e6117d682da239c06b1fd929417a9eeb7041e8640c66e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159683718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe64f3a27e0086cf28d100c5cdb3a54ffda116c006bf09dd047eb6da0d8d3b1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:53:52 GMT
ENV ROS_DISTRO=rolling
# Wed, 06 Mar 2024 04:54:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:54:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:54:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:54:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d93a44684bbcbc78e29bcab36972dab63fec251f48a63ecfb1ae10ba3a9f52`  
		Last Modified: Wed, 06 Mar 2024 05:05:50 GMT  
		Size: 124.2 MB (124186646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c637203e66d84fab8aecbd4017a80ec1df09a80ac25baabf93d3f3efc6e0de`  
		Last Modified: Wed, 06 Mar 2024 05:05:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5d4d17f39682d3bfd32d842801e2909be503388975252d5bb46ef68a3166724a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155043033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ea638ed33f92eaf96d9e2509eca402a6fed2eab43244bddac1719f86ba1a51`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:40:26 GMT
ENV ROS_DISTRO=rolling
# Wed, 06 Mar 2024 04:41:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:07 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:41:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:41:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e9f987cc75510f54eba22ea4c1450f3139c22b93a5eeb8bcae0d809c4cd265`  
		Last Modified: Wed, 06 Mar 2024 04:51:59 GMT  
		Size: 121.6 MB (121624541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b18819c6978fced567e004c8375f87c123872f5cd215d40d4b80847f0a0800f`  
		Last Modified: Wed, 06 Mar 2024 04:51:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core-jammy`

```console
$ docker pull ros@sha256:570426983cdb163f2d153a2ef30c1baa3146836d177827d935f76d664d5b2646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:c0a01b8e7d9f303a7e8e6117d682da239c06b1fd929417a9eeb7041e8640c66e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159683718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe64f3a27e0086cf28d100c5cdb3a54ffda116c006bf09dd047eb6da0d8d3b1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:38:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:38:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:38:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:38:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:53:52 GMT
ENV ROS_DISTRO=rolling
# Wed, 06 Mar 2024 04:54:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:54:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:54:41 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:54:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245302db8c782aad3e60dbc2c6cc71b982caf3a150f34ad3ddfa3873c4afd18`  
		Last Modified: Wed, 06 Mar 2024 05:00:32 GMT  
		Size: 1.2 MB (1214254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065bd93f975bd7a496ad9d6312581c6d64f03b230b9ca3829dbadc7df514d696`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 3.8 MB (3829030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21651d6299722310fafbd8d55e99a101acc2aa71c40e4946a01b52aaa8e7d1a`  
		Last Modified: Wed, 06 Mar 2024 05:00:29 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda16934b4f07a26c7574f2b3bdbd276fe4ebd92195a2da898279b1641c1b93`  
		Last Modified: Wed, 06 Mar 2024 05:00:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d93a44684bbcbc78e29bcab36972dab63fec251f48a63ecfb1ae10ba3a9f52`  
		Last Modified: Wed, 06 Mar 2024 05:05:50 GMT  
		Size: 124.2 MB (124186646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c637203e66d84fab8aecbd4017a80ec1df09a80ac25baabf93d3f3efc6e0de`  
		Last Modified: Wed, 06 Mar 2024 05:05:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5d4d17f39682d3bfd32d842801e2909be503388975252d5bb46ef68a3166724a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155043033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ea638ed33f92eaf96d9e2509eca402a6fed2eab43244bddac1719f86ba1a51`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:22:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:12 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:23:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 06 Mar 2024 04:23:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LANG=C.UTF-8
# Wed, 06 Mar 2024 04:23:14 GMT
ENV LC_ALL=C.UTF-8
# Wed, 06 Mar 2024 04:40:26 GMT
ENV ROS_DISTRO=rolling
# Wed, 06 Mar 2024 04:41:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:41:07 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 06 Mar 2024 04:41:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 06 Mar 2024 04:41:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d472c7021f09198221e9864d5f974ac0880e8a921ce52d10f07682c7d269d9`  
		Last Modified: Wed, 06 Mar 2024 04:46:41 GMT  
		Size: 1.2 MB (1214571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddc1eb7e09f11933336d721fee07b2e73c2d0cc9ceb50462c713bd99350d64d`  
		Last Modified: Wed, 06 Mar 2024 04:46:39 GMT  
		Size: 3.8 MB (3800790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb9554fb5801e48e7721a54e3892fbd4c4b675a16540507e0faf60f75e35c81`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9778cd3755235be294c16dde0b5f92534492d14c1ef8c5e375599a7e184de4d`  
		Last Modified: Wed, 06 Mar 2024 04:46:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e9f987cc75510f54eba22ea4c1450f3139c22b93a5eeb8bcae0d809c4cd265`  
		Last Modified: Wed, 06 Mar 2024 04:51:59 GMT  
		Size: 121.6 MB (121624541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b18819c6978fced567e004c8375f87c123872f5cd215d40d4b80847f0a0800f`  
		Last Modified: Wed, 06 Mar 2024 04:51:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
