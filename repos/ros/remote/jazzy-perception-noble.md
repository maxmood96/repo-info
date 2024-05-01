## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:70df82c9c8b8952e807d623a8d824d10bee7be05ff7100e9d48d78721f53047b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:b4b7ea311b3c467b5c061080d29de4dc120488522eb96d47786065b31aa95ab1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.7 MB (629738420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ddd7d19427343547671b6edbe6eb3d299d9d37daa4da5117f17348eab16e40c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:00:09 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:00:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:00:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:00:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:00:11 GMT
ADD file:019ce26ec491bab156f6a15e93164ae5351fd38c7fff11d00c69c18e31e9dde3 in / 
# Tue, 23 Apr 2024 22:00:11 GMT
CMD ["/bin/bash"]
# Fri, 26 Apr 2024 00:02:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 00:02:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 21:29:48 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-testing-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 30 Apr 2024 21:29:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-testing-archive-keyring.gpg ] http://packages.ros.org/ros2-testing/ubuntu noble main" > /etc/apt/sources.list.d/ros2-testing.list
# Tue, 30 Apr 2024 21:29:49 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:29:49 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:29:49 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 23:22:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 23:22:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 30 Apr 2024 23:22:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 23:22:51 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 23:24:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 23:24:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 30 Apr 2024 23:24:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 30 Apr 2024 23:25:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 23:27:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8f5159575f7bbbce11277d1532c12d73076587ebb492562917370449a8c5e7fa`  
		Last Modified: Wed, 24 Apr 2024 17:16:59 GMT  
		Size: 29.7 MB (29702068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d685d4b1835697d792719b9d32a49e6f2ff490bf4864a1e921e19bdcf9b574`  
		Last Modified: Fri, 26 Apr 2024 00:16:06 GMT  
		Size: 680.6 KB (680624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4876135551aef0e8eb1671e4e34d581297f7255ba571e4bd11321bc6ebbb4ca0`  
		Last Modified: Fri, 26 Apr 2024 00:16:05 GMT  
		Size: 4.6 MB (4615573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89fe2ec06dadb4203f1134cd0a4db95d383b2e3b74ceea6eaf13f446ba3a192`  
		Last Modified: Tue, 30 Apr 2024 23:28:19 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e0049a6452236b3d343a2c4ef39d5d4f3a10cf8c9cd905f102b537099ae33c`  
		Last Modified: Tue, 30 Apr 2024 23:28:19 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde9645b516e92c3c078f25655fb83a2e7ef751c8ea0232a2380ca19a26b5a48`  
		Last Modified: Tue, 30 Apr 2024 23:28:38 GMT  
		Size: 128.5 MB (128523063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58aabe751358c1e8c5d6c30492977cdbe557ac66da8b9c123ba6bfd2d49c5e3`  
		Last Modified: Tue, 30 Apr 2024 23:28:19 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d6d1825be4f9c2f6efbc21aafbeb2d4f371b90e7b4fc3f7c70f0a8ba10b3b9`  
		Last Modified: Tue, 30 Apr 2024 23:29:03 GMT  
		Size: 114.3 MB (114306774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18fad7a3c3dec2031224eab9e284458528c0ea2ec75427eafbbb609fa72f00b`  
		Last Modified: Tue, 30 Apr 2024 23:28:48 GMT  
		Size: 308.4 KB (308381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5f61a028e7a15b34862fb805f21aa50571356d49c3898a88b66fa365baa7ea`  
		Last Modified: Tue, 30 Apr 2024 23:28:48 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0289aedc3217b314a6be9a7fc66e70170b6b8f08cf665143bfa215d6c52e8561`  
		Last Modified: Tue, 30 Apr 2024 23:28:52 GMT  
		Size: 27.7 MB (27666018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e43ecfc13baaa991b635bc0a4ca1afdf490dfc57ebdd7af014c11034a77842`  
		Last Modified: Tue, 30 Apr 2024 23:30:01 GMT  
		Size: 323.9 MB (323930911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f5dcafeb75ca15bd2d7ab551cb4ef89208f3a8d972a99bdb7dad9e55c010086f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.8 MB (572797240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e8cc8a0c9f926488fd8fc7f31fa226be6089ebfac1f5be8d3e904402dc7b58`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Apr 2024 22:03:43 GMT
ARG RELEASE
# Tue, 23 Apr 2024 22:03:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 22:03:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 22:03:43 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 23 Apr 2024 22:03:45 GMT
ADD file:61020b87bc980abd05e75207205df7ecca6ea7023b3a5e804aabded0eebbf2e7 in / 
# Tue, 23 Apr 2024 22:03:45 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:40:03 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:40:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 22:21:07 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-testing-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 30 Apr 2024 22:21:08 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-testing-archive-keyring.gpg ] http://packages.ros.org/ros2-testing/ubuntu noble main" > /etc/apt/sources.list.d/ros2-testing.list
# Tue, 30 Apr 2024 22:21:08 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 22:21:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 22:21:08 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 23:55:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 23:55:14 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 30 Apr 2024 23:55:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 23:55:14 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 23:56:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 30 Apr 2024 23:56:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 30 Apr 2024 23:56:41 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 30 Apr 2024 23:57:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 01 May 2024 00:00:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec7cb58592b61e9a11cec56cc368247d061905f8eee62423f6dddd42173504b2`  
		Last Modified: Wed, 24 Apr 2024 17:24:38 GMT  
		Size: 29.0 MB (29037830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05eeec93563e0c4bee2b919df0e289aa0a06346104ee647ecb90c42f12aea54e`  
		Last Modified: Thu, 25 Apr 2024 23:53:26 GMT  
		Size: 680.9 KB (680947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d8d27f77c20bc7eb1198a0fc5a3a3f5f22edf40094d000e31aaf9d3ca83c88`  
		Last Modified: Thu, 25 Apr 2024 23:53:24 GMT  
		Size: 4.6 MB (4609997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cd4b5b72a1b898bdeb45d8fc3fd23247a5fd5ab1c6117138a092495942466c`  
		Last Modified: Wed, 01 May 2024 00:00:58 GMT  
		Size: 2.0 KB (2026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8d64a67472b41f6012691b8c43b6f71e2816c92cff68287894267a7121456c`  
		Last Modified: Wed, 01 May 2024 00:00:57 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8281a9e77f8f0f8895dc7cf25059627c964d189568127d04596d7c3ed6fb6252`  
		Last Modified: Wed, 01 May 2024 00:01:12 GMT  
		Size: 123.1 MB (123091890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628505832a45ff58607a29e51d5c4bbb5804debe3911e70c661b28206c15b4c9`  
		Last Modified: Wed, 01 May 2024 00:00:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1463f2c79fb08c2a929099157a79beb3bb3a4229f1aeb7d57f36b869f7022ea0`  
		Last Modified: Wed, 01 May 2024 00:01:33 GMT  
		Size: 111.2 MB (111162185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0265508cb7630db1bc677f9032f6e6bf275f70efc358c26259332c1a9c573fc`  
		Last Modified: Wed, 01 May 2024 00:01:22 GMT  
		Size: 308.4 KB (308381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46685569ffda2682881f46f4d48e927a06aa8a4b5504395cb95cdced636819a`  
		Last Modified: Wed, 01 May 2024 00:01:22 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c7e9df4cd0c6133e69488dbe71b48ec8c2042997e93c73f70e485600845fc6`  
		Last Modified: Wed, 01 May 2024 00:01:25 GMT  
		Size: 26.8 MB (26810995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c289485e6df74c8c8868429c42b5f33cbf4ad7b67f38d2bd47b3f04dd3a60c80`  
		Last Modified: Wed, 01 May 2024 00:02:14 GMT  
		Size: 277.1 MB (277090034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
