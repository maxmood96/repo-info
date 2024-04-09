## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:f1021dd861888471e99b184969952df6664745d01400f0e22f3db2d1a486340a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:9c6b1fd4cabc26028f9811becf9f7b86b28d7931e608255c641924c03c437c38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.9 MB (312928587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5199814c9885888b1775a73f195eba82bef47b7614e259ac984a51aec689b66f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 25 Feb 2024 04:22:40 GMT
ARG RELEASE
# Sun, 25 Feb 2024 04:22:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 25 Feb 2024 04:22:40 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 25 Feb 2024 04:22:42 GMT
ADD file:93f7775e4e5ce50f9e61bbd8f651e279ddd3add435e095c503b909e3da650623 in / 
# Sun, 25 Feb 2024 04:22:42 GMT
CMD ["/bin/bash"]
# Tue, 09 Apr 2024 01:10:35 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 01:10:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 01:10:58 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 09 Apr 2024 01:10:58 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 09 Apr 2024 01:10:58 GMT
ENV LANG=C.UTF-8
# Tue, 09 Apr 2024 01:10:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 09 Apr 2024 01:10:58 GMT
ENV ROS_DISTRO=rolling
# Tue, 09 Apr 2024 01:12:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 01:13:01 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 09 Apr 2024 01:13:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 09 Apr 2024 01:13:01 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 01:14:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 01:14:26 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 09 Apr 2024 01:14:31 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 09 Apr 2024 01:15:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80edb1aaf132005ee2bb2f811872efbbbf0cb9b8ec36897c5849798408c7047b`  
		Last Modified: Wed, 06 Mar 2024 04:17:28 GMT  
		Size: 30.6 MB (30551664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ae7a4b8533ed02de25c6db9cadf9d6185ec0c1449006f72c8c102f88d9c366`  
		Last Modified: Tue, 09 Apr 2024 01:16:20 GMT  
		Size: 678.8 KB (678804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687f996e40de6f8f6916bb8e6980652668cc0d05d02c25eadb51093298574fcb`  
		Last Modified: Tue, 09 Apr 2024 01:16:19 GMT  
		Size: 8.6 MB (8592662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56c22f3aa219c5138ff1bbc82374315aa1922757308b29877c35a3cb8b5e6ea`  
		Last Modified: Tue, 09 Apr 2024 01:16:18 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eec9388bb59844a59497d2429ee5f3f2015200df4fa2c240bb17af7f0f71468`  
		Last Modified: Tue, 09 Apr 2024 01:16:18 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d655d21d1312116546a5f98c784090af77df702fe99fdfc6a1c9a35eba60e5de`  
		Last Modified: Tue, 09 Apr 2024 01:16:37 GMT  
		Size: 131.0 MB (130982386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78161d0fd69b73de8cf9ceaa94a41d12f84426830950ed264cb4c2f7305e2d29`  
		Last Modified: Tue, 09 Apr 2024 01:16:18 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c8b87d727c91d29d462f1d74e4e23730ed1e3872ca84233a3ec6efd65828c3`  
		Last Modified: Tue, 09 Apr 2024 01:17:02 GMT  
		Size: 117.4 MB (117367025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2426d5cb0ec58cdd1563cc31ae0384c0193eb0441fd191af5a8cf5d926ef5525`  
		Last Modified: Tue, 09 Apr 2024 01:16:46 GMT  
		Size: 307.1 KB (307129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bb9995b3dd22894ce26995fe8c90d1fa9543fdf86f52f5e3615cf75aa9c1df`  
		Last Modified: Tue, 09 Apr 2024 01:16:46 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4ce9e86e8153669fcc14faa5b354a9c87f54c0272ea9d3421125a09ba7581b`  
		Last Modified: Tue, 09 Apr 2024 01:16:50 GMT  
		Size: 24.4 MB (24443916 bytes)  
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
