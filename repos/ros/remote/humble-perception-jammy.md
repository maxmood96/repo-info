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
