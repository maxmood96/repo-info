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
-	[`ros:humble`](#roshumble)
-	[`ros:humble-perception`](#roshumble-perception)
-	[`ros:humble-perception-jammy`](#roshumble-perception-jammy)
-	[`ros:humble-ros-base`](#roshumble-ros-base)
-	[`ros:humble-ros-base-jammy`](#roshumble-ros-base-jammy)
-	[`ros:humble-ros-core`](#roshumble-ros-core)
-	[`ros:humble-ros-core-jammy`](#roshumble-ros-core-jammy)
-	[`ros:jazzy`](#rosjazzy)
-	[`ros:jazzy-perception`](#rosjazzy-perception)
-	[`ros:jazzy-perception-noble`](#rosjazzy-perception-noble)
-	[`ros:jazzy-ros-base`](#rosjazzy-ros-base)
-	[`ros:jazzy-ros-base-noble`](#rosjazzy-ros-base-noble)
-	[`ros:jazzy-ros-core`](#rosjazzy-ros-core)
-	[`ros:jazzy-ros-core-noble`](#rosjazzy-ros-core-noble)
-	[`ros:kilted`](#roskilted)
-	[`ros:kilted-perception`](#roskilted-perception)
-	[`ros:kilted-perception-noble`](#roskilted-perception-noble)
-	[`ros:kilted-ros-base`](#roskilted-ros-base)
-	[`ros:kilted-ros-base-noble`](#roskilted-ros-base-noble)
-	[`ros:kilted-ros-core`](#roskilted-ros-core)
-	[`ros:kilted-ros-core-noble`](#roskilted-ros-core-noble)
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
-	[`ros:rolling-perception-noble`](#rosrolling-perception-noble)
-	[`ros:rolling-ros-base`](#rosrolling-ros-base)
-	[`ros:rolling-ros-base-noble`](#rosrolling-ros-base-noble)
-	[`ros:rolling-ros-core`](#rosrolling-ros-core)
-	[`ros:rolling-ros-core-noble`](#rosrolling-ros-core-noble)

## `ros:foxy`

```console
$ docker pull ros@sha256:34fbe32f5b1cd3eb25f6becaaa1d293bad754d64c31d96e638e4b30ed82f9f8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:foxy` - linux; amd64

```console
$ docker pull ros@sha256:078ac8eaffc953e97d4abf72f57da1fc33080b720b94bb1dc8c05ef4f7690367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255528741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d94b936914c0c299582ee509d62abd1fb86d1d181f68906a78efb53ed11289b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=foxy
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b6b4a7ecb05df2f70ab245fb4765a692ab3b761124a164ce42de55eb13f37a`  
		Last Modified: Mon, 09 Jun 2025 21:16:44 GMT  
		Size: 1.2 MB (1194822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c59f0b1081586aa99c6e582b439fdfb45aeb6d84953aaf308502434be8c6447`  
		Last Modified: Mon, 09 Jun 2025 21:16:45 GMT  
		Size: 10.0 MB (9982524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ee8b17bb34ee6c86ac4cc65d1afcdaca935dc6a6384c82b6e9270fc80796b`  
		Last Modified: Mon, 09 Jun 2025 21:16:45 GMT  
		Size: 4.0 KB (4042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4503d1eb268818ccfcfa60cce616bf269d09462dcce6bc97cddb4fc6c4093cc`  
		Last Modified: Mon, 09 Jun 2025 21:16:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac69b7953e35acff2c57bb856e9e8c7f5484f28093eedf764a04885357ec213`  
		Last Modified: Mon, 09 Jun 2025 21:16:54 GMT  
		Size: 121.5 MB (121535795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb82b370323b637277176e00ff105bfa5621b1c7d4e3364010bf52eed1af5165`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641f030e7bffcccfe0747baba44f7af6dd25fe525476bc3dfec496f0ca25231b`  
		Last Modified: Mon, 09 Jun 2025 21:39:32 GMT  
		Size: 73.3 MB (73324260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7992bd907c286578d31f6fa5849a571b36b7b96773c294e10ebd77f103066676`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 301.2 KB (301155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557e5ea1274e6719ae30e2c531a96fc11563836e1b355051cc6fee6456b1298b`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05613765d2b16f984507a7bceb0e742e814e822c16413dfe5a9d3eb3d6964980`  
		Last Modified: Mon, 09 Jun 2025 21:39:28 GMT  
		Size: 21.7 MB (21672813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy` - unknown; unknown

```console
$ docker pull ros@sha256:dff4a59ddac240692c3eb13999ffe63bf59de0633253cf39d524deba938f75e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22646736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b062eff39362fc854810dd58ba695860b169d46056706f2335964691c40672af`

```dockerfile
```

-	Layers:
	-	`sha256:50b901735eac590f22326e84eeedcf570de2072b887afbb5b9f93c6356262111`  
		Last Modified: Mon, 09 Jun 2025 22:17:24 GMT  
		Size: 22.6 MB (22629617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b6034fb143f7b17057c17af8739e99744162c20aa8da37a32f62337390f670e`  
		Last Modified: Mon, 09 Jun 2025 22:17:25 GMT  
		Size: 17.1 KB (17119 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:foxy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7bc031f0f6603d9ee6a21ccc0d8f6b9204d7f2a9e1dcbf9181cc0926c0e30a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230341771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc26bc4823a8f6a75600077ee19c659000952bef4c488a5b6db7101e7b6323a0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=foxy
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9c0dbae44ad3c2a486914616608617ea5ae7615405075d860ca9d037658472`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e5e017a927cc328a3bf6d46e7f5f8e4b6f03e2b8db2154f657bec065e0cb14`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e065b47e25afcc4719d7aa531dcb8d893610e9d8ad388e835a367718fb4897`  
		Last Modified: Mon, 09 Jun 2025 21:22:04 GMT  
		Size: 104.9 MB (104947330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bdbb3b522ee491f0b6571d32bf6183362277741d82a1edc73e3f7da2b246bd`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469ae630fae53c7ab2055ea3d53f0ca27a77a1a70f2d43f7b604ade498ac199e`  
		Last Modified: Mon, 09 Jun 2025 21:40:53 GMT  
		Size: 67.7 MB (67675196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3e71a66a3a86dc10acf882350a2523b1e91f63a713da6920a1adf47c46459`  
		Last Modified: Mon, 09 Jun 2025 21:40:49 GMT  
		Size: 301.2 KB (301152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e371813eea9c4f185fb2f53a18e98ccd8a84e1d9b06ef38727a07f34059570`  
		Last Modified: Mon, 09 Jun 2025 21:40:49 GMT  
		Size: 2.5 KB (2478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34406e2c7125d268c606619fec209daac599aed8ff794912378c2ace9488cb29`  
		Last Modified: Mon, 09 Jun 2025 21:40:51 GMT  
		Size: 20.4 MB (20399031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy` - unknown; unknown

```console
$ docker pull ros@sha256:d05593fbff060b58c59d1df728ea63a1b03e7729c4d21b1a8c3e7fbc23d92ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21566581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d2f7828474d6746cda7d49b0902cc26f931dc40d6127bcda25228b1650ac9d`

```dockerfile
```

-	Layers:
	-	`sha256:ee199d34c0becab0fc7f739e2f62b133a62f4fb33480343a0375dc2a107cd353`  
		Last Modified: Mon, 09 Jun 2025 22:17:39 GMT  
		Size: 21.5 MB (21549325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e5e0f353473f29a09dcf7cd9dda7d29044db2d358680183088ad9c6bef9fc31`  
		Last Modified: Mon, 09 Jun 2025 22:17:40 GMT  
		Size: 17.3 KB (17256 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:foxy-ros-base`

```console
$ docker pull ros@sha256:34fbe32f5b1cd3eb25f6becaaa1d293bad754d64c31d96e638e4b30ed82f9f8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:foxy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:078ac8eaffc953e97d4abf72f57da1fc33080b720b94bb1dc8c05ef4f7690367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255528741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d94b936914c0c299582ee509d62abd1fb86d1d181f68906a78efb53ed11289b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=foxy
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b6b4a7ecb05df2f70ab245fb4765a692ab3b761124a164ce42de55eb13f37a`  
		Last Modified: Mon, 09 Jun 2025 21:16:44 GMT  
		Size: 1.2 MB (1194822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c59f0b1081586aa99c6e582b439fdfb45aeb6d84953aaf308502434be8c6447`  
		Last Modified: Mon, 09 Jun 2025 21:16:45 GMT  
		Size: 10.0 MB (9982524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ee8b17bb34ee6c86ac4cc65d1afcdaca935dc6a6384c82b6e9270fc80796b`  
		Last Modified: Mon, 09 Jun 2025 21:16:45 GMT  
		Size: 4.0 KB (4042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4503d1eb268818ccfcfa60cce616bf269d09462dcce6bc97cddb4fc6c4093cc`  
		Last Modified: Mon, 09 Jun 2025 21:16:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac69b7953e35acff2c57bb856e9e8c7f5484f28093eedf764a04885357ec213`  
		Last Modified: Mon, 09 Jun 2025 21:16:54 GMT  
		Size: 121.5 MB (121535795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb82b370323b637277176e00ff105bfa5621b1c7d4e3364010bf52eed1af5165`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641f030e7bffcccfe0747baba44f7af6dd25fe525476bc3dfec496f0ca25231b`  
		Last Modified: Mon, 09 Jun 2025 21:39:32 GMT  
		Size: 73.3 MB (73324260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7992bd907c286578d31f6fa5849a571b36b7b96773c294e10ebd77f103066676`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 301.2 KB (301155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557e5ea1274e6719ae30e2c531a96fc11563836e1b355051cc6fee6456b1298b`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05613765d2b16f984507a7bceb0e742e814e822c16413dfe5a9d3eb3d6964980`  
		Last Modified: Mon, 09 Jun 2025 21:39:28 GMT  
		Size: 21.7 MB (21672813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:dff4a59ddac240692c3eb13999ffe63bf59de0633253cf39d524deba938f75e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22646736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b062eff39362fc854810dd58ba695860b169d46056706f2335964691c40672af`

```dockerfile
```

-	Layers:
	-	`sha256:50b901735eac590f22326e84eeedcf570de2072b887afbb5b9f93c6356262111`  
		Last Modified: Mon, 09 Jun 2025 22:17:24 GMT  
		Size: 22.6 MB (22629617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b6034fb143f7b17057c17af8739e99744162c20aa8da37a32f62337390f670e`  
		Last Modified: Mon, 09 Jun 2025 22:17:25 GMT  
		Size: 17.1 KB (17119 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:foxy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7bc031f0f6603d9ee6a21ccc0d8f6b9204d7f2a9e1dcbf9181cc0926c0e30a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230341771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc26bc4823a8f6a75600077ee19c659000952bef4c488a5b6db7101e7b6323a0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=foxy
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9c0dbae44ad3c2a486914616608617ea5ae7615405075d860ca9d037658472`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e5e017a927cc328a3bf6d46e7f5f8e4b6f03e2b8db2154f657bec065e0cb14`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e065b47e25afcc4719d7aa531dcb8d893610e9d8ad388e835a367718fb4897`  
		Last Modified: Mon, 09 Jun 2025 21:22:04 GMT  
		Size: 104.9 MB (104947330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bdbb3b522ee491f0b6571d32bf6183362277741d82a1edc73e3f7da2b246bd`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469ae630fae53c7ab2055ea3d53f0ca27a77a1a70f2d43f7b604ade498ac199e`  
		Last Modified: Mon, 09 Jun 2025 21:40:53 GMT  
		Size: 67.7 MB (67675196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3e71a66a3a86dc10acf882350a2523b1e91f63a713da6920a1adf47c46459`  
		Last Modified: Mon, 09 Jun 2025 21:40:49 GMT  
		Size: 301.2 KB (301152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e371813eea9c4f185fb2f53a18e98ccd8a84e1d9b06ef38727a07f34059570`  
		Last Modified: Mon, 09 Jun 2025 21:40:49 GMT  
		Size: 2.5 KB (2478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34406e2c7125d268c606619fec209daac599aed8ff794912378c2ace9488cb29`  
		Last Modified: Mon, 09 Jun 2025 21:40:51 GMT  
		Size: 20.4 MB (20399031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:d05593fbff060b58c59d1df728ea63a1b03e7729c4d21b1a8c3e7fbc23d92ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21566581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d2f7828474d6746cda7d49b0902cc26f931dc40d6127bcda25228b1650ac9d`

```dockerfile
```

-	Layers:
	-	`sha256:ee199d34c0becab0fc7f739e2f62b133a62f4fb33480343a0375dc2a107cd353`  
		Last Modified: Mon, 09 Jun 2025 22:17:39 GMT  
		Size: 21.5 MB (21549325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e5e0f353473f29a09dcf7cd9dda7d29044db2d358680183088ad9c6bef9fc31`  
		Last Modified: Mon, 09 Jun 2025 22:17:40 GMT  
		Size: 17.3 KB (17256 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:foxy-ros-base-focal`

```console
$ docker pull ros@sha256:34fbe32f5b1cd3eb25f6becaaa1d293bad754d64c31d96e638e4b30ed82f9f8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:foxy-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:078ac8eaffc953e97d4abf72f57da1fc33080b720b94bb1dc8c05ef4f7690367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255528741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d94b936914c0c299582ee509d62abd1fb86d1d181f68906a78efb53ed11289b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=foxy
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b6b4a7ecb05df2f70ab245fb4765a692ab3b761124a164ce42de55eb13f37a`  
		Last Modified: Mon, 09 Jun 2025 21:16:44 GMT  
		Size: 1.2 MB (1194822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c59f0b1081586aa99c6e582b439fdfb45aeb6d84953aaf308502434be8c6447`  
		Last Modified: Mon, 09 Jun 2025 21:16:45 GMT  
		Size: 10.0 MB (9982524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ee8b17bb34ee6c86ac4cc65d1afcdaca935dc6a6384c82b6e9270fc80796b`  
		Last Modified: Mon, 09 Jun 2025 21:16:45 GMT  
		Size: 4.0 KB (4042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4503d1eb268818ccfcfa60cce616bf269d09462dcce6bc97cddb4fc6c4093cc`  
		Last Modified: Mon, 09 Jun 2025 21:16:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac69b7953e35acff2c57bb856e9e8c7f5484f28093eedf764a04885357ec213`  
		Last Modified: Mon, 09 Jun 2025 21:16:54 GMT  
		Size: 121.5 MB (121535795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb82b370323b637277176e00ff105bfa5621b1c7d4e3364010bf52eed1af5165`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641f030e7bffcccfe0747baba44f7af6dd25fe525476bc3dfec496f0ca25231b`  
		Last Modified: Mon, 09 Jun 2025 21:39:32 GMT  
		Size: 73.3 MB (73324260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7992bd907c286578d31f6fa5849a571b36b7b96773c294e10ebd77f103066676`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 301.2 KB (301155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557e5ea1274e6719ae30e2c531a96fc11563836e1b355051cc6fee6456b1298b`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05613765d2b16f984507a7bceb0e742e814e822c16413dfe5a9d3eb3d6964980`  
		Last Modified: Mon, 09 Jun 2025 21:39:28 GMT  
		Size: 21.7 MB (21672813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:dff4a59ddac240692c3eb13999ffe63bf59de0633253cf39d524deba938f75e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22646736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b062eff39362fc854810dd58ba695860b169d46056706f2335964691c40672af`

```dockerfile
```

-	Layers:
	-	`sha256:50b901735eac590f22326e84eeedcf570de2072b887afbb5b9f93c6356262111`  
		Last Modified: Mon, 09 Jun 2025 22:17:24 GMT  
		Size: 22.6 MB (22629617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b6034fb143f7b17057c17af8739e99744162c20aa8da37a32f62337390f670e`  
		Last Modified: Mon, 09 Jun 2025 22:17:25 GMT  
		Size: 17.1 KB (17119 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:foxy-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7bc031f0f6603d9ee6a21ccc0d8f6b9204d7f2a9e1dcbf9181cc0926c0e30a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230341771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc26bc4823a8f6a75600077ee19c659000952bef4c488a5b6db7101e7b6323a0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=foxy
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9c0dbae44ad3c2a486914616608617ea5ae7615405075d860ca9d037658472`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e5e017a927cc328a3bf6d46e7f5f8e4b6f03e2b8db2154f657bec065e0cb14`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e065b47e25afcc4719d7aa531dcb8d893610e9d8ad388e835a367718fb4897`  
		Last Modified: Mon, 09 Jun 2025 21:22:04 GMT  
		Size: 104.9 MB (104947330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bdbb3b522ee491f0b6571d32bf6183362277741d82a1edc73e3f7da2b246bd`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469ae630fae53c7ab2055ea3d53f0ca27a77a1a70f2d43f7b604ade498ac199e`  
		Last Modified: Mon, 09 Jun 2025 21:40:53 GMT  
		Size: 67.7 MB (67675196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3e71a66a3a86dc10acf882350a2523b1e91f63a713da6920a1adf47c46459`  
		Last Modified: Mon, 09 Jun 2025 21:40:49 GMT  
		Size: 301.2 KB (301152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e371813eea9c4f185fb2f53a18e98ccd8a84e1d9b06ef38727a07f34059570`  
		Last Modified: Mon, 09 Jun 2025 21:40:49 GMT  
		Size: 2.5 KB (2478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34406e2c7125d268c606619fec209daac599aed8ff794912378c2ace9488cb29`  
		Last Modified: Mon, 09 Jun 2025 21:40:51 GMT  
		Size: 20.4 MB (20399031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:d05593fbff060b58c59d1df728ea63a1b03e7729c4d21b1a8c3e7fbc23d92ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21566581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d2f7828474d6746cda7d49b0902cc26f931dc40d6127bcda25228b1650ac9d`

```dockerfile
```

-	Layers:
	-	`sha256:ee199d34c0becab0fc7f739e2f62b133a62f4fb33480343a0375dc2a107cd353`  
		Last Modified: Mon, 09 Jun 2025 22:17:39 GMT  
		Size: 21.5 MB (21549325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e5e0f353473f29a09dcf7cd9dda7d29044db2d358680183088ad9c6bef9fc31`  
		Last Modified: Mon, 09 Jun 2025 22:17:40 GMT  
		Size: 17.3 KB (17256 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:foxy-ros-core`

```console
$ docker pull ros@sha256:33eea89feba24ddd6acc8a0f26a228fd51eaa04c5d613bce6484fecc5b9672d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:foxy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:37f516c975da9fffccad5722f6e283091076d27f63010437e6f0cbb8eee17200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160228052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30612372da30bb99f75b419609fe802646aa0c6b3c25a9f1d2b26fcb589edb06`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=foxy
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 07 Jun 2025 08:00:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b6b4a7ecb05df2f70ab245fb4765a692ab3b761124a164ce42de55eb13f37a`  
		Last Modified: Mon, 09 Jun 2025 21:16:44 GMT  
		Size: 1.2 MB (1194822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c59f0b1081586aa99c6e582b439fdfb45aeb6d84953aaf308502434be8c6447`  
		Last Modified: Mon, 09 Jun 2025 21:16:45 GMT  
		Size: 10.0 MB (9982524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ee8b17bb34ee6c86ac4cc65d1afcdaca935dc6a6384c82b6e9270fc80796b`  
		Last Modified: Mon, 09 Jun 2025 21:16:45 GMT  
		Size: 4.0 KB (4042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4503d1eb268818ccfcfa60cce616bf269d09462dcce6bc97cddb4fc6c4093cc`  
		Last Modified: Mon, 09 Jun 2025 21:16:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac69b7953e35acff2c57bb856e9e8c7f5484f28093eedf764a04885357ec213`  
		Last Modified: Mon, 09 Jun 2025 21:16:54 GMT  
		Size: 121.5 MB (121535795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb82b370323b637277176e00ff105bfa5621b1c7d4e3364010bf52eed1af5165`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:44100099fc13cc41f70b6ff2c828c155e3bb89d383b4341abff110f0181eab49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18632545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7517231377f3fbbb87f63c190dfc900be4ae92534943f10764982f70f76b55c3`

```dockerfile
```

-	Layers:
	-	`sha256:8032981490f8386c19b5abcc208184607fb91b79b2389697077d2cec528884c9`  
		Last Modified: Mon, 09 Jun 2025 22:17:33 GMT  
		Size: 18.6 MB (18616208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df57fb4951aab045f23edddbb9744b4397d1e67401002cf31d4728ade173eac4`  
		Last Modified: Mon, 09 Jun 2025 22:17:34 GMT  
		Size: 16.3 KB (16337 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:foxy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a2d2fce43c36a00a3294cf1b978359bb214dbab51c22ecfe80f5c9675373d4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141963914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3d1846b4748bca3a7b564a9a658dfd7f327e5bc3786e64d5fcadeabfd05998`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=foxy
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 07 Jun 2025 08:00:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9c0dbae44ad3c2a486914616608617ea5ae7615405075d860ca9d037658472`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e5e017a927cc328a3bf6d46e7f5f8e4b6f03e2b8db2154f657bec065e0cb14`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e065b47e25afcc4719d7aa531dcb8d893610e9d8ad388e835a367718fb4897`  
		Last Modified: Mon, 09 Jun 2025 21:22:04 GMT  
		Size: 104.9 MB (104947330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bdbb3b522ee491f0b6571d32bf6183362277741d82a1edc73e3f7da2b246bd`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:ee25430c3aae4129e4938cce0430fa409ac2865c5338012f8d5f7e2351ee9d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17551000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4758539f92d20dd7c92558e8ef489f1cbc6396b9668115e3205b26b553931bdf`

```dockerfile
```

-	Layers:
	-	`sha256:48d93cb3474a3e8cf25c65db57daa9ebefb7c3bf0478e21a3b9f11b96811979c`  
		Last Modified: Mon, 09 Jun 2025 22:17:50 GMT  
		Size: 17.5 MB (17534530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c40244fc71a0636c56d3030197efb6142bee9053c6a4c4a5d57132ab7c06aff`  
		Last Modified: Mon, 09 Jun 2025 22:17:50 GMT  
		Size: 16.5 KB (16470 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:foxy-ros-core-focal`

```console
$ docker pull ros@sha256:33eea89feba24ddd6acc8a0f26a228fd51eaa04c5d613bce6484fecc5b9672d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:foxy-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:37f516c975da9fffccad5722f6e283091076d27f63010437e6f0cbb8eee17200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160228052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30612372da30bb99f75b419609fe802646aa0c6b3c25a9f1d2b26fcb589edb06`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=foxy
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 07 Jun 2025 08:00:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b6b4a7ecb05df2f70ab245fb4765a692ab3b761124a164ce42de55eb13f37a`  
		Last Modified: Mon, 09 Jun 2025 21:16:44 GMT  
		Size: 1.2 MB (1194822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c59f0b1081586aa99c6e582b439fdfb45aeb6d84953aaf308502434be8c6447`  
		Last Modified: Mon, 09 Jun 2025 21:16:45 GMT  
		Size: 10.0 MB (9982524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ee8b17bb34ee6c86ac4cc65d1afcdaca935dc6a6384c82b6e9270fc80796b`  
		Last Modified: Mon, 09 Jun 2025 21:16:45 GMT  
		Size: 4.0 KB (4042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4503d1eb268818ccfcfa60cce616bf269d09462dcce6bc97cddb4fc6c4093cc`  
		Last Modified: Mon, 09 Jun 2025 21:16:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac69b7953e35acff2c57bb856e9e8c7f5484f28093eedf764a04885357ec213`  
		Last Modified: Mon, 09 Jun 2025 21:16:54 GMT  
		Size: 121.5 MB (121535795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb82b370323b637277176e00ff105bfa5621b1c7d4e3364010bf52eed1af5165`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:44100099fc13cc41f70b6ff2c828c155e3bb89d383b4341abff110f0181eab49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18632545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7517231377f3fbbb87f63c190dfc900be4ae92534943f10764982f70f76b55c3`

```dockerfile
```

-	Layers:
	-	`sha256:8032981490f8386c19b5abcc208184607fb91b79b2389697077d2cec528884c9`  
		Last Modified: Mon, 09 Jun 2025 22:17:33 GMT  
		Size: 18.6 MB (18616208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df57fb4951aab045f23edddbb9744b4397d1e67401002cf31d4728ade173eac4`  
		Last Modified: Mon, 09 Jun 2025 22:17:34 GMT  
		Size: 16.3 KB (16337 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:foxy-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a2d2fce43c36a00a3294cf1b978359bb214dbab51c22ecfe80f5c9675373d4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141963914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3d1846b4748bca3a7b564a9a658dfd7f327e5bc3786e64d5fcadeabfd05998`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=foxy
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 07 Jun 2025 08:00:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9c0dbae44ad3c2a486914616608617ea5ae7615405075d860ca9d037658472`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e5e017a927cc328a3bf6d46e7f5f8e4b6f03e2b8db2154f657bec065e0cb14`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e065b47e25afcc4719d7aa531dcb8d893610e9d8ad388e835a367718fb4897`  
		Last Modified: Mon, 09 Jun 2025 21:22:04 GMT  
		Size: 104.9 MB (104947330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bdbb3b522ee491f0b6571d32bf6183362277741d82a1edc73e3f7da2b246bd`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:ee25430c3aae4129e4938cce0430fa409ac2865c5338012f8d5f7e2351ee9d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17551000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4758539f92d20dd7c92558e8ef489f1cbc6396b9668115e3205b26b553931bdf`

```dockerfile
```

-	Layers:
	-	`sha256:48d93cb3474a3e8cf25c65db57daa9ebefb7c3bf0478e21a3b9f11b96811979c`  
		Last Modified: Mon, 09 Jun 2025 22:17:50 GMT  
		Size: 17.5 MB (17534530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c40244fc71a0636c56d3030197efb6142bee9053c6a4c4a5d57132ab7c06aff`  
		Last Modified: Mon, 09 Jun 2025 22:17:50 GMT  
		Size: 16.5 KB (16470 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:foxy-ros1-bridge`

```console
$ docker pull ros@sha256:b22bd431548c7f329c3c1f3c5417e40985b53f22e9857e22ff3e71d757967d18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:foxy-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:de1c8aaa89130f05dbd4975f80e27528a84f884063255e7644cecec05379eea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.7 MB (543656670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad4ca8a63bf5f732fb7b394814b4cce3056f177c61a1804ef6bc342b530c23e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=foxy
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS1_DISTRO=noetic
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS2_DISTRO=foxy
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.17.4-1*     ros-noetic-roscpp-tutorials=0.10.3-1*     ros-noetic-rospy-tutorials=0.10.3-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.7-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b6b4a7ecb05df2f70ab245fb4765a692ab3b761124a164ce42de55eb13f37a`  
		Last Modified: Mon, 09 Jun 2025 21:16:44 GMT  
		Size: 1.2 MB (1194822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c59f0b1081586aa99c6e582b439fdfb45aeb6d84953aaf308502434be8c6447`  
		Last Modified: Mon, 09 Jun 2025 21:16:45 GMT  
		Size: 10.0 MB (9982524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ee8b17bb34ee6c86ac4cc65d1afcdaca935dc6a6384c82b6e9270fc80796b`  
		Last Modified: Mon, 09 Jun 2025 21:16:45 GMT  
		Size: 4.0 KB (4042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4503d1eb268818ccfcfa60cce616bf269d09462dcce6bc97cddb4fc6c4093cc`  
		Last Modified: Mon, 09 Jun 2025 21:16:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac69b7953e35acff2c57bb856e9e8c7f5484f28093eedf764a04885357ec213`  
		Last Modified: Mon, 09 Jun 2025 21:16:54 GMT  
		Size: 121.5 MB (121535795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb82b370323b637277176e00ff105bfa5621b1c7d4e3364010bf52eed1af5165`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641f030e7bffcccfe0747baba44f7af6dd25fe525476bc3dfec496f0ca25231b`  
		Last Modified: Mon, 09 Jun 2025 21:39:32 GMT  
		Size: 73.3 MB (73324260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7992bd907c286578d31f6fa5849a571b36b7b96773c294e10ebd77f103066676`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 301.2 KB (301155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557e5ea1274e6719ae30e2c531a96fc11563836e1b355051cc6fee6456b1298b`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05613765d2b16f984507a7bceb0e742e814e822c16413dfe5a9d3eb3d6964980`  
		Last Modified: Mon, 09 Jun 2025 21:39:28 GMT  
		Size: 21.7 MB (21672813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e64fda5bae5a61863a5e59d0a5ef77d7c2bbf4a438b47eab0aa40199f15b43`  
		Last Modified: Mon, 09 Jun 2025 21:45:20 GMT  
		Size: 4.0 KB (4041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab802a4ff0e43df0a701f10b18cfda3603f618895a434c033d25e5075f46e78a`  
		Last Modified: Mon, 09 Jun 2025 21:45:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aae94330fcaff2780466afe5e118dab6e5e18206c0d3618361192644d1eb668`  
		Last Modified: Tue, 10 Jun 2025 04:38:50 GMT  
		Size: 266.6 MB (266595963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160682a67416d67f284ec74e1a471cb7b449f0dbef147bfe1ed59bd825fd0253`  
		Last Modified: Mon, 09 Jun 2025 21:45:23 GMT  
		Size: 21.5 MB (21527366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975b003866e73673e5446f5c6bca1a95bc533887b921162cb5ff7c860af12a6a`  
		Last Modified: Mon, 09 Jun 2025 21:45:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros1-bridge` - unknown; unknown

```console
$ docker pull ros@sha256:20636e794adce8327f41e9d59d1fc6d898bd37113d984aa5d782aea6aaf10269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43488904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7eab8b0dbde855009ec783110e3fd6fabda983dc73bb2720dc7af75ba509aa`

```dockerfile
```

-	Layers:
	-	`sha256:dff2c0e077e3576987993bc5faefbf6fc717a8265849d6497af5ab6402556a79`  
		Last Modified: Mon, 09 Jun 2025 22:17:45 GMT  
		Size: 43.5 MB (43461018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30f2c7c41fffdee2dd1ab8ba1456386dcba889f8063953f2066b9e334e30e96`  
		Last Modified: Mon, 09 Jun 2025 22:17:46 GMT  
		Size: 27.9 KB (27886 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:foxy-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2a45cf74cfdf4f6968094b656f3af4a8f99dc8d5ea370bac948328de2663a84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.4 MB (508401122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728409448ce4ecc91e60a5f48c4d0d0800a1295a2d6e139316002fb37fc56923`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=foxy
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS1_DISTRO=noetic
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS2_DISTRO=foxy
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.17.4-1*     ros-noetic-roscpp-tutorials=0.10.3-1*     ros-noetic-rospy-tutorials=0.10.3-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.7-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9c0dbae44ad3c2a486914616608617ea5ae7615405075d860ca9d037658472`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e5e017a927cc328a3bf6d46e7f5f8e4b6f03e2b8db2154f657bec065e0cb14`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e065b47e25afcc4719d7aa531dcb8d893610e9d8ad388e835a367718fb4897`  
		Last Modified: Mon, 09 Jun 2025 21:22:04 GMT  
		Size: 104.9 MB (104947330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bdbb3b522ee491f0b6571d32bf6183362277741d82a1edc73e3f7da2b246bd`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469ae630fae53c7ab2055ea3d53f0ca27a77a1a70f2d43f7b604ade498ac199e`  
		Last Modified: Mon, 09 Jun 2025 21:40:53 GMT  
		Size: 67.7 MB (67675196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3e71a66a3a86dc10acf882350a2523b1e91f63a713da6920a1adf47c46459`  
		Last Modified: Mon, 09 Jun 2025 21:40:49 GMT  
		Size: 301.2 KB (301152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e371813eea9c4f185fb2f53a18e98ccd8a84e1d9b06ef38727a07f34059570`  
		Last Modified: Mon, 09 Jun 2025 21:40:49 GMT  
		Size: 2.5 KB (2478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34406e2c7125d268c606619fec209daac599aed8ff794912378c2ace9488cb29`  
		Last Modified: Mon, 09 Jun 2025 21:40:51 GMT  
		Size: 20.4 MB (20399031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d68c10a7a245451454382c443b8762047c631763657f710726dd777a900cd03`  
		Last Modified: Mon, 09 Jun 2025 21:52:37 GMT  
		Size: 4.0 KB (4050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e03ce9014ab5e7ffb8c26d05d8a659767ce8534d5563a2d9fd0d876beec5cc`  
		Last Modified: Mon, 09 Jun 2025 21:52:38 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e954e2c82942236430969db994323bfbc2ea0235c053530747d99e6b03f779`  
		Last Modified: Mon, 09 Jun 2025 21:52:15 GMT  
		Size: 263.9 MB (263888200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f29a713482afc94946a4e6d95c626b06d87973e1fbf3bc2a998ba36611e75e`  
		Last Modified: Mon, 09 Jun 2025 21:52:39 GMT  
		Size: 14.2 MB (14166541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd5c3d11ef8ac05a7fda6f247518cc62232c4198e6e21ea18d7c61e7fede0e5`  
		Last Modified: Mon, 09 Jun 2025 21:52:38 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros1-bridge` - unknown; unknown

```console
$ docker pull ros@sha256:88f3a3a1f798961f3f54082051b6374403eabf5f48acbf3b3206069974a604b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41830004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1be3b8bdf918c686b1fb0647c07de2f0a23a22285084a9acc058bcf98bfb19`

```dockerfile
```

-	Layers:
	-	`sha256:783aa4088a7e20c04b34201cdb39b15ade9dad13f08fd5067d44f3f2c2621418`  
		Last Modified: Mon, 09 Jun 2025 22:18:39 GMT  
		Size: 41.8 MB (41801979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:723cdf002feaf93d7ec74e6c316c2bb9c31e999ee209d088ff4e275d19956d18`  
		Last Modified: Mon, 09 Jun 2025 22:18:40 GMT  
		Size: 28.0 KB (28025 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:b22bd431548c7f329c3c1f3c5417e40985b53f22e9857e22ff3e71d757967d18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:de1c8aaa89130f05dbd4975f80e27528a84f884063255e7644cecec05379eea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.7 MB (543656670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad4ca8a63bf5f732fb7b394814b4cce3056f177c61a1804ef6bc342b530c23e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=foxy
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS1_DISTRO=noetic
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS2_DISTRO=foxy
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.17.4-1*     ros-noetic-roscpp-tutorials=0.10.3-1*     ros-noetic-rospy-tutorials=0.10.3-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.7-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b6b4a7ecb05df2f70ab245fb4765a692ab3b761124a164ce42de55eb13f37a`  
		Last Modified: Mon, 09 Jun 2025 21:16:44 GMT  
		Size: 1.2 MB (1194822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c59f0b1081586aa99c6e582b439fdfb45aeb6d84953aaf308502434be8c6447`  
		Last Modified: Mon, 09 Jun 2025 21:16:45 GMT  
		Size: 10.0 MB (9982524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ee8b17bb34ee6c86ac4cc65d1afcdaca935dc6a6384c82b6e9270fc80796b`  
		Last Modified: Mon, 09 Jun 2025 21:16:45 GMT  
		Size: 4.0 KB (4042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4503d1eb268818ccfcfa60cce616bf269d09462dcce6bc97cddb4fc6c4093cc`  
		Last Modified: Mon, 09 Jun 2025 21:16:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac69b7953e35acff2c57bb856e9e8c7f5484f28093eedf764a04885357ec213`  
		Last Modified: Mon, 09 Jun 2025 21:16:54 GMT  
		Size: 121.5 MB (121535795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb82b370323b637277176e00ff105bfa5621b1c7d4e3364010bf52eed1af5165`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641f030e7bffcccfe0747baba44f7af6dd25fe525476bc3dfec496f0ca25231b`  
		Last Modified: Mon, 09 Jun 2025 21:39:32 GMT  
		Size: 73.3 MB (73324260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7992bd907c286578d31f6fa5849a571b36b7b96773c294e10ebd77f103066676`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 301.2 KB (301155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557e5ea1274e6719ae30e2c531a96fc11563836e1b355051cc6fee6456b1298b`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05613765d2b16f984507a7bceb0e742e814e822c16413dfe5a9d3eb3d6964980`  
		Last Modified: Mon, 09 Jun 2025 21:39:28 GMT  
		Size: 21.7 MB (21672813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e64fda5bae5a61863a5e59d0a5ef77d7c2bbf4a438b47eab0aa40199f15b43`  
		Last Modified: Mon, 09 Jun 2025 21:45:20 GMT  
		Size: 4.0 KB (4041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab802a4ff0e43df0a701f10b18cfda3603f618895a434c033d25e5075f46e78a`  
		Last Modified: Mon, 09 Jun 2025 21:45:21 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aae94330fcaff2780466afe5e118dab6e5e18206c0d3618361192644d1eb668`  
		Last Modified: Tue, 10 Jun 2025 04:38:50 GMT  
		Size: 266.6 MB (266595963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160682a67416d67f284ec74e1a471cb7b449f0dbef147bfe1ed59bd825fd0253`  
		Last Modified: Mon, 09 Jun 2025 21:45:23 GMT  
		Size: 21.5 MB (21527366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975b003866e73673e5446f5c6bca1a95bc533887b921162cb5ff7c860af12a6a`  
		Last Modified: Mon, 09 Jun 2025 21:45:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros1-bridge-focal` - unknown; unknown

```console
$ docker pull ros@sha256:20636e794adce8327f41e9d59d1fc6d898bd37113d984aa5d782aea6aaf10269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43488904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7eab8b0dbde855009ec783110e3fd6fabda983dc73bb2720dc7af75ba509aa`

```dockerfile
```

-	Layers:
	-	`sha256:dff2c0e077e3576987993bc5faefbf6fc717a8265849d6497af5ab6402556a79`  
		Last Modified: Mon, 09 Jun 2025 22:17:45 GMT  
		Size: 43.5 MB (43461018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30f2c7c41fffdee2dd1ab8ba1456386dcba889f8063953f2066b9e334e30e96`  
		Last Modified: Mon, 09 Jun 2025 22:17:46 GMT  
		Size: 27.9 KB (27886 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2a45cf74cfdf4f6968094b656f3af4a8f99dc8d5ea370bac948328de2663a84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.4 MB (508401122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728409448ce4ecc91e60a5f48c4d0d0800a1295a2d6e139316002fb37fc56923`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=foxy
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS1_DISTRO=noetic
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS2_DISTRO=foxy
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.17.4-1*     ros-noetic-roscpp-tutorials=0.10.3-1*     ros-noetic-rospy-tutorials=0.10.3-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.7-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9c0dbae44ad3c2a486914616608617ea5ae7615405075d860ca9d037658472`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e5e017a927cc328a3bf6d46e7f5f8e4b6f03e2b8db2154f657bec065e0cb14`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e065b47e25afcc4719d7aa531dcb8d893610e9d8ad388e835a367718fb4897`  
		Last Modified: Mon, 09 Jun 2025 21:22:04 GMT  
		Size: 104.9 MB (104947330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bdbb3b522ee491f0b6571d32bf6183362277741d82a1edc73e3f7da2b246bd`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469ae630fae53c7ab2055ea3d53f0ca27a77a1a70f2d43f7b604ade498ac199e`  
		Last Modified: Mon, 09 Jun 2025 21:40:53 GMT  
		Size: 67.7 MB (67675196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae3e71a66a3a86dc10acf882350a2523b1e91f63a713da6920a1adf47c46459`  
		Last Modified: Mon, 09 Jun 2025 21:40:49 GMT  
		Size: 301.2 KB (301152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e371813eea9c4f185fb2f53a18e98ccd8a84e1d9b06ef38727a07f34059570`  
		Last Modified: Mon, 09 Jun 2025 21:40:49 GMT  
		Size: 2.5 KB (2478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34406e2c7125d268c606619fec209daac599aed8ff794912378c2ace9488cb29`  
		Last Modified: Mon, 09 Jun 2025 21:40:51 GMT  
		Size: 20.4 MB (20399031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d68c10a7a245451454382c443b8762047c631763657f710726dd777a900cd03`  
		Last Modified: Mon, 09 Jun 2025 21:52:37 GMT  
		Size: 4.0 KB (4050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e03ce9014ab5e7ffb8c26d05d8a659767ce8534d5563a2d9fd0d876beec5cc`  
		Last Modified: Mon, 09 Jun 2025 21:52:38 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e954e2c82942236430969db994323bfbc2ea0235c053530747d99e6b03f779`  
		Last Modified: Mon, 09 Jun 2025 21:52:15 GMT  
		Size: 263.9 MB (263888200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f29a713482afc94946a4e6d95c626b06d87973e1fbf3bc2a998ba36611e75e`  
		Last Modified: Mon, 09 Jun 2025 21:52:39 GMT  
		Size: 14.2 MB (14166541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd5c3d11ef8ac05a7fda6f247518cc62232c4198e6e21ea18d7c61e7fede0e5`  
		Last Modified: Mon, 09 Jun 2025 21:52:38 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros1-bridge-focal` - unknown; unknown

```console
$ docker pull ros@sha256:88f3a3a1f798961f3f54082051b6374403eabf5f48acbf3b3206069974a604b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41830004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1be3b8bdf918c686b1fb0647c07de2f0a23a22285084a9acc058bcf98bfb19`

```dockerfile
```

-	Layers:
	-	`sha256:783aa4088a7e20c04b34201cdb39b15ade9dad13f08fd5067d44f3f2c2621418`  
		Last Modified: Mon, 09 Jun 2025 22:18:39 GMT  
		Size: 41.8 MB (41801979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:723cdf002feaf93d7ec74e6c316c2bb9c31e999ee209d088ff4e275d19956d18`  
		Last Modified: Mon, 09 Jun 2025 22:18:40 GMT  
		Size: 28.0 KB (28025 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:galactic`

```console
$ docker pull ros@sha256:f0d881da46516a06ffa1c241dd7e41a60a45b6fdeb71fe4100258f928186b08f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:galactic` - linux; amd64

```console
$ docker pull ros@sha256:02854831d159fd68b0666c827513c155ea54c0e8d3f08b2af551cdc47f423e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239541550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15b34f9aa6e3e006701be5152f2a6e7735778b5f4c568cc439b3e448d376729`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 May 2021 09:27:44 GMT
ARG RELEASE
# Tue, 25 May 2021 09:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 May 2021 09:27:44 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 25 May 2021 09:27:44 GMT
CMD ["/bin/bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENV LANG=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 May 2021 09:27:44 GMT
CMD ["bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11052161241e41a57b1cbb6ef459473de4ccf5cc8cb12c67052f79b515002f0a`  
		Last Modified: Mon, 09 Jun 2025 21:16:47 GMT  
		Size: 1.2 MB (1194828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931cee7ca53b99f574090e76c6443814931e6dc63cd60275d83c8a8618882c45`  
		Last Modified: Mon, 09 Jun 2025 21:16:47 GMT  
		Size: 10.0 MB (9982545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff0cd693b0e9a7b595721f2c18fc344735cff6dd852a68e4566e97c4abe888c`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 4.0 KB (4043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff68de3e6e4d94da44fd46aaac8d51e075d6b4d2e63547ee4661ccc80f1b6538`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64f09c9c0a539389b70e14ae98f3b1b07c00c6cc24224d7f35361e11faccfe`  
		Last Modified: Mon, 09 Jun 2025 21:16:52 GMT  
		Size: 105.1 MB (105130927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cae04d994b8a94412416c264258dcac3f5b4d7632662ba09ae69b75c995d411`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253e2d090968ae89743bbc0954bbaff92e4d1cf5edb29f37fb2280091749d623`  
		Last Modified: Mon, 09 Jun 2025 21:39:31 GMT  
		Size: 73.3 MB (73268914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc26cf621e6a72aaa5d3eb0f5a09aee8538a839398139f320377d2a72f53c5d`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 308.6 KB (308610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf544bbac493b95c4a165fc116cd06e7f0b5a0d5f4d33c5badb04d06c596dbf`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d465cf5a0978d969e83313b858f2bf01cb90f173f91ad5a034d3de674974931`  
		Last Modified: Mon, 09 Jun 2025 21:39:28 GMT  
		Size: 22.1 MB (22138329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic` - unknown; unknown

```console
$ docker pull ros@sha256:21eecbb14cdccafdd9eea4494e67d0b610d33f049a9e604bf397949aa037d08d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21776179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50d373342349c84c900c827495e61a0b5daf1e33a0db46139bb7ee2422aff7c`

```dockerfile
```

-	Layers:
	-	`sha256:33b77849b3a644d939b5ef2694a67a48efc5db2b4c469a34ac94599d7ed66c48`  
		Last Modified: Mon, 09 Jun 2025 22:17:53 GMT  
		Size: 21.8 MB (21758992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e414fa61cc8920d268a7f6382f4a23d43170d3a948c7f50733ed052a6eb595a0`  
		Last Modified: Mon, 09 Jun 2025 22:17:54 GMT  
		Size: 17.2 KB (17187 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:galactic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a5f283e06383d5ca3740b46cfd8da263b6e4adf188937708dcf41818cacc143f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227175359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc83cfa592bc4cb5899fabac74678125039a96f07f7ef32b07d4b0dc973ab4f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 May 2021 09:27:44 GMT
ARG RELEASE
# Tue, 25 May 2021 09:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 May 2021 09:27:44 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 25 May 2021 09:27:44 GMT
CMD ["/bin/bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENV LANG=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 May 2021 09:27:44 GMT
CMD ["bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9c0dbae44ad3c2a486914616608617ea5ae7615405075d860ca9d037658472`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dabd21457018d5fffe84a3291535b717890deff8c93a12e7cf4a69e1f23614c`  
		Last Modified: Mon, 09 Jun 2025 21:23:15 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc9cc0fca6354a9e10d48dc43c584ba2f2bfe621df6f2466584a2a5bc12ce5`  
		Last Modified: Mon, 09 Jun 2025 21:23:22 GMT  
		Size: 100.7 MB (100749299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908c356d108f7fc63c325ef52dfc5ceb7c197b2ad917d5c4e64c4d0ce9992940`  
		Last Modified: Mon, 09 Jun 2025 21:23:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5acbcd197ca2dd8f85a827ba1ed6820e86c136f1ab4985faaf3bf8cbfa5a739`  
		Last Modified: Mon, 09 Jun 2025 21:42:36 GMT  
		Size: 67.6 MB (67617373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208649ea3be9f05fa2e17c11294e68dc52f05a0923235b10ca3df0213eec0efa`  
		Last Modified: Mon, 09 Jun 2025 21:42:32 GMT  
		Size: 308.6 KB (308607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d142d51b07449e8ce86f0d2de6671d5b67a4d18fc5fc90600f4e3e432b3ae4`  
		Last Modified: Mon, 09 Jun 2025 21:42:32 GMT  
		Size: 2.5 KB (2468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90e400c2e79021db0693711a8489954b121a4d0785902a1f433ed75e65ffefa`  
		Last Modified: Mon, 09 Jun 2025 21:42:35 GMT  
		Size: 21.5 MB (21481027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic` - unknown; unknown

```console
$ docker pull ros@sha256:4c5e44de34c8f5117d7258ad65472e2f1f853fce628e55dbb82e88a6c0e2d246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21796899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4851f085dc150a1982d92510983a60fe5251c61f79e09c487c1ae2533f48e8e4`

```dockerfile
```

-	Layers:
	-	`sha256:f9fb3e303297b47cdab714de2fe062cf76939a6b2520714d4c3d7e79024ec19d`  
		Last Modified: Mon, 09 Jun 2025 22:18:10 GMT  
		Size: 21.8 MB (21779575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cfcd5600be104f04ae7e10878137770c88bcd1c10dc34d8fa236030fe3ccaad`  
		Last Modified: Mon, 09 Jun 2025 22:18:11 GMT  
		Size: 17.3 KB (17324 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:galactic-ros-base`

```console
$ docker pull ros@sha256:f0d881da46516a06ffa1c241dd7e41a60a45b6fdeb71fe4100258f928186b08f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:galactic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:02854831d159fd68b0666c827513c155ea54c0e8d3f08b2af551cdc47f423e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239541550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15b34f9aa6e3e006701be5152f2a6e7735778b5f4c568cc439b3e448d376729`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 May 2021 09:27:44 GMT
ARG RELEASE
# Tue, 25 May 2021 09:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 May 2021 09:27:44 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 25 May 2021 09:27:44 GMT
CMD ["/bin/bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENV LANG=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 May 2021 09:27:44 GMT
CMD ["bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11052161241e41a57b1cbb6ef459473de4ccf5cc8cb12c67052f79b515002f0a`  
		Last Modified: Mon, 09 Jun 2025 21:16:47 GMT  
		Size: 1.2 MB (1194828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931cee7ca53b99f574090e76c6443814931e6dc63cd60275d83c8a8618882c45`  
		Last Modified: Mon, 09 Jun 2025 21:16:47 GMT  
		Size: 10.0 MB (9982545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff0cd693b0e9a7b595721f2c18fc344735cff6dd852a68e4566e97c4abe888c`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 4.0 KB (4043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff68de3e6e4d94da44fd46aaac8d51e075d6b4d2e63547ee4661ccc80f1b6538`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64f09c9c0a539389b70e14ae98f3b1b07c00c6cc24224d7f35361e11faccfe`  
		Last Modified: Mon, 09 Jun 2025 21:16:52 GMT  
		Size: 105.1 MB (105130927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cae04d994b8a94412416c264258dcac3f5b4d7632662ba09ae69b75c995d411`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253e2d090968ae89743bbc0954bbaff92e4d1cf5edb29f37fb2280091749d623`  
		Last Modified: Mon, 09 Jun 2025 21:39:31 GMT  
		Size: 73.3 MB (73268914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc26cf621e6a72aaa5d3eb0f5a09aee8538a839398139f320377d2a72f53c5d`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 308.6 KB (308610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf544bbac493b95c4a165fc116cd06e7f0b5a0d5f4d33c5badb04d06c596dbf`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d465cf5a0978d969e83313b858f2bf01cb90f173f91ad5a034d3de674974931`  
		Last Modified: Mon, 09 Jun 2025 21:39:28 GMT  
		Size: 22.1 MB (22138329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:21eecbb14cdccafdd9eea4494e67d0b610d33f049a9e604bf397949aa037d08d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21776179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50d373342349c84c900c827495e61a0b5daf1e33a0db46139bb7ee2422aff7c`

```dockerfile
```

-	Layers:
	-	`sha256:33b77849b3a644d939b5ef2694a67a48efc5db2b4c469a34ac94599d7ed66c48`  
		Last Modified: Mon, 09 Jun 2025 22:17:53 GMT  
		Size: 21.8 MB (21758992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e414fa61cc8920d268a7f6382f4a23d43170d3a948c7f50733ed052a6eb595a0`  
		Last Modified: Mon, 09 Jun 2025 22:17:54 GMT  
		Size: 17.2 KB (17187 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:galactic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a5f283e06383d5ca3740b46cfd8da263b6e4adf188937708dcf41818cacc143f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227175359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc83cfa592bc4cb5899fabac74678125039a96f07f7ef32b07d4b0dc973ab4f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 May 2021 09:27:44 GMT
ARG RELEASE
# Tue, 25 May 2021 09:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 May 2021 09:27:44 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 25 May 2021 09:27:44 GMT
CMD ["/bin/bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENV LANG=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 May 2021 09:27:44 GMT
CMD ["bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9c0dbae44ad3c2a486914616608617ea5ae7615405075d860ca9d037658472`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dabd21457018d5fffe84a3291535b717890deff8c93a12e7cf4a69e1f23614c`  
		Last Modified: Mon, 09 Jun 2025 21:23:15 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc9cc0fca6354a9e10d48dc43c584ba2f2bfe621df6f2466584a2a5bc12ce5`  
		Last Modified: Mon, 09 Jun 2025 21:23:22 GMT  
		Size: 100.7 MB (100749299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908c356d108f7fc63c325ef52dfc5ceb7c197b2ad917d5c4e64c4d0ce9992940`  
		Last Modified: Mon, 09 Jun 2025 21:23:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5acbcd197ca2dd8f85a827ba1ed6820e86c136f1ab4985faaf3bf8cbfa5a739`  
		Last Modified: Mon, 09 Jun 2025 21:42:36 GMT  
		Size: 67.6 MB (67617373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208649ea3be9f05fa2e17c11294e68dc52f05a0923235b10ca3df0213eec0efa`  
		Last Modified: Mon, 09 Jun 2025 21:42:32 GMT  
		Size: 308.6 KB (308607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d142d51b07449e8ce86f0d2de6671d5b67a4d18fc5fc90600f4e3e432b3ae4`  
		Last Modified: Mon, 09 Jun 2025 21:42:32 GMT  
		Size: 2.5 KB (2468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90e400c2e79021db0693711a8489954b121a4d0785902a1f433ed75e65ffefa`  
		Last Modified: Mon, 09 Jun 2025 21:42:35 GMT  
		Size: 21.5 MB (21481027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:4c5e44de34c8f5117d7258ad65472e2f1f853fce628e55dbb82e88a6c0e2d246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21796899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4851f085dc150a1982d92510983a60fe5251c61f79e09c487c1ae2533f48e8e4`

```dockerfile
```

-	Layers:
	-	`sha256:f9fb3e303297b47cdab714de2fe062cf76939a6b2520714d4c3d7e79024ec19d`  
		Last Modified: Mon, 09 Jun 2025 22:18:10 GMT  
		Size: 21.8 MB (21779575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cfcd5600be104f04ae7e10878137770c88bcd1c10dc34d8fa236030fe3ccaad`  
		Last Modified: Mon, 09 Jun 2025 22:18:11 GMT  
		Size: 17.3 KB (17324 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:galactic-ros-base-focal`

```console
$ docker pull ros@sha256:f0d881da46516a06ffa1c241dd7e41a60a45b6fdeb71fe4100258f928186b08f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:galactic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:02854831d159fd68b0666c827513c155ea54c0e8d3f08b2af551cdc47f423e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239541550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15b34f9aa6e3e006701be5152f2a6e7735778b5f4c568cc439b3e448d376729`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 May 2021 09:27:44 GMT
ARG RELEASE
# Tue, 25 May 2021 09:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 May 2021 09:27:44 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 25 May 2021 09:27:44 GMT
CMD ["/bin/bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENV LANG=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 May 2021 09:27:44 GMT
CMD ["bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11052161241e41a57b1cbb6ef459473de4ccf5cc8cb12c67052f79b515002f0a`  
		Last Modified: Mon, 09 Jun 2025 21:16:47 GMT  
		Size: 1.2 MB (1194828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931cee7ca53b99f574090e76c6443814931e6dc63cd60275d83c8a8618882c45`  
		Last Modified: Mon, 09 Jun 2025 21:16:47 GMT  
		Size: 10.0 MB (9982545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff0cd693b0e9a7b595721f2c18fc344735cff6dd852a68e4566e97c4abe888c`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 4.0 KB (4043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff68de3e6e4d94da44fd46aaac8d51e075d6b4d2e63547ee4661ccc80f1b6538`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64f09c9c0a539389b70e14ae98f3b1b07c00c6cc24224d7f35361e11faccfe`  
		Last Modified: Mon, 09 Jun 2025 21:16:52 GMT  
		Size: 105.1 MB (105130927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cae04d994b8a94412416c264258dcac3f5b4d7632662ba09ae69b75c995d411`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253e2d090968ae89743bbc0954bbaff92e4d1cf5edb29f37fb2280091749d623`  
		Last Modified: Mon, 09 Jun 2025 21:39:31 GMT  
		Size: 73.3 MB (73268914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc26cf621e6a72aaa5d3eb0f5a09aee8538a839398139f320377d2a72f53c5d`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 308.6 KB (308610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf544bbac493b95c4a165fc116cd06e7f0b5a0d5f4d33c5badb04d06c596dbf`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d465cf5a0978d969e83313b858f2bf01cb90f173f91ad5a034d3de674974931`  
		Last Modified: Mon, 09 Jun 2025 21:39:28 GMT  
		Size: 22.1 MB (22138329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:21eecbb14cdccafdd9eea4494e67d0b610d33f049a9e604bf397949aa037d08d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21776179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50d373342349c84c900c827495e61a0b5daf1e33a0db46139bb7ee2422aff7c`

```dockerfile
```

-	Layers:
	-	`sha256:33b77849b3a644d939b5ef2694a67a48efc5db2b4c469a34ac94599d7ed66c48`  
		Last Modified: Mon, 09 Jun 2025 22:17:53 GMT  
		Size: 21.8 MB (21758992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e414fa61cc8920d268a7f6382f4a23d43170d3a948c7f50733ed052a6eb595a0`  
		Last Modified: Mon, 09 Jun 2025 22:17:54 GMT  
		Size: 17.2 KB (17187 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:galactic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a5f283e06383d5ca3740b46cfd8da263b6e4adf188937708dcf41818cacc143f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227175359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc83cfa592bc4cb5899fabac74678125039a96f07f7ef32b07d4b0dc973ab4f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 May 2021 09:27:44 GMT
ARG RELEASE
# Tue, 25 May 2021 09:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 May 2021 09:27:44 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 25 May 2021 09:27:44 GMT
CMD ["/bin/bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENV LANG=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 May 2021 09:27:44 GMT
CMD ["bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9c0dbae44ad3c2a486914616608617ea5ae7615405075d860ca9d037658472`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dabd21457018d5fffe84a3291535b717890deff8c93a12e7cf4a69e1f23614c`  
		Last Modified: Mon, 09 Jun 2025 21:23:15 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc9cc0fca6354a9e10d48dc43c584ba2f2bfe621df6f2466584a2a5bc12ce5`  
		Last Modified: Mon, 09 Jun 2025 21:23:22 GMT  
		Size: 100.7 MB (100749299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908c356d108f7fc63c325ef52dfc5ceb7c197b2ad917d5c4e64c4d0ce9992940`  
		Last Modified: Mon, 09 Jun 2025 21:23:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5acbcd197ca2dd8f85a827ba1ed6820e86c136f1ab4985faaf3bf8cbfa5a739`  
		Last Modified: Mon, 09 Jun 2025 21:42:36 GMT  
		Size: 67.6 MB (67617373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208649ea3be9f05fa2e17c11294e68dc52f05a0923235b10ca3df0213eec0efa`  
		Last Modified: Mon, 09 Jun 2025 21:42:32 GMT  
		Size: 308.6 KB (308607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d142d51b07449e8ce86f0d2de6671d5b67a4d18fc5fc90600f4e3e432b3ae4`  
		Last Modified: Mon, 09 Jun 2025 21:42:32 GMT  
		Size: 2.5 KB (2468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90e400c2e79021db0693711a8489954b121a4d0785902a1f433ed75e65ffefa`  
		Last Modified: Mon, 09 Jun 2025 21:42:35 GMT  
		Size: 21.5 MB (21481027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:4c5e44de34c8f5117d7258ad65472e2f1f853fce628e55dbb82e88a6c0e2d246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21796899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4851f085dc150a1982d92510983a60fe5251c61f79e09c487c1ae2533f48e8e4`

```dockerfile
```

-	Layers:
	-	`sha256:f9fb3e303297b47cdab714de2fe062cf76939a6b2520714d4c3d7e79024ec19d`  
		Last Modified: Mon, 09 Jun 2025 22:18:10 GMT  
		Size: 21.8 MB (21779575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cfcd5600be104f04ae7e10878137770c88bcd1c10dc34d8fa236030fe3ccaad`  
		Last Modified: Mon, 09 Jun 2025 22:18:11 GMT  
		Size: 17.3 KB (17324 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:galactic-ros-core`

```console
$ docker pull ros@sha256:a3717e650d2c1ebdc85166a3f64b49c2cf8338679babff36cae622c93c8a0d81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:galactic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:f433ebe87c80db8d001b366688da325536a5603c1be2a766ef4284096bf1d78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143823215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c549bf02d5f5c532d835fb1b85a744a23e7c9521a9e773e2c84dcee30463e9e5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=galactic
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 07 Jun 2025 08:00:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11052161241e41a57b1cbb6ef459473de4ccf5cc8cb12c67052f79b515002f0a`  
		Last Modified: Mon, 09 Jun 2025 21:16:47 GMT  
		Size: 1.2 MB (1194828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931cee7ca53b99f574090e76c6443814931e6dc63cd60275d83c8a8618882c45`  
		Last Modified: Mon, 09 Jun 2025 21:16:47 GMT  
		Size: 10.0 MB (9982545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff0cd693b0e9a7b595721f2c18fc344735cff6dd852a68e4566e97c4abe888c`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 4.0 KB (4043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff68de3e6e4d94da44fd46aaac8d51e075d6b4d2e63547ee4661ccc80f1b6538`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64f09c9c0a539389b70e14ae98f3b1b07c00c6cc24224d7f35361e11faccfe`  
		Last Modified: Mon, 09 Jun 2025 21:16:52 GMT  
		Size: 105.1 MB (105130927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cae04d994b8a94412416c264258dcac3f5b4d7632662ba09ae69b75c995d411`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:ec5efeb461ee54afd417411274bbb1c6d2cbea7bc9c320292ede300b4a7f239e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17533939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42a6fa891c8a5d787a6d7e3a1036b59a5ab0424990380fcbac5a30381e76373`

```dockerfile
```

-	Layers:
	-	`sha256:43e8dbd1f7ca4668035f3b1a23afc26c35fd078140a0059545b779198d0362de`  
		Last Modified: Mon, 09 Jun 2025 22:18:01 GMT  
		Size: 17.5 MB (17517546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64b651d5f72059331b9033f24be143c321b1d4c6802cca239bd5e27ea8ea7fab`  
		Last Modified: Mon, 09 Jun 2025 22:18:02 GMT  
		Size: 16.4 KB (16393 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:galactic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:885ea35a786ad8da5e0b08b90a6f53e2c16f9a80efc98b1ed20ebfe03f20c3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137765884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02efb2bb05c593a26f2bc99066834cd024a1cee8d76363e5e2819173f907954`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=galactic
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 07 Jun 2025 08:00:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9c0dbae44ad3c2a486914616608617ea5ae7615405075d860ca9d037658472`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dabd21457018d5fffe84a3291535b717890deff8c93a12e7cf4a69e1f23614c`  
		Last Modified: Mon, 09 Jun 2025 21:23:15 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc9cc0fca6354a9e10d48dc43c584ba2f2bfe621df6f2466584a2a5bc12ce5`  
		Last Modified: Mon, 09 Jun 2025 21:23:22 GMT  
		Size: 100.7 MB (100749299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908c356d108f7fc63c325ef52dfc5ceb7c197b2ad917d5c4e64c4d0ce9992940`  
		Last Modified: Mon, 09 Jun 2025 21:23:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:1b8ff4f1c4d1a398f009fcc9e62f2828af9312e7262ff309ea5e85a4df27bd1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17526365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa252d53c24c1b75b58763b52888a8995267f98cf7edfbaa5a981cc70a562dc1`

```dockerfile
```

-	Layers:
	-	`sha256:b1378a615dd898c97194716bf04077290c94cdf87e57caf705d7d03bba6fc6e8`  
		Last Modified: Mon, 09 Jun 2025 22:18:15 GMT  
		Size: 17.5 MB (17509838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8584669a13ff3781bbf6ad0f824ce8a47bc69402095019e601e69a12f347c89d`  
		Last Modified: Mon, 09 Jun 2025 22:18:16 GMT  
		Size: 16.5 KB (16527 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:galactic-ros-core-focal`

```console
$ docker pull ros@sha256:a3717e650d2c1ebdc85166a3f64b49c2cf8338679babff36cae622c93c8a0d81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:galactic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:f433ebe87c80db8d001b366688da325536a5603c1be2a766ef4284096bf1d78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143823215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c549bf02d5f5c532d835fb1b85a744a23e7c9521a9e773e2c84dcee30463e9e5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=galactic
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 07 Jun 2025 08:00:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11052161241e41a57b1cbb6ef459473de4ccf5cc8cb12c67052f79b515002f0a`  
		Last Modified: Mon, 09 Jun 2025 21:16:47 GMT  
		Size: 1.2 MB (1194828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931cee7ca53b99f574090e76c6443814931e6dc63cd60275d83c8a8618882c45`  
		Last Modified: Mon, 09 Jun 2025 21:16:47 GMT  
		Size: 10.0 MB (9982545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff0cd693b0e9a7b595721f2c18fc344735cff6dd852a68e4566e97c4abe888c`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 4.0 KB (4043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff68de3e6e4d94da44fd46aaac8d51e075d6b4d2e63547ee4661ccc80f1b6538`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64f09c9c0a539389b70e14ae98f3b1b07c00c6cc24224d7f35361e11faccfe`  
		Last Modified: Mon, 09 Jun 2025 21:16:52 GMT  
		Size: 105.1 MB (105130927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cae04d994b8a94412416c264258dcac3f5b4d7632662ba09ae69b75c995d411`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:ec5efeb461ee54afd417411274bbb1c6d2cbea7bc9c320292ede300b4a7f239e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17533939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42a6fa891c8a5d787a6d7e3a1036b59a5ab0424990380fcbac5a30381e76373`

```dockerfile
```

-	Layers:
	-	`sha256:43e8dbd1f7ca4668035f3b1a23afc26c35fd078140a0059545b779198d0362de`  
		Last Modified: Mon, 09 Jun 2025 22:18:01 GMT  
		Size: 17.5 MB (17517546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64b651d5f72059331b9033f24be143c321b1d4c6802cca239bd5e27ea8ea7fab`  
		Last Modified: Mon, 09 Jun 2025 22:18:02 GMT  
		Size: 16.4 KB (16393 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:galactic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:885ea35a786ad8da5e0b08b90a6f53e2c16f9a80efc98b1ed20ebfe03f20c3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137765884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02efb2bb05c593a26f2bc99066834cd024a1cee8d76363e5e2819173f907954`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=galactic
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 07 Jun 2025 08:00:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9c0dbae44ad3c2a486914616608617ea5ae7615405075d860ca9d037658472`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dabd21457018d5fffe84a3291535b717890deff8c93a12e7cf4a69e1f23614c`  
		Last Modified: Mon, 09 Jun 2025 21:23:15 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc9cc0fca6354a9e10d48dc43c584ba2f2bfe621df6f2466584a2a5bc12ce5`  
		Last Modified: Mon, 09 Jun 2025 21:23:22 GMT  
		Size: 100.7 MB (100749299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908c356d108f7fc63c325ef52dfc5ceb7c197b2ad917d5c4e64c4d0ce9992940`  
		Last Modified: Mon, 09 Jun 2025 21:23:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:1b8ff4f1c4d1a398f009fcc9e62f2828af9312e7262ff309ea5e85a4df27bd1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17526365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa252d53c24c1b75b58763b52888a8995267f98cf7edfbaa5a981cc70a562dc1`

```dockerfile
```

-	Layers:
	-	`sha256:b1378a615dd898c97194716bf04077290c94cdf87e57caf705d7d03bba6fc6e8`  
		Last Modified: Mon, 09 Jun 2025 22:18:15 GMT  
		Size: 17.5 MB (17509838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8584669a13ff3781bbf6ad0f824ce8a47bc69402095019e601e69a12f347c89d`  
		Last Modified: Mon, 09 Jun 2025 22:18:16 GMT  
		Size: 16.5 KB (16527 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:galactic-ros1-bridge`

```console
$ docker pull ros@sha256:12819852beb1dc8a77c7b97acc359121bd3dd392b0c28228b63ae23eef58ebbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:galactic-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:ecca8a5fd119a1f0a64f72d211c87797dbf463a3066d272e2761d1fb4a4a4853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.7 MB (524740442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb1fe4ae95e6b8ea4caa2f02f0a5940d623846a7db98d27f3bee14d55a4f020`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 May 2021 09:27:44 GMT
ARG RELEASE
# Tue, 25 May 2021 09:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 May 2021 09:27:44 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 25 May 2021 09:27:44 GMT
CMD ["/bin/bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENV LANG=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 May 2021 09:27:44 GMT
CMD ["bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS1_DISTRO=noetic
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS2_DISTRO=galactic
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.17.4-1*     ros-noetic-roscpp-tutorials=0.10.3-1*     ros-noetic-rospy-tutorials=0.10.3-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.4-1*     ros-galactic-demo-nodes-py=0.14.4-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11052161241e41a57b1cbb6ef459473de4ccf5cc8cb12c67052f79b515002f0a`  
		Last Modified: Mon, 09 Jun 2025 21:16:47 GMT  
		Size: 1.2 MB (1194828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931cee7ca53b99f574090e76c6443814931e6dc63cd60275d83c8a8618882c45`  
		Last Modified: Mon, 09 Jun 2025 21:16:47 GMT  
		Size: 10.0 MB (9982545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff0cd693b0e9a7b595721f2c18fc344735cff6dd852a68e4566e97c4abe888c`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 4.0 KB (4043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff68de3e6e4d94da44fd46aaac8d51e075d6b4d2e63547ee4661ccc80f1b6538`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64f09c9c0a539389b70e14ae98f3b1b07c00c6cc24224d7f35361e11faccfe`  
		Last Modified: Mon, 09 Jun 2025 21:16:52 GMT  
		Size: 105.1 MB (105130927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cae04d994b8a94412416c264258dcac3f5b4d7632662ba09ae69b75c995d411`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253e2d090968ae89743bbc0954bbaff92e4d1cf5edb29f37fb2280091749d623`  
		Last Modified: Mon, 09 Jun 2025 21:39:31 GMT  
		Size: 73.3 MB (73268914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc26cf621e6a72aaa5d3eb0f5a09aee8538a839398139f320377d2a72f53c5d`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 308.6 KB (308610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf544bbac493b95c4a165fc116cd06e7f0b5a0d5f4d33c5badb04d06c596dbf`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d465cf5a0978d969e83313b858f2bf01cb90f173f91ad5a034d3de674974931`  
		Last Modified: Mon, 09 Jun 2025 21:39:28 GMT  
		Size: 22.1 MB (22138329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b954ef683d62fc2852ffb3b371c3a5309c6c4eceb36f18fc83970e3ee0dd260e`  
		Last Modified: Mon, 09 Jun 2025 21:46:05 GMT  
		Size: 4.0 KB (4044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed0b7dba42feec029c3b9857de60d1cae93757e4a625b55c9209b67245fd602`  
		Last Modified: Mon, 09 Jun 2025 21:46:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5452b5c26559d932e2261ae0c995ca3dfff21bf6b2d3bc658b0e48f06dfd84`  
		Last Modified: Tue, 10 Jun 2025 05:27:52 GMT  
		Size: 268.9 MB (268866483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a63ec30fab27e3e0e2cb88adfcf44b2217c9b701d6dc71bdaead55823c3be3d`  
		Last Modified: Mon, 09 Jun 2025 21:46:06 GMT  
		Size: 16.3 MB (16327804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a309ba382fb3dfbf713287041481766354e04b25ca4130fd3245f7f3b49ee5b`  
		Last Modified: Mon, 09 Jun 2025 21:46:05 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros1-bridge` - unknown; unknown

```console
$ docker pull ros@sha256:3327e7e1f8e07589ce6bbc2c36ac122e0caf05301cc5d9dab5cc54f0315446ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42214401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e119bc78c96b691212dc4ae01dfd355ab9267962ad5fb817be375764ef2c4a`

```dockerfile
```

-	Layers:
	-	`sha256:f62b0bf5b9d055031e1730803d37329f3f4e0d34cbb9863e659b79b91c910764`  
		Last Modified: Mon, 09 Jun 2025 22:18:14 GMT  
		Size: 42.2 MB (42186408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26dccc8caab279b52f11d6667419651f69b0e8e60e18d8022844d116891c8361`  
		Last Modified: Mon, 09 Jun 2025 22:18:15 GMT  
		Size: 28.0 KB (27993 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:galactic-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:34eabc2c6e2c8426a5ee96cd3ed5ad12c3a811276089e013384fdcb09337ce24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **509.1 MB (509116232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef4607a6ff1348f28869194675d40447af6ada82df0dbafb155e5c2fd63163b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 May 2021 09:27:44 GMT
ARG RELEASE
# Tue, 25 May 2021 09:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 May 2021 09:27:44 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 25 May 2021 09:27:44 GMT
CMD ["/bin/bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENV LANG=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 May 2021 09:27:44 GMT
CMD ["bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS1_DISTRO=noetic
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS2_DISTRO=galactic
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.17.4-1*     ros-noetic-roscpp-tutorials=0.10.3-1*     ros-noetic-rospy-tutorials=0.10.3-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.4-1*     ros-galactic-demo-nodes-py=0.14.4-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9c0dbae44ad3c2a486914616608617ea5ae7615405075d860ca9d037658472`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dabd21457018d5fffe84a3291535b717890deff8c93a12e7cf4a69e1f23614c`  
		Last Modified: Mon, 09 Jun 2025 21:23:15 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc9cc0fca6354a9e10d48dc43c584ba2f2bfe621df6f2466584a2a5bc12ce5`  
		Last Modified: Mon, 09 Jun 2025 21:23:22 GMT  
		Size: 100.7 MB (100749299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908c356d108f7fc63c325ef52dfc5ceb7c197b2ad917d5c4e64c4d0ce9992940`  
		Last Modified: Mon, 09 Jun 2025 21:23:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5acbcd197ca2dd8f85a827ba1ed6820e86c136f1ab4985faaf3bf8cbfa5a739`  
		Last Modified: Mon, 09 Jun 2025 21:42:36 GMT  
		Size: 67.6 MB (67617373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208649ea3be9f05fa2e17c11294e68dc52f05a0923235b10ca3df0213eec0efa`  
		Last Modified: Mon, 09 Jun 2025 21:42:32 GMT  
		Size: 308.6 KB (308607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d142d51b07449e8ce86f0d2de6671d5b67a4d18fc5fc90600f4e3e432b3ae4`  
		Last Modified: Mon, 09 Jun 2025 21:42:32 GMT  
		Size: 2.5 KB (2468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90e400c2e79021db0693711a8489954b121a4d0785902a1f433ed75e65ffefa`  
		Last Modified: Mon, 09 Jun 2025 21:42:35 GMT  
		Size: 21.5 MB (21481027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fba43c0e277a98c13c0ecea35c9eedaa63f8a2f263e674cdf2a6d22f24e506`  
		Last Modified: Mon, 09 Jun 2025 21:55:25 GMT  
		Size: 4.0 KB (4049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727a7e0e2dfb57d918aa4bfedaf0abc94868d9b34bc669b577cf2f0ff6cd7f98`  
		Last Modified: Mon, 09 Jun 2025 21:55:25 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01256842ea5c742a75d0e3e54d342c3864a54dd084f70815aef4e91c423da4c`  
		Last Modified: Mon, 09 Jun 2025 21:55:18 GMT  
		Size: 266.1 MB (266089651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc8f12c340362f1e3bf27d871896d0b2b603ddf1365a5c2fa4df695e1ac6c7d`  
		Last Modified: Mon, 09 Jun 2025 21:55:26 GMT  
		Size: 15.8 MB (15846612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7180df42ee70eb2a1d4aaa73a06cc909ee5be98932ba27865712ff396f5991f`  
		Last Modified: Mon, 09 Jun 2025 21:55:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros1-bridge` - unknown; unknown

```console
$ docker pull ros@sha256:ce3a5df97bd35ed5e3c71064e07f0e65fbb601e03f13d6d8082b47e8838eab75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42109690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71f45fd34ed072a79d0e1f99957aba4b5cf133204971195936510556af7020a`

```dockerfile
```

-	Layers:
	-	`sha256:127524945f7611120269313c5bd8ff9092024b269137dad0533ab9d9f6ca9773`  
		Last Modified: Mon, 09 Jun 2025 22:18:57 GMT  
		Size: 42.1 MB (42081557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c14df5383ee125710147bc37871b35a2aef6dcb54368898d466bfa52561e709f`  
		Last Modified: Mon, 09 Jun 2025 22:18:58 GMT  
		Size: 28.1 KB (28133 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:galactic-ros1-bridge-focal`

```console
$ docker pull ros@sha256:12819852beb1dc8a77c7b97acc359121bd3dd392b0c28228b63ae23eef58ebbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:galactic-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:ecca8a5fd119a1f0a64f72d211c87797dbf463a3066d272e2761d1fb4a4a4853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.7 MB (524740442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb1fe4ae95e6b8ea4caa2f02f0a5940d623846a7db98d27f3bee14d55a4f020`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 May 2021 09:27:44 GMT
ARG RELEASE
# Tue, 25 May 2021 09:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 May 2021 09:27:44 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 25 May 2021 09:27:44 GMT
CMD ["/bin/bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENV LANG=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 May 2021 09:27:44 GMT
CMD ["bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS1_DISTRO=noetic
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS2_DISTRO=galactic
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.17.4-1*     ros-noetic-roscpp-tutorials=0.10.3-1*     ros-noetic-rospy-tutorials=0.10.3-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.4-1*     ros-galactic-demo-nodes-py=0.14.4-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11052161241e41a57b1cbb6ef459473de4ccf5cc8cb12c67052f79b515002f0a`  
		Last Modified: Mon, 09 Jun 2025 21:16:47 GMT  
		Size: 1.2 MB (1194828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931cee7ca53b99f574090e76c6443814931e6dc63cd60275d83c8a8618882c45`  
		Last Modified: Mon, 09 Jun 2025 21:16:47 GMT  
		Size: 10.0 MB (9982545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff0cd693b0e9a7b595721f2c18fc344735cff6dd852a68e4566e97c4abe888c`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 4.0 KB (4043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff68de3e6e4d94da44fd46aaac8d51e075d6b4d2e63547ee4661ccc80f1b6538`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64f09c9c0a539389b70e14ae98f3b1b07c00c6cc24224d7f35361e11faccfe`  
		Last Modified: Mon, 09 Jun 2025 21:16:52 GMT  
		Size: 105.1 MB (105130927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cae04d994b8a94412416c264258dcac3f5b4d7632662ba09ae69b75c995d411`  
		Last Modified: Mon, 09 Jun 2025 21:16:46 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253e2d090968ae89743bbc0954bbaff92e4d1cf5edb29f37fb2280091749d623`  
		Last Modified: Mon, 09 Jun 2025 21:39:31 GMT  
		Size: 73.3 MB (73268914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc26cf621e6a72aaa5d3eb0f5a09aee8538a839398139f320377d2a72f53c5d`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 308.6 KB (308610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf544bbac493b95c4a165fc116cd06e7f0b5a0d5f4d33c5badb04d06c596dbf`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d465cf5a0978d969e83313b858f2bf01cb90f173f91ad5a034d3de674974931`  
		Last Modified: Mon, 09 Jun 2025 21:39:28 GMT  
		Size: 22.1 MB (22138329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b954ef683d62fc2852ffb3b371c3a5309c6c4eceb36f18fc83970e3ee0dd260e`  
		Last Modified: Mon, 09 Jun 2025 21:46:05 GMT  
		Size: 4.0 KB (4044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed0b7dba42feec029c3b9857de60d1cae93757e4a625b55c9209b67245fd602`  
		Last Modified: Mon, 09 Jun 2025 21:46:05 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5452b5c26559d932e2261ae0c995ca3dfff21bf6b2d3bc658b0e48f06dfd84`  
		Last Modified: Tue, 10 Jun 2025 05:27:52 GMT  
		Size: 268.9 MB (268866483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a63ec30fab27e3e0e2cb88adfcf44b2217c9b701d6dc71bdaead55823c3be3d`  
		Last Modified: Mon, 09 Jun 2025 21:46:06 GMT  
		Size: 16.3 MB (16327804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a309ba382fb3dfbf713287041481766354e04b25ca4130fd3245f7f3b49ee5b`  
		Last Modified: Mon, 09 Jun 2025 21:46:05 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros1-bridge-focal` - unknown; unknown

```console
$ docker pull ros@sha256:3327e7e1f8e07589ce6bbc2c36ac122e0caf05301cc5d9dab5cc54f0315446ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42214401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e119bc78c96b691212dc4ae01dfd355ab9267962ad5fb817be375764ef2c4a`

```dockerfile
```

-	Layers:
	-	`sha256:f62b0bf5b9d055031e1730803d37329f3f4e0d34cbb9863e659b79b91c910764`  
		Last Modified: Mon, 09 Jun 2025 22:18:14 GMT  
		Size: 42.2 MB (42186408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26dccc8caab279b52f11d6667419651f69b0e8e60e18d8022844d116891c8361`  
		Last Modified: Mon, 09 Jun 2025 22:18:15 GMT  
		Size: 28.0 KB (27993 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:galactic-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:34eabc2c6e2c8426a5ee96cd3ed5ad12c3a811276089e013384fdcb09337ce24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **509.1 MB (509116232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef4607a6ff1348f28869194675d40447af6ada82df0dbafb155e5c2fd63163b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 May 2021 09:27:44 GMT
ARG RELEASE
# Tue, 25 May 2021 09:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 May 2021 09:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 25 May 2021 09:27:44 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 25 May 2021 09:27:44 GMT
CMD ["/bin/bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENV LANG=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 May 2021 09:27:44 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 25 May 2021 09:27:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 May 2021 09:27:44 GMT
CMD ["bash"]
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS1_DISTRO=noetic
# Sat, 07 Jun 2025 08:04:40 GMT
ENV ROS2_DISTRO=galactic
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.17.4-1*     ros-noetic-roscpp-tutorials=0.10.3-1*     ros-noetic-rospy-tutorials=0.10.3-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.4-1*     ros-galactic-demo-nodes-py=0.14.4-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:04:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9c0dbae44ad3c2a486914616608617ea5ae7615405075d860ca9d037658472`  
		Last Modified: Mon, 09 Jun 2025 21:21:57 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dabd21457018d5fffe84a3291535b717890deff8c93a12e7cf4a69e1f23614c`  
		Last Modified: Mon, 09 Jun 2025 21:23:15 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc9cc0fca6354a9e10d48dc43c584ba2f2bfe621df6f2466584a2a5bc12ce5`  
		Last Modified: Mon, 09 Jun 2025 21:23:22 GMT  
		Size: 100.7 MB (100749299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908c356d108f7fc63c325ef52dfc5ceb7c197b2ad917d5c4e64c4d0ce9992940`  
		Last Modified: Mon, 09 Jun 2025 21:23:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5acbcd197ca2dd8f85a827ba1ed6820e86c136f1ab4985faaf3bf8cbfa5a739`  
		Last Modified: Mon, 09 Jun 2025 21:42:36 GMT  
		Size: 67.6 MB (67617373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208649ea3be9f05fa2e17c11294e68dc52f05a0923235b10ca3df0213eec0efa`  
		Last Modified: Mon, 09 Jun 2025 21:42:32 GMT  
		Size: 308.6 KB (308607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d142d51b07449e8ce86f0d2de6671d5b67a4d18fc5fc90600f4e3e432b3ae4`  
		Last Modified: Mon, 09 Jun 2025 21:42:32 GMT  
		Size: 2.5 KB (2468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90e400c2e79021db0693711a8489954b121a4d0785902a1f433ed75e65ffefa`  
		Last Modified: Mon, 09 Jun 2025 21:42:35 GMT  
		Size: 21.5 MB (21481027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fba43c0e277a98c13c0ecea35c9eedaa63f8a2f263e674cdf2a6d22f24e506`  
		Last Modified: Mon, 09 Jun 2025 21:55:25 GMT  
		Size: 4.0 KB (4049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727a7e0e2dfb57d918aa4bfedaf0abc94868d9b34bc669b577cf2f0ff6cd7f98`  
		Last Modified: Mon, 09 Jun 2025 21:55:25 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01256842ea5c742a75d0e3e54d342c3864a54dd084f70815aef4e91c423da4c`  
		Last Modified: Mon, 09 Jun 2025 21:55:18 GMT  
		Size: 266.1 MB (266089651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc8f12c340362f1e3bf27d871896d0b2b603ddf1365a5c2fa4df695e1ac6c7d`  
		Last Modified: Mon, 09 Jun 2025 21:55:26 GMT  
		Size: 15.8 MB (15846612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7180df42ee70eb2a1d4aaa73a06cc909ee5be98932ba27865712ff396f5991f`  
		Last Modified: Mon, 09 Jun 2025 21:55:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros1-bridge-focal` - unknown; unknown

```console
$ docker pull ros@sha256:ce3a5df97bd35ed5e3c71064e07f0e65fbb601e03f13d6d8082b47e8838eab75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42109690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71f45fd34ed072a79d0e1f99957aba4b5cf133204971195936510556af7020a`

```dockerfile
```

-	Layers:
	-	`sha256:127524945f7611120269313c5bd8ff9092024b269137dad0533ab9d9f6ca9773`  
		Last Modified: Mon, 09 Jun 2025 22:18:57 GMT  
		Size: 42.1 MB (42081557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c14df5383ee125710147bc37871b35a2aef6dcb54368898d466bfa52561e709f`  
		Last Modified: Mon, 09 Jun 2025 22:18:58 GMT  
		Size: 28.1 KB (28133 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble`

```console
$ docker pull ros@sha256:d66b8a36f8c6cad03526188c8dcd2cb17096aff73a1af628990ab118794479ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:6ae2d4d3bf17eb8b13eff00824be6abf90f337eba12ebbe319f984c1d9f26792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (262981180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168e1f658ab579833f7ff97e00c52f1637240d742daae16ce3246bf6dfd2f209`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25b611258b9e589c289c2fb50570b97c455ad6e5e6e9de251b753fab9c5618c`  
		Last Modified: Tue, 03 Jun 2025 17:07:39 GMT  
		Size: 1.2 MB (1214039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdf6d82836139f37c4872db40ac59c01b82bfce2b74e5ba795b14ee21f7bc4e`  
		Last Modified: Tue, 03 Jun 2025 17:07:38 GMT  
		Size: 6.0 MB (5991843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8ee3eb0604e23957531406bba2fdaa67f77da515ebbafa7e8f318d462c40be`  
		Last Modified: Tue, 03 Jun 2025 17:07:37 GMT  
		Size: 97.2 KB (97179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67910d3d301a88382773a066be8c81a350d18c243ade54d61ec50923c5e7583`  
		Last Modified: Tue, 03 Jun 2025 17:07:47 GMT  
		Size: 104.5 MB (104532630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d1c867fd17fe66471be29077931fd8ec1699a13818eb93034e99868ecd7bd3`  
		Last Modified: Tue, 03 Jun 2025 17:07:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c35195e7507c24005520a8c45874a499a1bf080555373c57a5d59b1a2df30b6`  
		Last Modified: Tue, 03 Jun 2025 17:09:44 GMT  
		Size: 98.0 MB (97954050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c64fea9ecf8685a15c2e72575fde6075df9337d0daff01a2707185e92209ef`  
		Last Modified: Tue, 03 Jun 2025 17:09:31 GMT  
		Size: 362.1 KB (362150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba527436b8c305a48ac0cc16f3a7e43f9ea5f827c368c8b90c0fffeed8273e03`  
		Last Modified: Tue, 03 Jun 2025 17:09:32 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5237a367af95b4bc5cef912321b337fe2e5d66f06a23ad973680596da45b35`  
		Last Modified: Tue, 03 Jun 2025 17:09:34 GMT  
		Size: 23.3 MB (23293629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:3f9a1f71a07eeee1d89c2ad93a5a3d2ac24ae2e416db0045d901b25dc26b98f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23029026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bcd344793f2c51eb8da1c190bf0ed7340dd88a97cf388d91a9ab5cfb3641ed`

```dockerfile
```

-	Layers:
	-	`sha256:dec6754de12c5c273127119636a801198a3de05c2e6aa7911fda9b935583a54b`  
		Last Modified: Tue, 03 Jun 2025 19:17:27 GMT  
		Size: 23.0 MB (23012635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51171abc4c4a0cde6313f059dc67861e4ac2e78c764b0af0a0857e4d5b1bd3fc`  
		Last Modified: Tue, 03 Jun 2025 19:17:28 GMT  
		Size: 16.4 KB (16391 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:19292be2584cd845db9b5542b76546a7e5da661bcac15f1804d2c1cbb68467d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255409086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6a8d0d8d582d4cfdd0c7b9e2b03f3befcc80db56d8e63074ecb9105ec73b8a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee5308cdd15f77e44b92e47b6f1d16733b65fab16dcd7978a623f62dd7f8bb6`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 1.2 MB (1214200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73381c2c31e36b7d9ed2c02345b213f909f409fb89bafae890235d56bc9e732a`  
		Last Modified: Tue, 03 Jun 2025 16:19:13 GMT  
		Size: 5.9 MB (5936692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5d02a65bd7f7a1fc39a15acf77d63c54244aaaf22429febec588ea14ffccb2`  
		Last Modified: Tue, 03 Jun 2025 16:19:11 GMT  
		Size: 97.2 KB (97234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe74201331921b71dbaff57f282e63b8c2a23276f1e7169c2bda36a5df74e77a`  
		Last Modified: Tue, 03 Jun 2025 16:19:27 GMT  
		Size: 102.3 MB (102252252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced1014ed7cbc1c9aa8f3a96a4bb6e1deaaf93f58041c5d88da2356ee7b4266f`  
		Last Modified: Tue, 03 Jun 2025 16:18:55 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f371b330eabe98b4c2f7a23612c6b1e42a4956672754821ddf5872050a558eb4`  
		Last Modified: Tue, 03 Jun 2025 17:09:53 GMT  
		Size: 95.5 MB (95506704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42eaf8eb4130d56998aaeb0e2ba32f8c3a358eae317fcc40d60886b6021008de`  
		Last Modified: Tue, 03 Jun 2025 17:09:37 GMT  
		Size: 362.2 KB (362154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014dcb0d353b6d71d8ee54ea5ea2da373e2d203f95d5aa144a904474030c8f6e`  
		Last Modified: Tue, 03 Jun 2025 17:09:37 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa21615c56eef2e3c96f602ed9e098526eebb513ac0e2d5ba41b462cea49278`  
		Last Modified: Tue, 03 Jun 2025 17:09:41 GMT  
		Size: 22.7 MB (22681600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble` - unknown; unknown

```console
$ docker pull ros@sha256:ec37020439d18152fd259a5d6f242dc62d3856e1ccecc11f77aabd1ff5c5c0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23042179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f0cd94ca0f26a5bd27e47c2292056ae159e15f778b2d7e6ecb6d7ec7ca8414`

```dockerfile
```

-	Layers:
	-	`sha256:3fd7739ab610e44cd8a172462b5d39eb9be018c2619daa3c23e80de27f82e039`  
		Last Modified: Tue, 03 Jun 2025 19:17:45 GMT  
		Size: 23.0 MB (23025651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6aff5c76f0803b84b6c1353d30ff26b3426ace202704137c99555c427643e9e`  
		Last Modified: Tue, 03 Jun 2025 19:17:46 GMT  
		Size: 16.5 KB (16528 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception`

```console
$ docker pull ros@sha256:f0872bc83294fd5710d64488f967d42ffdacd8ba4f055070b1ad649fdddbbee1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:aad34eb5ac95fbc95852d30f35da21389160cb3e0ce5ae906de4e9ebabd27436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.9 MB (954881666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb3b4f1e5d9d8252c2920ad5a446aaf76a36955b220b5d641a60f9f7a5a688a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25b611258b9e589c289c2fb50570b97c455ad6e5e6e9de251b753fab9c5618c`  
		Last Modified: Tue, 03 Jun 2025 17:07:39 GMT  
		Size: 1.2 MB (1214039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdf6d82836139f37c4872db40ac59c01b82bfce2b74e5ba795b14ee21f7bc4e`  
		Last Modified: Tue, 03 Jun 2025 17:07:38 GMT  
		Size: 6.0 MB (5991843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8ee3eb0604e23957531406bba2fdaa67f77da515ebbafa7e8f318d462c40be`  
		Last Modified: Tue, 03 Jun 2025 17:07:37 GMT  
		Size: 97.2 KB (97179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67910d3d301a88382773a066be8c81a350d18c243ade54d61ec50923c5e7583`  
		Last Modified: Tue, 03 Jun 2025 17:07:47 GMT  
		Size: 104.5 MB (104532630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d1c867fd17fe66471be29077931fd8ec1699a13818eb93034e99868ecd7bd3`  
		Last Modified: Tue, 03 Jun 2025 17:07:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c35195e7507c24005520a8c45874a499a1bf080555373c57a5d59b1a2df30b6`  
		Last Modified: Tue, 03 Jun 2025 17:09:44 GMT  
		Size: 98.0 MB (97954050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c64fea9ecf8685a15c2e72575fde6075df9337d0daff01a2707185e92209ef`  
		Last Modified: Tue, 03 Jun 2025 17:09:31 GMT  
		Size: 362.1 KB (362150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba527436b8c305a48ac0cc16f3a7e43f9ea5f827c368c8b90c0fffeed8273e03`  
		Last Modified: Tue, 03 Jun 2025 17:09:32 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5237a367af95b4bc5cef912321b337fe2e5d66f06a23ad973680596da45b35`  
		Last Modified: Tue, 03 Jun 2025 17:09:34 GMT  
		Size: 23.3 MB (23293629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f67574391c6248d252beef7f3f3df9b52aa95d006539811d108744f05933bf5`  
		Last Modified: Tue, 03 Jun 2025 19:17:47 GMT  
		Size: 691.9 MB (691900486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:1aefeb33696d112cd9641bb574ac321625a8fe30bc78a2e863e9975b0e2f11b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57835186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b42aed5c01e3a0aeff1d67c25ea23d4378570cb2b6c058b5099e369b17ef71`

```dockerfile
```

-	Layers:
	-	`sha256:8cbde98693e47eb19cb39ee623c52eb0a20fe5af4b34367d0491fb1991f8ace9`  
		Last Modified: Tue, 03 Jun 2025 19:17:35 GMT  
		Size: 57.8 MB (57825791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e829e418ba86d42b3aa03beec0c81730b86086a283286556a9b335eddf656eed`  
		Last Modified: Tue, 03 Jun 2025 19:17:37 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:72d3d5732dd8247e52175e5a4f54a8cb8c82f192f9dcf96e6eec66fb57ae0057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.2 MB (915197125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3b7d9255f02d28916a1535996b7cac717bfc6021d8ee29ce80fef94336f63d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee5308cdd15f77e44b92e47b6f1d16733b65fab16dcd7978a623f62dd7f8bb6`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 1.2 MB (1214200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73381c2c31e36b7d9ed2c02345b213f909f409fb89bafae890235d56bc9e732a`  
		Last Modified: Tue, 03 Jun 2025 16:19:13 GMT  
		Size: 5.9 MB (5936692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5d02a65bd7f7a1fc39a15acf77d63c54244aaaf22429febec588ea14ffccb2`  
		Last Modified: Tue, 03 Jun 2025 16:19:11 GMT  
		Size: 97.2 KB (97234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe74201331921b71dbaff57f282e63b8c2a23276f1e7169c2bda36a5df74e77a`  
		Last Modified: Tue, 03 Jun 2025 16:19:27 GMT  
		Size: 102.3 MB (102252252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced1014ed7cbc1c9aa8f3a96a4bb6e1deaaf93f58041c5d88da2356ee7b4266f`  
		Last Modified: Tue, 03 Jun 2025 16:18:55 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f371b330eabe98b4c2f7a23612c6b1e42a4956672754821ddf5872050a558eb4`  
		Last Modified: Tue, 03 Jun 2025 17:09:53 GMT  
		Size: 95.5 MB (95506704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42eaf8eb4130d56998aaeb0e2ba32f8c3a358eae317fcc40d60886b6021008de`  
		Last Modified: Tue, 03 Jun 2025 17:09:37 GMT  
		Size: 362.2 KB (362154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014dcb0d353b6d71d8ee54ea5ea2da373e2d203f95d5aa144a904474030c8f6e`  
		Last Modified: Tue, 03 Jun 2025 17:09:37 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa21615c56eef2e3c96f602ed9e098526eebb513ac0e2d5ba41b462cea49278`  
		Last Modified: Tue, 03 Jun 2025 17:09:41 GMT  
		Size: 22.7 MB (22681600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dfa6906e2ea85de0e1680f6e3c427525e720a8b824f41b6940fba7aefb7fbc`  
		Last Modified: Tue, 03 Jun 2025 17:54:21 GMT  
		Size: 659.8 MB (659788039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception` - unknown; unknown

```console
$ docker pull ros@sha256:52bc806baf40be74602a3ec21f1ff98a3cdae0f006a8a8cd70ca1cd0a5aa5306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57830168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eaf56ee38fa3e8144790a313d51b47c88811c2027edf13eb713f05fd73c25be`

```dockerfile
```

-	Layers:
	-	`sha256:7c7d2a9307f4c8ec88bee684f58d7bd6df5d47b02b7f226c4d4dc21ca5b0c115`  
		Last Modified: Tue, 03 Jun 2025 19:19:18 GMT  
		Size: 57.8 MB (57820693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc6d3a2db78d00a8859dd4d555d6cb7c4735c41e9b3e6334ca0e9a105ad0e618`  
		Last Modified: Tue, 03 Jun 2025 19:19:19 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:f0872bc83294fd5710d64488f967d42ffdacd8ba4f055070b1ad649fdddbbee1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:aad34eb5ac95fbc95852d30f35da21389160cb3e0ce5ae906de4e9ebabd27436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.9 MB (954881666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb3b4f1e5d9d8252c2920ad5a446aaf76a36955b220b5d641a60f9f7a5a688a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25b611258b9e589c289c2fb50570b97c455ad6e5e6e9de251b753fab9c5618c`  
		Last Modified: Tue, 03 Jun 2025 17:07:39 GMT  
		Size: 1.2 MB (1214039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdf6d82836139f37c4872db40ac59c01b82bfce2b74e5ba795b14ee21f7bc4e`  
		Last Modified: Tue, 03 Jun 2025 17:07:38 GMT  
		Size: 6.0 MB (5991843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8ee3eb0604e23957531406bba2fdaa67f77da515ebbafa7e8f318d462c40be`  
		Last Modified: Tue, 03 Jun 2025 17:07:37 GMT  
		Size: 97.2 KB (97179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67910d3d301a88382773a066be8c81a350d18c243ade54d61ec50923c5e7583`  
		Last Modified: Tue, 03 Jun 2025 17:07:47 GMT  
		Size: 104.5 MB (104532630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d1c867fd17fe66471be29077931fd8ec1699a13818eb93034e99868ecd7bd3`  
		Last Modified: Tue, 03 Jun 2025 17:07:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c35195e7507c24005520a8c45874a499a1bf080555373c57a5d59b1a2df30b6`  
		Last Modified: Tue, 03 Jun 2025 17:09:44 GMT  
		Size: 98.0 MB (97954050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c64fea9ecf8685a15c2e72575fde6075df9337d0daff01a2707185e92209ef`  
		Last Modified: Tue, 03 Jun 2025 17:09:31 GMT  
		Size: 362.1 KB (362150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba527436b8c305a48ac0cc16f3a7e43f9ea5f827c368c8b90c0fffeed8273e03`  
		Last Modified: Tue, 03 Jun 2025 17:09:32 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5237a367af95b4bc5cef912321b337fe2e5d66f06a23ad973680596da45b35`  
		Last Modified: Tue, 03 Jun 2025 17:09:34 GMT  
		Size: 23.3 MB (23293629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f67574391c6248d252beef7f3f3df9b52aa95d006539811d108744f05933bf5`  
		Last Modified: Tue, 03 Jun 2025 19:17:47 GMT  
		Size: 691.9 MB (691900486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:1aefeb33696d112cd9641bb574ac321625a8fe30bc78a2e863e9975b0e2f11b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57835186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b42aed5c01e3a0aeff1d67c25ea23d4378570cb2b6c058b5099e369b17ef71`

```dockerfile
```

-	Layers:
	-	`sha256:8cbde98693e47eb19cb39ee623c52eb0a20fe5af4b34367d0491fb1991f8ace9`  
		Last Modified: Tue, 03 Jun 2025 19:17:35 GMT  
		Size: 57.8 MB (57825791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e829e418ba86d42b3aa03beec0c81730b86086a283286556a9b335eddf656eed`  
		Last Modified: Tue, 03 Jun 2025 19:17:37 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:72d3d5732dd8247e52175e5a4f54a8cb8c82f192f9dcf96e6eec66fb57ae0057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.2 MB (915197125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3b7d9255f02d28916a1535996b7cac717bfc6021d8ee29ce80fef94336f63d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 May 2022 18:52:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee5308cdd15f77e44b92e47b6f1d16733b65fab16dcd7978a623f62dd7f8bb6`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 1.2 MB (1214200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73381c2c31e36b7d9ed2c02345b213f909f409fb89bafae890235d56bc9e732a`  
		Last Modified: Tue, 03 Jun 2025 16:19:13 GMT  
		Size: 5.9 MB (5936692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5d02a65bd7f7a1fc39a15acf77d63c54244aaaf22429febec588ea14ffccb2`  
		Last Modified: Tue, 03 Jun 2025 16:19:11 GMT  
		Size: 97.2 KB (97234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe74201331921b71dbaff57f282e63b8c2a23276f1e7169c2bda36a5df74e77a`  
		Last Modified: Tue, 03 Jun 2025 16:19:27 GMT  
		Size: 102.3 MB (102252252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced1014ed7cbc1c9aa8f3a96a4bb6e1deaaf93f58041c5d88da2356ee7b4266f`  
		Last Modified: Tue, 03 Jun 2025 16:18:55 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f371b330eabe98b4c2f7a23612c6b1e42a4956672754821ddf5872050a558eb4`  
		Last Modified: Tue, 03 Jun 2025 17:09:53 GMT  
		Size: 95.5 MB (95506704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42eaf8eb4130d56998aaeb0e2ba32f8c3a358eae317fcc40d60886b6021008de`  
		Last Modified: Tue, 03 Jun 2025 17:09:37 GMT  
		Size: 362.2 KB (362154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014dcb0d353b6d71d8ee54ea5ea2da373e2d203f95d5aa144a904474030c8f6e`  
		Last Modified: Tue, 03 Jun 2025 17:09:37 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa21615c56eef2e3c96f602ed9e098526eebb513ac0e2d5ba41b462cea49278`  
		Last Modified: Tue, 03 Jun 2025 17:09:41 GMT  
		Size: 22.7 MB (22681600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dfa6906e2ea85de0e1680f6e3c427525e720a8b824f41b6940fba7aefb7fbc`  
		Last Modified: Tue, 03 Jun 2025 17:54:21 GMT  
		Size: 659.8 MB (659788039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-perception-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:52bc806baf40be74602a3ec21f1ff98a3cdae0f006a8a8cd70ca1cd0a5aa5306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57830168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eaf56ee38fa3e8144790a313d51b47c88811c2027edf13eb713f05fd73c25be`

```dockerfile
```

-	Layers:
	-	`sha256:7c7d2a9307f4c8ec88bee684f58d7bd6df5d47b02b7f226c4d4dc21ca5b0c115`  
		Last Modified: Tue, 03 Jun 2025 19:19:18 GMT  
		Size: 57.8 MB (57820693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc6d3a2db78d00a8859dd4d555d6cb7c4735c41e9b3e6334ca0e9a105ad0e618`  
		Last Modified: Tue, 03 Jun 2025 19:19:19 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:d66b8a36f8c6cad03526188c8dcd2cb17096aff73a1af628990ab118794479ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:6ae2d4d3bf17eb8b13eff00824be6abf90f337eba12ebbe319f984c1d9f26792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (262981180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168e1f658ab579833f7ff97e00c52f1637240d742daae16ce3246bf6dfd2f209`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25b611258b9e589c289c2fb50570b97c455ad6e5e6e9de251b753fab9c5618c`  
		Last Modified: Tue, 03 Jun 2025 17:07:39 GMT  
		Size: 1.2 MB (1214039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdf6d82836139f37c4872db40ac59c01b82bfce2b74e5ba795b14ee21f7bc4e`  
		Last Modified: Tue, 03 Jun 2025 17:07:38 GMT  
		Size: 6.0 MB (5991843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8ee3eb0604e23957531406bba2fdaa67f77da515ebbafa7e8f318d462c40be`  
		Last Modified: Tue, 03 Jun 2025 17:07:37 GMT  
		Size: 97.2 KB (97179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67910d3d301a88382773a066be8c81a350d18c243ade54d61ec50923c5e7583`  
		Last Modified: Tue, 03 Jun 2025 17:07:47 GMT  
		Size: 104.5 MB (104532630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d1c867fd17fe66471be29077931fd8ec1699a13818eb93034e99868ecd7bd3`  
		Last Modified: Tue, 03 Jun 2025 17:07:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c35195e7507c24005520a8c45874a499a1bf080555373c57a5d59b1a2df30b6`  
		Last Modified: Tue, 03 Jun 2025 17:09:44 GMT  
		Size: 98.0 MB (97954050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c64fea9ecf8685a15c2e72575fde6075df9337d0daff01a2707185e92209ef`  
		Last Modified: Tue, 03 Jun 2025 17:09:31 GMT  
		Size: 362.1 KB (362150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba527436b8c305a48ac0cc16f3a7e43f9ea5f827c368c8b90c0fffeed8273e03`  
		Last Modified: Tue, 03 Jun 2025 17:09:32 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5237a367af95b4bc5cef912321b337fe2e5d66f06a23ad973680596da45b35`  
		Last Modified: Tue, 03 Jun 2025 17:09:34 GMT  
		Size: 23.3 MB (23293629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:3f9a1f71a07eeee1d89c2ad93a5a3d2ac24ae2e416db0045d901b25dc26b98f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23029026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bcd344793f2c51eb8da1c190bf0ed7340dd88a97cf388d91a9ab5cfb3641ed`

```dockerfile
```

-	Layers:
	-	`sha256:dec6754de12c5c273127119636a801198a3de05c2e6aa7911fda9b935583a54b`  
		Last Modified: Tue, 03 Jun 2025 19:17:27 GMT  
		Size: 23.0 MB (23012635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51171abc4c4a0cde6313f059dc67861e4ac2e78c764b0af0a0857e4d5b1bd3fc`  
		Last Modified: Tue, 03 Jun 2025 19:17:28 GMT  
		Size: 16.4 KB (16391 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:19292be2584cd845db9b5542b76546a7e5da661bcac15f1804d2c1cbb68467d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255409086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6a8d0d8d582d4cfdd0c7b9e2b03f3befcc80db56d8e63074ecb9105ec73b8a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee5308cdd15f77e44b92e47b6f1d16733b65fab16dcd7978a623f62dd7f8bb6`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 1.2 MB (1214200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73381c2c31e36b7d9ed2c02345b213f909f409fb89bafae890235d56bc9e732a`  
		Last Modified: Tue, 03 Jun 2025 16:19:13 GMT  
		Size: 5.9 MB (5936692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5d02a65bd7f7a1fc39a15acf77d63c54244aaaf22429febec588ea14ffccb2`  
		Last Modified: Tue, 03 Jun 2025 16:19:11 GMT  
		Size: 97.2 KB (97234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe74201331921b71dbaff57f282e63b8c2a23276f1e7169c2bda36a5df74e77a`  
		Last Modified: Tue, 03 Jun 2025 16:19:27 GMT  
		Size: 102.3 MB (102252252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced1014ed7cbc1c9aa8f3a96a4bb6e1deaaf93f58041c5d88da2356ee7b4266f`  
		Last Modified: Tue, 03 Jun 2025 16:18:55 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f371b330eabe98b4c2f7a23612c6b1e42a4956672754821ddf5872050a558eb4`  
		Last Modified: Tue, 03 Jun 2025 17:09:53 GMT  
		Size: 95.5 MB (95506704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42eaf8eb4130d56998aaeb0e2ba32f8c3a358eae317fcc40d60886b6021008de`  
		Last Modified: Tue, 03 Jun 2025 17:09:37 GMT  
		Size: 362.2 KB (362154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014dcb0d353b6d71d8ee54ea5ea2da373e2d203f95d5aa144a904474030c8f6e`  
		Last Modified: Tue, 03 Jun 2025 17:09:37 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa21615c56eef2e3c96f602ed9e098526eebb513ac0e2d5ba41b462cea49278`  
		Last Modified: Tue, 03 Jun 2025 17:09:41 GMT  
		Size: 22.7 MB (22681600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:ec37020439d18152fd259a5d6f242dc62d3856e1ccecc11f77aabd1ff5c5c0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23042179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f0cd94ca0f26a5bd27e47c2292056ae159e15f778b2d7e6ecb6d7ec7ca8414`

```dockerfile
```

-	Layers:
	-	`sha256:3fd7739ab610e44cd8a172462b5d39eb9be018c2619daa3c23e80de27f82e039`  
		Last Modified: Tue, 03 Jun 2025 19:17:45 GMT  
		Size: 23.0 MB (23025651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6aff5c76f0803b84b6c1353d30ff26b3426ace202704137c99555c427643e9e`  
		Last Modified: Tue, 03 Jun 2025 19:17:46 GMT  
		Size: 16.5 KB (16528 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:d66b8a36f8c6cad03526188c8dcd2cb17096aff73a1af628990ab118794479ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:6ae2d4d3bf17eb8b13eff00824be6abf90f337eba12ebbe319f984c1d9f26792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (262981180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168e1f658ab579833f7ff97e00c52f1637240d742daae16ce3246bf6dfd2f209`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25b611258b9e589c289c2fb50570b97c455ad6e5e6e9de251b753fab9c5618c`  
		Last Modified: Tue, 03 Jun 2025 17:07:39 GMT  
		Size: 1.2 MB (1214039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdf6d82836139f37c4872db40ac59c01b82bfce2b74e5ba795b14ee21f7bc4e`  
		Last Modified: Tue, 03 Jun 2025 17:07:38 GMT  
		Size: 6.0 MB (5991843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8ee3eb0604e23957531406bba2fdaa67f77da515ebbafa7e8f318d462c40be`  
		Last Modified: Tue, 03 Jun 2025 17:07:37 GMT  
		Size: 97.2 KB (97179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67910d3d301a88382773a066be8c81a350d18c243ade54d61ec50923c5e7583`  
		Last Modified: Tue, 03 Jun 2025 17:07:47 GMT  
		Size: 104.5 MB (104532630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d1c867fd17fe66471be29077931fd8ec1699a13818eb93034e99868ecd7bd3`  
		Last Modified: Tue, 03 Jun 2025 17:07:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c35195e7507c24005520a8c45874a499a1bf080555373c57a5d59b1a2df30b6`  
		Last Modified: Tue, 03 Jun 2025 17:09:44 GMT  
		Size: 98.0 MB (97954050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c64fea9ecf8685a15c2e72575fde6075df9337d0daff01a2707185e92209ef`  
		Last Modified: Tue, 03 Jun 2025 17:09:31 GMT  
		Size: 362.1 KB (362150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba527436b8c305a48ac0cc16f3a7e43f9ea5f827c368c8b90c0fffeed8273e03`  
		Last Modified: Tue, 03 Jun 2025 17:09:32 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5237a367af95b4bc5cef912321b337fe2e5d66f06a23ad973680596da45b35`  
		Last Modified: Tue, 03 Jun 2025 17:09:34 GMT  
		Size: 23.3 MB (23293629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:3f9a1f71a07eeee1d89c2ad93a5a3d2ac24ae2e416db0045d901b25dc26b98f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23029026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bcd344793f2c51eb8da1c190bf0ed7340dd88a97cf388d91a9ab5cfb3641ed`

```dockerfile
```

-	Layers:
	-	`sha256:dec6754de12c5c273127119636a801198a3de05c2e6aa7911fda9b935583a54b`  
		Last Modified: Tue, 03 Jun 2025 19:17:27 GMT  
		Size: 23.0 MB (23012635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51171abc4c4a0cde6313f059dc67861e4ac2e78c764b0af0a0857e4d5b1bd3fc`  
		Last Modified: Tue, 03 Jun 2025 19:17:28 GMT  
		Size: 16.4 KB (16391 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:19292be2584cd845db9b5542b76546a7e5da661bcac15f1804d2c1cbb68467d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255409086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6a8d0d8d582d4cfdd0c7b9e2b03f3befcc80db56d8e63074ecb9105ec73b8a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 May 2022 20:32:40 GMT
ARG RELEASE
# Mon, 23 May 2022 20:32:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 May 2022 20:32:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 23 May 2022 20:32:40 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Mon, 23 May 2022 20:32:40 GMT
CMD ["/bin/bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENV LANG=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV LC_ALL=C.UTF-8
# Mon, 23 May 2022 20:32:40 GMT
ENV ROS_DISTRO=humble
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 23 May 2022 20:32:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 23 May 2022 20:32:40 GMT
CMD ["bash"]
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 23 May 2022 20:32:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee5308cdd15f77e44b92e47b6f1d16733b65fab16dcd7978a623f62dd7f8bb6`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 1.2 MB (1214200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73381c2c31e36b7d9ed2c02345b213f909f409fb89bafae890235d56bc9e732a`  
		Last Modified: Tue, 03 Jun 2025 16:19:13 GMT  
		Size: 5.9 MB (5936692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5d02a65bd7f7a1fc39a15acf77d63c54244aaaf22429febec588ea14ffccb2`  
		Last Modified: Tue, 03 Jun 2025 16:19:11 GMT  
		Size: 97.2 KB (97234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe74201331921b71dbaff57f282e63b8c2a23276f1e7169c2bda36a5df74e77a`  
		Last Modified: Tue, 03 Jun 2025 16:19:27 GMT  
		Size: 102.3 MB (102252252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced1014ed7cbc1c9aa8f3a96a4bb6e1deaaf93f58041c5d88da2356ee7b4266f`  
		Last Modified: Tue, 03 Jun 2025 16:18:55 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f371b330eabe98b4c2f7a23612c6b1e42a4956672754821ddf5872050a558eb4`  
		Last Modified: Tue, 03 Jun 2025 17:09:53 GMT  
		Size: 95.5 MB (95506704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42eaf8eb4130d56998aaeb0e2ba32f8c3a358eae317fcc40d60886b6021008de`  
		Last Modified: Tue, 03 Jun 2025 17:09:37 GMT  
		Size: 362.2 KB (362154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014dcb0d353b6d71d8ee54ea5ea2da373e2d203f95d5aa144a904474030c8f6e`  
		Last Modified: Tue, 03 Jun 2025 17:09:37 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa21615c56eef2e3c96f602ed9e098526eebb513ac0e2d5ba41b462cea49278`  
		Last Modified: Tue, 03 Jun 2025 17:09:41 GMT  
		Size: 22.7 MB (22681600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-base-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:ec37020439d18152fd259a5d6f242dc62d3856e1ccecc11f77aabd1ff5c5c0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23042179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f0cd94ca0f26a5bd27e47c2292056ae159e15f778b2d7e6ecb6d7ec7ca8414`

```dockerfile
```

-	Layers:
	-	`sha256:3fd7739ab610e44cd8a172462b5d39eb9be018c2619daa3c23e80de27f82e039`  
		Last Modified: Tue, 03 Jun 2025 19:17:45 GMT  
		Size: 23.0 MB (23025651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6aff5c76f0803b84b6c1353d30ff26b3426ace202704137c99555c427643e9e`  
		Last Modified: Tue, 03 Jun 2025 19:17:46 GMT  
		Size: 16.5 KB (16528 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:d1d39c8398c6c8f0fb5fa0f1898695c9c11b17aa3822b1474abd42e69b771f33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:6f11ebdfeb935dcfa070150abeae56bbc82e5c27278867cb514978ccae9f1c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141368890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002ca501eadabf55dd190260c11a97b461793b6bdeeb711c8e88709dfb5bbfd9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25b611258b9e589c289c2fb50570b97c455ad6e5e6e9de251b753fab9c5618c`  
		Last Modified: Tue, 03 Jun 2025 17:07:39 GMT  
		Size: 1.2 MB (1214039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdf6d82836139f37c4872db40ac59c01b82bfce2b74e5ba795b14ee21f7bc4e`  
		Last Modified: Tue, 03 Jun 2025 17:07:38 GMT  
		Size: 6.0 MB (5991843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8ee3eb0604e23957531406bba2fdaa67f77da515ebbafa7e8f318d462c40be`  
		Last Modified: Tue, 03 Jun 2025 17:07:37 GMT  
		Size: 97.2 KB (97179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67910d3d301a88382773a066be8c81a350d18c243ade54d61ec50923c5e7583`  
		Last Modified: Tue, 03 Jun 2025 17:07:47 GMT  
		Size: 104.5 MB (104532630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d1c867fd17fe66471be29077931fd8ec1699a13818eb93034e99868ecd7bd3`  
		Last Modified: Tue, 03 Jun 2025 17:07:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:191f1550725d80669d12edc455e17f0e5163b2b1ffecc06fb8fe2e6801862496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17203214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a4d216ed97f262ab7ed40c6967575b2844c08d3c31f4a4216b8c7e3f9216ca`

```dockerfile
```

-	Layers:
	-	`sha256:5ff846ed63a1685c5d4963019fa30d683dc415b1d81d05dd5abf406332eedbea`  
		Last Modified: Tue, 03 Jun 2025 19:17:39 GMT  
		Size: 17.2 MB (17188557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f88e022820fb282eafff57fb8bb64434c0a25f7f1d3bbfa7be9dc23be2c1ffa8`  
		Last Modified: Tue, 03 Jun 2025 19:17:40 GMT  
		Size: 14.7 KB (14657 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:844044a61caaac8d303d0e25ade24afca7bbeb0f066b89a5963987022eecd9e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136856156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d96501dc6e13ebed3129186d7387b48485b46d975d1d762051d509f3363d65`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee5308cdd15f77e44b92e47b6f1d16733b65fab16dcd7978a623f62dd7f8bb6`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 1.2 MB (1214200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73381c2c31e36b7d9ed2c02345b213f909f409fb89bafae890235d56bc9e732a`  
		Last Modified: Tue, 03 Jun 2025 16:19:13 GMT  
		Size: 5.9 MB (5936692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5d02a65bd7f7a1fc39a15acf77d63c54244aaaf22429febec588ea14ffccb2`  
		Last Modified: Tue, 03 Jun 2025 16:19:11 GMT  
		Size: 97.2 KB (97234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe74201331921b71dbaff57f282e63b8c2a23276f1e7169c2bda36a5df74e77a`  
		Last Modified: Tue, 03 Jun 2025 16:19:27 GMT  
		Size: 102.3 MB (102252252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced1014ed7cbc1c9aa8f3a96a4bb6e1deaaf93f58041c5d88da2356ee7b4266f`  
		Last Modified: Tue, 03 Jun 2025 16:18:55 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:e58b0ee9bdcd2199e920270181f27a77d7bcae525f9261e43599909525f9b293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17189688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e463e08ecc906c1e0a8f01af074b7ad6758e49b74a00a66b15c684d8cc39b140`

```dockerfile
```

-	Layers:
	-	`sha256:c5cf0d69500ef67f2658c591f928c3298f8204f17dfc4a66ee0696eb63d8a9ed`  
		Last Modified: Tue, 03 Jun 2025 19:17:53 GMT  
		Size: 17.2 MB (17174906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d37ef719f292d3410ff64d1aaad711e038ee48db26c6cfc2abc6e46f81345c`  
		Last Modified: Tue, 03 Jun 2025 19:17:54 GMT  
		Size: 14.8 KB (14782 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:d1d39c8398c6c8f0fb5fa0f1898695c9c11b17aa3822b1474abd42e69b771f33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:6f11ebdfeb935dcfa070150abeae56bbc82e5c27278867cb514978ccae9f1c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141368890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002ca501eadabf55dd190260c11a97b461793b6bdeeb711c8e88709dfb5bbfd9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25b611258b9e589c289c2fb50570b97c455ad6e5e6e9de251b753fab9c5618c`  
		Last Modified: Tue, 03 Jun 2025 17:07:39 GMT  
		Size: 1.2 MB (1214039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdf6d82836139f37c4872db40ac59c01b82bfce2b74e5ba795b14ee21f7bc4e`  
		Last Modified: Tue, 03 Jun 2025 17:07:38 GMT  
		Size: 6.0 MB (5991843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8ee3eb0604e23957531406bba2fdaa67f77da515ebbafa7e8f318d462c40be`  
		Last Modified: Tue, 03 Jun 2025 17:07:37 GMT  
		Size: 97.2 KB (97179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67910d3d301a88382773a066be8c81a350d18c243ade54d61ec50923c5e7583`  
		Last Modified: Tue, 03 Jun 2025 17:07:47 GMT  
		Size: 104.5 MB (104532630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d1c867fd17fe66471be29077931fd8ec1699a13818eb93034e99868ecd7bd3`  
		Last Modified: Tue, 03 Jun 2025 17:07:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:191f1550725d80669d12edc455e17f0e5163b2b1ffecc06fb8fe2e6801862496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17203214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a4d216ed97f262ab7ed40c6967575b2844c08d3c31f4a4216b8c7e3f9216ca`

```dockerfile
```

-	Layers:
	-	`sha256:5ff846ed63a1685c5d4963019fa30d683dc415b1d81d05dd5abf406332eedbea`  
		Last Modified: Tue, 03 Jun 2025 19:17:39 GMT  
		Size: 17.2 MB (17188557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f88e022820fb282eafff57fb8bb64434c0a25f7f1d3bbfa7be9dc23be2c1ffa8`  
		Last Modified: Tue, 03 Jun 2025 19:17:40 GMT  
		Size: 14.7 KB (14657 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:844044a61caaac8d303d0e25ade24afca7bbeb0f066b89a5963987022eecd9e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136856156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d96501dc6e13ebed3129186d7387b48485b46d975d1d762051d509f3363d65`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.jammy_all.deb     && echo "1600cb8cc28258a39bffc1736a75bcbf52d1f2db371a4d020c1b187d2a5a083b /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee5308cdd15f77e44b92e47b6f1d16733b65fab16dcd7978a623f62dd7f8bb6`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 1.2 MB (1214200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73381c2c31e36b7d9ed2c02345b213f909f409fb89bafae890235d56bc9e732a`  
		Last Modified: Tue, 03 Jun 2025 16:19:13 GMT  
		Size: 5.9 MB (5936692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5d02a65bd7f7a1fc39a15acf77d63c54244aaaf22429febec588ea14ffccb2`  
		Last Modified: Tue, 03 Jun 2025 16:19:11 GMT  
		Size: 97.2 KB (97234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe74201331921b71dbaff57f282e63b8c2a23276f1e7169c2bda36a5df74e77a`  
		Last Modified: Tue, 03 Jun 2025 16:19:27 GMT  
		Size: 102.3 MB (102252252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced1014ed7cbc1c9aa8f3a96a4bb6e1deaaf93f58041c5d88da2356ee7b4266f`  
		Last Modified: Tue, 03 Jun 2025 16:18:55 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:humble-ros-core-jammy` - unknown; unknown

```console
$ docker pull ros@sha256:e58b0ee9bdcd2199e920270181f27a77d7bcae525f9261e43599909525f9b293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17189688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e463e08ecc906c1e0a8f01af074b7ad6758e49b74a00a66b15c684d8cc39b140`

```dockerfile
```

-	Layers:
	-	`sha256:c5cf0d69500ef67f2658c591f928c3298f8204f17dfc4a66ee0696eb63d8a9ed`  
		Last Modified: Tue, 03 Jun 2025 19:17:53 GMT  
		Size: 17.2 MB (17174906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d37ef719f292d3410ff64d1aaad711e038ee48db26c6cfc2abc6e46f81345c`  
		Last Modified: Tue, 03 Jun 2025 19:17:54 GMT  
		Size: 14.8 KB (14782 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy`

```console
$ docker pull ros@sha256:026816c588cc465b3838721edd970a66827bd6a4618e49969d8e5dfa977c660e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:1b01c30c300bf57e1e429e466c4d88d9c9beb1298fd3ef5c4fa18b928ad67b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295661118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210ea2138a721c7166913e5c06fcde48d532753cfbeed14356284de4d7d28500`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8869d62bea26cae8ab2f85ad14f208e76c7f463db4bd3681f8df7f2db1aa70`  
		Last Modified: Tue, 03 Jun 2025 17:07:43 GMT  
		Size: 683.8 KB (683775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdda66f6933d387b046b7278b307c4a50b054916c1d33878ff0ea47b11ea288`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 6.7 MB (6745523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4f7f179852ccfe99b50eece2eff5ed1fc42d17227c23e8500f4e1f0366c8b6`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 94.0 KB (94050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc086dd908beb9598940d79e43ce727c4d66a6c4c9a83ef3dbc532efd3ac556`  
		Last Modified: Tue, 03 Jun 2025 17:07:52 GMT  
		Size: 119.9 MB (119908702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d3aa09250ecc0281476638d2d5996ff648156fed57cfa9bebf82c4ebf962b0`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d996ba9b4edd88c0a1218a4f6b9e82aacbb4cd9c0f44a02d8052de578268d1c`  
		Last Modified: Tue, 03 Jun 2025 17:09:50 GMT  
		Size: 110.2 MB (110179284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c6c6b25ec0196eb5046ea65df46a24cb5bb13006dc63bca159185fe044eb30`  
		Last Modified: Tue, 03 Jun 2025 17:09:34 GMT  
		Size: 365.5 KB (365545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943b1a661f69478625db6adb1761fd8f1ccec92717bd44cdfe2b5a06e75f2cb0`  
		Last Modified: Tue, 03 Jun 2025 17:09:32 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb6de655debbb5b7b335e7467749f8aa7e61315197004beb93d7c89b07a9182`  
		Last Modified: Tue, 03 Jun 2025 17:09:38 GMT  
		Size: 28.0 MB (27966270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:208e9324840cc54d335b55663183bc50f2177a5052f52dc053b117e3023a411c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23975352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5c00592be208c22b3e14f803385c3ea66ea35f32064bfb4a1059370ee90fe1`

```dockerfile
```

-	Layers:
	-	`sha256:d07942c31bff532d3129903744c4a7e2d332dc1cc78361cd9214daad305739c5`  
		Last Modified: Tue, 03 Jun 2025 19:17:53 GMT  
		Size: 24.0 MB (23958688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33a9c88c866c53e68ec30b286a828168dfb46d32d402dcf2f9186da2a977e8f3`  
		Last Modified: Tue, 03 Jun 2025 19:17:54 GMT  
		Size: 16.7 KB (16664 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0e1497ee844bb1ff2078ff00b005c05b57d0c42a669832c2c5c1d65f39fba896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284104470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff0eda86dadd0da69f7273b932e2fe6608e9fef9f2e9c8e39aa228b102838ca`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ba7c57b0ec01c10fc7cf681ee099c37c987498c25b1b8cb4a29128ced96907`  
		Last Modified: Tue, 03 Jun 2025 16:22:11 GMT  
		Size: 114.7 MB (114689282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f79a5b3df57a487c18df3ed8e9513b75c70fe5101db46ee91d23db81aada5`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedc0bf39755013a910d8ad1b32b6f3f9b9312ce259a79006dd3607186145d52`  
		Last Modified: Tue, 03 Jun 2025 17:12:16 GMT  
		Size: 105.6 MB (105593170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94701b4069614f2698aa75959641413e64967923478ef666610963cbac10ccd3`  
		Last Modified: Tue, 03 Jun 2025 17:12:06 GMT  
		Size: 365.5 KB (365548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7434caed03c758a0b9a196d1551d0566ab0ec6c0e6bf60c1c9f8781f89c879a`  
		Last Modified: Tue, 03 Jun 2025 17:12:06 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781027cdaf47969f8306b57e6d33eaaeb74013c708798b7c6c7288103ba9595`  
		Last Modified: Tue, 03 Jun 2025 17:12:09 GMT  
		Size: 27.1 MB (27064676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy` - unknown; unknown

```console
$ docker pull ros@sha256:2afa6387c997352b229bb14d702b93943f67478b00f4e36911328585c5ef04dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23997767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9d366cc100fcea3333bfcf3e3be89217240945e35a7abd45aace3e7f23d494`

```dockerfile
```

-	Layers:
	-	`sha256:b08db0fa85af9540e10577f9163cfe79c3de70f554f78301db879d7dec8c42df`  
		Last Modified: Tue, 03 Jun 2025 19:18:16 GMT  
		Size: 24.0 MB (23980954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3701caf148a35f3d36eb094ad32ebfeb5ce8986d19a04d29a6e940c9df59d93`  
		Last Modified: Tue, 03 Jun 2025 19:18:17 GMT  
		Size: 16.8 KB (16813 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:2cf1d3940a8fafb123bce354840517cc73bc7ae9795fe7131a503db5c4f2093e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:de4ebe99b08d3836e4a7e321e87411e80b3fbcd1b9879eca6235612ca67aa023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1076264209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8e0f8fe6cbadc57a21c094776551e44d396237427c619318da9bb4a874d44c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8869d62bea26cae8ab2f85ad14f208e76c7f463db4bd3681f8df7f2db1aa70`  
		Last Modified: Tue, 03 Jun 2025 17:07:43 GMT  
		Size: 683.8 KB (683775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdda66f6933d387b046b7278b307c4a50b054916c1d33878ff0ea47b11ea288`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 6.7 MB (6745523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4f7f179852ccfe99b50eece2eff5ed1fc42d17227c23e8500f4e1f0366c8b6`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 94.0 KB (94050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc086dd908beb9598940d79e43ce727c4d66a6c4c9a83ef3dbc532efd3ac556`  
		Last Modified: Tue, 03 Jun 2025 17:07:52 GMT  
		Size: 119.9 MB (119908702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d3aa09250ecc0281476638d2d5996ff648156fed57cfa9bebf82c4ebf962b0`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d996ba9b4edd88c0a1218a4f6b9e82aacbb4cd9c0f44a02d8052de578268d1c`  
		Last Modified: Tue, 03 Jun 2025 17:09:50 GMT  
		Size: 110.2 MB (110179284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c6c6b25ec0196eb5046ea65df46a24cb5bb13006dc63bca159185fe044eb30`  
		Last Modified: Tue, 03 Jun 2025 17:09:34 GMT  
		Size: 365.5 KB (365545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943b1a661f69478625db6adb1761fd8f1ccec92717bd44cdfe2b5a06e75f2cb0`  
		Last Modified: Tue, 03 Jun 2025 17:09:32 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb6de655debbb5b7b335e7467749f8aa7e61315197004beb93d7c89b07a9182`  
		Last Modified: Tue, 03 Jun 2025 17:09:38 GMT  
		Size: 28.0 MB (27966270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc50a40fa49ed9f01a972f677ffc41239589ee12e26ac82438ec6776413bd0be`  
		Last Modified: Tue, 03 Jun 2025 20:48:37 GMT  
		Size: 780.6 MB (780603091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:046c9623e5a1ada62ef847141175908f40a41bbb10df5a3f534247f2f55f28dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59868003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363c178ce11ed3d567777710375cf323eb90e1c995775c269ac7454b31a1b762`

```dockerfile
```

-	Layers:
	-	`sha256:264afef4a45c0400b42039ad16568af9575bd48bb40dc45646643447ecb7ff39`  
		Last Modified: Tue, 03 Jun 2025 19:18:00 GMT  
		Size: 59.9 MB (59858621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc14dca7e3197f1ab997206b3a2f54c0bc10eab982be8c9a21505a5d9b084164`  
		Last Modified: Tue, 03 Jun 2025 19:18:02 GMT  
		Size: 9.4 KB (9382 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e382657e8307c3d96ef26fd8f6b278b32f1a8160e084a29c463b36566b0dddab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **974.9 MB (974862258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21afb422fc28ebce1ad43d086bfa8dbb8f6f513f21eeb344c87ce9f51b685b05`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ba7c57b0ec01c10fc7cf681ee099c37c987498c25b1b8cb4a29128ced96907`  
		Last Modified: Tue, 03 Jun 2025 16:22:11 GMT  
		Size: 114.7 MB (114689282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f79a5b3df57a487c18df3ed8e9513b75c70fe5101db46ee91d23db81aada5`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedc0bf39755013a910d8ad1b32b6f3f9b9312ce259a79006dd3607186145d52`  
		Last Modified: Tue, 03 Jun 2025 17:12:16 GMT  
		Size: 105.6 MB (105593170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94701b4069614f2698aa75959641413e64967923478ef666610963cbac10ccd3`  
		Last Modified: Tue, 03 Jun 2025 17:12:06 GMT  
		Size: 365.5 KB (365548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7434caed03c758a0b9a196d1551d0566ab0ec6c0e6bf60c1c9f8781f89c879a`  
		Last Modified: Tue, 03 Jun 2025 17:12:06 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781027cdaf47969f8306b57e6d33eaaeb74013c708798b7c6c7288103ba9595`  
		Last Modified: Tue, 03 Jun 2025 17:12:09 GMT  
		Size: 27.1 MB (27064676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6faf6b462279f62c4ab4e2b672c45387d260df6ea23126ccf0f58da92114612`  
		Last Modified: Tue, 03 Jun 2025 18:46:16 GMT  
		Size: 690.8 MB (690757788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception` - unknown; unknown

```console
$ docker pull ros@sha256:998fb887f4c965109b01719f09ffa96c99f22a3d559f263f80b69d0954ff1b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59819748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86bf67b1fa8bb527620567e307d01187aa155d113fb732d2533ea49ec34792a5`

```dockerfile
```

-	Layers:
	-	`sha256:f7299e63cbb5c7686bf54574126bd82e9838dfa3dec4502022be42a20a480b2b`  
		Last Modified: Tue, 03 Jun 2025 19:19:40 GMT  
		Size: 59.8 MB (59810286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c97c55beb3763c67f17e5496d8a87af2fa407a4de9c18dc557cf1240fd951af`  
		Last Modified: Tue, 03 Jun 2025 19:19:42 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:2cf1d3940a8fafb123bce354840517cc73bc7ae9795fe7131a503db5c4f2093e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:de4ebe99b08d3836e4a7e321e87411e80b3fbcd1b9879eca6235612ca67aa023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1076264209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8e0f8fe6cbadc57a21c094776551e44d396237427c619318da9bb4a874d44c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8869d62bea26cae8ab2f85ad14f208e76c7f463db4bd3681f8df7f2db1aa70`  
		Last Modified: Tue, 03 Jun 2025 17:07:43 GMT  
		Size: 683.8 KB (683775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdda66f6933d387b046b7278b307c4a50b054916c1d33878ff0ea47b11ea288`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 6.7 MB (6745523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4f7f179852ccfe99b50eece2eff5ed1fc42d17227c23e8500f4e1f0366c8b6`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 94.0 KB (94050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc086dd908beb9598940d79e43ce727c4d66a6c4c9a83ef3dbc532efd3ac556`  
		Last Modified: Tue, 03 Jun 2025 17:07:52 GMT  
		Size: 119.9 MB (119908702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d3aa09250ecc0281476638d2d5996ff648156fed57cfa9bebf82c4ebf962b0`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d996ba9b4edd88c0a1218a4f6b9e82aacbb4cd9c0f44a02d8052de578268d1c`  
		Last Modified: Tue, 03 Jun 2025 17:09:50 GMT  
		Size: 110.2 MB (110179284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c6c6b25ec0196eb5046ea65df46a24cb5bb13006dc63bca159185fe044eb30`  
		Last Modified: Tue, 03 Jun 2025 17:09:34 GMT  
		Size: 365.5 KB (365545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943b1a661f69478625db6adb1761fd8f1ccec92717bd44cdfe2b5a06e75f2cb0`  
		Last Modified: Tue, 03 Jun 2025 17:09:32 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb6de655debbb5b7b335e7467749f8aa7e61315197004beb93d7c89b07a9182`  
		Last Modified: Tue, 03 Jun 2025 17:09:38 GMT  
		Size: 28.0 MB (27966270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc50a40fa49ed9f01a972f677ffc41239589ee12e26ac82438ec6776413bd0be`  
		Last Modified: Tue, 03 Jun 2025 20:48:37 GMT  
		Size: 780.6 MB (780603091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:046c9623e5a1ada62ef847141175908f40a41bbb10df5a3f534247f2f55f28dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59868003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363c178ce11ed3d567777710375cf323eb90e1c995775c269ac7454b31a1b762`

```dockerfile
```

-	Layers:
	-	`sha256:264afef4a45c0400b42039ad16568af9575bd48bb40dc45646643447ecb7ff39`  
		Last Modified: Tue, 03 Jun 2025 19:18:00 GMT  
		Size: 59.9 MB (59858621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc14dca7e3197f1ab997206b3a2f54c0bc10eab982be8c9a21505a5d9b084164`  
		Last Modified: Tue, 03 Jun 2025 19:18:02 GMT  
		Size: 9.4 KB (9382 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e382657e8307c3d96ef26fd8f6b278b32f1a8160e084a29c463b36566b0dddab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **974.9 MB (974862258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21afb422fc28ebce1ad43d086bfa8dbb8f6f513f21eeb344c87ce9f51b685b05`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ba7c57b0ec01c10fc7cf681ee099c37c987498c25b1b8cb4a29128ced96907`  
		Last Modified: Tue, 03 Jun 2025 16:22:11 GMT  
		Size: 114.7 MB (114689282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f79a5b3df57a487c18df3ed8e9513b75c70fe5101db46ee91d23db81aada5`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedc0bf39755013a910d8ad1b32b6f3f9b9312ce259a79006dd3607186145d52`  
		Last Modified: Tue, 03 Jun 2025 17:12:16 GMT  
		Size: 105.6 MB (105593170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94701b4069614f2698aa75959641413e64967923478ef666610963cbac10ccd3`  
		Last Modified: Tue, 03 Jun 2025 17:12:06 GMT  
		Size: 365.5 KB (365548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7434caed03c758a0b9a196d1551d0566ab0ec6c0e6bf60c1c9f8781f89c879a`  
		Last Modified: Tue, 03 Jun 2025 17:12:06 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781027cdaf47969f8306b57e6d33eaaeb74013c708798b7c6c7288103ba9595`  
		Last Modified: Tue, 03 Jun 2025 17:12:09 GMT  
		Size: 27.1 MB (27064676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6faf6b462279f62c4ab4e2b672c45387d260df6ea23126ccf0f58da92114612`  
		Last Modified: Tue, 03 Jun 2025 18:46:16 GMT  
		Size: 690.8 MB (690757788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:998fb887f4c965109b01719f09ffa96c99f22a3d559f263f80b69d0954ff1b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59819748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86bf67b1fa8bb527620567e307d01187aa155d113fb732d2533ea49ec34792a5`

```dockerfile
```

-	Layers:
	-	`sha256:f7299e63cbb5c7686bf54574126bd82e9838dfa3dec4502022be42a20a480b2b`  
		Last Modified: Tue, 03 Jun 2025 19:19:40 GMT  
		Size: 59.8 MB (59810286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c97c55beb3763c67f17e5496d8a87af2fa407a4de9c18dc557cf1240fd951af`  
		Last Modified: Tue, 03 Jun 2025 19:19:42 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:026816c588cc465b3838721edd970a66827bd6a4618e49969d8e5dfa977c660e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:1b01c30c300bf57e1e429e466c4d88d9c9beb1298fd3ef5c4fa18b928ad67b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295661118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210ea2138a721c7166913e5c06fcde48d532753cfbeed14356284de4d7d28500`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8869d62bea26cae8ab2f85ad14f208e76c7f463db4bd3681f8df7f2db1aa70`  
		Last Modified: Tue, 03 Jun 2025 17:07:43 GMT  
		Size: 683.8 KB (683775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdda66f6933d387b046b7278b307c4a50b054916c1d33878ff0ea47b11ea288`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 6.7 MB (6745523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4f7f179852ccfe99b50eece2eff5ed1fc42d17227c23e8500f4e1f0366c8b6`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 94.0 KB (94050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc086dd908beb9598940d79e43ce727c4d66a6c4c9a83ef3dbc532efd3ac556`  
		Last Modified: Tue, 03 Jun 2025 17:07:52 GMT  
		Size: 119.9 MB (119908702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d3aa09250ecc0281476638d2d5996ff648156fed57cfa9bebf82c4ebf962b0`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d996ba9b4edd88c0a1218a4f6b9e82aacbb4cd9c0f44a02d8052de578268d1c`  
		Last Modified: Tue, 03 Jun 2025 17:09:50 GMT  
		Size: 110.2 MB (110179284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c6c6b25ec0196eb5046ea65df46a24cb5bb13006dc63bca159185fe044eb30`  
		Last Modified: Tue, 03 Jun 2025 17:09:34 GMT  
		Size: 365.5 KB (365545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943b1a661f69478625db6adb1761fd8f1ccec92717bd44cdfe2b5a06e75f2cb0`  
		Last Modified: Tue, 03 Jun 2025 17:09:32 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb6de655debbb5b7b335e7467749f8aa7e61315197004beb93d7c89b07a9182`  
		Last Modified: Tue, 03 Jun 2025 17:09:38 GMT  
		Size: 28.0 MB (27966270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:208e9324840cc54d335b55663183bc50f2177a5052f52dc053b117e3023a411c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23975352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5c00592be208c22b3e14f803385c3ea66ea35f32064bfb4a1059370ee90fe1`

```dockerfile
```

-	Layers:
	-	`sha256:d07942c31bff532d3129903744c4a7e2d332dc1cc78361cd9214daad305739c5`  
		Last Modified: Tue, 03 Jun 2025 19:17:53 GMT  
		Size: 24.0 MB (23958688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33a9c88c866c53e68ec30b286a828168dfb46d32d402dcf2f9186da2a977e8f3`  
		Last Modified: Tue, 03 Jun 2025 19:17:54 GMT  
		Size: 16.7 KB (16664 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0e1497ee844bb1ff2078ff00b005c05b57d0c42a669832c2c5c1d65f39fba896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284104470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff0eda86dadd0da69f7273b932e2fe6608e9fef9f2e9c8e39aa228b102838ca`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ba7c57b0ec01c10fc7cf681ee099c37c987498c25b1b8cb4a29128ced96907`  
		Last Modified: Tue, 03 Jun 2025 16:22:11 GMT  
		Size: 114.7 MB (114689282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f79a5b3df57a487c18df3ed8e9513b75c70fe5101db46ee91d23db81aada5`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedc0bf39755013a910d8ad1b32b6f3f9b9312ce259a79006dd3607186145d52`  
		Last Modified: Tue, 03 Jun 2025 17:12:16 GMT  
		Size: 105.6 MB (105593170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94701b4069614f2698aa75959641413e64967923478ef666610963cbac10ccd3`  
		Last Modified: Tue, 03 Jun 2025 17:12:06 GMT  
		Size: 365.5 KB (365548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7434caed03c758a0b9a196d1551d0566ab0ec6c0e6bf60c1c9f8781f89c879a`  
		Last Modified: Tue, 03 Jun 2025 17:12:06 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781027cdaf47969f8306b57e6d33eaaeb74013c708798b7c6c7288103ba9595`  
		Last Modified: Tue, 03 Jun 2025 17:12:09 GMT  
		Size: 27.1 MB (27064676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:2afa6387c997352b229bb14d702b93943f67478b00f4e36911328585c5ef04dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23997767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9d366cc100fcea3333bfcf3e3be89217240945e35a7abd45aace3e7f23d494`

```dockerfile
```

-	Layers:
	-	`sha256:b08db0fa85af9540e10577f9163cfe79c3de70f554f78301db879d7dec8c42df`  
		Last Modified: Tue, 03 Jun 2025 19:18:16 GMT  
		Size: 24.0 MB (23980954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3701caf148a35f3d36eb094ad32ebfeb5ce8986d19a04d29a6e940c9df59d93`  
		Last Modified: Tue, 03 Jun 2025 19:18:17 GMT  
		Size: 16.8 KB (16813 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:026816c588cc465b3838721edd970a66827bd6a4618e49969d8e5dfa977c660e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:1b01c30c300bf57e1e429e466c4d88d9c9beb1298fd3ef5c4fa18b928ad67b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295661118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210ea2138a721c7166913e5c06fcde48d532753cfbeed14356284de4d7d28500`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8869d62bea26cae8ab2f85ad14f208e76c7f463db4bd3681f8df7f2db1aa70`  
		Last Modified: Tue, 03 Jun 2025 17:07:43 GMT  
		Size: 683.8 KB (683775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdda66f6933d387b046b7278b307c4a50b054916c1d33878ff0ea47b11ea288`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 6.7 MB (6745523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4f7f179852ccfe99b50eece2eff5ed1fc42d17227c23e8500f4e1f0366c8b6`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 94.0 KB (94050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc086dd908beb9598940d79e43ce727c4d66a6c4c9a83ef3dbc532efd3ac556`  
		Last Modified: Tue, 03 Jun 2025 17:07:52 GMT  
		Size: 119.9 MB (119908702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d3aa09250ecc0281476638d2d5996ff648156fed57cfa9bebf82c4ebf962b0`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d996ba9b4edd88c0a1218a4f6b9e82aacbb4cd9c0f44a02d8052de578268d1c`  
		Last Modified: Tue, 03 Jun 2025 17:09:50 GMT  
		Size: 110.2 MB (110179284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c6c6b25ec0196eb5046ea65df46a24cb5bb13006dc63bca159185fe044eb30`  
		Last Modified: Tue, 03 Jun 2025 17:09:34 GMT  
		Size: 365.5 KB (365545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943b1a661f69478625db6adb1761fd8f1ccec92717bd44cdfe2b5a06e75f2cb0`  
		Last Modified: Tue, 03 Jun 2025 17:09:32 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb6de655debbb5b7b335e7467749f8aa7e61315197004beb93d7c89b07a9182`  
		Last Modified: Tue, 03 Jun 2025 17:09:38 GMT  
		Size: 28.0 MB (27966270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:208e9324840cc54d335b55663183bc50f2177a5052f52dc053b117e3023a411c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23975352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5c00592be208c22b3e14f803385c3ea66ea35f32064bfb4a1059370ee90fe1`

```dockerfile
```

-	Layers:
	-	`sha256:d07942c31bff532d3129903744c4a7e2d332dc1cc78361cd9214daad305739c5`  
		Last Modified: Tue, 03 Jun 2025 19:17:53 GMT  
		Size: 24.0 MB (23958688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33a9c88c866c53e68ec30b286a828168dfb46d32d402dcf2f9186da2a977e8f3`  
		Last Modified: Tue, 03 Jun 2025 19:17:54 GMT  
		Size: 16.7 KB (16664 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0e1497ee844bb1ff2078ff00b005c05b57d0c42a669832c2c5c1d65f39fba896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284104470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff0eda86dadd0da69f7273b932e2fe6608e9fef9f2e9c8e39aa228b102838ca`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ba7c57b0ec01c10fc7cf681ee099c37c987498c25b1b8cb4a29128ced96907`  
		Last Modified: Tue, 03 Jun 2025 16:22:11 GMT  
		Size: 114.7 MB (114689282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f79a5b3df57a487c18df3ed8e9513b75c70fe5101db46ee91d23db81aada5`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedc0bf39755013a910d8ad1b32b6f3f9b9312ce259a79006dd3607186145d52`  
		Last Modified: Tue, 03 Jun 2025 17:12:16 GMT  
		Size: 105.6 MB (105593170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94701b4069614f2698aa75959641413e64967923478ef666610963cbac10ccd3`  
		Last Modified: Tue, 03 Jun 2025 17:12:06 GMT  
		Size: 365.5 KB (365548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7434caed03c758a0b9a196d1551d0566ab0ec6c0e6bf60c1c9f8781f89c879a`  
		Last Modified: Tue, 03 Jun 2025 17:12:06 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781027cdaf47969f8306b57e6d33eaaeb74013c708798b7c6c7288103ba9595`  
		Last Modified: Tue, 03 Jun 2025 17:12:09 GMT  
		Size: 27.1 MB (27064676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:2afa6387c997352b229bb14d702b93943f67478b00f4e36911328585c5ef04dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23997767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9d366cc100fcea3333bfcf3e3be89217240945e35a7abd45aace3e7f23d494`

```dockerfile
```

-	Layers:
	-	`sha256:b08db0fa85af9540e10577f9163cfe79c3de70f554f78301db879d7dec8c42df`  
		Last Modified: Tue, 03 Jun 2025 19:18:16 GMT  
		Size: 24.0 MB (23980954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3701caf148a35f3d36eb094ad32ebfeb5ce8986d19a04d29a6e940c9df59d93`  
		Last Modified: Tue, 03 Jun 2025 19:18:17 GMT  
		Size: 16.8 KB (16813 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:74c939fe0a0bedcb8c7d1e17fbbcc37ab88af905f3285925d2cb76b07ccc4f48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:3b55be422844d2a9c682fdd4779f7d24a6d4e745bc2e414a9ebb146a3365ef33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157147583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3e7ee0736ba128fd732427f05dd546f442ad376222e6825c672c6ab0a7d9ba`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=jazzy
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8869d62bea26cae8ab2f85ad14f208e76c7f463db4bd3681f8df7f2db1aa70`  
		Last Modified: Tue, 03 Jun 2025 17:07:43 GMT  
		Size: 683.8 KB (683775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdda66f6933d387b046b7278b307c4a50b054916c1d33878ff0ea47b11ea288`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 6.7 MB (6745523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4f7f179852ccfe99b50eece2eff5ed1fc42d17227c23e8500f4e1f0366c8b6`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 94.0 KB (94050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc086dd908beb9598940d79e43ce727c4d66a6c4c9a83ef3dbc532efd3ac556`  
		Last Modified: Tue, 03 Jun 2025 17:07:52 GMT  
		Size: 119.9 MB (119908702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d3aa09250ecc0281476638d2d5996ff648156fed57cfa9bebf82c4ebf962b0`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:abdb1f148880591670df2d6f728648451a6aed21290ecf59e20e2a54ea07f338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17903836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6562731f1a629aa2353df862294832e878626c38fe22af4cee9931a4f4440f57`

```dockerfile
```

-	Layers:
	-	`sha256:f7e93457220064bcb784dc9179ca611a1db2f15d8dd2a6227543a9a7da7c2704`  
		Last Modified: Tue, 03 Jun 2025 19:18:08 GMT  
		Size: 17.9 MB (17889193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e03c758fce3a51dada0ad8ea9fdd3f1c63d4bf41432e0ad052b92f2530a4952d`  
		Last Modified: Tue, 03 Jun 2025 19:18:09 GMT  
		Size: 14.6 KB (14643 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f0f544ab38dfcb7881d3cc27fed901b607aeae73dd338be2bc4ade64730d8c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151078619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40c51e3ddcb1d5f0c96fdb7a0d20fc013b73ad75a1330113a0387dede85cc1e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=jazzy
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ba7c57b0ec01c10fc7cf681ee099c37c987498c25b1b8cb4a29128ced96907`  
		Last Modified: Tue, 03 Jun 2025 16:22:11 GMT  
		Size: 114.7 MB (114689282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f79a5b3df57a487c18df3ed8e9513b75c70fe5101db46ee91d23db81aada5`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:922d207499d162145ef6e07737098d013a11fd475545442e0359f1133262c192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17877966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e917c6dae250c12763f6e3bc5eb1dfff511ded06230d7c788c1a0010dcf95ff`

```dockerfile
```

-	Layers:
	-	`sha256:776a42a15da74246dc945dbfa2d74f1e4675c1e0723177d16aa3ed3b63b46a67`  
		Last Modified: Tue, 03 Jun 2025 19:18:23 GMT  
		Size: 17.9 MB (17863199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17311a044bd03688fdb89dd0ec43efe1e34643339be9817e9cd4aba29b58ffc2`  
		Last Modified: Tue, 03 Jun 2025 19:18:24 GMT  
		Size: 14.8 KB (14767 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:74c939fe0a0bedcb8c7d1e17fbbcc37ab88af905f3285925d2cb76b07ccc4f48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:3b55be422844d2a9c682fdd4779f7d24a6d4e745bc2e414a9ebb146a3365ef33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157147583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3e7ee0736ba128fd732427f05dd546f442ad376222e6825c672c6ab0a7d9ba`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=jazzy
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8869d62bea26cae8ab2f85ad14f208e76c7f463db4bd3681f8df7f2db1aa70`  
		Last Modified: Tue, 03 Jun 2025 17:07:43 GMT  
		Size: 683.8 KB (683775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdda66f6933d387b046b7278b307c4a50b054916c1d33878ff0ea47b11ea288`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 6.7 MB (6745523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4f7f179852ccfe99b50eece2eff5ed1fc42d17227c23e8500f4e1f0366c8b6`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 94.0 KB (94050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc086dd908beb9598940d79e43ce727c4d66a6c4c9a83ef3dbc532efd3ac556`  
		Last Modified: Tue, 03 Jun 2025 17:07:52 GMT  
		Size: 119.9 MB (119908702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d3aa09250ecc0281476638d2d5996ff648156fed57cfa9bebf82c4ebf962b0`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:abdb1f148880591670df2d6f728648451a6aed21290ecf59e20e2a54ea07f338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17903836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6562731f1a629aa2353df862294832e878626c38fe22af4cee9931a4f4440f57`

```dockerfile
```

-	Layers:
	-	`sha256:f7e93457220064bcb784dc9179ca611a1db2f15d8dd2a6227543a9a7da7c2704`  
		Last Modified: Tue, 03 Jun 2025 19:18:08 GMT  
		Size: 17.9 MB (17889193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e03c758fce3a51dada0ad8ea9fdd3f1c63d4bf41432e0ad052b92f2530a4952d`  
		Last Modified: Tue, 03 Jun 2025 19:18:09 GMT  
		Size: 14.6 KB (14643 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f0f544ab38dfcb7881d3cc27fed901b607aeae73dd338be2bc4ade64730d8c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151078619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40c51e3ddcb1d5f0c96fdb7a0d20fc013b73ad75a1330113a0387dede85cc1e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=jazzy
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ba7c57b0ec01c10fc7cf681ee099c37c987498c25b1b8cb4a29128ced96907`  
		Last Modified: Tue, 03 Jun 2025 16:22:11 GMT  
		Size: 114.7 MB (114689282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f79a5b3df57a487c18df3ed8e9513b75c70fe5101db46ee91d23db81aada5`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:jazzy-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:922d207499d162145ef6e07737098d013a11fd475545442e0359f1133262c192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17877966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e917c6dae250c12763f6e3bc5eb1dfff511ded06230d7c788c1a0010dcf95ff`

```dockerfile
```

-	Layers:
	-	`sha256:776a42a15da74246dc945dbfa2d74f1e4675c1e0723177d16aa3ed3b63b46a67`  
		Last Modified: Tue, 03 Jun 2025 19:18:23 GMT  
		Size: 17.9 MB (17863199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17311a044bd03688fdb89dd0ec43efe1e34643339be9817e9cd4aba29b58ffc2`  
		Last Modified: Tue, 03 Jun 2025 19:18:24 GMT  
		Size: 14.8 KB (14767 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted`

```console
$ docker pull ros@sha256:0c933e161f6434be229bb5c1d3fd9442b0bfda562429731046500994337b4d16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted` - linux; amd64

```console
$ docker pull ros@sha256:8975664720534fb178de9c6223880f527240bf202042ec2d9bda4696c8ca48ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308210310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0289388d8db682cbfe62c775cf4d0a1f74f08bc2f0b24316e5d9cf58db72dffb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc922f2ce7df1733459b033fa462a421a0413670300a8b9c5c35ab7b81bc65eb`  
		Last Modified: Tue, 03 Jun 2025 16:19:30 GMT  
		Size: 683.8 KB (683816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01414ea5181d9da01a2e35570eba4ae2e37593bd21d531dfdf78f234660a7b3c`  
		Last Modified: Tue, 03 Jun 2025 16:19:32 GMT  
		Size: 6.7 MB (6745536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a09807d31167f2bd782983408d9ff7419d23b415ca575a3c7b3619165ad094`  
		Last Modified: Tue, 03 Jun 2025 16:19:31 GMT  
		Size: 94.0 KB (94039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099b8cd8b60f4a5d2476fd99e6adc027584cdef11cf59f36cc9b81b31e0ebf4`  
		Last Modified: Tue, 03 Jun 2025 17:07:48 GMT  
		Size: 132.4 MB (132407147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5402357658db93f168fcdf893f1c237364dea1ba24a8b5536a3c46e931231791`  
		Last Modified: Tue, 03 Jun 2025 16:19:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2760e6e89b71699480f8948db367864cbf4a35b90d807163f094494c524c2b1c`  
		Last Modified: Tue, 03 Jun 2025 17:09:53 GMT  
		Size: 110.2 MB (110182872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87d239340021c39b9ae17dd1ad6e2bdfa92f900c692b22d4241368481334529`  
		Last Modified: Tue, 03 Jun 2025 17:09:39 GMT  
		Size: 343.7 KB (343730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc049f401682dbbb9f894685070e5d9b0cba96536602e5b27d53355e49b7ff07`  
		Last Modified: Tue, 03 Jun 2025 17:09:40 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5aa038c7c32f417f8539341ca0488c6b029047e95884c31aca6a67db8edf6d`  
		Last Modified: Tue, 03 Jun 2025 17:09:44 GMT  
		Size: 28.0 MB (28035155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:705bb42260b5eea59f972664e7c390942a582e14eccee6d55684626642ea86ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24067828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9365f9d5fe47bec26b30cf0742e09127cdbdf332b439859aa91ba45333c6a47`

```dockerfile
```

-	Layers:
	-	`sha256:058b746fad09678d97175f02b1e7abf8107f3fb2e3bc0f10eafd16ab9d222711`  
		Last Modified: Tue, 03 Jun 2025 19:18:21 GMT  
		Size: 24.1 MB (24051438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f707ac09cd92d91007c2d744e1824c4fef91673244e897dbf4ffba3b70b9aa25`  
		Last Modified: Tue, 03 Jun 2025 19:18:22 GMT  
		Size: 16.4 KB (16390 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:121b240facf831793df5059cd6d046df42bf06d9ded16cba346f55bf41dca693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296564597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80210824f1e527ecf46665696e3cbe5c93641bb3761990b4c95fb47a171c91d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc24d4fa426deae9efc62cbc01e2c3bb6b1c57bb5d84b579c4f9c66cbe7134`  
		Last Modified: Tue, 03 Jun 2025 18:04:08 GMT  
		Size: 127.1 MB (127103875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cbbfd9589f7267a767b8f6ae79bf51b4c883e0a07f96139115cc4f1275110f`  
		Last Modified: Tue, 03 Jun 2025 16:23:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07caf8524de34d67d57f2d53ff16540c50ffd4a8515c4f8fb920b3a8467d9a0`  
		Last Modified: Tue, 03 Jun 2025 17:13:37 GMT  
		Size: 105.6 MB (105596816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3310082fb526791a2fd6dd8b7db9d9d2d4bedf73089c00d1c00a145b3cabd7fc`  
		Last Modified: Tue, 03 Jun 2025 17:13:30 GMT  
		Size: 343.7 KB (343730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017b43e885b2baa4a904b1d45c018b239b5e48ea556a2a972f4828509e59adb5`  
		Last Modified: Tue, 03 Jun 2025 17:13:29 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c526d3858a93fb6548b4e772344dacc787c3418de5ec76d7be75e226cb7783`  
		Last Modified: Tue, 03 Jun 2025 17:13:32 GMT  
		Size: 27.1 MB (27128379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted` - unknown; unknown

```console
$ docker pull ros@sha256:a801e0d3581e4df194579d019dc4719a205e552f088083037c09897ceafa7d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24090219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781554c1600d66dd1a189a1e6075f5571ef9ae3edd69cc423ede6e8ae7bc4940`

```dockerfile
```

-	Layers:
	-	`sha256:5ec662ecc6252c10cd12bd7a35b2658260162a954b890e8c196b6593e23874ea`  
		Last Modified: Tue, 03 Jun 2025 19:18:41 GMT  
		Size: 24.1 MB (24073692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e1726bfbe8ada67482bc5938d588ddba5fcfc4aa566f4b9bc64039d44d94bb7`  
		Last Modified: Tue, 03 Jun 2025 19:18:42 GMT  
		Size: 16.5 KB (16527 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception`

```console
$ docker pull ros@sha256:ca1add8668b7f3619328affff18c72a6160cde1d85241c51436dae77e293f8eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception` - linux; amd64

```console
$ docker pull ros@sha256:546aac0eeffa0943f6912c23af0efa62ad7b187a3d01ab71ab7b8a38faa60275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1089277886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b14c24431435142b8cf4610bb4d438cb9241e38ad7f954eec16d40b68dce6f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc922f2ce7df1733459b033fa462a421a0413670300a8b9c5c35ab7b81bc65eb`  
		Last Modified: Tue, 03 Jun 2025 16:19:30 GMT  
		Size: 683.8 KB (683816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01414ea5181d9da01a2e35570eba4ae2e37593bd21d531dfdf78f234660a7b3c`  
		Last Modified: Tue, 03 Jun 2025 16:19:32 GMT  
		Size: 6.7 MB (6745536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a09807d31167f2bd782983408d9ff7419d23b415ca575a3c7b3619165ad094`  
		Last Modified: Tue, 03 Jun 2025 16:19:31 GMT  
		Size: 94.0 KB (94039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099b8cd8b60f4a5d2476fd99e6adc027584cdef11cf59f36cc9b81b31e0ebf4`  
		Last Modified: Tue, 03 Jun 2025 17:07:48 GMT  
		Size: 132.4 MB (132407147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5402357658db93f168fcdf893f1c237364dea1ba24a8b5536a3c46e931231791`  
		Last Modified: Tue, 03 Jun 2025 16:19:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2760e6e89b71699480f8948db367864cbf4a35b90d807163f094494c524c2b1c`  
		Last Modified: Tue, 03 Jun 2025 17:09:53 GMT  
		Size: 110.2 MB (110182872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87d239340021c39b9ae17dd1ad6e2bdfa92f900c692b22d4241368481334529`  
		Last Modified: Tue, 03 Jun 2025 17:09:39 GMT  
		Size: 343.7 KB (343730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc049f401682dbbb9f894685070e5d9b0cba96536602e5b27d53355e49b7ff07`  
		Last Modified: Tue, 03 Jun 2025 17:09:40 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5aa038c7c32f417f8539341ca0488c6b029047e95884c31aca6a67db8edf6d`  
		Last Modified: Tue, 03 Jun 2025 17:09:44 GMT  
		Size: 28.0 MB (28035155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910602e69e66a1c59ee2737ab00fa9a113e8789504b8e425892e10fc3b6a2da8`  
		Last Modified: Tue, 03 Jun 2025 17:54:49 GMT  
		Size: 781.1 MB (781067576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:75e51cf47b3016df9606305344bdbba224b85c7b1f545e0575838a95f8750d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59970890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23a0780f6d3694eee9317b88ce129337339ef6a3549a513b72cc0bfb6eb08f2`

```dockerfile
```

-	Layers:
	-	`sha256:a414c569b6fccc39562dfb526c99ce7f2db815233fd7e9ce5d814f5e4182f37c`  
		Last Modified: Tue, 03 Jun 2025 19:18:31 GMT  
		Size: 60.0 MB (59961495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c40fe2cbcfe864c58bba5a3665b351fea005b02bb97d51164b7d83b9c64970ca`  
		Last Modified: Tue, 03 Jun 2025 19:18:33 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3c354eddd9d7ec8ab36f34a4477d0561ad2d833775e4fbfa7f208fc6edf5d3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.8 MB (987847888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86cfacd10f18fc3e9996f657e50e2ad5cda49f495527733cb3ae4012d6e9dc3f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc24d4fa426deae9efc62cbc01e2c3bb6b1c57bb5d84b579c4f9c66cbe7134`  
		Last Modified: Tue, 03 Jun 2025 18:04:08 GMT  
		Size: 127.1 MB (127103875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cbbfd9589f7267a767b8f6ae79bf51b4c883e0a07f96139115cc4f1275110f`  
		Last Modified: Tue, 03 Jun 2025 16:23:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07caf8524de34d67d57f2d53ff16540c50ffd4a8515c4f8fb920b3a8467d9a0`  
		Last Modified: Tue, 03 Jun 2025 17:13:37 GMT  
		Size: 105.6 MB (105596816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3310082fb526791a2fd6dd8b7db9d9d2d4bedf73089c00d1c00a145b3cabd7fc`  
		Last Modified: Tue, 03 Jun 2025 17:13:30 GMT  
		Size: 343.7 KB (343730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017b43e885b2baa4a904b1d45c018b239b5e48ea556a2a972f4828509e59adb5`  
		Last Modified: Tue, 03 Jun 2025 17:13:29 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c526d3858a93fb6548b4e772344dacc787c3418de5ec76d7be75e226cb7783`  
		Last Modified: Tue, 03 Jun 2025 17:13:32 GMT  
		Size: 27.1 MB (27128379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89f2bcdbfcaa52d114143ced1cfe5056df821a0ecd09b105c9828d99e5d2ce8`  
		Last Modified: Tue, 03 Jun 2025 19:21:00 GMT  
		Size: 691.3 MB (691283291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception` - unknown; unknown

```console
$ docker pull ros@sha256:454ac3b487aa611233064c701fb45f09e9dedfb901c5137d8cf559ad838f263a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59922635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5724da4991e8d76e8566bbc9e4487bcfe4ef768ea4b8791373e2d950562b735a`

```dockerfile
```

-	Layers:
	-	`sha256:e534fc4de8bbb3018d38148f8d77f8871e56d94decd08af90f16170c443541d5`  
		Last Modified: Tue, 03 Jun 2025 19:20:00 GMT  
		Size: 59.9 MB (59913160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a75af4b2c0c88922b34ef647d1824949542ef9782eda38647dba5297011e6110`  
		Last Modified: Tue, 03 Jun 2025 19:20:02 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-perception-noble`

```console
$ docker pull ros@sha256:ca1add8668b7f3619328affff18c72a6160cde1d85241c51436dae77e293f8eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:546aac0eeffa0943f6912c23af0efa62ad7b187a3d01ab71ab7b8a38faa60275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1089277886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b14c24431435142b8cf4610bb4d438cb9241e38ad7f954eec16d40b68dce6f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc922f2ce7df1733459b033fa462a421a0413670300a8b9c5c35ab7b81bc65eb`  
		Last Modified: Tue, 03 Jun 2025 16:19:30 GMT  
		Size: 683.8 KB (683816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01414ea5181d9da01a2e35570eba4ae2e37593bd21d531dfdf78f234660a7b3c`  
		Last Modified: Tue, 03 Jun 2025 16:19:32 GMT  
		Size: 6.7 MB (6745536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a09807d31167f2bd782983408d9ff7419d23b415ca575a3c7b3619165ad094`  
		Last Modified: Tue, 03 Jun 2025 16:19:31 GMT  
		Size: 94.0 KB (94039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099b8cd8b60f4a5d2476fd99e6adc027584cdef11cf59f36cc9b81b31e0ebf4`  
		Last Modified: Tue, 03 Jun 2025 17:07:48 GMT  
		Size: 132.4 MB (132407147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5402357658db93f168fcdf893f1c237364dea1ba24a8b5536a3c46e931231791`  
		Last Modified: Tue, 03 Jun 2025 16:19:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2760e6e89b71699480f8948db367864cbf4a35b90d807163f094494c524c2b1c`  
		Last Modified: Tue, 03 Jun 2025 17:09:53 GMT  
		Size: 110.2 MB (110182872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87d239340021c39b9ae17dd1ad6e2bdfa92f900c692b22d4241368481334529`  
		Last Modified: Tue, 03 Jun 2025 17:09:39 GMT  
		Size: 343.7 KB (343730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc049f401682dbbb9f894685070e5d9b0cba96536602e5b27d53355e49b7ff07`  
		Last Modified: Tue, 03 Jun 2025 17:09:40 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5aa038c7c32f417f8539341ca0488c6b029047e95884c31aca6a67db8edf6d`  
		Last Modified: Tue, 03 Jun 2025 17:09:44 GMT  
		Size: 28.0 MB (28035155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910602e69e66a1c59ee2737ab00fa9a113e8789504b8e425892e10fc3b6a2da8`  
		Last Modified: Tue, 03 Jun 2025 17:54:49 GMT  
		Size: 781.1 MB (781067576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:75e51cf47b3016df9606305344bdbba224b85c7b1f545e0575838a95f8750d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59970890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23a0780f6d3694eee9317b88ce129337339ef6a3549a513b72cc0bfb6eb08f2`

```dockerfile
```

-	Layers:
	-	`sha256:a414c569b6fccc39562dfb526c99ce7f2db815233fd7e9ce5d814f5e4182f37c`  
		Last Modified: Tue, 03 Jun 2025 19:18:31 GMT  
		Size: 60.0 MB (59961495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c40fe2cbcfe864c58bba5a3665b351fea005b02bb97d51164b7d83b9c64970ca`  
		Last Modified: Tue, 03 Jun 2025 19:18:33 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3c354eddd9d7ec8ab36f34a4477d0561ad2d833775e4fbfa7f208fc6edf5d3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.8 MB (987847888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86cfacd10f18fc3e9996f657e50e2ad5cda49f495527733cb3ae4012d6e9dc3f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-perception=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc24d4fa426deae9efc62cbc01e2c3bb6b1c57bb5d84b579c4f9c66cbe7134`  
		Last Modified: Tue, 03 Jun 2025 18:04:08 GMT  
		Size: 127.1 MB (127103875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cbbfd9589f7267a767b8f6ae79bf51b4c883e0a07f96139115cc4f1275110f`  
		Last Modified: Tue, 03 Jun 2025 16:23:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07caf8524de34d67d57f2d53ff16540c50ffd4a8515c4f8fb920b3a8467d9a0`  
		Last Modified: Tue, 03 Jun 2025 17:13:37 GMT  
		Size: 105.6 MB (105596816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3310082fb526791a2fd6dd8b7db9d9d2d4bedf73089c00d1c00a145b3cabd7fc`  
		Last Modified: Tue, 03 Jun 2025 17:13:30 GMT  
		Size: 343.7 KB (343730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017b43e885b2baa4a904b1d45c018b239b5e48ea556a2a972f4828509e59adb5`  
		Last Modified: Tue, 03 Jun 2025 17:13:29 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c526d3858a93fb6548b4e772344dacc787c3418de5ec76d7be75e226cb7783`  
		Last Modified: Tue, 03 Jun 2025 17:13:32 GMT  
		Size: 27.1 MB (27128379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89f2bcdbfcaa52d114143ced1cfe5056df821a0ecd09b105c9828d99e5d2ce8`  
		Last Modified: Tue, 03 Jun 2025 19:21:00 GMT  
		Size: 691.3 MB (691283291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:454ac3b487aa611233064c701fb45f09e9dedfb901c5137d8cf559ad838f263a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59922635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5724da4991e8d76e8566bbc9e4487bcfe4ef768ea4b8791373e2d950562b735a`

```dockerfile
```

-	Layers:
	-	`sha256:e534fc4de8bbb3018d38148f8d77f8871e56d94decd08af90f16170c443541d5`  
		Last Modified: Tue, 03 Jun 2025 19:20:00 GMT  
		Size: 59.9 MB (59913160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a75af4b2c0c88922b34ef647d1824949542ef9782eda38647dba5297011e6110`  
		Last Modified: Tue, 03 Jun 2025 19:20:02 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base`

```console
$ docker pull ros@sha256:0c933e161f6434be229bb5c1d3fd9442b0bfda562429731046500994337b4d16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:8975664720534fb178de9c6223880f527240bf202042ec2d9bda4696c8ca48ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308210310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0289388d8db682cbfe62c775cf4d0a1f74f08bc2f0b24316e5d9cf58db72dffb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc922f2ce7df1733459b033fa462a421a0413670300a8b9c5c35ab7b81bc65eb`  
		Last Modified: Tue, 03 Jun 2025 16:19:30 GMT  
		Size: 683.8 KB (683816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01414ea5181d9da01a2e35570eba4ae2e37593bd21d531dfdf78f234660a7b3c`  
		Last Modified: Tue, 03 Jun 2025 16:19:32 GMT  
		Size: 6.7 MB (6745536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a09807d31167f2bd782983408d9ff7419d23b415ca575a3c7b3619165ad094`  
		Last Modified: Tue, 03 Jun 2025 16:19:31 GMT  
		Size: 94.0 KB (94039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099b8cd8b60f4a5d2476fd99e6adc027584cdef11cf59f36cc9b81b31e0ebf4`  
		Last Modified: Tue, 03 Jun 2025 17:07:48 GMT  
		Size: 132.4 MB (132407147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5402357658db93f168fcdf893f1c237364dea1ba24a8b5536a3c46e931231791`  
		Last Modified: Tue, 03 Jun 2025 16:19:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2760e6e89b71699480f8948db367864cbf4a35b90d807163f094494c524c2b1c`  
		Last Modified: Tue, 03 Jun 2025 17:09:53 GMT  
		Size: 110.2 MB (110182872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87d239340021c39b9ae17dd1ad6e2bdfa92f900c692b22d4241368481334529`  
		Last Modified: Tue, 03 Jun 2025 17:09:39 GMT  
		Size: 343.7 KB (343730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc049f401682dbbb9f894685070e5d9b0cba96536602e5b27d53355e49b7ff07`  
		Last Modified: Tue, 03 Jun 2025 17:09:40 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5aa038c7c32f417f8539341ca0488c6b029047e95884c31aca6a67db8edf6d`  
		Last Modified: Tue, 03 Jun 2025 17:09:44 GMT  
		Size: 28.0 MB (28035155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:705bb42260b5eea59f972664e7c390942a582e14eccee6d55684626642ea86ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24067828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9365f9d5fe47bec26b30cf0742e09127cdbdf332b439859aa91ba45333c6a47`

```dockerfile
```

-	Layers:
	-	`sha256:058b746fad09678d97175f02b1e7abf8107f3fb2e3bc0f10eafd16ab9d222711`  
		Last Modified: Tue, 03 Jun 2025 19:18:21 GMT  
		Size: 24.1 MB (24051438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f707ac09cd92d91007c2d744e1824c4fef91673244e897dbf4ffba3b70b9aa25`  
		Last Modified: Tue, 03 Jun 2025 19:18:22 GMT  
		Size: 16.4 KB (16390 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:121b240facf831793df5059cd6d046df42bf06d9ded16cba346f55bf41dca693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296564597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80210824f1e527ecf46665696e3cbe5c93641bb3761990b4c95fb47a171c91d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc24d4fa426deae9efc62cbc01e2c3bb6b1c57bb5d84b579c4f9c66cbe7134`  
		Last Modified: Tue, 03 Jun 2025 18:04:08 GMT  
		Size: 127.1 MB (127103875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cbbfd9589f7267a767b8f6ae79bf51b4c883e0a07f96139115cc4f1275110f`  
		Last Modified: Tue, 03 Jun 2025 16:23:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07caf8524de34d67d57f2d53ff16540c50ffd4a8515c4f8fb920b3a8467d9a0`  
		Last Modified: Tue, 03 Jun 2025 17:13:37 GMT  
		Size: 105.6 MB (105596816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3310082fb526791a2fd6dd8b7db9d9d2d4bedf73089c00d1c00a145b3cabd7fc`  
		Last Modified: Tue, 03 Jun 2025 17:13:30 GMT  
		Size: 343.7 KB (343730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017b43e885b2baa4a904b1d45c018b239b5e48ea556a2a972f4828509e59adb5`  
		Last Modified: Tue, 03 Jun 2025 17:13:29 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c526d3858a93fb6548b4e772344dacc787c3418de5ec76d7be75e226cb7783`  
		Last Modified: Tue, 03 Jun 2025 17:13:32 GMT  
		Size: 27.1 MB (27128379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:a801e0d3581e4df194579d019dc4719a205e552f088083037c09897ceafa7d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24090219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781554c1600d66dd1a189a1e6075f5571ef9ae3edd69cc423ede6e8ae7bc4940`

```dockerfile
```

-	Layers:
	-	`sha256:5ec662ecc6252c10cd12bd7a35b2658260162a954b890e8c196b6593e23874ea`  
		Last Modified: Tue, 03 Jun 2025 19:18:41 GMT  
		Size: 24.1 MB (24073692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e1726bfbe8ada67482bc5938d588ddba5fcfc4aa566f4b9bc64039d44d94bb7`  
		Last Modified: Tue, 03 Jun 2025 19:18:42 GMT  
		Size: 16.5 KB (16527 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-base-noble`

```console
$ docker pull ros@sha256:0c933e161f6434be229bb5c1d3fd9442b0bfda562429731046500994337b4d16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:8975664720534fb178de9c6223880f527240bf202042ec2d9bda4696c8ca48ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308210310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0289388d8db682cbfe62c775cf4d0a1f74f08bc2f0b24316e5d9cf58db72dffb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc922f2ce7df1733459b033fa462a421a0413670300a8b9c5c35ab7b81bc65eb`  
		Last Modified: Tue, 03 Jun 2025 16:19:30 GMT  
		Size: 683.8 KB (683816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01414ea5181d9da01a2e35570eba4ae2e37593bd21d531dfdf78f234660a7b3c`  
		Last Modified: Tue, 03 Jun 2025 16:19:32 GMT  
		Size: 6.7 MB (6745536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a09807d31167f2bd782983408d9ff7419d23b415ca575a3c7b3619165ad094`  
		Last Modified: Tue, 03 Jun 2025 16:19:31 GMT  
		Size: 94.0 KB (94039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099b8cd8b60f4a5d2476fd99e6adc027584cdef11cf59f36cc9b81b31e0ebf4`  
		Last Modified: Tue, 03 Jun 2025 17:07:48 GMT  
		Size: 132.4 MB (132407147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5402357658db93f168fcdf893f1c237364dea1ba24a8b5536a3c46e931231791`  
		Last Modified: Tue, 03 Jun 2025 16:19:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2760e6e89b71699480f8948db367864cbf4a35b90d807163f094494c524c2b1c`  
		Last Modified: Tue, 03 Jun 2025 17:09:53 GMT  
		Size: 110.2 MB (110182872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87d239340021c39b9ae17dd1ad6e2bdfa92f900c692b22d4241368481334529`  
		Last Modified: Tue, 03 Jun 2025 17:09:39 GMT  
		Size: 343.7 KB (343730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc049f401682dbbb9f894685070e5d9b0cba96536602e5b27d53355e49b7ff07`  
		Last Modified: Tue, 03 Jun 2025 17:09:40 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5aa038c7c32f417f8539341ca0488c6b029047e95884c31aca6a67db8edf6d`  
		Last Modified: Tue, 03 Jun 2025 17:09:44 GMT  
		Size: 28.0 MB (28035155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:705bb42260b5eea59f972664e7c390942a582e14eccee6d55684626642ea86ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24067828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9365f9d5fe47bec26b30cf0742e09127cdbdf332b439859aa91ba45333c6a47`

```dockerfile
```

-	Layers:
	-	`sha256:058b746fad09678d97175f02b1e7abf8107f3fb2e3bc0f10eafd16ab9d222711`  
		Last Modified: Tue, 03 Jun 2025 19:18:21 GMT  
		Size: 24.1 MB (24051438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f707ac09cd92d91007c2d744e1824c4fef91673244e897dbf4ffba3b70b9aa25`  
		Last Modified: Tue, 03 Jun 2025 19:18:22 GMT  
		Size: 16.4 KB (16390 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:121b240facf831793df5059cd6d046df42bf06d9ded16cba346f55bf41dca693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296564597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80210824f1e527ecf46665696e3cbe5c93641bb3761990b4c95fb47a171c91d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 23 May 2025 20:53:19 GMT
ARG RELEASE
# Fri, 23 May 2025 20:53:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 20:53:19 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 23 May 2025 20:53:19 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Fri, 23 May 2025 20:53:19 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 23 May 2025 20:53:19 GMT
ENV ROS_DISTRO=kilted
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 23 May 2025 20:53:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 23 May 2025 20:53:19 GMT
CMD ["bash"]
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Fri, 23 May 2025 20:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-base=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc24d4fa426deae9efc62cbc01e2c3bb6b1c57bb5d84b579c4f9c66cbe7134`  
		Last Modified: Tue, 03 Jun 2025 18:04:08 GMT  
		Size: 127.1 MB (127103875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cbbfd9589f7267a767b8f6ae79bf51b4c883e0a07f96139115cc4f1275110f`  
		Last Modified: Tue, 03 Jun 2025 16:23:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07caf8524de34d67d57f2d53ff16540c50ffd4a8515c4f8fb920b3a8467d9a0`  
		Last Modified: Tue, 03 Jun 2025 17:13:37 GMT  
		Size: 105.6 MB (105596816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3310082fb526791a2fd6dd8b7db9d9d2d4bedf73089c00d1c00a145b3cabd7fc`  
		Last Modified: Tue, 03 Jun 2025 17:13:30 GMT  
		Size: 343.7 KB (343730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017b43e885b2baa4a904b1d45c018b239b5e48ea556a2a972f4828509e59adb5`  
		Last Modified: Tue, 03 Jun 2025 17:13:29 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c526d3858a93fb6548b4e772344dacc787c3418de5ec76d7be75e226cb7783`  
		Last Modified: Tue, 03 Jun 2025 17:13:32 GMT  
		Size: 27.1 MB (27128379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:a801e0d3581e4df194579d019dc4719a205e552f088083037c09897ceafa7d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24090219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781554c1600d66dd1a189a1e6075f5571ef9ae3edd69cc423ede6e8ae7bc4940`

```dockerfile
```

-	Layers:
	-	`sha256:5ec662ecc6252c10cd12bd7a35b2658260162a954b890e8c196b6593e23874ea`  
		Last Modified: Tue, 03 Jun 2025 19:18:41 GMT  
		Size: 24.1 MB (24073692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e1726bfbe8ada67482bc5938d588ddba5fcfc4aa566f4b9bc64039d44d94bb7`  
		Last Modified: Tue, 03 Jun 2025 19:18:42 GMT  
		Size: 16.5 KB (16527 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core`

```console
$ docker pull ros@sha256:d131921dd52cf6a177e6db8892fb041c6ee0ef4603fa0809bfd59902afeb4dba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:cb608d2f68918df824d96d83c20146fee2bede581465c4e783ca32d357098230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.6 MB (169646071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8e71eada499702c83f9670e3233065771df8e92f4cac83824560b6c9e81880`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=kilted
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc922f2ce7df1733459b033fa462a421a0413670300a8b9c5c35ab7b81bc65eb`  
		Last Modified: Tue, 03 Jun 2025 16:19:30 GMT  
		Size: 683.8 KB (683816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01414ea5181d9da01a2e35570eba4ae2e37593bd21d531dfdf78f234660a7b3c`  
		Last Modified: Tue, 03 Jun 2025 16:19:32 GMT  
		Size: 6.7 MB (6745536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a09807d31167f2bd782983408d9ff7419d23b415ca575a3c7b3619165ad094`  
		Last Modified: Tue, 03 Jun 2025 16:19:31 GMT  
		Size: 94.0 KB (94039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099b8cd8b60f4a5d2476fd99e6adc027584cdef11cf59f36cc9b81b31e0ebf4`  
		Last Modified: Tue, 03 Jun 2025 17:07:48 GMT  
		Size: 132.4 MB (132407147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5402357658db93f168fcdf893f1c237364dea1ba24a8b5536a3c46e931231791`  
		Last Modified: Tue, 03 Jun 2025 16:19:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:c7b61c091dc4fcfd58ce8e922b63e10b8c90d8488c76056485db25420bd94cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17989768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02400998c0251977cfb851cccc7cdd553c3480520d7f4a578aa70281915ba2b6`

```dockerfile
```

-	Layers:
	-	`sha256:e61d4a4bb340ade677faf130dbc8dff71d529970379d850b04f818212d83abb8`  
		Last Modified: Tue, 03 Jun 2025 19:18:33 GMT  
		Size: 18.0 MB (17975116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6274e98d7ca40d6772020d7c9c0fc7a4c2957f6378042989997974563309ea1`  
		Last Modified: Tue, 03 Jun 2025 19:18:34 GMT  
		Size: 14.7 KB (14652 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3a59e1d3bf002d97f35c4788b0f9607df7c543f799249e1d949d14f6860ce19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163493213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25b7cb805ae659154b95231eb8d806ccd78235d35fc4c5f682eb45f33293e23`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=kilted
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc24d4fa426deae9efc62cbc01e2c3bb6b1c57bb5d84b579c4f9c66cbe7134`  
		Last Modified: Tue, 03 Jun 2025 18:04:08 GMT  
		Size: 127.1 MB (127103875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cbbfd9589f7267a767b8f6ae79bf51b4c883e0a07f96139115cc4f1275110f`  
		Last Modified: Tue, 03 Jun 2025 16:23:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:797e08c3ae30c3fc3edd850cf027e88c135693cb5eb5d5624d8c96710c6f620e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17963899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aab3eedf5d659abc219852bc29d1fc0c08cd0a6b5d71400cb8967506cb9578a`

```dockerfile
```

-	Layers:
	-	`sha256:d877afd5470e46e3789d10198445355641123b425d04a55cfeb2261065a7e1b8`  
		Last Modified: Tue, 03 Jun 2025 19:18:48 GMT  
		Size: 17.9 MB (17949122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e596059d56191b71959bfee069398446b83b1db2466149cd9a2a75f067e379`  
		Last Modified: Tue, 03 Jun 2025 19:18:49 GMT  
		Size: 14.8 KB (14777 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:kilted-ros-core-noble`

```console
$ docker pull ros@sha256:d131921dd52cf6a177e6db8892fb041c6ee0ef4603fa0809bfd59902afeb4dba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:kilted-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:cb608d2f68918df824d96d83c20146fee2bede581465c4e783ca32d357098230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.6 MB (169646071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8e71eada499702c83f9670e3233065771df8e92f4cac83824560b6c9e81880`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=kilted
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc922f2ce7df1733459b033fa462a421a0413670300a8b9c5c35ab7b81bc65eb`  
		Last Modified: Tue, 03 Jun 2025 16:19:30 GMT  
		Size: 683.8 KB (683816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01414ea5181d9da01a2e35570eba4ae2e37593bd21d531dfdf78f234660a7b3c`  
		Last Modified: Tue, 03 Jun 2025 16:19:32 GMT  
		Size: 6.7 MB (6745536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a09807d31167f2bd782983408d9ff7419d23b415ca575a3c7b3619165ad094`  
		Last Modified: Tue, 03 Jun 2025 16:19:31 GMT  
		Size: 94.0 KB (94039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099b8cd8b60f4a5d2476fd99e6adc027584cdef11cf59f36cc9b81b31e0ebf4`  
		Last Modified: Tue, 03 Jun 2025 17:07:48 GMT  
		Size: 132.4 MB (132407147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5402357658db93f168fcdf893f1c237364dea1ba24a8b5536a3c46e931231791`  
		Last Modified: Tue, 03 Jun 2025 16:19:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:c7b61c091dc4fcfd58ce8e922b63e10b8c90d8488c76056485db25420bd94cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17989768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02400998c0251977cfb851cccc7cdd553c3480520d7f4a578aa70281915ba2b6`

```dockerfile
```

-	Layers:
	-	`sha256:e61d4a4bb340ade677faf130dbc8dff71d529970379d850b04f818212d83abb8`  
		Last Modified: Tue, 03 Jun 2025 19:18:33 GMT  
		Size: 18.0 MB (17975116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6274e98d7ca40d6772020d7c9c0fc7a4c2957f6378042989997974563309ea1`  
		Last Modified: Tue, 03 Jun 2025 19:18:34 GMT  
		Size: 14.7 KB (14652 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:kilted-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3a59e1d3bf002d97f35c4788b0f9607df7c543f799249e1d949d14f6860ce19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163493213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25b7cb805ae659154b95231eb8d806ccd78235d35fc4c5f682eb45f33293e23`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=kilted
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kilted-ros-core=0.12.0-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc24d4fa426deae9efc62cbc01e2c3bb6b1c57bb5d84b579c4f9c66cbe7134`  
		Last Modified: Tue, 03 Jun 2025 18:04:08 GMT  
		Size: 127.1 MB (127103875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cbbfd9589f7267a767b8f6ae79bf51b4c883e0a07f96139115cc4f1275110f`  
		Last Modified: Tue, 03 Jun 2025 16:23:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:kilted-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:797e08c3ae30c3fc3edd850cf027e88c135693cb5eb5d5624d8c96710c6f620e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17963899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aab3eedf5d659abc219852bc29d1fc0c08cd0a6b5d71400cb8967506cb9578a`

```dockerfile
```

-	Layers:
	-	`sha256:d877afd5470e46e3789d10198445355641123b425d04a55cfeb2261065a7e1b8`  
		Last Modified: Tue, 03 Jun 2025 19:18:48 GMT  
		Size: 17.9 MB (17949122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e596059d56191b71959bfee069398446b83b1db2466149cd9a2a75f067e379`  
		Last Modified: Tue, 03 Jun 2025 19:18:49 GMT  
		Size: 14.8 KB (14777 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:latest`

```console
$ docker pull ros@sha256:026816c588cc465b3838721edd970a66827bd6a4618e49969d8e5dfa977c660e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:1b01c30c300bf57e1e429e466c4d88d9c9beb1298fd3ef5c4fa18b928ad67b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295661118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210ea2138a721c7166913e5c06fcde48d532753cfbeed14356284de4d7d28500`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8869d62bea26cae8ab2f85ad14f208e76c7f463db4bd3681f8df7f2db1aa70`  
		Last Modified: Tue, 03 Jun 2025 17:07:43 GMT  
		Size: 683.8 KB (683775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdda66f6933d387b046b7278b307c4a50b054916c1d33878ff0ea47b11ea288`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 6.7 MB (6745523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4f7f179852ccfe99b50eece2eff5ed1fc42d17227c23e8500f4e1f0366c8b6`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 94.0 KB (94050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc086dd908beb9598940d79e43ce727c4d66a6c4c9a83ef3dbc532efd3ac556`  
		Last Modified: Tue, 03 Jun 2025 17:07:52 GMT  
		Size: 119.9 MB (119908702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d3aa09250ecc0281476638d2d5996ff648156fed57cfa9bebf82c4ebf962b0`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d996ba9b4edd88c0a1218a4f6b9e82aacbb4cd9c0f44a02d8052de578268d1c`  
		Last Modified: Tue, 03 Jun 2025 17:09:50 GMT  
		Size: 110.2 MB (110179284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c6c6b25ec0196eb5046ea65df46a24cb5bb13006dc63bca159185fe044eb30`  
		Last Modified: Tue, 03 Jun 2025 17:09:34 GMT  
		Size: 365.5 KB (365545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943b1a661f69478625db6adb1761fd8f1ccec92717bd44cdfe2b5a06e75f2cb0`  
		Last Modified: Tue, 03 Jun 2025 17:09:32 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb6de655debbb5b7b335e7467749f8aa7e61315197004beb93d7c89b07a9182`  
		Last Modified: Tue, 03 Jun 2025 17:09:38 GMT  
		Size: 28.0 MB (27966270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:208e9324840cc54d335b55663183bc50f2177a5052f52dc053b117e3023a411c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23975352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5c00592be208c22b3e14f803385c3ea66ea35f32064bfb4a1059370ee90fe1`

```dockerfile
```

-	Layers:
	-	`sha256:d07942c31bff532d3129903744c4a7e2d332dc1cc78361cd9214daad305739c5`  
		Last Modified: Tue, 03 Jun 2025 19:17:53 GMT  
		Size: 24.0 MB (23958688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33a9c88c866c53e68ec30b286a828168dfb46d32d402dcf2f9186da2a977e8f3`  
		Last Modified: Tue, 03 Jun 2025 19:17:54 GMT  
		Size: 16.7 KB (16664 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0e1497ee844bb1ff2078ff00b005c05b57d0c42a669832c2c5c1d65f39fba896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284104470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff0eda86dadd0da69f7273b932e2fe6608e9fef9f2e9c8e39aa228b102838ca`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Apr 2024 21:39:21 GMT
ARG RELEASE
# Tue, 30 Apr 2024 21:39:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Apr 2024 21:39:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Apr 2024 21:39:21 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["/bin/bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LANG=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV LC_ALL=C.UTF-8
# Tue, 30 Apr 2024 21:39:21 GMT
ENV ROS_DISTRO=jazzy
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 30 Apr 2024 21:39:21 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Tue, 30 Apr 2024 21:39:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ba7c57b0ec01c10fc7cf681ee099c37c987498c25b1b8cb4a29128ced96907`  
		Last Modified: Tue, 03 Jun 2025 16:22:11 GMT  
		Size: 114.7 MB (114689282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737f79a5b3df57a487c18df3ed8e9513b75c70fe5101db46ee91d23db81aada5`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedc0bf39755013a910d8ad1b32b6f3f9b9312ce259a79006dd3607186145d52`  
		Last Modified: Tue, 03 Jun 2025 17:12:16 GMT  
		Size: 105.6 MB (105593170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94701b4069614f2698aa75959641413e64967923478ef666610963cbac10ccd3`  
		Last Modified: Tue, 03 Jun 2025 17:12:06 GMT  
		Size: 365.5 KB (365548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7434caed03c758a0b9a196d1551d0566ab0ec6c0e6bf60c1c9f8781f89c879a`  
		Last Modified: Tue, 03 Jun 2025 17:12:06 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781027cdaf47969f8306b57e6d33eaaeb74013c708798b7c6c7288103ba9595`  
		Last Modified: Tue, 03 Jun 2025 17:12:09 GMT  
		Size: 27.1 MB (27064676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:latest` - unknown; unknown

```console
$ docker pull ros@sha256:2afa6387c997352b229bb14d702b93943f67478b00f4e36911328585c5ef04dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23997767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9d366cc100fcea3333bfcf3e3be89217240945e35a7abd45aace3e7f23d494`

```dockerfile
```

-	Layers:
	-	`sha256:b08db0fa85af9540e10577f9163cfe79c3de70f554f78301db879d7dec8c42df`  
		Last Modified: Tue, 03 Jun 2025 19:18:16 GMT  
		Size: 24.0 MB (23980954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3701caf148a35f3d36eb094ad32ebfeb5ce8986d19a04d29a6e940c9df59d93`  
		Last Modified: Tue, 03 Jun 2025 19:18:17 GMT  
		Size: 16.8 KB (16813 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic`

```console
$ docker pull ros@sha256:72b8bc59035dc0a5b8e07aae28c16caa84192971d72d207c72ed734fb1d5e97d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:4f01fa743be43da0e14ddf2ac29b5118d9c0eb4057c9761c13303b8a52fa9c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.3 MB (460272792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607ca0f020489b85d74ef5ae2f0ce8e901813af48008b0a622fc06cd41bf0d1b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da4792f7f416db06c00bc26bb845d00bd1c6f16f3e10a4c7d0031c91656aa3e`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 1.2 MB (1194841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20358ca2eb5aafdeb52607c52f0c03ee909a919235fc1041db00d58da1c59b6`  
		Last Modified: Mon, 09 Jun 2025 21:17:15 GMT  
		Size: 10.0 MB (9982583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dce350d6ea44ccf7fac3a7bdda0989aca3a6b72ffbfc14104e3b18810c2de33`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 4.0 KB (4045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ca0507171d76ea79443c6b48e8e4038c3555f8ca12aef4cd82ca0ca7a43786`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cc10980325859d6423bbc515001cb577760dc73999bb2e18e811a24877c5cb`  
		Last Modified: Mon, 09 Jun 2025 21:38:06 GMT  
		Size: 370.5 MB (370502304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6932d16c264574201be5a55ba79dd248dab8a2a0a32b8cdf30af3e1c5e86f806`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342ecf093a9124f383e5acc3a78d21be9e4f20515e24b2e0c8169a199d845c1c`  
		Last Modified: Mon, 09 Jun 2025 21:39:32 GMT  
		Size: 49.8 MB (49754505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c240714a1b7806b225c5f9dde0ab272ceaa47a40ac7b752cbe0370bbaf3976e`  
		Last Modified: Mon, 09 Jun 2025 21:39:27 GMT  
		Size: 348.0 KB (348012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0451913b17a56844e9c92165120da313434cba935ddb3353799081a241b27c`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 975.6 KB (975633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:c081b974b2e84ce8ba0066b91664245b12a4217c7bf3121b382cfffea9522495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31302280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3aba0ed8be28e189623a99f7b2b073874abfb184f1742a959bb3bc8c2e327c`

```dockerfile
```

-	Layers:
	-	`sha256:f743f4f945c8627b2c94cb0fb0f577742f5489ec6d509d3d8ce4a38f0ba03a06`  
		Last Modified: Mon, 09 Jun 2025 22:18:34 GMT  
		Size: 31.3 MB (31288594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5145030147e7ed7e8d1f4d7fa5d65e7f95d250e533960a796d0481506eb56d0`  
		Last Modified: Mon, 09 Jun 2025 22:18:34 GMT  
		Size: 13.7 KB (13686 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:31818b9103a0d47738690ff8eaacb928520bf92017fc1c6c4d5cdad9261fa1c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292791861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae49cc2167e0598b690cd174a01b8457d8d2f9eca339bedb7b77d4d1c87b38b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Thu, 08 May 2025 17:24:17 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfcc4cfce76b5bf1c5a2d77d213c53e381bd6af934ace80b7dd575fae26fbc2`  
		Last Modified: Mon, 09 Jun 2025 21:26:48 GMT  
		Size: 1.2 MB (1194843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbedf4f0754ca72166025a791ca6d481ebf5eabf3a71098223375b9e239ab5e`  
		Last Modified: Mon, 09 Jun 2025 21:26:50 GMT  
		Size: 8.5 MB (8495172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b93f56f8bb23cd9397a52b8507218a13ec5c99454df623bcb512756c0e3b65c`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d92492254010b5a5b3b8e25ef8ec55aa5095c585ca3229bc0eeef8d85b8360`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24987496e81c5b0ad1b96e1e2aa860aa62af52099656d4f90b854a1ea854ef88`  
		Last Modified: Mon, 09 Jun 2025 22:21:50 GMT  
		Size: 228.4 MB (228378250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d5d7d2be5c7ee349e5b07c644259548f6e8ab647d692c695bb392c00cc8ee0`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c0306cc8cd95c4d090ded2ccdb527b61a1fa1b77279dcd9d99caee9665231f`  
		Last Modified: Mon, 09 Jun 2025 21:50:36 GMT  
		Size: 29.8 MB (29845900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60f895b7132ec2355664c60f7339ba7673f3bc1e481242742ec7c0a792f400b`  
		Last Modified: Mon, 09 Jun 2025 21:50:35 GMT  
		Size: 348.0 KB (348006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f31d7a3f2c23ccacb5df0f3b9478367ec6c1b2527626899c0d3c6c0386685a1`  
		Last Modified: Mon, 09 Jun 2025 21:50:35 GMT  
		Size: 901.1 KB (901107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:02961273e4e5adbf0edbaa55e408869e8a76c8e89bfb3e44cc748d1d47775f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30012724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c4c950bdfdef4c337e4fde12825560ac2c5ab3ed6b230fc9554bed950d65da`

```dockerfile
```

-	Layers:
	-	`sha256:38dd0a9571edf6b5307ea32643bbb13e20f6963b38e69461f06341aa9100f589`  
		Last Modified: Mon, 09 Jun 2025 22:19:07 GMT  
		Size: 30.0 MB (29998944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35dd4a9dda0678fcd4bb804ba29e39fb44b9355c78cd00f096b6a69c4da32903`  
		Last Modified: Mon, 09 Jun 2025 22:19:08 GMT  
		Size: 13.8 KB (13780 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c84e573d2f2beb679ea5b03015eb2876e9962657c23d0073e4ae9d7ba41c4700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.7 MB (443727066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547fd10070fcb8190d04b6923e9f20800c6097d062870239d07a40a140316bc0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfbcdfd0b57613941270f9d51dd852e2113c510314bc16442dac6b7ccd93bb4`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 4.1 KB (4051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85112d048ca69cba46cedbe7609be6b1388da46a96c5f25f3074b3d03ed5cada`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f86eac5764b45f84c9f74da912d260c33bea9dce19480b68f6d9e8d5c6b757`  
		Last Modified: Mon, 09 Jun 2025 22:32:16 GMT  
		Size: 361.4 MB (361381917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9cab4e76df8ec2a87814d4b7ac61519a9a8786d329cee9df51b06f8a16ae76`  
		Last Modified: Mon, 09 Jun 2025 21:45:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8965a1cbf95bb1c0a0fdbf2e84e831095239fa093c88df83b4813cd360bf61d`  
		Last Modified: Mon, 09 Jun 2025 23:22:48 GMT  
		Size: 44.0 MB (44025805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96c9101971e6e544417587498e848cd906a5072fe880df3a870c6735f518bf5`  
		Last Modified: Mon, 09 Jun 2025 22:23:05 GMT  
		Size: 348.0 KB (348026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679ea0da59a1556edaba85a9966e6296db829e778f72481bfbe4a9859f6c4c2`  
		Last Modified: Mon, 09 Jun 2025 22:23:09 GMT  
		Size: 954.7 KB (954730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:80cd2330c77e06fd24483ecb5250a44626836ec998f0a2b60031e9390d36af50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31126389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058ada81e83a7ad06c91ec5bf8d1fbbf0c28599b8f50e4b6383e22791f7165ed`

```dockerfile
```

-	Layers:
	-	`sha256:24ae88e3a88ca1e8f5519b268d395f9ce7a38287005086ed99b5e5abcdc37593`  
		Last Modified: Tue, 10 Jun 2025 01:18:32 GMT  
		Size: 31.1 MB (31112581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:525a91b30b35d8653b39c21d12dd3de1790c39fab37b1945e7e5c58d69fec318`  
		Last Modified: Tue, 10 Jun 2025 01:18:34 GMT  
		Size: 13.8 KB (13808 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:32370c500818eaefb8491d7d85e9f415541b7f4bfec8afc59c4240653e7a77e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:ef5fdebeaa881604208c067f96d42b61331825309e559c093e24e9e89c7d3d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **953.0 MB (953023137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d1e228d78fdb8d64b885b3a15a6b05732187206079883723b81f3dc87f7eb7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da4792f7f416db06c00bc26bb845d00bd1c6f16f3e10a4c7d0031c91656aa3e`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 1.2 MB (1194841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20358ca2eb5aafdeb52607c52f0c03ee909a919235fc1041db00d58da1c59b6`  
		Last Modified: Mon, 09 Jun 2025 21:17:15 GMT  
		Size: 10.0 MB (9982583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dce350d6ea44ccf7fac3a7bdda0989aca3a6b72ffbfc14104e3b18810c2de33`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 4.0 KB (4045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ca0507171d76ea79443c6b48e8e4038c3555f8ca12aef4cd82ca0ca7a43786`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cc10980325859d6423bbc515001cb577760dc73999bb2e18e811a24877c5cb`  
		Last Modified: Mon, 09 Jun 2025 21:38:06 GMT  
		Size: 370.5 MB (370502304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6932d16c264574201be5a55ba79dd248dab8a2a0a32b8cdf30af3e1c5e86f806`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342ecf093a9124f383e5acc3a78d21be9e4f20515e24b2e0c8169a199d845c1c`  
		Last Modified: Mon, 09 Jun 2025 21:39:32 GMT  
		Size: 49.8 MB (49754505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c240714a1b7806b225c5f9dde0ab272ceaa47a40ac7b752cbe0370bbaf3976e`  
		Last Modified: Mon, 09 Jun 2025 21:39:27 GMT  
		Size: 348.0 KB (348012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0451913b17a56844e9c92165120da313434cba935ddb3353799081a241b27c`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 975.6 KB (975633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281e59625cef2e9db605bf16166bd89c3dd232e78ed0dcdcd563b7893aa85ba3`  
		Last Modified: Tue, 10 Jun 2025 00:01:06 GMT  
		Size: 492.8 MB (492750345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:db8251d53d5c9539ee64f406ca69c5cedbe3d894efc9bff3f792e4ef5057ca22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53739964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d22f8356ce708dcea7b039482148d9135ea7974309d628290e8b0f5b4621f3`

```dockerfile
```

-	Layers:
	-	`sha256:dc3773e4d74b9393c411008916dc91aa2d7d6dd3a4918c7e6872b66579e98878`  
		Last Modified: Mon, 09 Jun 2025 22:18:39 GMT  
		Size: 53.7 MB (53730591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80d0934d33825d3fea55238e02051fbdebb494b9638955248d524a9d29405ba3`  
		Last Modified: Mon, 09 Jun 2025 22:18:40 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:d7efbaa115a4a825bdc1f90869df8ad35ed3e3eb6b6b3643abb8f877136b66ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.3 MB (730298178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995d91d47349518216523bccdc7d0593305ee53562e721467a4787f15188b2a5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Thu, 08 May 2025 17:24:17 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfcc4cfce76b5bf1c5a2d77d213c53e381bd6af934ace80b7dd575fae26fbc2`  
		Last Modified: Mon, 09 Jun 2025 21:26:48 GMT  
		Size: 1.2 MB (1194843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbedf4f0754ca72166025a791ca6d481ebf5eabf3a71098223375b9e239ab5e`  
		Last Modified: Mon, 09 Jun 2025 21:26:50 GMT  
		Size: 8.5 MB (8495172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b93f56f8bb23cd9397a52b8507218a13ec5c99454df623bcb512756c0e3b65c`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d92492254010b5a5b3b8e25ef8ec55aa5095c585ca3229bc0eeef8d85b8360`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24987496e81c5b0ad1b96e1e2aa860aa62af52099656d4f90b854a1ea854ef88`  
		Last Modified: Mon, 09 Jun 2025 22:21:50 GMT  
		Size: 228.4 MB (228378250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d5d7d2be5c7ee349e5b07c644259548f6e8ab647d692c695bb392c00cc8ee0`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c0306cc8cd95c4d090ded2ccdb527b61a1fa1b77279dcd9d99caee9665231f`  
		Last Modified: Mon, 09 Jun 2025 21:50:36 GMT  
		Size: 29.8 MB (29845900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60f895b7132ec2355664c60f7339ba7673f3bc1e481242742ec7c0a792f400b`  
		Last Modified: Mon, 09 Jun 2025 21:50:35 GMT  
		Size: 348.0 KB (348006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f31d7a3f2c23ccacb5df0f3b9478367ec6c1b2527626899c0d3c6c0386685a1`  
		Last Modified: Mon, 09 Jun 2025 21:50:35 GMT  
		Size: 901.1 KB (901107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72144390a2a542ff23fda8fe3461654816cd91594878a1029d7197a649333a54`  
		Last Modified: Mon, 09 Jun 2025 22:38:17 GMT  
		Size: 437.5 MB (437506317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:fa86167eab0b7a9df620f6ef2ae3adcc284d87fefda29b22f0b14c8940747b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52464673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf5a208671fc459661a3f7858f76e166585f4aa250083d11fb19efbd8aa0454`

```dockerfile
```

-	Layers:
	-	`sha256:2dfc448a893133e4d2df58110950ed24036fddbb6f2a4c42123159f7515c966b`  
		Last Modified: Tue, 10 Jun 2025 01:18:48 GMT  
		Size: 52.5 MB (52455239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f505f527d26f2ef883856404c4045e61e0d29db33a171e94e5a69e628ac3c1`  
		Last Modified: Tue, 10 Jun 2025 01:18:49 GMT  
		Size: 9.4 KB (9434 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fa8a2054fdbbe5d74054681e5ab88ea2b1b02cf1f68feb71083c90ae88c6ef6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **907.0 MB (906986380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c7e5698db4a1cf6a46a76f19ff551acb51b66fb799bcd06289be0b11caa471`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfbcdfd0b57613941270f9d51dd852e2113c510314bc16442dac6b7ccd93bb4`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 4.1 KB (4051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85112d048ca69cba46cedbe7609be6b1388da46a96c5f25f3074b3d03ed5cada`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f86eac5764b45f84c9f74da912d260c33bea9dce19480b68f6d9e8d5c6b757`  
		Last Modified: Mon, 09 Jun 2025 22:32:16 GMT  
		Size: 361.4 MB (361381917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9cab4e76df8ec2a87814d4b7ac61519a9a8786d329cee9df51b06f8a16ae76`  
		Last Modified: Mon, 09 Jun 2025 21:45:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8965a1cbf95bb1c0a0fdbf2e84e831095239fa093c88df83b4813cd360bf61d`  
		Last Modified: Mon, 09 Jun 2025 23:22:48 GMT  
		Size: 44.0 MB (44025805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96c9101971e6e544417587498e848cd906a5072fe880df3a870c6735f518bf5`  
		Last Modified: Mon, 09 Jun 2025 22:23:05 GMT  
		Size: 348.0 KB (348026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679ea0da59a1556edaba85a9966e6296db829e778f72481bfbe4a9859f6c4c2`  
		Last Modified: Mon, 09 Jun 2025 22:23:09 GMT  
		Size: 954.7 KB (954730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e716aef459894de40b20955ac0ac75e343d47ba24a293a310e828c3a4c8ce70`  
		Last Modified: Tue, 10 Jun 2025 04:58:23 GMT  
		Size: 463.3 MB (463259314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:1a32d960102ccb3b00fc1a03f651e635b5f82971954ab338cf059ff923abb9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53583004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b1d0f1a004945510423272c396a6d608060d5bd86220b839656a4ea3399ad7`

```dockerfile
```

-	Layers:
	-	`sha256:493356d0c2543bdcbb8784bda13e7e0ca5b279ff3975d2c6ddf7361dd1bf58a4`  
		Last Modified: Tue, 10 Jun 2025 01:19:47 GMT  
		Size: 53.6 MB (53573551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:323c13b9db44e4e32b2cacd68646ca58d74255b872286957e71b6698160012e8`  
		Last Modified: Tue, 10 Jun 2025 01:19:48 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:32370c500818eaefb8491d7d85e9f415541b7f4bfec8afc59c4240653e7a77e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:ef5fdebeaa881604208c067f96d42b61331825309e559c093e24e9e89c7d3d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **953.0 MB (953023137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d1e228d78fdb8d64b885b3a15a6b05732187206079883723b81f3dc87f7eb7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da4792f7f416db06c00bc26bb845d00bd1c6f16f3e10a4c7d0031c91656aa3e`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 1.2 MB (1194841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20358ca2eb5aafdeb52607c52f0c03ee909a919235fc1041db00d58da1c59b6`  
		Last Modified: Mon, 09 Jun 2025 21:17:15 GMT  
		Size: 10.0 MB (9982583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dce350d6ea44ccf7fac3a7bdda0989aca3a6b72ffbfc14104e3b18810c2de33`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 4.0 KB (4045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ca0507171d76ea79443c6b48e8e4038c3555f8ca12aef4cd82ca0ca7a43786`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cc10980325859d6423bbc515001cb577760dc73999bb2e18e811a24877c5cb`  
		Last Modified: Mon, 09 Jun 2025 21:38:06 GMT  
		Size: 370.5 MB (370502304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6932d16c264574201be5a55ba79dd248dab8a2a0a32b8cdf30af3e1c5e86f806`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342ecf093a9124f383e5acc3a78d21be9e4f20515e24b2e0c8169a199d845c1c`  
		Last Modified: Mon, 09 Jun 2025 21:39:32 GMT  
		Size: 49.8 MB (49754505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c240714a1b7806b225c5f9dde0ab272ceaa47a40ac7b752cbe0370bbaf3976e`  
		Last Modified: Mon, 09 Jun 2025 21:39:27 GMT  
		Size: 348.0 KB (348012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0451913b17a56844e9c92165120da313434cba935ddb3353799081a241b27c`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 975.6 KB (975633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281e59625cef2e9db605bf16166bd89c3dd232e78ed0dcdcd563b7893aa85ba3`  
		Last Modified: Tue, 10 Jun 2025 00:01:06 GMT  
		Size: 492.8 MB (492750345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:db8251d53d5c9539ee64f406ca69c5cedbe3d894efc9bff3f792e4ef5057ca22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53739964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d22f8356ce708dcea7b039482148d9135ea7974309d628290e8b0f5b4621f3`

```dockerfile
```

-	Layers:
	-	`sha256:dc3773e4d74b9393c411008916dc91aa2d7d6dd3a4918c7e6872b66579e98878`  
		Last Modified: Mon, 09 Jun 2025 22:18:39 GMT  
		Size: 53.7 MB (53730591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80d0934d33825d3fea55238e02051fbdebb494b9638955248d524a9d29405ba3`  
		Last Modified: Mon, 09 Jun 2025 22:18:40 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:d7efbaa115a4a825bdc1f90869df8ad35ed3e3eb6b6b3643abb8f877136b66ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.3 MB (730298178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995d91d47349518216523bccdc7d0593305ee53562e721467a4787f15188b2a5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Thu, 08 May 2025 17:24:17 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfcc4cfce76b5bf1c5a2d77d213c53e381bd6af934ace80b7dd575fae26fbc2`  
		Last Modified: Mon, 09 Jun 2025 21:26:48 GMT  
		Size: 1.2 MB (1194843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbedf4f0754ca72166025a791ca6d481ebf5eabf3a71098223375b9e239ab5e`  
		Last Modified: Mon, 09 Jun 2025 21:26:50 GMT  
		Size: 8.5 MB (8495172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b93f56f8bb23cd9397a52b8507218a13ec5c99454df623bcb512756c0e3b65c`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d92492254010b5a5b3b8e25ef8ec55aa5095c585ca3229bc0eeef8d85b8360`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24987496e81c5b0ad1b96e1e2aa860aa62af52099656d4f90b854a1ea854ef88`  
		Last Modified: Mon, 09 Jun 2025 22:21:50 GMT  
		Size: 228.4 MB (228378250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d5d7d2be5c7ee349e5b07c644259548f6e8ab647d692c695bb392c00cc8ee0`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c0306cc8cd95c4d090ded2ccdb527b61a1fa1b77279dcd9d99caee9665231f`  
		Last Modified: Mon, 09 Jun 2025 21:50:36 GMT  
		Size: 29.8 MB (29845900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60f895b7132ec2355664c60f7339ba7673f3bc1e481242742ec7c0a792f400b`  
		Last Modified: Mon, 09 Jun 2025 21:50:35 GMT  
		Size: 348.0 KB (348006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f31d7a3f2c23ccacb5df0f3b9478367ec6c1b2527626899c0d3c6c0386685a1`  
		Last Modified: Mon, 09 Jun 2025 21:50:35 GMT  
		Size: 901.1 KB (901107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72144390a2a542ff23fda8fe3461654816cd91594878a1029d7197a649333a54`  
		Last Modified: Mon, 09 Jun 2025 22:38:17 GMT  
		Size: 437.5 MB (437506317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:fa86167eab0b7a9df620f6ef2ae3adcc284d87fefda29b22f0b14c8940747b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52464673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf5a208671fc459661a3f7858f76e166585f4aa250083d11fb19efbd8aa0454`

```dockerfile
```

-	Layers:
	-	`sha256:2dfc448a893133e4d2df58110950ed24036fddbb6f2a4c42123159f7515c966b`  
		Last Modified: Tue, 10 Jun 2025 01:18:48 GMT  
		Size: 52.5 MB (52455239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f505f527d26f2ef883856404c4045e61e0d29db33a171e94e5a69e628ac3c1`  
		Last Modified: Tue, 10 Jun 2025 01:18:49 GMT  
		Size: 9.4 KB (9434 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fa8a2054fdbbe5d74054681e5ab88ea2b1b02cf1f68feb71083c90ae88c6ef6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **907.0 MB (906986380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c7e5698db4a1cf6a46a76f19ff551acb51b66fb799bcd06289be0b11caa471`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfbcdfd0b57613941270f9d51dd852e2113c510314bc16442dac6b7ccd93bb4`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 4.1 KB (4051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85112d048ca69cba46cedbe7609be6b1388da46a96c5f25f3074b3d03ed5cada`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f86eac5764b45f84c9f74da912d260c33bea9dce19480b68f6d9e8d5c6b757`  
		Last Modified: Mon, 09 Jun 2025 22:32:16 GMT  
		Size: 361.4 MB (361381917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9cab4e76df8ec2a87814d4b7ac61519a9a8786d329cee9df51b06f8a16ae76`  
		Last Modified: Mon, 09 Jun 2025 21:45:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8965a1cbf95bb1c0a0fdbf2e84e831095239fa093c88df83b4813cd360bf61d`  
		Last Modified: Mon, 09 Jun 2025 23:22:48 GMT  
		Size: 44.0 MB (44025805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96c9101971e6e544417587498e848cd906a5072fe880df3a870c6735f518bf5`  
		Last Modified: Mon, 09 Jun 2025 22:23:05 GMT  
		Size: 348.0 KB (348026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679ea0da59a1556edaba85a9966e6296db829e778f72481bfbe4a9859f6c4c2`  
		Last Modified: Mon, 09 Jun 2025 22:23:09 GMT  
		Size: 954.7 KB (954730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e716aef459894de40b20955ac0ac75e343d47ba24a293a310e828c3a4c8ce70`  
		Last Modified: Tue, 10 Jun 2025 04:58:23 GMT  
		Size: 463.3 MB (463259314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:1a32d960102ccb3b00fc1a03f651e635b5f82971954ab338cf059ff923abb9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53583004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b1d0f1a004945510423272c396a6d608060d5bd86220b839656a4ea3399ad7`

```dockerfile
```

-	Layers:
	-	`sha256:493356d0c2543bdcbb8784bda13e7e0ca5b279ff3975d2c6ddf7361dd1bf58a4`  
		Last Modified: Tue, 10 Jun 2025 01:19:47 GMT  
		Size: 53.6 MB (53573551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:323c13b9db44e4e32b2cacd68646ca58d74255b872286957e71b6698160012e8`  
		Last Modified: Tue, 10 Jun 2025 01:19:48 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:7cf0b9f6546abeba308ea42cb7ad3453f3e520e1af57cdf179fe915c939674bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:819dc13d1e8e8f6f0df66146ff8b9afb994f654b8eb5b718584ca5bccf6983a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.1 MB (476141159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac4b7aa185b0f5de02f1516f659f83790705400948ad4a5d0c7bdd4462bda08`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da4792f7f416db06c00bc26bb845d00bd1c6f16f3e10a4c7d0031c91656aa3e`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 1.2 MB (1194841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20358ca2eb5aafdeb52607c52f0c03ee909a919235fc1041db00d58da1c59b6`  
		Last Modified: Mon, 09 Jun 2025 21:17:15 GMT  
		Size: 10.0 MB (9982583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dce350d6ea44ccf7fac3a7bdda0989aca3a6b72ffbfc14104e3b18810c2de33`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 4.0 KB (4045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ca0507171d76ea79443c6b48e8e4038c3555f8ca12aef4cd82ca0ca7a43786`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cc10980325859d6423bbc515001cb577760dc73999bb2e18e811a24877c5cb`  
		Last Modified: Mon, 09 Jun 2025 21:38:06 GMT  
		Size: 370.5 MB (370502304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6932d16c264574201be5a55ba79dd248dab8a2a0a32b8cdf30af3e1c5e86f806`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342ecf093a9124f383e5acc3a78d21be9e4f20515e24b2e0c8169a199d845c1c`  
		Last Modified: Mon, 09 Jun 2025 21:39:32 GMT  
		Size: 49.8 MB (49754505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c240714a1b7806b225c5f9dde0ab272ceaa47a40ac7b752cbe0370bbaf3976e`  
		Last Modified: Mon, 09 Jun 2025 21:39:27 GMT  
		Size: 348.0 KB (348012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0451913b17a56844e9c92165120da313434cba935ddb3353799081a241b27c`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 975.6 KB (975633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5c979472dedcc14f42e4c345a68bbccd5ee6689cdbea9aea3388abac746eae`  
		Last Modified: Mon, 09 Jun 2025 21:45:21 GMT  
		Size: 15.9 MB (15868367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:011af3585742a3aa13be9e24ebec7e2f0b382a0ee956547f1fa02c98ec11b4dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 MB (33095128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bd71d9e9fec1b6584170789d96f9c5a501374b7c23770ad037bb674ff1acd7`

```dockerfile
```

-	Layers:
	-	`sha256:aa673f3c50f2a58d98d83ec7d28ca3cccc494a6682d5d34ea17e781ba3caf054`  
		Last Modified: Mon, 09 Jun 2025 22:18:42 GMT  
		Size: 33.1 MB (33085802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d08fb5d206986bf50ffd47387701e39bc891e6001aef5bd1bcaa04f8813bc7`  
		Last Modified: Mon, 09 Jun 2025 22:18:43 GMT  
		Size: 9.3 KB (9326 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:0e46c6eb785948624a2bcdb9802be787e07404baf8557d690be3f8c2f43e85d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.9 MB (306867689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de30855f5bcfa7185bf62c66933f5e15081d173a58fba10028898c366d382e8a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Thu, 08 May 2025 17:24:17 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfcc4cfce76b5bf1c5a2d77d213c53e381bd6af934ace80b7dd575fae26fbc2`  
		Last Modified: Mon, 09 Jun 2025 21:26:48 GMT  
		Size: 1.2 MB (1194843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbedf4f0754ca72166025a791ca6d481ebf5eabf3a71098223375b9e239ab5e`  
		Last Modified: Mon, 09 Jun 2025 21:26:50 GMT  
		Size: 8.5 MB (8495172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b93f56f8bb23cd9397a52b8507218a13ec5c99454df623bcb512756c0e3b65c`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d92492254010b5a5b3b8e25ef8ec55aa5095c585ca3229bc0eeef8d85b8360`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24987496e81c5b0ad1b96e1e2aa860aa62af52099656d4f90b854a1ea854ef88`  
		Last Modified: Mon, 09 Jun 2025 22:21:50 GMT  
		Size: 228.4 MB (228378250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d5d7d2be5c7ee349e5b07c644259548f6e8ab647d692c695bb392c00cc8ee0`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c0306cc8cd95c4d090ded2ccdb527b61a1fa1b77279dcd9d99caee9665231f`  
		Last Modified: Mon, 09 Jun 2025 21:50:36 GMT  
		Size: 29.8 MB (29845900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60f895b7132ec2355664c60f7339ba7673f3bc1e481242742ec7c0a792f400b`  
		Last Modified: Mon, 09 Jun 2025 21:50:35 GMT  
		Size: 348.0 KB (348006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f31d7a3f2c23ccacb5df0f3b9478367ec6c1b2527626899c0d3c6c0386685a1`  
		Last Modified: Mon, 09 Jun 2025 21:50:35 GMT  
		Size: 901.1 KB (901107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20997e5d1479935eeec91d2bb3b2b3bb6d06e94918fa9176bb8830a91eaeef2e`  
		Last Modified: Mon, 09 Jun 2025 22:28:34 GMT  
		Size: 14.1 MB (14075828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:5fa4024acc84524e80b5abd50a30052918f5f05ed8c7ee6fd19a1e3efee607f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31793741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2551a80f128e5f415427839faef0a42f4aacd5f095a80518424c01200bae20`

```dockerfile
```

-	Layers:
	-	`sha256:75573b92887cab5acecdaf8e455e7c13915fb0887125e4e730670712bf4fb706`  
		Last Modified: Tue, 10 Jun 2025 01:18:23 GMT  
		Size: 31.8 MB (31784355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe5bc595c811d4ec098ae72263ce2b2bc76b266320e2bdf0168b9ff53fa13b1`  
		Last Modified: Tue, 10 Jun 2025 01:18:24 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cd7cb65c389840ae730d0ab10e3abe0c7cb915512aea26fd2a38a74fd4557adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.2 MB (459190609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f2585c17b1fa7afd57b4f528b67028eae322dc4f4d446070819fc12f4be4b4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfbcdfd0b57613941270f9d51dd852e2113c510314bc16442dac6b7ccd93bb4`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 4.1 KB (4051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85112d048ca69cba46cedbe7609be6b1388da46a96c5f25f3074b3d03ed5cada`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f86eac5764b45f84c9f74da912d260c33bea9dce19480b68f6d9e8d5c6b757`  
		Last Modified: Mon, 09 Jun 2025 22:32:16 GMT  
		Size: 361.4 MB (361381917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9cab4e76df8ec2a87814d4b7ac61519a9a8786d329cee9df51b06f8a16ae76`  
		Last Modified: Mon, 09 Jun 2025 21:45:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8965a1cbf95bb1c0a0fdbf2e84e831095239fa093c88df83b4813cd360bf61d`  
		Last Modified: Mon, 09 Jun 2025 23:22:48 GMT  
		Size: 44.0 MB (44025805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96c9101971e6e544417587498e848cd906a5072fe880df3a870c6735f518bf5`  
		Last Modified: Mon, 09 Jun 2025 22:23:05 GMT  
		Size: 348.0 KB (348026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679ea0da59a1556edaba85a9966e6296db829e778f72481bfbe4a9859f6c4c2`  
		Last Modified: Mon, 09 Jun 2025 22:23:09 GMT  
		Size: 954.7 KB (954730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad97ee94f10247ee0fac2f50fdf26e67a5e5ed47312834edeffab79da355382`  
		Last Modified: Mon, 09 Jun 2025 23:11:14 GMT  
		Size: 15.5 MB (15463543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:d1ae62e56b7ecbbded7bc6b667ef3790fc3e2b196ac9045841b4231b6103df77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32918039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28b6e15ead3b532cb486dd1890e8040972bbf8a5096ca4a740c02508590dc3c`

```dockerfile
```

-	Layers:
	-	`sha256:432b1ab837be5ee2a7138cd09df60b2a1a3c75163de0bb3c12192989f52c8a52`  
		Last Modified: Tue, 10 Jun 2025 01:18:52 GMT  
		Size: 32.9 MB (32908633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff90afb88018e7a33fc4829d2cae3170598f3fc580e76d52c5335525c733ab70`  
		Last Modified: Tue, 10 Jun 2025 01:18:53 GMT  
		Size: 9.4 KB (9406 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:7cf0b9f6546abeba308ea42cb7ad3453f3e520e1af57cdf179fe915c939674bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:819dc13d1e8e8f6f0df66146ff8b9afb994f654b8eb5b718584ca5bccf6983a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.1 MB (476141159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac4b7aa185b0f5de02f1516f659f83790705400948ad4a5d0c7bdd4462bda08`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da4792f7f416db06c00bc26bb845d00bd1c6f16f3e10a4c7d0031c91656aa3e`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 1.2 MB (1194841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20358ca2eb5aafdeb52607c52f0c03ee909a919235fc1041db00d58da1c59b6`  
		Last Modified: Mon, 09 Jun 2025 21:17:15 GMT  
		Size: 10.0 MB (9982583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dce350d6ea44ccf7fac3a7bdda0989aca3a6b72ffbfc14104e3b18810c2de33`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 4.0 KB (4045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ca0507171d76ea79443c6b48e8e4038c3555f8ca12aef4cd82ca0ca7a43786`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cc10980325859d6423bbc515001cb577760dc73999bb2e18e811a24877c5cb`  
		Last Modified: Mon, 09 Jun 2025 21:38:06 GMT  
		Size: 370.5 MB (370502304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6932d16c264574201be5a55ba79dd248dab8a2a0a32b8cdf30af3e1c5e86f806`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342ecf093a9124f383e5acc3a78d21be9e4f20515e24b2e0c8169a199d845c1c`  
		Last Modified: Mon, 09 Jun 2025 21:39:32 GMT  
		Size: 49.8 MB (49754505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c240714a1b7806b225c5f9dde0ab272ceaa47a40ac7b752cbe0370bbaf3976e`  
		Last Modified: Mon, 09 Jun 2025 21:39:27 GMT  
		Size: 348.0 KB (348012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0451913b17a56844e9c92165120da313434cba935ddb3353799081a241b27c`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 975.6 KB (975633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5c979472dedcc14f42e4c345a68bbccd5ee6689cdbea9aea3388abac746eae`  
		Last Modified: Mon, 09 Jun 2025 21:45:21 GMT  
		Size: 15.9 MB (15868367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:011af3585742a3aa13be9e24ebec7e2f0b382a0ee956547f1fa02c98ec11b4dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 MB (33095128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bd71d9e9fec1b6584170789d96f9c5a501374b7c23770ad037bb674ff1acd7`

```dockerfile
```

-	Layers:
	-	`sha256:aa673f3c50f2a58d98d83ec7d28ca3cccc494a6682d5d34ea17e781ba3caf054`  
		Last Modified: Mon, 09 Jun 2025 22:18:42 GMT  
		Size: 33.1 MB (33085802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d08fb5d206986bf50ffd47387701e39bc891e6001aef5bd1bcaa04f8813bc7`  
		Last Modified: Mon, 09 Jun 2025 22:18:43 GMT  
		Size: 9.3 KB (9326 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:0e46c6eb785948624a2bcdb9802be787e07404baf8557d690be3f8c2f43e85d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.9 MB (306867689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de30855f5bcfa7185bf62c66933f5e15081d173a58fba10028898c366d382e8a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Thu, 08 May 2025 17:24:17 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfcc4cfce76b5bf1c5a2d77d213c53e381bd6af934ace80b7dd575fae26fbc2`  
		Last Modified: Mon, 09 Jun 2025 21:26:48 GMT  
		Size: 1.2 MB (1194843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbedf4f0754ca72166025a791ca6d481ebf5eabf3a71098223375b9e239ab5e`  
		Last Modified: Mon, 09 Jun 2025 21:26:50 GMT  
		Size: 8.5 MB (8495172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b93f56f8bb23cd9397a52b8507218a13ec5c99454df623bcb512756c0e3b65c`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d92492254010b5a5b3b8e25ef8ec55aa5095c585ca3229bc0eeef8d85b8360`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24987496e81c5b0ad1b96e1e2aa860aa62af52099656d4f90b854a1ea854ef88`  
		Last Modified: Mon, 09 Jun 2025 22:21:50 GMT  
		Size: 228.4 MB (228378250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d5d7d2be5c7ee349e5b07c644259548f6e8ab647d692c695bb392c00cc8ee0`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c0306cc8cd95c4d090ded2ccdb527b61a1fa1b77279dcd9d99caee9665231f`  
		Last Modified: Mon, 09 Jun 2025 21:50:36 GMT  
		Size: 29.8 MB (29845900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60f895b7132ec2355664c60f7339ba7673f3bc1e481242742ec7c0a792f400b`  
		Last Modified: Mon, 09 Jun 2025 21:50:35 GMT  
		Size: 348.0 KB (348006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f31d7a3f2c23ccacb5df0f3b9478367ec6c1b2527626899c0d3c6c0386685a1`  
		Last Modified: Mon, 09 Jun 2025 21:50:35 GMT  
		Size: 901.1 KB (901107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20997e5d1479935eeec91d2bb3b2b3bb6d06e94918fa9176bb8830a91eaeef2e`  
		Last Modified: Mon, 09 Jun 2025 22:28:34 GMT  
		Size: 14.1 MB (14075828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:5fa4024acc84524e80b5abd50a30052918f5f05ed8c7ee6fd19a1e3efee607f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31793741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2551a80f128e5f415427839faef0a42f4aacd5f095a80518424c01200bae20`

```dockerfile
```

-	Layers:
	-	`sha256:75573b92887cab5acecdaf8e455e7c13915fb0887125e4e730670712bf4fb706`  
		Last Modified: Tue, 10 Jun 2025 01:18:23 GMT  
		Size: 31.8 MB (31784355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe5bc595c811d4ec098ae72263ce2b2bc76b266320e2bdf0168b9ff53fa13b1`  
		Last Modified: Tue, 10 Jun 2025 01:18:24 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cd7cb65c389840ae730d0ab10e3abe0c7cb915512aea26fd2a38a74fd4557adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.2 MB (459190609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f2585c17b1fa7afd57b4f528b67028eae322dc4f4d446070819fc12f4be4b4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfbcdfd0b57613941270f9d51dd852e2113c510314bc16442dac6b7ccd93bb4`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 4.1 KB (4051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85112d048ca69cba46cedbe7609be6b1388da46a96c5f25f3074b3d03ed5cada`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f86eac5764b45f84c9f74da912d260c33bea9dce19480b68f6d9e8d5c6b757`  
		Last Modified: Mon, 09 Jun 2025 22:32:16 GMT  
		Size: 361.4 MB (361381917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9cab4e76df8ec2a87814d4b7ac61519a9a8786d329cee9df51b06f8a16ae76`  
		Last Modified: Mon, 09 Jun 2025 21:45:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8965a1cbf95bb1c0a0fdbf2e84e831095239fa093c88df83b4813cd360bf61d`  
		Last Modified: Mon, 09 Jun 2025 23:22:48 GMT  
		Size: 44.0 MB (44025805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96c9101971e6e544417587498e848cd906a5072fe880df3a870c6735f518bf5`  
		Last Modified: Mon, 09 Jun 2025 22:23:05 GMT  
		Size: 348.0 KB (348026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679ea0da59a1556edaba85a9966e6296db829e778f72481bfbe4a9859f6c4c2`  
		Last Modified: Mon, 09 Jun 2025 22:23:09 GMT  
		Size: 954.7 KB (954730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad97ee94f10247ee0fac2f50fdf26e67a5e5ed47312834edeffab79da355382`  
		Last Modified: Mon, 09 Jun 2025 23:11:14 GMT  
		Size: 15.5 MB (15463543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:d1ae62e56b7ecbbded7bc6b667ef3790fc3e2b196ac9045841b4231b6103df77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32918039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28b6e15ead3b532cb486dd1890e8040972bbf8a5096ca4a740c02508590dc3c`

```dockerfile
```

-	Layers:
	-	`sha256:432b1ab837be5ee2a7138cd09df60b2a1a3c75163de0bb3c12192989f52c8a52`  
		Last Modified: Tue, 10 Jun 2025 01:18:52 GMT  
		Size: 32.9 MB (32908633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff90afb88018e7a33fc4829d2cae3170598f3fc580e76d52c5335525c733ab70`  
		Last Modified: Tue, 10 Jun 2025 01:18:53 GMT  
		Size: 9.4 KB (9406 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:72b8bc59035dc0a5b8e07aae28c16caa84192971d72d207c72ed734fb1d5e97d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:4f01fa743be43da0e14ddf2ac29b5118d9c0eb4057c9761c13303b8a52fa9c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.3 MB (460272792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607ca0f020489b85d74ef5ae2f0ce8e901813af48008b0a622fc06cd41bf0d1b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da4792f7f416db06c00bc26bb845d00bd1c6f16f3e10a4c7d0031c91656aa3e`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 1.2 MB (1194841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20358ca2eb5aafdeb52607c52f0c03ee909a919235fc1041db00d58da1c59b6`  
		Last Modified: Mon, 09 Jun 2025 21:17:15 GMT  
		Size: 10.0 MB (9982583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dce350d6ea44ccf7fac3a7bdda0989aca3a6b72ffbfc14104e3b18810c2de33`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 4.0 KB (4045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ca0507171d76ea79443c6b48e8e4038c3555f8ca12aef4cd82ca0ca7a43786`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cc10980325859d6423bbc515001cb577760dc73999bb2e18e811a24877c5cb`  
		Last Modified: Mon, 09 Jun 2025 21:38:06 GMT  
		Size: 370.5 MB (370502304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6932d16c264574201be5a55ba79dd248dab8a2a0a32b8cdf30af3e1c5e86f806`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342ecf093a9124f383e5acc3a78d21be9e4f20515e24b2e0c8169a199d845c1c`  
		Last Modified: Mon, 09 Jun 2025 21:39:32 GMT  
		Size: 49.8 MB (49754505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c240714a1b7806b225c5f9dde0ab272ceaa47a40ac7b752cbe0370bbaf3976e`  
		Last Modified: Mon, 09 Jun 2025 21:39:27 GMT  
		Size: 348.0 KB (348012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0451913b17a56844e9c92165120da313434cba935ddb3353799081a241b27c`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 975.6 KB (975633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:c081b974b2e84ce8ba0066b91664245b12a4217c7bf3121b382cfffea9522495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31302280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3aba0ed8be28e189623a99f7b2b073874abfb184f1742a959bb3bc8c2e327c`

```dockerfile
```

-	Layers:
	-	`sha256:f743f4f945c8627b2c94cb0fb0f577742f5489ec6d509d3d8ce4a38f0ba03a06`  
		Last Modified: Mon, 09 Jun 2025 22:18:34 GMT  
		Size: 31.3 MB (31288594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5145030147e7ed7e8d1f4d7fa5d65e7f95d250e533960a796d0481506eb56d0`  
		Last Modified: Mon, 09 Jun 2025 22:18:34 GMT  
		Size: 13.7 KB (13686 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:31818b9103a0d47738690ff8eaacb928520bf92017fc1c6c4d5cdad9261fa1c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292791861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae49cc2167e0598b690cd174a01b8457d8d2f9eca339bedb7b77d4d1c87b38b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Thu, 08 May 2025 17:24:17 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfcc4cfce76b5bf1c5a2d77d213c53e381bd6af934ace80b7dd575fae26fbc2`  
		Last Modified: Mon, 09 Jun 2025 21:26:48 GMT  
		Size: 1.2 MB (1194843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbedf4f0754ca72166025a791ca6d481ebf5eabf3a71098223375b9e239ab5e`  
		Last Modified: Mon, 09 Jun 2025 21:26:50 GMT  
		Size: 8.5 MB (8495172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b93f56f8bb23cd9397a52b8507218a13ec5c99454df623bcb512756c0e3b65c`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d92492254010b5a5b3b8e25ef8ec55aa5095c585ca3229bc0eeef8d85b8360`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24987496e81c5b0ad1b96e1e2aa860aa62af52099656d4f90b854a1ea854ef88`  
		Last Modified: Mon, 09 Jun 2025 22:21:50 GMT  
		Size: 228.4 MB (228378250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d5d7d2be5c7ee349e5b07c644259548f6e8ab647d692c695bb392c00cc8ee0`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c0306cc8cd95c4d090ded2ccdb527b61a1fa1b77279dcd9d99caee9665231f`  
		Last Modified: Mon, 09 Jun 2025 21:50:36 GMT  
		Size: 29.8 MB (29845900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60f895b7132ec2355664c60f7339ba7673f3bc1e481242742ec7c0a792f400b`  
		Last Modified: Mon, 09 Jun 2025 21:50:35 GMT  
		Size: 348.0 KB (348006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f31d7a3f2c23ccacb5df0f3b9478367ec6c1b2527626899c0d3c6c0386685a1`  
		Last Modified: Mon, 09 Jun 2025 21:50:35 GMT  
		Size: 901.1 KB (901107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:02961273e4e5adbf0edbaa55e408869e8a76c8e89bfb3e44cc748d1d47775f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30012724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c4c950bdfdef4c337e4fde12825560ac2c5ab3ed6b230fc9554bed950d65da`

```dockerfile
```

-	Layers:
	-	`sha256:38dd0a9571edf6b5307ea32643bbb13e20f6963b38e69461f06341aa9100f589`  
		Last Modified: Mon, 09 Jun 2025 22:19:07 GMT  
		Size: 30.0 MB (29998944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35dd4a9dda0678fcd4bb804ba29e39fb44b9355c78cd00f096b6a69c4da32903`  
		Last Modified: Mon, 09 Jun 2025 22:19:08 GMT  
		Size: 13.8 KB (13780 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c84e573d2f2beb679ea5b03015eb2876e9962657c23d0073e4ae9d7ba41c4700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.7 MB (443727066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547fd10070fcb8190d04b6923e9f20800c6097d062870239d07a40a140316bc0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfbcdfd0b57613941270f9d51dd852e2113c510314bc16442dac6b7ccd93bb4`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 4.1 KB (4051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85112d048ca69cba46cedbe7609be6b1388da46a96c5f25f3074b3d03ed5cada`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f86eac5764b45f84c9f74da912d260c33bea9dce19480b68f6d9e8d5c6b757`  
		Last Modified: Mon, 09 Jun 2025 22:32:16 GMT  
		Size: 361.4 MB (361381917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9cab4e76df8ec2a87814d4b7ac61519a9a8786d329cee9df51b06f8a16ae76`  
		Last Modified: Mon, 09 Jun 2025 21:45:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8965a1cbf95bb1c0a0fdbf2e84e831095239fa093c88df83b4813cd360bf61d`  
		Last Modified: Mon, 09 Jun 2025 23:22:48 GMT  
		Size: 44.0 MB (44025805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96c9101971e6e544417587498e848cd906a5072fe880df3a870c6735f518bf5`  
		Last Modified: Mon, 09 Jun 2025 22:23:05 GMT  
		Size: 348.0 KB (348026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679ea0da59a1556edaba85a9966e6296db829e778f72481bfbe4a9859f6c4c2`  
		Last Modified: Mon, 09 Jun 2025 22:23:09 GMT  
		Size: 954.7 KB (954730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:80cd2330c77e06fd24483ecb5250a44626836ec998f0a2b60031e9390d36af50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31126389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058ada81e83a7ad06c91ec5bf8d1fbbf0c28599b8f50e4b6383e22791f7165ed`

```dockerfile
```

-	Layers:
	-	`sha256:24ae88e3a88ca1e8f5519b268d395f9ce7a38287005086ed99b5e5abcdc37593`  
		Last Modified: Tue, 10 Jun 2025 01:18:32 GMT  
		Size: 31.1 MB (31112581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:525a91b30b35d8653b39c21d12dd3de1790c39fab37b1945e7e5c58d69fec318`  
		Last Modified: Tue, 10 Jun 2025 01:18:34 GMT  
		Size: 13.8 KB (13808 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:72b8bc59035dc0a5b8e07aae28c16caa84192971d72d207c72ed734fb1d5e97d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:4f01fa743be43da0e14ddf2ac29b5118d9c0eb4057c9761c13303b8a52fa9c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.3 MB (460272792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607ca0f020489b85d74ef5ae2f0ce8e901813af48008b0a622fc06cd41bf0d1b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da4792f7f416db06c00bc26bb845d00bd1c6f16f3e10a4c7d0031c91656aa3e`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 1.2 MB (1194841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20358ca2eb5aafdeb52607c52f0c03ee909a919235fc1041db00d58da1c59b6`  
		Last Modified: Mon, 09 Jun 2025 21:17:15 GMT  
		Size: 10.0 MB (9982583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dce350d6ea44ccf7fac3a7bdda0989aca3a6b72ffbfc14104e3b18810c2de33`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 4.0 KB (4045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ca0507171d76ea79443c6b48e8e4038c3555f8ca12aef4cd82ca0ca7a43786`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cc10980325859d6423bbc515001cb577760dc73999bb2e18e811a24877c5cb`  
		Last Modified: Mon, 09 Jun 2025 21:38:06 GMT  
		Size: 370.5 MB (370502304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6932d16c264574201be5a55ba79dd248dab8a2a0a32b8cdf30af3e1c5e86f806`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342ecf093a9124f383e5acc3a78d21be9e4f20515e24b2e0c8169a199d845c1c`  
		Last Modified: Mon, 09 Jun 2025 21:39:32 GMT  
		Size: 49.8 MB (49754505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c240714a1b7806b225c5f9dde0ab272ceaa47a40ac7b752cbe0370bbaf3976e`  
		Last Modified: Mon, 09 Jun 2025 21:39:27 GMT  
		Size: 348.0 KB (348012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0451913b17a56844e9c92165120da313434cba935ddb3353799081a241b27c`  
		Last Modified: Mon, 09 Jun 2025 21:39:26 GMT  
		Size: 975.6 KB (975633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:c081b974b2e84ce8ba0066b91664245b12a4217c7bf3121b382cfffea9522495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31302280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3aba0ed8be28e189623a99f7b2b073874abfb184f1742a959bb3bc8c2e327c`

```dockerfile
```

-	Layers:
	-	`sha256:f743f4f945c8627b2c94cb0fb0f577742f5489ec6d509d3d8ce4a38f0ba03a06`  
		Last Modified: Mon, 09 Jun 2025 22:18:34 GMT  
		Size: 31.3 MB (31288594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5145030147e7ed7e8d1f4d7fa5d65e7f95d250e533960a796d0481506eb56d0`  
		Last Modified: Mon, 09 Jun 2025 22:18:34 GMT  
		Size: 13.7 KB (13686 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:31818b9103a0d47738690ff8eaacb928520bf92017fc1c6c4d5cdad9261fa1c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292791861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae49cc2167e0598b690cd174a01b8457d8d2f9eca339bedb7b77d4d1c87b38b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Thu, 08 May 2025 17:24:17 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfcc4cfce76b5bf1c5a2d77d213c53e381bd6af934ace80b7dd575fae26fbc2`  
		Last Modified: Mon, 09 Jun 2025 21:26:48 GMT  
		Size: 1.2 MB (1194843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbedf4f0754ca72166025a791ca6d481ebf5eabf3a71098223375b9e239ab5e`  
		Last Modified: Mon, 09 Jun 2025 21:26:50 GMT  
		Size: 8.5 MB (8495172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b93f56f8bb23cd9397a52b8507218a13ec5c99454df623bcb512756c0e3b65c`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d92492254010b5a5b3b8e25ef8ec55aa5095c585ca3229bc0eeef8d85b8360`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24987496e81c5b0ad1b96e1e2aa860aa62af52099656d4f90b854a1ea854ef88`  
		Last Modified: Mon, 09 Jun 2025 22:21:50 GMT  
		Size: 228.4 MB (228378250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d5d7d2be5c7ee349e5b07c644259548f6e8ab647d692c695bb392c00cc8ee0`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c0306cc8cd95c4d090ded2ccdb527b61a1fa1b77279dcd9d99caee9665231f`  
		Last Modified: Mon, 09 Jun 2025 21:50:36 GMT  
		Size: 29.8 MB (29845900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60f895b7132ec2355664c60f7339ba7673f3bc1e481242742ec7c0a792f400b`  
		Last Modified: Mon, 09 Jun 2025 21:50:35 GMT  
		Size: 348.0 KB (348006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f31d7a3f2c23ccacb5df0f3b9478367ec6c1b2527626899c0d3c6c0386685a1`  
		Last Modified: Mon, 09 Jun 2025 21:50:35 GMT  
		Size: 901.1 KB (901107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:02961273e4e5adbf0edbaa55e408869e8a76c8e89bfb3e44cc748d1d47775f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30012724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c4c950bdfdef4c337e4fde12825560ac2c5ab3ed6b230fc9554bed950d65da`

```dockerfile
```

-	Layers:
	-	`sha256:38dd0a9571edf6b5307ea32643bbb13e20f6963b38e69461f06341aa9100f589`  
		Last Modified: Mon, 09 Jun 2025 22:19:07 GMT  
		Size: 30.0 MB (29998944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35dd4a9dda0678fcd4bb804ba29e39fb44b9355c78cd00f096b6a69c4da32903`  
		Last Modified: Mon, 09 Jun 2025 22:19:08 GMT  
		Size: 13.8 KB (13780 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c84e573d2f2beb679ea5b03015eb2876e9962657c23d0073e4ae9d7ba41c4700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.7 MB (443727066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547fd10070fcb8190d04b6923e9f20800c6097d062870239d07a40a140316bc0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Nov 2020 19:36:01 GMT
ARG RELEASE
# Tue, 17 Nov 2020 19:36:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Nov 2020 19:36:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Nov 2020 19:36:01 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LANG=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV LC_ALL=C.UTF-8
# Tue, 17 Nov 2020 19:36:01 GMT
ENV ROS_DISTRO=noetic
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 17 Nov 2020 19:36:01 GMT
CMD ["bash"]
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfbcdfd0b57613941270f9d51dd852e2113c510314bc16442dac6b7ccd93bb4`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 4.1 KB (4051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85112d048ca69cba46cedbe7609be6b1388da46a96c5f25f3074b3d03ed5cada`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f86eac5764b45f84c9f74da912d260c33bea9dce19480b68f6d9e8d5c6b757`  
		Last Modified: Mon, 09 Jun 2025 22:32:16 GMT  
		Size: 361.4 MB (361381917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9cab4e76df8ec2a87814d4b7ac61519a9a8786d329cee9df51b06f8a16ae76`  
		Last Modified: Mon, 09 Jun 2025 21:45:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8965a1cbf95bb1c0a0fdbf2e84e831095239fa093c88df83b4813cd360bf61d`  
		Last Modified: Mon, 09 Jun 2025 23:22:48 GMT  
		Size: 44.0 MB (44025805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96c9101971e6e544417587498e848cd906a5072fe880df3a870c6735f518bf5`  
		Last Modified: Mon, 09 Jun 2025 22:23:05 GMT  
		Size: 348.0 KB (348026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679ea0da59a1556edaba85a9966e6296db829e778f72481bfbe4a9859f6c4c2`  
		Last Modified: Mon, 09 Jun 2025 22:23:09 GMT  
		Size: 954.7 KB (954730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:80cd2330c77e06fd24483ecb5250a44626836ec998f0a2b60031e9390d36af50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31126389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058ada81e83a7ad06c91ec5bf8d1fbbf0c28599b8f50e4b6383e22791f7165ed`

```dockerfile
```

-	Layers:
	-	`sha256:24ae88e3a88ca1e8f5519b268d395f9ce7a38287005086ed99b5e5abcdc37593`  
		Last Modified: Tue, 10 Jun 2025 01:18:32 GMT  
		Size: 31.1 MB (31112581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:525a91b30b35d8653b39c21d12dd3de1790c39fab37b1945e7e5c58d69fec318`  
		Last Modified: Tue, 10 Jun 2025 01:18:34 GMT  
		Size: 13.8 KB (13808 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:fd6279f04e51fa61201a791da9a156129941887b95b614ae0cec7865ef49de4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:4c1435fd85be3edde3820f0d132ab30a6b030209dce4fa3ac428a2aa5a763caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.2 MB (409194642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9281103cce09d925abe6b7134ab3c5b7bb9158e57a2204c51175217dda4dfe9a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=noetic
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 07 Jun 2025 08:00:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da4792f7f416db06c00bc26bb845d00bd1c6f16f3e10a4c7d0031c91656aa3e`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 1.2 MB (1194841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20358ca2eb5aafdeb52607c52f0c03ee909a919235fc1041db00d58da1c59b6`  
		Last Modified: Mon, 09 Jun 2025 21:17:15 GMT  
		Size: 10.0 MB (9982583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dce350d6ea44ccf7fac3a7bdda0989aca3a6b72ffbfc14104e3b18810c2de33`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 4.0 KB (4045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ca0507171d76ea79443c6b48e8e4038c3555f8ca12aef4cd82ca0ca7a43786`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cc10980325859d6423bbc515001cb577760dc73999bb2e18e811a24877c5cb`  
		Last Modified: Mon, 09 Jun 2025 21:38:06 GMT  
		Size: 370.5 MB (370502304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6932d16c264574201be5a55ba79dd248dab8a2a0a32b8cdf30af3e1c5e86f806`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:acff80a38330a5a31d0736188c6f91a6220386cb22d5b19408f60acc98cd582b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29781814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c24c58ac29d31ce7d0aa7430c667961e4b5181a5e91efb301ac607f0ca640f9`

```dockerfile
```

-	Layers:
	-	`sha256:bf597893336763c20337f61fa235a39c41a481325d1f6a9ab15bb920f947b93a`  
		Last Modified: Mon, 09 Jun 2025 22:18:58 GMT  
		Size: 29.8 MB (29765457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4da31b4968be25636f6e96bc2ce17cbed293aecc74937629fce47cca4065560`  
		Last Modified: Mon, 09 Jun 2025 22:19:00 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:c9e79028edfa3207701777e232184aa095648173286b93c3b19d9a97d3d6c654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.7 MB (261696848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caab418962bcabcb4389a9852474cf889e69a8d8d42aed069ceadf6e08e87170`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:45:56 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:45:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:45:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:45:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:45:59 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 08 Apr 2025 10:45:59 GMT
CMD ["/bin/bash"]
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=noetic
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 07 Jun 2025 08:00:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Thu, 08 May 2025 17:24:17 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfcc4cfce76b5bf1c5a2d77d213c53e381bd6af934ace80b7dd575fae26fbc2`  
		Last Modified: Mon, 09 Jun 2025 21:26:48 GMT  
		Size: 1.2 MB (1194843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbedf4f0754ca72166025a791ca6d481ebf5eabf3a71098223375b9e239ab5e`  
		Last Modified: Mon, 09 Jun 2025 21:26:50 GMT  
		Size: 8.5 MB (8495172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b93f56f8bb23cd9397a52b8507218a13ec5c99454df623bcb512756c0e3b65c`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d92492254010b5a5b3b8e25ef8ec55aa5095c585ca3229bc0eeef8d85b8360`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24987496e81c5b0ad1b96e1e2aa860aa62af52099656d4f90b854a1ea854ef88`  
		Last Modified: Mon, 09 Jun 2025 22:21:50 GMT  
		Size: 228.4 MB (228378250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d5d7d2be5c7ee349e5b07c644259548f6e8ab647d692c695bb392c00cc8ee0`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:4c3fe52db1c08dad3c7b6b220a14c86045074042d36e2c837dc2e40edd56be00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28755073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fb167ab0b004a48773cd9ba1e91987d02409e11ceb243fab07138e5769e8b6`

```dockerfile
```

-	Layers:
	-	`sha256:345b20852b51b4b6a90c0fabf2ca2dd4375862857d3eae23f1cfb10b7c447edb`  
		Last Modified: Mon, 09 Jun 2025 22:19:29 GMT  
		Size: 28.7 MB (28738610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31718c26115b6a7913cdc7b31880af107a5250f8ed21e8e0a487886e86c638da`  
		Last Modified: Mon, 09 Jun 2025 22:19:30 GMT  
		Size: 16.5 KB (16463 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:446b7e7c0ee9571f99fc8d3e1ef435baf74bcc773df03e227aaf9324c4cfc487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.4 MB (398398505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3a318d716d43e4d58ff35bfb131e0c92a6d772bdc9b48a60c8b85cb45f3ab1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=noetic
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 07 Jun 2025 08:00:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfbcdfd0b57613941270f9d51dd852e2113c510314bc16442dac6b7ccd93bb4`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 4.1 KB (4051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85112d048ca69cba46cedbe7609be6b1388da46a96c5f25f3074b3d03ed5cada`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f86eac5764b45f84c9f74da912d260c33bea9dce19480b68f6d9e8d5c6b757`  
		Last Modified: Mon, 09 Jun 2025 22:32:16 GMT  
		Size: 361.4 MB (361381917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9cab4e76df8ec2a87814d4b7ac61519a9a8786d329cee9df51b06f8a16ae76`  
		Last Modified: Mon, 09 Jun 2025 21:45:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:b82397ddb14c1819024f3133edd632651900407665e47afb69a7a70ca4698c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 MB (29577759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00752124d606eab9110ae3b228009aec9a84d6e855f843d44c7f21d59e4b9f5`

```dockerfile
```

-	Layers:
	-	`sha256:1c5a7501f9ea236e6fed5cb2b25a2eac5942a034eb162f3a8571451242cfcce0`  
		Last Modified: Mon, 09 Jun 2025 22:19:59 GMT  
		Size: 29.6 MB (29561268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b13f1cc9ce0308d5c8ea9a10a3ad42a6fa44f30f50c2e5bd97d8b926ac07b0c9`  
		Last Modified: Mon, 09 Jun 2025 22:20:00 GMT  
		Size: 16.5 KB (16491 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:fd6279f04e51fa61201a791da9a156129941887b95b614ae0cec7865ef49de4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:4c1435fd85be3edde3820f0d132ab30a6b030209dce4fa3ac428a2aa5a763caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.2 MB (409194642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9281103cce09d925abe6b7134ab3c5b7bb9158e57a2204c51175217dda4dfe9a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=noetic
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 07 Jun 2025 08:00:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da4792f7f416db06c00bc26bb845d00bd1c6f16f3e10a4c7d0031c91656aa3e`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 1.2 MB (1194841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20358ca2eb5aafdeb52607c52f0c03ee909a919235fc1041db00d58da1c59b6`  
		Last Modified: Mon, 09 Jun 2025 21:17:15 GMT  
		Size: 10.0 MB (9982583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dce350d6ea44ccf7fac3a7bdda0989aca3a6b72ffbfc14104e3b18810c2de33`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 4.0 KB (4045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ca0507171d76ea79443c6b48e8e4038c3555f8ca12aef4cd82ca0ca7a43786`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cc10980325859d6423bbc515001cb577760dc73999bb2e18e811a24877c5cb`  
		Last Modified: Mon, 09 Jun 2025 21:38:06 GMT  
		Size: 370.5 MB (370502304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6932d16c264574201be5a55ba79dd248dab8a2a0a32b8cdf30af3e1c5e86f806`  
		Last Modified: Mon, 09 Jun 2025 21:17:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:acff80a38330a5a31d0736188c6f91a6220386cb22d5b19408f60acc98cd582b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29781814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c24c58ac29d31ce7d0aa7430c667961e4b5181a5e91efb301ac607f0ca640f9`

```dockerfile
```

-	Layers:
	-	`sha256:bf597893336763c20337f61fa235a39c41a481325d1f6a9ab15bb920f947b93a`  
		Last Modified: Mon, 09 Jun 2025 22:18:58 GMT  
		Size: 29.8 MB (29765457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4da31b4968be25636f6e96bc2ce17cbed293aecc74937629fce47cca4065560`  
		Last Modified: Mon, 09 Jun 2025 22:19:00 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:c9e79028edfa3207701777e232184aa095648173286b93c3b19d9a97d3d6c654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.7 MB (261696848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caab418962bcabcb4389a9852474cf889e69a8d8d42aed069ceadf6e08e87170`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:45:56 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:45:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:45:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:45:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:45:59 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 08 Apr 2025 10:45:59 GMT
CMD ["/bin/bash"]
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=noetic
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 07 Jun 2025 08:00:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Thu, 08 May 2025 17:24:17 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfcc4cfce76b5bf1c5a2d77d213c53e381bd6af934ace80b7dd575fae26fbc2`  
		Last Modified: Mon, 09 Jun 2025 21:26:48 GMT  
		Size: 1.2 MB (1194843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbedf4f0754ca72166025a791ca6d481ebf5eabf3a71098223375b9e239ab5e`  
		Last Modified: Mon, 09 Jun 2025 21:26:50 GMT  
		Size: 8.5 MB (8495172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b93f56f8bb23cd9397a52b8507218a13ec5c99454df623bcb512756c0e3b65c`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 4.0 KB (4046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d92492254010b5a5b3b8e25ef8ec55aa5095c585ca3229bc0eeef8d85b8360`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24987496e81c5b0ad1b96e1e2aa860aa62af52099656d4f90b854a1ea854ef88`  
		Last Modified: Mon, 09 Jun 2025 22:21:50 GMT  
		Size: 228.4 MB (228378250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d5d7d2be5c7ee349e5b07c644259548f6e8ab647d692c695bb392c00cc8ee0`  
		Last Modified: Mon, 09 Jun 2025 21:26:49 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:4c3fe52db1c08dad3c7b6b220a14c86045074042d36e2c837dc2e40edd56be00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28755073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fb167ab0b004a48773cd9ba1e91987d02409e11ceb243fab07138e5769e8b6`

```dockerfile
```

-	Layers:
	-	`sha256:345b20852b51b4b6a90c0fabf2ca2dd4375862857d3eae23f1cfb10b7c447edb`  
		Last Modified: Mon, 09 Jun 2025 22:19:29 GMT  
		Size: 28.7 MB (28738610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31718c26115b6a7913cdc7b31880af107a5250f8ed21e8e0a487886e86c638da`  
		Last Modified: Mon, 09 Jun 2025 22:19:30 GMT  
		Size: 16.5 KB (16463 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:446b7e7c0ee9571f99fc8d3e1ef435baf74bcc773df03e227aaf9324c4cfc487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.4 MB (398398505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3a318d716d43e4d58ff35bfb131e0c92a6d772bdc9b48a60c8b85cb45f3ab1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN set -eux;        key='4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-snapshots-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-snapshots-archive-keyring.gpg ] http://snapshots.ros.org/noetic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros1-snapshots.list # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LANG=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV LC_ALL=C.UTF-8
# Sat, 07 Jun 2025 08:00:06 GMT
ENV ROS_DISTRO=noetic
# Sat, 07 Jun 2025 08:00:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Sat, 07 Jun 2025 08:00:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 07 Jun 2025 08:00:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319399392fed996cb432aafbbb08c95cf91e53ae1976fe24cd4dc8d638ab251`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 1.2 MB (1194699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fec1006c3522403b0feafac48aeded8531636ac44d158910db311cb217659`  
		Last Modified: Mon, 09 Jun 2025 21:21:56 GMT  
		Size: 9.8 MB (9839701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfbcdfd0b57613941270f9d51dd852e2113c510314bc16442dac6b7ccd93bb4`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 4.1 KB (4051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85112d048ca69cba46cedbe7609be6b1388da46a96c5f25f3074b3d03ed5cada`  
		Last Modified: Mon, 09 Jun 2025 21:45:16 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f86eac5764b45f84c9f74da912d260c33bea9dce19480b68f6d9e8d5c6b757`  
		Last Modified: Mon, 09 Jun 2025 22:32:16 GMT  
		Size: 361.4 MB (361381917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9cab4e76df8ec2a87814d4b7ac61519a9a8786d329cee9df51b06f8a16ae76`  
		Last Modified: Mon, 09 Jun 2025 21:45:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:b82397ddb14c1819024f3133edd632651900407665e47afb69a7a70ca4698c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 MB (29577759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00752124d606eab9110ae3b228009aec9a84d6e855f843d44c7f21d59e4b9f5`

```dockerfile
```

-	Layers:
	-	`sha256:1c5a7501f9ea236e6fed5cb2b25a2eac5942a034eb162f3a8571451242cfcce0`  
		Last Modified: Mon, 09 Jun 2025 22:19:59 GMT  
		Size: 29.6 MB (29561268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b13f1cc9ce0308d5c8ea9a10a3ad42a6fa44f30f50c2e5bd97d8b926ac07b0c9`  
		Last Modified: Mon, 09 Jun 2025 22:20:00 GMT  
		Size: 16.5 KB (16491 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling`

```console
$ docker pull ros@sha256:210a32e27f2854fa97f4910aa2265562055c2d3002120c477be75d89b389888b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:3feb4d69ed93992d7b49d271a71b5575d5bed5ab646ba6ee38cae9aa87ea2d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (296048190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fab77d160612f877741cfa7217a58fbf732fa6e04cb87c1677d3099554378f0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfec2bd3b8a8f3149ca52fdd8464cc064b20a97e958bb5eb957e5b7915305000`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 683.8 KB (683801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fd1b31239b2b35443682de4bbe0887e0c643f5eb132ac575e10939de024389`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 6.7 MB (6745479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca0363a0b27809e7e539adb870f5b03b5ca8f2306972a10b327fb08237cbc8d`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 94.0 KB (94040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230eccfcfedb004370eed4e1c1f60b458a47d4e95994d4a128760d0914abca62`  
		Last Modified: Tue, 03 Jun 2025 17:07:49 GMT  
		Size: 120.3 MB (120308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6969676f34d01f0babe0b34b6b856a9a446b5d4eb7c892d7518f26d14ddaf5ee`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3954bf150c0d49e6d74db1a5d2b4d6570c4ab4c65b9a577104b7ac61566b3a7e`  
		Last Modified: Tue, 03 Jun 2025 17:09:36 GMT  
		Size: 110.2 MB (110182190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceba3bab3f8fe24c8fc9585595879d8f6f868ecd6478ad3709275d08bdb302d3`  
		Last Modified: Tue, 03 Jun 2025 17:09:27 GMT  
		Size: 345.2 KB (345211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533a6a75acc942e5de996b2186911beebd15b860314a71ba703deaa5f6aeba1e`  
		Last Modified: Tue, 03 Jun 2025 17:09:27 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c847ce82317f1f015c442ef92e2df42c44e8c72d961ad6f436cacb503d5e2d5a`  
		Last Modified: Tue, 03 Jun 2025 17:09:36 GMT  
		Size: 28.0 MB (27970572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:d12aa3b7b2860bd76e7c37125a978c76407f9e8899d03b3519f991a3c99be949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23946088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a8b5933fdceaca79bfac2a1e642bbdf669cfe8e0ca31bb38c1c96bc6f59e68`

```dockerfile
```

-	Layers:
	-	`sha256:fd68cca3fb2a8359b6c5502c5ae0f5c4ad9f6fbce5a6bc6aa1c2561c3e85e39e`  
		Last Modified: Tue, 03 Jun 2025 19:18:49 GMT  
		Size: 23.9 MB (23929680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ad97f7d0e94501e41311e0a13f5f9448eff468493dbe14cff6cebfd5580061`  
		Last Modified: Tue, 03 Jun 2025 19:18:50 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c79cb507b64b5e5d2acd3ec68b4a747dcc5412c57294f68f7719f7e87256f13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284464321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9969b2710279ec1fdd20d9c86a9c21998a4f7ff51370779f5672006cd53a130f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd2483f06750140b5ef1d9528213984e55b6d22ec6260f43ebb6d9d32604e64`  
		Last Modified: Tue, 03 Jun 2025 16:24:19 GMT  
		Size: 115.1 MB (115069346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ff94e561c546a1336514aa0a8683915423278ab9bf7fdc6580fcff40f64e26`  
		Last Modified: Tue, 03 Jun 2025 16:24:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ee15e60a6b4f2e94d7ea44ffadb43de986c57c1efd5949178c6e8ca09725bf`  
		Last Modified: Tue, 03 Jun 2025 17:15:35 GMT  
		Size: 105.6 MB (105595486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba8562f5f48d7a0d879f6d9ddad45ef49cf00bf690ac7ef334d9c9ce7091bbc`  
		Last Modified: Tue, 03 Jun 2025 17:15:08 GMT  
		Size: 345.2 KB (345215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b24a6aa92e176ae9c16c4107cbfeb29fd061d0e6317e95406c3218cf08e96`  
		Last Modified: Tue, 03 Jun 2025 17:15:07 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523672174b6d88922a7eebb2d1ebfb5361bc77559dd09c08f9c9cbe7a855604b`  
		Last Modified: Tue, 03 Jun 2025 17:15:11 GMT  
		Size: 27.1 MB (27062440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling` - unknown; unknown

```console
$ docker pull ros@sha256:f52d6a9683dd216f453d7a84993eb06e167f1673899d162f7bf563374856bf63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23968479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d53578bd2e08e4da5213cf3b8c39a375fe5b31803b68e31a2224f10056eb99`

```dockerfile
```

-	Layers:
	-	`sha256:df243a2905387e1ee40b1b029748969b91330661a6e2103637c4887b5eefa6ad`  
		Last Modified: Tue, 03 Jun 2025 19:19:07 GMT  
		Size: 24.0 MB (23951934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f8cc75fd28906bd9b5bf5e51326b5018e70937186fc5ba45f288792b9386bff`  
		Last Modified: Tue, 03 Jun 2025 19:19:08 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:798a723225796a1bea8735d954a38035bb946cbeee11c71640db01677d92ea8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:dcc537033332d0b6d529fcccc8cec6d8dc1f36f9989411faa05b2db621124c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1076852624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7afaeb0f6fda19fcbdf3f1dbc88ef35e35af0cb057e4e6b3175b5a71d2b376`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfec2bd3b8a8f3149ca52fdd8464cc064b20a97e958bb5eb957e5b7915305000`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 683.8 KB (683801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fd1b31239b2b35443682de4bbe0887e0c643f5eb132ac575e10939de024389`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 6.7 MB (6745479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca0363a0b27809e7e539adb870f5b03b5ca8f2306972a10b327fb08237cbc8d`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 94.0 KB (94040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230eccfcfedb004370eed4e1c1f60b458a47d4e95994d4a128760d0914abca62`  
		Last Modified: Tue, 03 Jun 2025 17:07:49 GMT  
		Size: 120.3 MB (120308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6969676f34d01f0babe0b34b6b856a9a446b5d4eb7c892d7518f26d14ddaf5ee`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3954bf150c0d49e6d74db1a5d2b4d6570c4ab4c65b9a577104b7ac61566b3a7e`  
		Last Modified: Tue, 03 Jun 2025 17:09:36 GMT  
		Size: 110.2 MB (110182190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceba3bab3f8fe24c8fc9585595879d8f6f868ecd6478ad3709275d08bdb302d3`  
		Last Modified: Tue, 03 Jun 2025 17:09:27 GMT  
		Size: 345.2 KB (345211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533a6a75acc942e5de996b2186911beebd15b860314a71ba703deaa5f6aeba1e`  
		Last Modified: Tue, 03 Jun 2025 17:09:27 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c847ce82317f1f015c442ef92e2df42c44e8c72d961ad6f436cacb503d5e2d5a`  
		Last Modified: Tue, 03 Jun 2025 17:09:36 GMT  
		Size: 28.0 MB (27970572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10db0817839e16c700162efb170904730f0a5f267c8b1dfb02132ae47cace6ae`  
		Last Modified: Tue, 03 Jun 2025 19:22:31 GMT  
		Size: 780.8 MB (780804434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:4639866a8c7e89c0627770661bce6147387c4460994d2063f1f9a8b90a703b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59845326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6adc09ae99fb26a1a7c4010d6965a055c8f4f38fed6d35d370b24450344de616`

```dockerfile
```

-	Layers:
	-	`sha256:3eeb62ea365d75d0b41c42c28a1718ccfb2b7c215ac219e276340a34770697b7`  
		Last Modified: Tue, 03 Jun 2025 19:18:55 GMT  
		Size: 59.8 MB (59835922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86825c66abef002e8378d3a94a98d2030e186d2c2388d5f0a48386f23a076619`  
		Last Modified: Tue, 03 Jun 2025 19:18:57 GMT  
		Size: 9.4 KB (9404 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cd2169194fa099dbd8f1e3a2ee6b8ce97e195846976927493208fb6ced657c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **975.5 MB (975499606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98cba738a75cf8b2c8c5677e9e1f984253f10844ae2a5fdc712b8e5a6b69082`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd2483f06750140b5ef1d9528213984e55b6d22ec6260f43ebb6d9d32604e64`  
		Last Modified: Tue, 03 Jun 2025 16:24:19 GMT  
		Size: 115.1 MB (115069346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ff94e561c546a1336514aa0a8683915423278ab9bf7fdc6580fcff40f64e26`  
		Last Modified: Tue, 03 Jun 2025 16:24:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ee15e60a6b4f2e94d7ea44ffadb43de986c57c1efd5949178c6e8ca09725bf`  
		Last Modified: Tue, 03 Jun 2025 17:15:35 GMT  
		Size: 105.6 MB (105595486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba8562f5f48d7a0d879f6d9ddad45ef49cf00bf690ac7ef334d9c9ce7091bbc`  
		Last Modified: Tue, 03 Jun 2025 17:15:08 GMT  
		Size: 345.2 KB (345215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b24a6aa92e176ae9c16c4107cbfeb29fd061d0e6317e95406c3218cf08e96`  
		Last Modified: Tue, 03 Jun 2025 17:15:07 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523672174b6d88922a7eebb2d1ebfb5361bc77559dd09c08f9c9cbe7a855604b`  
		Last Modified: Tue, 03 Jun 2025 17:15:11 GMT  
		Size: 27.1 MB (27062440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10971441dcc1bf6a5bd937e6f581e951b5c355290b9aef4eede1272cd6736eea`  
		Last Modified: Fri, 06 Jun 2025 13:56:56 GMT  
		Size: 691.0 MB (691035285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception` - unknown; unknown

```console
$ docker pull ros@sha256:be61bcfdc93c74a523bfcf94742a01a90344c0bbe930967c91e7159912114a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59797071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00515e5dac7750558c15a136132a6d448db12534485b39a213c26ead1efa735e`

```dockerfile
```

-	Layers:
	-	`sha256:931685824977a3f5db5072a45968a8f852d5b5acffd76251688e161a5ea5dbec`  
		Last Modified: Tue, 03 Jun 2025 19:20:43 GMT  
		Size: 59.8 MB (59787587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8588f456d0c75104e9c4cfe44540e8294ed344675783209e1e46b80f0c9e389`  
		Last Modified: Tue, 03 Jun 2025 19:20:45 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:798a723225796a1bea8735d954a38035bb946cbeee11c71640db01677d92ea8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:dcc537033332d0b6d529fcccc8cec6d8dc1f36f9989411faa05b2db621124c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1076852624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7afaeb0f6fda19fcbdf3f1dbc88ef35e35af0cb057e4e6b3175b5a71d2b376`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfec2bd3b8a8f3149ca52fdd8464cc064b20a97e958bb5eb957e5b7915305000`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 683.8 KB (683801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fd1b31239b2b35443682de4bbe0887e0c643f5eb132ac575e10939de024389`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 6.7 MB (6745479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca0363a0b27809e7e539adb870f5b03b5ca8f2306972a10b327fb08237cbc8d`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 94.0 KB (94040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230eccfcfedb004370eed4e1c1f60b458a47d4e95994d4a128760d0914abca62`  
		Last Modified: Tue, 03 Jun 2025 17:07:49 GMT  
		Size: 120.3 MB (120308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6969676f34d01f0babe0b34b6b856a9a446b5d4eb7c892d7518f26d14ddaf5ee`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3954bf150c0d49e6d74db1a5d2b4d6570c4ab4c65b9a577104b7ac61566b3a7e`  
		Last Modified: Tue, 03 Jun 2025 17:09:36 GMT  
		Size: 110.2 MB (110182190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceba3bab3f8fe24c8fc9585595879d8f6f868ecd6478ad3709275d08bdb302d3`  
		Last Modified: Tue, 03 Jun 2025 17:09:27 GMT  
		Size: 345.2 KB (345211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533a6a75acc942e5de996b2186911beebd15b860314a71ba703deaa5f6aeba1e`  
		Last Modified: Tue, 03 Jun 2025 17:09:27 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c847ce82317f1f015c442ef92e2df42c44e8c72d961ad6f436cacb503d5e2d5a`  
		Last Modified: Tue, 03 Jun 2025 17:09:36 GMT  
		Size: 28.0 MB (27970572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10db0817839e16c700162efb170904730f0a5f267c8b1dfb02132ae47cace6ae`  
		Last Modified: Tue, 03 Jun 2025 19:22:31 GMT  
		Size: 780.8 MB (780804434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:4639866a8c7e89c0627770661bce6147387c4460994d2063f1f9a8b90a703b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59845326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6adc09ae99fb26a1a7c4010d6965a055c8f4f38fed6d35d370b24450344de616`

```dockerfile
```

-	Layers:
	-	`sha256:3eeb62ea365d75d0b41c42c28a1718ccfb2b7c215ac219e276340a34770697b7`  
		Last Modified: Tue, 03 Jun 2025 19:18:55 GMT  
		Size: 59.8 MB (59835922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86825c66abef002e8378d3a94a98d2030e186d2c2388d5f0a48386f23a076619`  
		Last Modified: Tue, 03 Jun 2025 19:18:57 GMT  
		Size: 9.4 KB (9404 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cd2169194fa099dbd8f1e3a2ee6b8ce97e195846976927493208fb6ced657c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **975.5 MB (975499606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98cba738a75cf8b2c8c5677e9e1f984253f10844ae2a5fdc712b8e5a6b69082`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd2483f06750140b5ef1d9528213984e55b6d22ec6260f43ebb6d9d32604e64`  
		Last Modified: Tue, 03 Jun 2025 16:24:19 GMT  
		Size: 115.1 MB (115069346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ff94e561c546a1336514aa0a8683915423278ab9bf7fdc6580fcff40f64e26`  
		Last Modified: Tue, 03 Jun 2025 16:24:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ee15e60a6b4f2e94d7ea44ffadb43de986c57c1efd5949178c6e8ca09725bf`  
		Last Modified: Tue, 03 Jun 2025 17:15:35 GMT  
		Size: 105.6 MB (105595486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba8562f5f48d7a0d879f6d9ddad45ef49cf00bf690ac7ef334d9c9ce7091bbc`  
		Last Modified: Tue, 03 Jun 2025 17:15:08 GMT  
		Size: 345.2 KB (345215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b24a6aa92e176ae9c16c4107cbfeb29fd061d0e6317e95406c3218cf08e96`  
		Last Modified: Tue, 03 Jun 2025 17:15:07 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523672174b6d88922a7eebb2d1ebfb5361bc77559dd09c08f9c9cbe7a855604b`  
		Last Modified: Tue, 03 Jun 2025 17:15:11 GMT  
		Size: 27.1 MB (27062440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10971441dcc1bf6a5bd937e6f581e951b5c355290b9aef4eede1272cd6736eea`  
		Last Modified: Fri, 06 Jun 2025 13:56:56 GMT  
		Size: 691.0 MB (691035285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-perception-noble` - unknown; unknown

```console
$ docker pull ros@sha256:be61bcfdc93c74a523bfcf94742a01a90344c0bbe930967c91e7159912114a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59797071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00515e5dac7750558c15a136132a6d448db12534485b39a213c26ead1efa735e`

```dockerfile
```

-	Layers:
	-	`sha256:931685824977a3f5db5072a45968a8f852d5b5acffd76251688e161a5ea5dbec`  
		Last Modified: Tue, 03 Jun 2025 19:20:43 GMT  
		Size: 59.8 MB (59787587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8588f456d0c75104e9c4cfe44540e8294ed344675783209e1e46b80f0c9e389`  
		Last Modified: Tue, 03 Jun 2025 19:20:45 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:210a32e27f2854fa97f4910aa2265562055c2d3002120c477be75d89b389888b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:3feb4d69ed93992d7b49d271a71b5575d5bed5ab646ba6ee38cae9aa87ea2d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (296048190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fab77d160612f877741cfa7217a58fbf732fa6e04cb87c1677d3099554378f0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfec2bd3b8a8f3149ca52fdd8464cc064b20a97e958bb5eb957e5b7915305000`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 683.8 KB (683801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fd1b31239b2b35443682de4bbe0887e0c643f5eb132ac575e10939de024389`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 6.7 MB (6745479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca0363a0b27809e7e539adb870f5b03b5ca8f2306972a10b327fb08237cbc8d`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 94.0 KB (94040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230eccfcfedb004370eed4e1c1f60b458a47d4e95994d4a128760d0914abca62`  
		Last Modified: Tue, 03 Jun 2025 17:07:49 GMT  
		Size: 120.3 MB (120308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6969676f34d01f0babe0b34b6b856a9a446b5d4eb7c892d7518f26d14ddaf5ee`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3954bf150c0d49e6d74db1a5d2b4d6570c4ab4c65b9a577104b7ac61566b3a7e`  
		Last Modified: Tue, 03 Jun 2025 17:09:36 GMT  
		Size: 110.2 MB (110182190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceba3bab3f8fe24c8fc9585595879d8f6f868ecd6478ad3709275d08bdb302d3`  
		Last Modified: Tue, 03 Jun 2025 17:09:27 GMT  
		Size: 345.2 KB (345211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533a6a75acc942e5de996b2186911beebd15b860314a71ba703deaa5f6aeba1e`  
		Last Modified: Tue, 03 Jun 2025 17:09:27 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c847ce82317f1f015c442ef92e2df42c44e8c72d961ad6f436cacb503d5e2d5a`  
		Last Modified: Tue, 03 Jun 2025 17:09:36 GMT  
		Size: 28.0 MB (27970572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:d12aa3b7b2860bd76e7c37125a978c76407f9e8899d03b3519f991a3c99be949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23946088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a8b5933fdceaca79bfac2a1e642bbdf669cfe8e0ca31bb38c1c96bc6f59e68`

```dockerfile
```

-	Layers:
	-	`sha256:fd68cca3fb2a8359b6c5502c5ae0f5c4ad9f6fbce5a6bc6aa1c2561c3e85e39e`  
		Last Modified: Tue, 03 Jun 2025 19:18:49 GMT  
		Size: 23.9 MB (23929680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ad97f7d0e94501e41311e0a13f5f9448eff468493dbe14cff6cebfd5580061`  
		Last Modified: Tue, 03 Jun 2025 19:18:50 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c79cb507b64b5e5d2acd3ec68b4a747dcc5412c57294f68f7719f7e87256f13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284464321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9969b2710279ec1fdd20d9c86a9c21998a4f7ff51370779f5672006cd53a130f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd2483f06750140b5ef1d9528213984e55b6d22ec6260f43ebb6d9d32604e64`  
		Last Modified: Tue, 03 Jun 2025 16:24:19 GMT  
		Size: 115.1 MB (115069346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ff94e561c546a1336514aa0a8683915423278ab9bf7fdc6580fcff40f64e26`  
		Last Modified: Tue, 03 Jun 2025 16:24:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ee15e60a6b4f2e94d7ea44ffadb43de986c57c1efd5949178c6e8ca09725bf`  
		Last Modified: Tue, 03 Jun 2025 17:15:35 GMT  
		Size: 105.6 MB (105595486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba8562f5f48d7a0d879f6d9ddad45ef49cf00bf690ac7ef334d9c9ce7091bbc`  
		Last Modified: Tue, 03 Jun 2025 17:15:08 GMT  
		Size: 345.2 KB (345215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b24a6aa92e176ae9c16c4107cbfeb29fd061d0e6317e95406c3218cf08e96`  
		Last Modified: Tue, 03 Jun 2025 17:15:07 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523672174b6d88922a7eebb2d1ebfb5361bc77559dd09c08f9c9cbe7a855604b`  
		Last Modified: Tue, 03 Jun 2025 17:15:11 GMT  
		Size: 27.1 MB (27062440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:f52d6a9683dd216f453d7a84993eb06e167f1673899d162f7bf563374856bf63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23968479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d53578bd2e08e4da5213cf3b8c39a375fe5b31803b68e31a2224f10056eb99`

```dockerfile
```

-	Layers:
	-	`sha256:df243a2905387e1ee40b1b029748969b91330661a6e2103637c4887b5eefa6ad`  
		Last Modified: Tue, 03 Jun 2025 19:19:07 GMT  
		Size: 24.0 MB (23951934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f8cc75fd28906bd9b5bf5e51326b5018e70937186fc5ba45f288792b9386bff`  
		Last Modified: Tue, 03 Jun 2025 19:19:08 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:210a32e27f2854fa97f4910aa2265562055c2d3002120c477be75d89b389888b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:3feb4d69ed93992d7b49d271a71b5575d5bed5ab646ba6ee38cae9aa87ea2d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (296048190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fab77d160612f877741cfa7217a58fbf732fa6e04cb87c1677d3099554378f0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfec2bd3b8a8f3149ca52fdd8464cc064b20a97e958bb5eb957e5b7915305000`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 683.8 KB (683801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fd1b31239b2b35443682de4bbe0887e0c643f5eb132ac575e10939de024389`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 6.7 MB (6745479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca0363a0b27809e7e539adb870f5b03b5ca8f2306972a10b327fb08237cbc8d`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 94.0 KB (94040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230eccfcfedb004370eed4e1c1f60b458a47d4e95994d4a128760d0914abca62`  
		Last Modified: Tue, 03 Jun 2025 17:07:49 GMT  
		Size: 120.3 MB (120308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6969676f34d01f0babe0b34b6b856a9a446b5d4eb7c892d7518f26d14ddaf5ee`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3954bf150c0d49e6d74db1a5d2b4d6570c4ab4c65b9a577104b7ac61566b3a7e`  
		Last Modified: Tue, 03 Jun 2025 17:09:36 GMT  
		Size: 110.2 MB (110182190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceba3bab3f8fe24c8fc9585595879d8f6f868ecd6478ad3709275d08bdb302d3`  
		Last Modified: Tue, 03 Jun 2025 17:09:27 GMT  
		Size: 345.2 KB (345211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533a6a75acc942e5de996b2186911beebd15b860314a71ba703deaa5f6aeba1e`  
		Last Modified: Tue, 03 Jun 2025 17:09:27 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c847ce82317f1f015c442ef92e2df42c44e8c72d961ad6f436cacb503d5e2d5a`  
		Last Modified: Tue, 03 Jun 2025 17:09:36 GMT  
		Size: 28.0 MB (27970572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:d12aa3b7b2860bd76e7c37125a978c76407f9e8899d03b3519f991a3c99be949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23946088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a8b5933fdceaca79bfac2a1e642bbdf669cfe8e0ca31bb38c1c96bc6f59e68`

```dockerfile
```

-	Layers:
	-	`sha256:fd68cca3fb2a8359b6c5502c5ae0f5c4ad9f6fbce5a6bc6aa1c2561c3e85e39e`  
		Last Modified: Tue, 03 Jun 2025 19:18:49 GMT  
		Size: 23.9 MB (23929680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ad97f7d0e94501e41311e0a13f5f9448eff468493dbe14cff6cebfd5580061`  
		Last Modified: Tue, 03 Jun 2025 19:18:50 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c79cb507b64b5e5d2acd3ec68b4a747dcc5412c57294f68f7719f7e87256f13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284464321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9969b2710279ec1fdd20d9c86a9c21998a4f7ff51370779f5672006cd53a130f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:53:23 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:53:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:53:23 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 10 Feb 2025 08:53:23 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:53:23 GMT
ENV ROS_DISTRO=rolling
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:53:23 GMT
CMD ["bash"]
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update # buildkit
# Mon, 10 Feb 2025 08:53:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd2483f06750140b5ef1d9528213984e55b6d22ec6260f43ebb6d9d32604e64`  
		Last Modified: Tue, 03 Jun 2025 16:24:19 GMT  
		Size: 115.1 MB (115069346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ff94e561c546a1336514aa0a8683915423278ab9bf7fdc6580fcff40f64e26`  
		Last Modified: Tue, 03 Jun 2025 16:24:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ee15e60a6b4f2e94d7ea44ffadb43de986c57c1efd5949178c6e8ca09725bf`  
		Last Modified: Tue, 03 Jun 2025 17:15:35 GMT  
		Size: 105.6 MB (105595486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba8562f5f48d7a0d879f6d9ddad45ef49cf00bf690ac7ef334d9c9ce7091bbc`  
		Last Modified: Tue, 03 Jun 2025 17:15:08 GMT  
		Size: 345.2 KB (345215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b24a6aa92e176ae9c16c4107cbfeb29fd061d0e6317e95406c3218cf08e96`  
		Last Modified: Tue, 03 Jun 2025 17:15:07 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523672174b6d88922a7eebb2d1ebfb5361bc77559dd09c08f9c9cbe7a855604b`  
		Last Modified: Tue, 03 Jun 2025 17:15:11 GMT  
		Size: 27.1 MB (27062440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-base-noble` - unknown; unknown

```console
$ docker pull ros@sha256:f52d6a9683dd216f453d7a84993eb06e167f1673899d162f7bf563374856bf63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23968479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d53578bd2e08e4da5213cf3b8c39a375fe5b31803b68e31a2224f10056eb99`

```dockerfile
```

-	Layers:
	-	`sha256:df243a2905387e1ee40b1b029748969b91330661a6e2103637c4887b5eefa6ad`  
		Last Modified: Tue, 03 Jun 2025 19:19:07 GMT  
		Size: 24.0 MB (23951934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f8cc75fd28906bd9b5bf5e51326b5018e70937186fc5ba45f288792b9386bff`  
		Last Modified: Tue, 03 Jun 2025 19:19:08 GMT  
		Size: 16.5 KB (16545 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:4916f3a1119ae50707f18b391f095af128cdcde73c7aa18a7ebb1a284a042474
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:0bc569c5ef8866372fb294e4045789a9455227d78065fdc6778d2e83b09b3aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157547754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6047aa36c852fcef58a62938b9b30427639d22360d6836cd42911401f752cb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=rolling
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfec2bd3b8a8f3149ca52fdd8464cc064b20a97e958bb5eb957e5b7915305000`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 683.8 KB (683801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fd1b31239b2b35443682de4bbe0887e0c643f5eb132ac575e10939de024389`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 6.7 MB (6745479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca0363a0b27809e7e539adb870f5b03b5ca8f2306972a10b327fb08237cbc8d`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 94.0 KB (94040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230eccfcfedb004370eed4e1c1f60b458a47d4e95994d4a128760d0914abca62`  
		Last Modified: Tue, 03 Jun 2025 17:07:49 GMT  
		Size: 120.3 MB (120308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6969676f34d01f0babe0b34b6b856a9a446b5d4eb7c892d7518f26d14ddaf5ee`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:777a5cc6a5a933045b71d5310f876eb58d1ade80508ef6f3b82ddf7417b5f73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17868091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2169d46452102ab16701d1974a1108a95946646bd2c0b2af79f98844d060c37e`

```dockerfile
```

-	Layers:
	-	`sha256:085d71fe61e31ba0a0081cb03a1de8fc5988895d50bdedd5f283f44998bb408c`  
		Last Modified: Tue, 03 Jun 2025 19:19:01 GMT  
		Size: 17.9 MB (17853427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84d36cd23ed47bd955ccf4d7556ba3f06680a0f8780337329dafc01b2f0e8af6`  
		Last Modified: Tue, 03 Jun 2025 19:19:02 GMT  
		Size: 14.7 KB (14664 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9773c590fdd55b0af001bedbe3b95414ba89809b06c05955e63b0efe16343f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151458684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cd6aa4cd7559ddc99287153004c4429cd2b2c38ab0175faa145030f166e4e8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=rolling
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd2483f06750140b5ef1d9528213984e55b6d22ec6260f43ebb6d9d32604e64`  
		Last Modified: Tue, 03 Jun 2025 16:24:19 GMT  
		Size: 115.1 MB (115069346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ff94e561c546a1336514aa0a8683915423278ab9bf7fdc6580fcff40f64e26`  
		Last Modified: Tue, 03 Jun 2025 16:24:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:900520548ee44ab74f8b8b7b3d02a170b8c5f7bae444534405699db4ed6e0ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854a5d361e7db4a3535476538e06211edb3a2e7b5aeb84ed9545d899e618eac0`

```dockerfile
```

-	Layers:
	-	`sha256:a787b6b14c8b7a7c9ade9112e7b9c5aee4128c6a17014c3d3a3e9c739a9668a7`  
		Last Modified: Tue, 03 Jun 2025 19:19:17 GMT  
		Size: 17.8 MB (17827433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d9fd8f7a6bcee5eac879ee871298baeffca21fa21516e9d7a57c846a320f91a`  
		Last Modified: Tue, 03 Jun 2025 19:19:17 GMT  
		Size: 14.8 KB (14790 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:4916f3a1119ae50707f18b391f095af128cdcde73c7aa18a7ebb1a284a042474
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:0bc569c5ef8866372fb294e4045789a9455227d78065fdc6778d2e83b09b3aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157547754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6047aa36c852fcef58a62938b9b30427639d22360d6836cd42911401f752cb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=rolling
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfec2bd3b8a8f3149ca52fdd8464cc064b20a97e958bb5eb957e5b7915305000`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 683.8 KB (683801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fd1b31239b2b35443682de4bbe0887e0c643f5eb132ac575e10939de024389`  
		Last Modified: Tue, 03 Jun 2025 17:07:42 GMT  
		Size: 6.7 MB (6745479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca0363a0b27809e7e539adb870f5b03b5ca8f2306972a10b327fb08237cbc8d`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 94.0 KB (94040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230eccfcfedb004370eed4e1c1f60b458a47d4e95994d4a128760d0914abca62`  
		Last Modified: Tue, 03 Jun 2025 17:07:49 GMT  
		Size: 120.3 MB (120308902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6969676f34d01f0babe0b34b6b856a9a446b5d4eb7c892d7518f26d14ddaf5ee`  
		Last Modified: Tue, 03 Jun 2025 17:07:41 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:777a5cc6a5a933045b71d5310f876eb58d1ade80508ef6f3b82ddf7417b5f73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17868091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2169d46452102ab16701d1974a1108a95946646bd2c0b2af79f98844d060c37e`

```dockerfile
```

-	Layers:
	-	`sha256:085d71fe61e31ba0a0081cb03a1de8fc5988895d50bdedd5f283f44998bb408c`  
		Last Modified: Tue, 03 Jun 2025 19:19:01 GMT  
		Size: 17.9 MB (17853427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84d36cd23ed47bd955ccf4d7556ba3f06680a0f8780337329dafc01b2f0e8af6`  
		Last Modified: Tue, 03 Jun 2025 19:19:02 GMT  
		Size: 14.7 KB (14664 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9773c590fdd55b0af001bedbe3b95414ba89809b06c05955e63b0efe16343f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151458684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cd6aa4cd7559ddc99287153004c4429cd2b2c38ab0175faa145030f166e4e8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Tue, 03 Jun 2025 04:32:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     ca-certificates     curl     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
RUN curl -L -s -o /tmp/ros2-apt-source.deb https://github.com/ros-infrastructure/ros-apt-source/releases/download/1.1.0/ros2-apt-source_1.1.0.noble_all.deb     && echo "35441f3092fd05773a3c397fab38661bec466584c7a1f1c05366579997cb5fe7 /tmp/ros2-apt-source.deb" | sha256sum --strict --check     && apt-get update     && apt-get install /tmp/ros2-apt-source.deb     && rm -f /tmp/ros2-apt-source.deb     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Jun 2025 04:32:14 GMT
ENV ROS_DISTRO=rolling
# Tue, 03 Jun 2025 04:32:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.12.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Tue, 03 Jun 2025 04:32:14 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Jun 2025 04:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53fe1e2017fff7e98b20b2da2163f1490b2cf016eb94e1e8327d5e6133fed8`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 684.0 KB (683990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab34cb0b6b6e950f1d468b84aa6c011ff2c12764c125ea77d46032ffa46e1a`  
		Last Modified: Tue, 03 Jun 2025 16:21:49 GMT  
		Size: 6.8 MB (6759025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370382b92e73d710705f3a0ce8123b24b72c27c4fa225dda1a02672c744e317c`  
		Last Modified: Tue, 03 Jun 2025 16:21:47 GMT  
		Size: 94.2 KB (94228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd2483f06750140b5ef1d9528213984e55b6d22ec6260f43ebb6d9d32604e64`  
		Last Modified: Tue, 03 Jun 2025 16:24:19 GMT  
		Size: 115.1 MB (115069346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ff94e561c546a1336514aa0a8683915423278ab9bf7fdc6580fcff40f64e26`  
		Last Modified: Tue, 03 Jun 2025 16:24:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:rolling-ros-core-noble` - unknown; unknown

```console
$ docker pull ros@sha256:900520548ee44ab74f8b8b7b3d02a170b8c5f7bae444534405699db4ed6e0ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17842223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854a5d361e7db4a3535476538e06211edb3a2e7b5aeb84ed9545d899e618eac0`

```dockerfile
```

-	Layers:
	-	`sha256:a787b6b14c8b7a7c9ade9112e7b9c5aee4128c6a17014c3d3a3e9c739a9668a7`  
		Last Modified: Tue, 03 Jun 2025 19:19:17 GMT  
		Size: 17.8 MB (17827433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d9fd8f7a6bcee5eac879ee871298baeffca21fa21516e9d7a57c846a320f91a`  
		Last Modified: Tue, 03 Jun 2025 19:19:17 GMT  
		Size: 14.8 KB (14790 bytes)  
		MIME: application/vnd.in-toto+json
