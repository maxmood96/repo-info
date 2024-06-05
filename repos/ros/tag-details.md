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
-	[`ros:jazzy`](#rosjazzy)
-	[`ros:jazzy-perception`](#rosjazzy-perception)
-	[`ros:jazzy-perception-noble`](#rosjazzy-perception-noble)
-	[`ros:jazzy-ros-base`](#rosjazzy-ros-base)
-	[`ros:jazzy-ros-base-noble`](#rosjazzy-ros-base-noble)
-	[`ros:jazzy-ros-core`](#rosjazzy-ros-core)
-	[`ros:jazzy-ros-core-noble`](#rosjazzy-ros-core-noble)
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

## `ros:humble`

```console
$ docker pull ros@sha256:6982bbd69e78cf4008b2526d6f931219510eff723b55eae347052be4c8f19ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:29bbc51955f8a91963798e6280c1590266c228471ba0f8ddb78a41f9e9752b00
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.3 MB (263298656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17479423a3ae32772caa989bab03638da4d4b28941e741c7ed7e40cb85e7d088`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:53:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:53:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:53:35 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Jun 2024 05:55:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:55:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:55:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:55:25 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:56:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:56:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:56:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:57:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd8a5936f50eae12a88b5309a7de594460a6cf0c083562c45bbfaf2adc9a79f`  
		Last Modified: Wed, 05 Jun 2024 06:25:59 GMT  
		Size: 1.2 MB (1214743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa0ba2a85d3d446a820f12f96585c9af6c9ab8a6b478961fbb02d3907c0163a`  
		Last Modified: Wed, 05 Jun 2024 06:25:58 GMT  
		Size: 3.8 MB (3829597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca54b5ce5f2343afd4e77db2ceca0fcc8a71a8e5533981f969ecd86a66e9e9f8`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8030e81e3d2a09ca6a076294871304d566e86bed912d99d12e82f213fec4cc1d`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23269b6ea3b8c08068fc3d3fe7a01cc8bd003219a35aec775f12155e737d6cfd`  
		Last Modified: Wed, 05 Jun 2024 06:26:13 GMT  
		Size: 106.5 MB (106507928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f125e0532049fe2777507da2edb7b12c248da0a9d074fa3043ba1405b80a9b2`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4bc00ea17676350d16ec75b469e205e9415ebee3ab68473e595a6ad96c1cb0`  
		Last Modified: Wed, 05 Jun 2024 06:26:34 GMT  
		Size: 98.2 MB (98153054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb06de83a3792c1712e62dc67e451ebac0861c13efe8e5c7868db4005e73797`  
		Last Modified: Wed, 05 Jun 2024 06:26:22 GMT  
		Size: 324.7 KB (324740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cafd9f34a66cf722480d56c08a90d31c78896016d7a81945712ba94e121d26`  
		Last Modified: Wed, 05 Jun 2024 06:26:22 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9200aa16c06bb4b2ff18680d36f42006535265b5ac135148f7d7b907d93e29ac`  
		Last Modified: Wed, 05 Jun 2024 06:26:25 GMT  
		Size: 22.8 MB (22824392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:71693ebc082da36705b25072b77bb52a42a73d049602216ed3171b65a22700ea
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255937670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b561e5ec61535944a02403c32e8cebe3be847334f2b00d19153742f9bd234e6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:13:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:13:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Jun 2024 05:15:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:15:46 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:15:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:15:46 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:17:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:17:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:17:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:18:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f530a91a61927d0b4523bb8e4f14381cb7f7d9817c6204686d6bb5250cde836`  
		Last Modified: Wed, 05 Jun 2024 05:50:31 GMT  
		Size: 1.2 MB (1216480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a544f7ab76cc1c3437117889feb865f388e0c55099600b53c55efa34156f2fff`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 3.8 MB (3802894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f54cb7fba17b8889b6330bdd6ef5007d394b7fb9e815eb9f2af1fa6b936965`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a069ee1709898d9feb67e4cfe34cab6b60d1f4e6e228834e3605bee3deb8181`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7105d19b1f065fb946586c01532f71e7a80d63bd49f6aeec2acb29fbebb900f5`  
		Last Modified: Wed, 05 Jun 2024 05:50:49 GMT  
		Size: 104.2 MB (104236607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ed8cd760956e27b0b391e9870d1076fbf68380c0c71814d49120cd37d2bda9`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb4ccb2bbb7400a6f6044af60a4d3dcf2663a0871f005456042c23a61df3519`  
		Last Modified: Wed, 05 Jun 2024 05:51:08 GMT  
		Size: 95.7 MB (95713365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055b2579f4a3a4150c53593f639d9b51bd4acae4c72a1f06c1f66bc4b35f1fcd`  
		Last Modified: Wed, 05 Jun 2024 05:50:57 GMT  
		Size: 324.7 KB (324739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9743a79bf3af1d25fa2d5b114ba3d6a81f02966c6ead80289131d3de9e8452`  
		Last Modified: Wed, 05 Jun 2024 05:50:57 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b583dfc7042595ae5838b88a40d5feb0217901dde3b5ddac77e3b23c3c737573`  
		Last Modified: Wed, 05 Jun 2024 05:51:01 GMT  
		Size: 22.2 MB (22236354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception`

```console
$ docker pull ros@sha256:88b1c931214b198949a26df1b977c2b3ed7c4f1b4494e9cdb2b65e52aa3cef5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:9d0a234e8968e8c2fb6a372998640e8649f05a75aaa4587b9fd23e39c696d575
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.8 MB (954826606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa074b9ea856bbed471f1ba13bf6dbf77e569233c4fb365eb5c83e77db703366`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:53:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:53:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:53:35 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Jun 2024 05:55:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:55:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:55:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:55:25 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:56:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:56:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:56:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:57:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:06:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd8a5936f50eae12a88b5309a7de594460a6cf0c083562c45bbfaf2adc9a79f`  
		Last Modified: Wed, 05 Jun 2024 06:25:59 GMT  
		Size: 1.2 MB (1214743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa0ba2a85d3d446a820f12f96585c9af6c9ab8a6b478961fbb02d3907c0163a`  
		Last Modified: Wed, 05 Jun 2024 06:25:58 GMT  
		Size: 3.8 MB (3829597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca54b5ce5f2343afd4e77db2ceca0fcc8a71a8e5533981f969ecd86a66e9e9f8`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8030e81e3d2a09ca6a076294871304d566e86bed912d99d12e82f213fec4cc1d`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23269b6ea3b8c08068fc3d3fe7a01cc8bd003219a35aec775f12155e737d6cfd`  
		Last Modified: Wed, 05 Jun 2024 06:26:13 GMT  
		Size: 106.5 MB (106507928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f125e0532049fe2777507da2edb7b12c248da0a9d074fa3043ba1405b80a9b2`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4bc00ea17676350d16ec75b469e205e9415ebee3ab68473e595a6ad96c1cb0`  
		Last Modified: Wed, 05 Jun 2024 06:26:34 GMT  
		Size: 98.2 MB (98153054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb06de83a3792c1712e62dc67e451ebac0861c13efe8e5c7868db4005e73797`  
		Last Modified: Wed, 05 Jun 2024 06:26:22 GMT  
		Size: 324.7 KB (324740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cafd9f34a66cf722480d56c08a90d31c78896016d7a81945712ba94e121d26`  
		Last Modified: Wed, 05 Jun 2024 06:26:22 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9200aa16c06bb4b2ff18680d36f42006535265b5ac135148f7d7b907d93e29ac`  
		Last Modified: Wed, 05 Jun 2024 06:26:25 GMT  
		Size: 22.8 MB (22824392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152771a7549d5b98f375618ab9ffa808eb174baef69ee606887c9e0cdd336ae8`  
		Last Modified: Wed, 05 Jun 2024 06:28:12 GMT  
		Size: 691.5 MB (691527950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7aca638db11345349c18296c5585f4172c050026bc9b7d06dc7ec7087374e6f7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.4 MB (915363636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f111da1596b1936d3d6fd8a6862abe1c44c8c6248f2767f4aa6237156c4359e1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:13:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:13:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Jun 2024 05:15:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:15:46 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:15:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:15:46 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:17:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:17:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:17:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:18:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:28:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f530a91a61927d0b4523bb8e4f14381cb7f7d9817c6204686d6bb5250cde836`  
		Last Modified: Wed, 05 Jun 2024 05:50:31 GMT  
		Size: 1.2 MB (1216480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a544f7ab76cc1c3437117889feb865f388e0c55099600b53c55efa34156f2fff`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 3.8 MB (3802894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f54cb7fba17b8889b6330bdd6ef5007d394b7fb9e815eb9f2af1fa6b936965`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a069ee1709898d9feb67e4cfe34cab6b60d1f4e6e228834e3605bee3deb8181`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7105d19b1f065fb946586c01532f71e7a80d63bd49f6aeec2acb29fbebb900f5`  
		Last Modified: Wed, 05 Jun 2024 05:50:49 GMT  
		Size: 104.2 MB (104236607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ed8cd760956e27b0b391e9870d1076fbf68380c0c71814d49120cd37d2bda9`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb4ccb2bbb7400a6f6044af60a4d3dcf2663a0871f005456042c23a61df3519`  
		Last Modified: Wed, 05 Jun 2024 05:51:08 GMT  
		Size: 95.7 MB (95713365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055b2579f4a3a4150c53593f639d9b51bd4acae4c72a1f06c1f66bc4b35f1fcd`  
		Last Modified: Wed, 05 Jun 2024 05:50:57 GMT  
		Size: 324.7 KB (324739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9743a79bf3af1d25fa2d5b114ba3d6a81f02966c6ead80289131d3de9e8452`  
		Last Modified: Wed, 05 Jun 2024 05:50:57 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b583dfc7042595ae5838b88a40d5feb0217901dde3b5ddac77e3b23c3c737573`  
		Last Modified: Wed, 05 Jun 2024 05:51:01 GMT  
		Size: 22.2 MB (22236354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e980cefc24b629cab20b19ac33c713392ca4ff4e769fd68864936c072e2c1c6`  
		Last Modified: Wed, 05 Jun 2024 05:52:40 GMT  
		Size: 659.4 MB (659425966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:88b1c931214b198949a26df1b977c2b3ed7c4f1b4494e9cdb2b65e52aa3cef5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:9d0a234e8968e8c2fb6a372998640e8649f05a75aaa4587b9fd23e39c696d575
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.8 MB (954826606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa074b9ea856bbed471f1ba13bf6dbf77e569233c4fb365eb5c83e77db703366`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:53:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:53:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:53:35 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Jun 2024 05:55:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:55:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:55:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:55:25 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:56:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:56:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:56:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:57:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:06:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd8a5936f50eae12a88b5309a7de594460a6cf0c083562c45bbfaf2adc9a79f`  
		Last Modified: Wed, 05 Jun 2024 06:25:59 GMT  
		Size: 1.2 MB (1214743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa0ba2a85d3d446a820f12f96585c9af6c9ab8a6b478961fbb02d3907c0163a`  
		Last Modified: Wed, 05 Jun 2024 06:25:58 GMT  
		Size: 3.8 MB (3829597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca54b5ce5f2343afd4e77db2ceca0fcc8a71a8e5533981f969ecd86a66e9e9f8`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8030e81e3d2a09ca6a076294871304d566e86bed912d99d12e82f213fec4cc1d`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23269b6ea3b8c08068fc3d3fe7a01cc8bd003219a35aec775f12155e737d6cfd`  
		Last Modified: Wed, 05 Jun 2024 06:26:13 GMT  
		Size: 106.5 MB (106507928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f125e0532049fe2777507da2edb7b12c248da0a9d074fa3043ba1405b80a9b2`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4bc00ea17676350d16ec75b469e205e9415ebee3ab68473e595a6ad96c1cb0`  
		Last Modified: Wed, 05 Jun 2024 06:26:34 GMT  
		Size: 98.2 MB (98153054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb06de83a3792c1712e62dc67e451ebac0861c13efe8e5c7868db4005e73797`  
		Last Modified: Wed, 05 Jun 2024 06:26:22 GMT  
		Size: 324.7 KB (324740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cafd9f34a66cf722480d56c08a90d31c78896016d7a81945712ba94e121d26`  
		Last Modified: Wed, 05 Jun 2024 06:26:22 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9200aa16c06bb4b2ff18680d36f42006535265b5ac135148f7d7b907d93e29ac`  
		Last Modified: Wed, 05 Jun 2024 06:26:25 GMT  
		Size: 22.8 MB (22824392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152771a7549d5b98f375618ab9ffa808eb174baef69ee606887c9e0cdd336ae8`  
		Last Modified: Wed, 05 Jun 2024 06:28:12 GMT  
		Size: 691.5 MB (691527950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7aca638db11345349c18296c5585f4172c050026bc9b7d06dc7ec7087374e6f7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.4 MB (915363636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f111da1596b1936d3d6fd8a6862abe1c44c8c6248f2767f4aa6237156c4359e1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:13:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:13:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Jun 2024 05:15:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:15:46 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:15:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:15:46 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:17:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:17:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:17:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:18:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:28:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f530a91a61927d0b4523bb8e4f14381cb7f7d9817c6204686d6bb5250cde836`  
		Last Modified: Wed, 05 Jun 2024 05:50:31 GMT  
		Size: 1.2 MB (1216480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a544f7ab76cc1c3437117889feb865f388e0c55099600b53c55efa34156f2fff`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 3.8 MB (3802894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f54cb7fba17b8889b6330bdd6ef5007d394b7fb9e815eb9f2af1fa6b936965`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a069ee1709898d9feb67e4cfe34cab6b60d1f4e6e228834e3605bee3deb8181`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7105d19b1f065fb946586c01532f71e7a80d63bd49f6aeec2acb29fbebb900f5`  
		Last Modified: Wed, 05 Jun 2024 05:50:49 GMT  
		Size: 104.2 MB (104236607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ed8cd760956e27b0b391e9870d1076fbf68380c0c71814d49120cd37d2bda9`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb4ccb2bbb7400a6f6044af60a4d3dcf2663a0871f005456042c23a61df3519`  
		Last Modified: Wed, 05 Jun 2024 05:51:08 GMT  
		Size: 95.7 MB (95713365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055b2579f4a3a4150c53593f639d9b51bd4acae4c72a1f06c1f66bc4b35f1fcd`  
		Last Modified: Wed, 05 Jun 2024 05:50:57 GMT  
		Size: 324.7 KB (324739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9743a79bf3af1d25fa2d5b114ba3d6a81f02966c6ead80289131d3de9e8452`  
		Last Modified: Wed, 05 Jun 2024 05:50:57 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b583dfc7042595ae5838b88a40d5feb0217901dde3b5ddac77e3b23c3c737573`  
		Last Modified: Wed, 05 Jun 2024 05:51:01 GMT  
		Size: 22.2 MB (22236354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e980cefc24b629cab20b19ac33c713392ca4ff4e769fd68864936c072e2c1c6`  
		Last Modified: Wed, 05 Jun 2024 05:52:40 GMT  
		Size: 659.4 MB (659425966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:6982bbd69e78cf4008b2526d6f931219510eff723b55eae347052be4c8f19ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:29bbc51955f8a91963798e6280c1590266c228471ba0f8ddb78a41f9e9752b00
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.3 MB (263298656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17479423a3ae32772caa989bab03638da4d4b28941e741c7ed7e40cb85e7d088`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:53:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:53:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:53:35 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Jun 2024 05:55:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:55:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:55:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:55:25 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:56:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:56:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:56:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:57:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd8a5936f50eae12a88b5309a7de594460a6cf0c083562c45bbfaf2adc9a79f`  
		Last Modified: Wed, 05 Jun 2024 06:25:59 GMT  
		Size: 1.2 MB (1214743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa0ba2a85d3d446a820f12f96585c9af6c9ab8a6b478961fbb02d3907c0163a`  
		Last Modified: Wed, 05 Jun 2024 06:25:58 GMT  
		Size: 3.8 MB (3829597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca54b5ce5f2343afd4e77db2ceca0fcc8a71a8e5533981f969ecd86a66e9e9f8`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8030e81e3d2a09ca6a076294871304d566e86bed912d99d12e82f213fec4cc1d`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23269b6ea3b8c08068fc3d3fe7a01cc8bd003219a35aec775f12155e737d6cfd`  
		Last Modified: Wed, 05 Jun 2024 06:26:13 GMT  
		Size: 106.5 MB (106507928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f125e0532049fe2777507da2edb7b12c248da0a9d074fa3043ba1405b80a9b2`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4bc00ea17676350d16ec75b469e205e9415ebee3ab68473e595a6ad96c1cb0`  
		Last Modified: Wed, 05 Jun 2024 06:26:34 GMT  
		Size: 98.2 MB (98153054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb06de83a3792c1712e62dc67e451ebac0861c13efe8e5c7868db4005e73797`  
		Last Modified: Wed, 05 Jun 2024 06:26:22 GMT  
		Size: 324.7 KB (324740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cafd9f34a66cf722480d56c08a90d31c78896016d7a81945712ba94e121d26`  
		Last Modified: Wed, 05 Jun 2024 06:26:22 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9200aa16c06bb4b2ff18680d36f42006535265b5ac135148f7d7b907d93e29ac`  
		Last Modified: Wed, 05 Jun 2024 06:26:25 GMT  
		Size: 22.8 MB (22824392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:71693ebc082da36705b25072b77bb52a42a73d049602216ed3171b65a22700ea
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255937670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b561e5ec61535944a02403c32e8cebe3be847334f2b00d19153742f9bd234e6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:13:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:13:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Jun 2024 05:15:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:15:46 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:15:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:15:46 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:17:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:17:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:17:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:18:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f530a91a61927d0b4523bb8e4f14381cb7f7d9817c6204686d6bb5250cde836`  
		Last Modified: Wed, 05 Jun 2024 05:50:31 GMT  
		Size: 1.2 MB (1216480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a544f7ab76cc1c3437117889feb865f388e0c55099600b53c55efa34156f2fff`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 3.8 MB (3802894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f54cb7fba17b8889b6330bdd6ef5007d394b7fb9e815eb9f2af1fa6b936965`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a069ee1709898d9feb67e4cfe34cab6b60d1f4e6e228834e3605bee3deb8181`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7105d19b1f065fb946586c01532f71e7a80d63bd49f6aeec2acb29fbebb900f5`  
		Last Modified: Wed, 05 Jun 2024 05:50:49 GMT  
		Size: 104.2 MB (104236607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ed8cd760956e27b0b391e9870d1076fbf68380c0c71814d49120cd37d2bda9`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb4ccb2bbb7400a6f6044af60a4d3dcf2663a0871f005456042c23a61df3519`  
		Last Modified: Wed, 05 Jun 2024 05:51:08 GMT  
		Size: 95.7 MB (95713365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055b2579f4a3a4150c53593f639d9b51bd4acae4c72a1f06c1f66bc4b35f1fcd`  
		Last Modified: Wed, 05 Jun 2024 05:50:57 GMT  
		Size: 324.7 KB (324739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9743a79bf3af1d25fa2d5b114ba3d6a81f02966c6ead80289131d3de9e8452`  
		Last Modified: Wed, 05 Jun 2024 05:50:57 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b583dfc7042595ae5838b88a40d5feb0217901dde3b5ddac77e3b23c3c737573`  
		Last Modified: Wed, 05 Jun 2024 05:51:01 GMT  
		Size: 22.2 MB (22236354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:6982bbd69e78cf4008b2526d6f931219510eff723b55eae347052be4c8f19ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:29bbc51955f8a91963798e6280c1590266c228471ba0f8ddb78a41f9e9752b00
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.3 MB (263298656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17479423a3ae32772caa989bab03638da4d4b28941e741c7ed7e40cb85e7d088`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:53:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:53:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:53:35 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Jun 2024 05:55:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:55:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:55:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:55:25 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:56:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:56:39 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:56:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:57:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd8a5936f50eae12a88b5309a7de594460a6cf0c083562c45bbfaf2adc9a79f`  
		Last Modified: Wed, 05 Jun 2024 06:25:59 GMT  
		Size: 1.2 MB (1214743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa0ba2a85d3d446a820f12f96585c9af6c9ab8a6b478961fbb02d3907c0163a`  
		Last Modified: Wed, 05 Jun 2024 06:25:58 GMT  
		Size: 3.8 MB (3829597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca54b5ce5f2343afd4e77db2ceca0fcc8a71a8e5533981f969ecd86a66e9e9f8`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8030e81e3d2a09ca6a076294871304d566e86bed912d99d12e82f213fec4cc1d`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23269b6ea3b8c08068fc3d3fe7a01cc8bd003219a35aec775f12155e737d6cfd`  
		Last Modified: Wed, 05 Jun 2024 06:26:13 GMT  
		Size: 106.5 MB (106507928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f125e0532049fe2777507da2edb7b12c248da0a9d074fa3043ba1405b80a9b2`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4bc00ea17676350d16ec75b469e205e9415ebee3ab68473e595a6ad96c1cb0`  
		Last Modified: Wed, 05 Jun 2024 06:26:34 GMT  
		Size: 98.2 MB (98153054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb06de83a3792c1712e62dc67e451ebac0861c13efe8e5c7868db4005e73797`  
		Last Modified: Wed, 05 Jun 2024 06:26:22 GMT  
		Size: 324.7 KB (324740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cafd9f34a66cf722480d56c08a90d31c78896016d7a81945712ba94e121d26`  
		Last Modified: Wed, 05 Jun 2024 06:26:22 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9200aa16c06bb4b2ff18680d36f42006535265b5ac135148f7d7b907d93e29ac`  
		Last Modified: Wed, 05 Jun 2024 06:26:25 GMT  
		Size: 22.8 MB (22824392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:71693ebc082da36705b25072b77bb52a42a73d049602216ed3171b65a22700ea
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255937670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b561e5ec61535944a02403c32e8cebe3be847334f2b00d19153742f9bd234e6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:13:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:13:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Jun 2024 05:15:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:15:46 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:15:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:15:46 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:17:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:17:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:17:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:18:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f530a91a61927d0b4523bb8e4f14381cb7f7d9817c6204686d6bb5250cde836`  
		Last Modified: Wed, 05 Jun 2024 05:50:31 GMT  
		Size: 1.2 MB (1216480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a544f7ab76cc1c3437117889feb865f388e0c55099600b53c55efa34156f2fff`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 3.8 MB (3802894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f54cb7fba17b8889b6330bdd6ef5007d394b7fb9e815eb9f2af1fa6b936965`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a069ee1709898d9feb67e4cfe34cab6b60d1f4e6e228834e3605bee3deb8181`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7105d19b1f065fb946586c01532f71e7a80d63bd49f6aeec2acb29fbebb900f5`  
		Last Modified: Wed, 05 Jun 2024 05:50:49 GMT  
		Size: 104.2 MB (104236607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ed8cd760956e27b0b391e9870d1076fbf68380c0c71814d49120cd37d2bda9`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb4ccb2bbb7400a6f6044af60a4d3dcf2663a0871f005456042c23a61df3519`  
		Last Modified: Wed, 05 Jun 2024 05:51:08 GMT  
		Size: 95.7 MB (95713365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055b2579f4a3a4150c53593f639d9b51bd4acae4c72a1f06c1f66bc4b35f1fcd`  
		Last Modified: Wed, 05 Jun 2024 05:50:57 GMT  
		Size: 324.7 KB (324739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9743a79bf3af1d25fa2d5b114ba3d6a81f02966c6ead80289131d3de9e8452`  
		Last Modified: Wed, 05 Jun 2024 05:50:57 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b583dfc7042595ae5838b88a40d5feb0217901dde3b5ddac77e3b23c3c737573`  
		Last Modified: Wed, 05 Jun 2024 05:51:01 GMT  
		Size: 22.2 MB (22236354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:d1505884e26c595d0410f4da743ace5ee0d5e8261a6006607dcdbf605d971eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:55bb3916b01217b7274926908328b69ae5c14c75deff49f74f8a9551a7068847
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141994039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2f6be46ffd1566129e707f61e72a52a8551fa520ad81f992959fcd252ed89e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:53:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:53:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:53:35 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Jun 2024 05:55:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:55:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:55:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:55:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd8a5936f50eae12a88b5309a7de594460a6cf0c083562c45bbfaf2adc9a79f`  
		Last Modified: Wed, 05 Jun 2024 06:25:59 GMT  
		Size: 1.2 MB (1214743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa0ba2a85d3d446a820f12f96585c9af6c9ab8a6b478961fbb02d3907c0163a`  
		Last Modified: Wed, 05 Jun 2024 06:25:58 GMT  
		Size: 3.8 MB (3829597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca54b5ce5f2343afd4e77db2ceca0fcc8a71a8e5533981f969ecd86a66e9e9f8`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8030e81e3d2a09ca6a076294871304d566e86bed912d99d12e82f213fec4cc1d`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23269b6ea3b8c08068fc3d3fe7a01cc8bd003219a35aec775f12155e737d6cfd`  
		Last Modified: Wed, 05 Jun 2024 06:26:13 GMT  
		Size: 106.5 MB (106507928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f125e0532049fe2777507da2edb7b12c248da0a9d074fa3043ba1405b80a9b2`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4c0165a6efc1c0756d8145889db522dc01fe6cb2710649478ce65e2eadc6c426
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137660776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1eee9fb6b724836f7969a80a2e20c7f6af017352d17cc0bd538120cc9d4993`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:13:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:13:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Jun 2024 05:15:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:15:46 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:15:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:15:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f530a91a61927d0b4523bb8e4f14381cb7f7d9817c6204686d6bb5250cde836`  
		Last Modified: Wed, 05 Jun 2024 05:50:31 GMT  
		Size: 1.2 MB (1216480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a544f7ab76cc1c3437117889feb865f388e0c55099600b53c55efa34156f2fff`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 3.8 MB (3802894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f54cb7fba17b8889b6330bdd6ef5007d394b7fb9e815eb9f2af1fa6b936965`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a069ee1709898d9feb67e4cfe34cab6b60d1f4e6e228834e3605bee3deb8181`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7105d19b1f065fb946586c01532f71e7a80d63bd49f6aeec2acb29fbebb900f5`  
		Last Modified: Wed, 05 Jun 2024 05:50:49 GMT  
		Size: 104.2 MB (104236607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ed8cd760956e27b0b391e9870d1076fbf68380c0c71814d49120cd37d2bda9`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:d1505884e26c595d0410f4da743ace5ee0d5e8261a6006607dcdbf605d971eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:55bb3916b01217b7274926908328b69ae5c14c75deff49f74f8a9551a7068847
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141994039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2f6be46ffd1566129e707f61e72a52a8551fa520ad81f992959fcd252ed89e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:53:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:53:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:53:35 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Jun 2024 05:55:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:55:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:55:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:55:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd8a5936f50eae12a88b5309a7de594460a6cf0c083562c45bbfaf2adc9a79f`  
		Last Modified: Wed, 05 Jun 2024 06:25:59 GMT  
		Size: 1.2 MB (1214743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa0ba2a85d3d446a820f12f96585c9af6c9ab8a6b478961fbb02d3907c0163a`  
		Last Modified: Wed, 05 Jun 2024 06:25:58 GMT  
		Size: 3.8 MB (3829597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca54b5ce5f2343afd4e77db2ceca0fcc8a71a8e5533981f969ecd86a66e9e9f8`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8030e81e3d2a09ca6a076294871304d566e86bed912d99d12e82f213fec4cc1d`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23269b6ea3b8c08068fc3d3fe7a01cc8bd003219a35aec775f12155e737d6cfd`  
		Last Modified: Wed, 05 Jun 2024 06:26:13 GMT  
		Size: 106.5 MB (106507928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f125e0532049fe2777507da2edb7b12c248da0a9d074fa3043ba1405b80a9b2`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4c0165a6efc1c0756d8145889db522dc01fe6cb2710649478ce65e2eadc6c426
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137660776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1eee9fb6b724836f7969a80a2e20c7f6af017352d17cc0bd538120cc9d4993`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:13:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:13:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Jun 2024 05:15:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:15:46 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:15:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:15:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f530a91a61927d0b4523bb8e4f14381cb7f7d9817c6204686d6bb5250cde836`  
		Last Modified: Wed, 05 Jun 2024 05:50:31 GMT  
		Size: 1.2 MB (1216480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a544f7ab76cc1c3437117889feb865f388e0c55099600b53c55efa34156f2fff`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 3.8 MB (3802894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f54cb7fba17b8889b6330bdd6ef5007d394b7fb9e815eb9f2af1fa6b936965`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a069ee1709898d9feb67e4cfe34cab6b60d1f4e6e228834e3605bee3deb8181`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7105d19b1f065fb946586c01532f71e7a80d63bd49f6aeec2acb29fbebb900f5`  
		Last Modified: Wed, 05 Jun 2024 05:50:49 GMT  
		Size: 104.2 MB (104236607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ed8cd760956e27b0b391e9870d1076fbf68380c0c71814d49120cd37d2bda9`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron`

```console
$ docker pull ros@sha256:0378be3497950bc286f262175e4463b50fdb7636cb9e002de58ed88710108da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron` - linux; amd64

```console
$ docker pull ros@sha256:1227ae73b097a51eb8245196671eb9bf4ea87ba1b0d91e8b146f2c05ed9e0ffa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268976942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93319acb40698b522723f30da8790e735d3be23457e217eff21ae50962895ab5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:53:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:53:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:53:35 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:06:24 GMT
ENV ROS_DISTRO=iron
# Wed, 05 Jun 2024 06:07:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:07:16 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:07:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:07:16 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 06:07:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:07:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 06:07:48 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 06:08:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd8a5936f50eae12a88b5309a7de594460a6cf0c083562c45bbfaf2adc9a79f`  
		Last Modified: Wed, 05 Jun 2024 06:25:59 GMT  
		Size: 1.2 MB (1214743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa0ba2a85d3d446a820f12f96585c9af6c9ab8a6b478961fbb02d3907c0163a`  
		Last Modified: Wed, 05 Jun 2024 06:25:58 GMT  
		Size: 3.8 MB (3829597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca54b5ce5f2343afd4e77db2ceca0fcc8a71a8e5533981f969ecd86a66e9e9f8`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8030e81e3d2a09ca6a076294871304d566e86bed912d99d12e82f213fec4cc1d`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa54e95d67c63dbf0cf8f753642cfe16d08165c0ef6bd6d75b0b04dbca492494`  
		Last Modified: Wed, 05 Jun 2024 06:28:41 GMT  
		Size: 124.3 MB (124271471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e178042e3b461503d611ef9ed1a289773f1b1cc2d271d007759b4d512390717a`  
		Last Modified: Wed, 05 Jun 2024 06:28:22 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f521d7494e3239c1ec45905b8a7e715d6967d11a327a565c4b0a35c5495b3901`  
		Last Modified: Wed, 05 Jun 2024 06:28:59 GMT  
		Size: 85.2 MB (85175274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f413fb95df485200b05df4effea1b1bffced12132eea05565570079cb17c38`  
		Last Modified: Wed, 05 Jun 2024 06:28:49 GMT  
		Size: 307.3 KB (307303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c4739db608ffd3b9933d1078a6f304391353159f79b516964267a0448f5c6e`  
		Last Modified: Wed, 05 Jun 2024 06:28:48 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78400d29e519e86a1c1f3a22bdd8d20687db690193fa5e65e03a2d2d11fbc85a`  
		Last Modified: Wed, 05 Jun 2024 06:28:52 GMT  
		Size: 23.7 MB (23734349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4677fc2e545662f89a0d1db753b5c9fd6d27c026a0a81d28377e16f65f8f055d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261473724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4dbb5c04fbe23aff1e594f0ee5e6cf77e76ef0a644cf6c3cc620b8f313d138`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:13:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:13:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:29:03 GMT
ENV ROS_DISTRO=iron
# Wed, 05 Jun 2024 05:29:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:29:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:29:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:29:53 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:30:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:30:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:30:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:30:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f530a91a61927d0b4523bb8e4f14381cb7f7d9817c6204686d6bb5250cde836`  
		Last Modified: Wed, 05 Jun 2024 05:50:31 GMT  
		Size: 1.2 MB (1216480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a544f7ab76cc1c3437117889feb865f388e0c55099600b53c55efa34156f2fff`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 3.8 MB (3802894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f54cb7fba17b8889b6330bdd6ef5007d394b7fb9e815eb9f2af1fa6b936965`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a069ee1709898d9feb67e4cfe34cab6b60d1f4e6e228834e3605bee3deb8181`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2e13045d4af22e2a09809ec5ad219bd0e69a32734c4302f98ed338a2ae3aae`  
		Last Modified: Wed, 05 Jun 2024 05:53:14 GMT  
		Size: 121.8 MB (121755785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ad376ac5d1a80d5e0f2c80959f053279c8ed358dde21e81fc687d3c864da7d`  
		Last Modified: Wed, 05 Jun 2024 05:52:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5e7c41deb8f9091e8fa011990bd0a3b57899972d538c4f92315133e5d13329`  
		Last Modified: Wed, 05 Jun 2024 05:53:34 GMT  
		Size: 82.9 MB (82860356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3deb503a6253699d5696d173dbae99c360e2ac7fa4666593353684bcee661e`  
		Last Modified: Wed, 05 Jun 2024 05:53:25 GMT  
		Size: 307.3 KB (307309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a94888eadc41fa54800510db3a24c90d9eabee89b8c83dd3827ab70ebec4e3e`  
		Last Modified: Wed, 05 Jun 2024 05:53:25 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67a7a87e96e5242bc809c27af71b6767d1eda0469965c8ebb996ae755fd5246`  
		Last Modified: Wed, 05 Jun 2024 05:53:30 GMT  
		Size: 23.1 MB (23123653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-perception`

```console
$ docker pull ros@sha256:123ce28c485c1325d6e36937d522cbed3db0cca83a74ece1af210c587375d17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception` - linux; amd64

```console
$ docker pull ros@sha256:09215169254ce1cb0623545841259f026b6ca6da5ec290531e7e8fb102c7a04c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.2 MB (961180345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1314827c82b35a3b683d1b5c45a7f8e2df3df19cf643db4f2720babe162361e9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:53:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:53:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:53:35 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:06:24 GMT
ENV ROS_DISTRO=iron
# Wed, 05 Jun 2024 06:07:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:07:16 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:07:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:07:16 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 06:07:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:07:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 06:07:48 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 06:08:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:09:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd8a5936f50eae12a88b5309a7de594460a6cf0c083562c45bbfaf2adc9a79f`  
		Last Modified: Wed, 05 Jun 2024 06:25:59 GMT  
		Size: 1.2 MB (1214743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa0ba2a85d3d446a820f12f96585c9af6c9ab8a6b478961fbb02d3907c0163a`  
		Last Modified: Wed, 05 Jun 2024 06:25:58 GMT  
		Size: 3.8 MB (3829597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca54b5ce5f2343afd4e77db2ceca0fcc8a71a8e5533981f969ecd86a66e9e9f8`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8030e81e3d2a09ca6a076294871304d566e86bed912d99d12e82f213fec4cc1d`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa54e95d67c63dbf0cf8f753642cfe16d08165c0ef6bd6d75b0b04dbca492494`  
		Last Modified: Wed, 05 Jun 2024 06:28:41 GMT  
		Size: 124.3 MB (124271471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e178042e3b461503d611ef9ed1a289773f1b1cc2d271d007759b4d512390717a`  
		Last Modified: Wed, 05 Jun 2024 06:28:22 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f521d7494e3239c1ec45905b8a7e715d6967d11a327a565c4b0a35c5495b3901`  
		Last Modified: Wed, 05 Jun 2024 06:28:59 GMT  
		Size: 85.2 MB (85175274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f413fb95df485200b05df4effea1b1bffced12132eea05565570079cb17c38`  
		Last Modified: Wed, 05 Jun 2024 06:28:49 GMT  
		Size: 307.3 KB (307303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c4739db608ffd3b9933d1078a6f304391353159f79b516964267a0448f5c6e`  
		Last Modified: Wed, 05 Jun 2024 06:28:48 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78400d29e519e86a1c1f3a22bdd8d20687db690193fa5e65e03a2d2d11fbc85a`  
		Last Modified: Wed, 05 Jun 2024 06:28:52 GMT  
		Size: 23.7 MB (23734349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f598db92475b5d6b206ffcd7ba13c02c6a3107bb13080042791c3136e73721`  
		Last Modified: Wed, 05 Jun 2024 06:30:38 GMT  
		Size: 692.2 MB (692203403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:83c8cada098357e7c08c7690bab7d76eaf6d93879cadd6bd595806273f8c44c7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.5 MB (921549166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3b5803398dce674c6354f0b7360ef78e95c2a60beec3cec58d4dc4c4aba33c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:13:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:13:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:29:03 GMT
ENV ROS_DISTRO=iron
# Wed, 05 Jun 2024 05:29:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:29:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:29:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:29:53 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:30:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:30:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:30:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:30:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:32:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f530a91a61927d0b4523bb8e4f14381cb7f7d9817c6204686d6bb5250cde836`  
		Last Modified: Wed, 05 Jun 2024 05:50:31 GMT  
		Size: 1.2 MB (1216480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a544f7ab76cc1c3437117889feb865f388e0c55099600b53c55efa34156f2fff`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 3.8 MB (3802894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f54cb7fba17b8889b6330bdd6ef5007d394b7fb9e815eb9f2af1fa6b936965`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a069ee1709898d9feb67e4cfe34cab6b60d1f4e6e228834e3605bee3deb8181`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2e13045d4af22e2a09809ec5ad219bd0e69a32734c4302f98ed338a2ae3aae`  
		Last Modified: Wed, 05 Jun 2024 05:53:14 GMT  
		Size: 121.8 MB (121755785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ad376ac5d1a80d5e0f2c80959f053279c8ed358dde21e81fc687d3c864da7d`  
		Last Modified: Wed, 05 Jun 2024 05:52:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5e7c41deb8f9091e8fa011990bd0a3b57899972d538c4f92315133e5d13329`  
		Last Modified: Wed, 05 Jun 2024 05:53:34 GMT  
		Size: 82.9 MB (82860356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3deb503a6253699d5696d173dbae99c360e2ac7fa4666593353684bcee661e`  
		Last Modified: Wed, 05 Jun 2024 05:53:25 GMT  
		Size: 307.3 KB (307309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a94888eadc41fa54800510db3a24c90d9eabee89b8c83dd3827ab70ebec4e3e`  
		Last Modified: Wed, 05 Jun 2024 05:53:25 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67a7a87e96e5242bc809c27af71b6767d1eda0469965c8ebb996ae755fd5246`  
		Last Modified: Wed, 05 Jun 2024 05:53:30 GMT  
		Size: 23.1 MB (23123653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4a1c356e28a759cd22138855e1714348c6dc76eb5b640f561e77323e86bdc0`  
		Last Modified: Wed, 05 Jun 2024 05:55:07 GMT  
		Size: 660.1 MB (660075442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:123ce28c485c1325d6e36937d522cbed3db0cca83a74ece1af210c587375d17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:09215169254ce1cb0623545841259f026b6ca6da5ec290531e7e8fb102c7a04c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.2 MB (961180345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1314827c82b35a3b683d1b5c45a7f8e2df3df19cf643db4f2720babe162361e9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:53:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:53:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:53:35 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:06:24 GMT
ENV ROS_DISTRO=iron
# Wed, 05 Jun 2024 06:07:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:07:16 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:07:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:07:16 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 06:07:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:07:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 06:07:48 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 06:08:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:09:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd8a5936f50eae12a88b5309a7de594460a6cf0c083562c45bbfaf2adc9a79f`  
		Last Modified: Wed, 05 Jun 2024 06:25:59 GMT  
		Size: 1.2 MB (1214743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa0ba2a85d3d446a820f12f96585c9af6c9ab8a6b478961fbb02d3907c0163a`  
		Last Modified: Wed, 05 Jun 2024 06:25:58 GMT  
		Size: 3.8 MB (3829597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca54b5ce5f2343afd4e77db2ceca0fcc8a71a8e5533981f969ecd86a66e9e9f8`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8030e81e3d2a09ca6a076294871304d566e86bed912d99d12e82f213fec4cc1d`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa54e95d67c63dbf0cf8f753642cfe16d08165c0ef6bd6d75b0b04dbca492494`  
		Last Modified: Wed, 05 Jun 2024 06:28:41 GMT  
		Size: 124.3 MB (124271471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e178042e3b461503d611ef9ed1a289773f1b1cc2d271d007759b4d512390717a`  
		Last Modified: Wed, 05 Jun 2024 06:28:22 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f521d7494e3239c1ec45905b8a7e715d6967d11a327a565c4b0a35c5495b3901`  
		Last Modified: Wed, 05 Jun 2024 06:28:59 GMT  
		Size: 85.2 MB (85175274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f413fb95df485200b05df4effea1b1bffced12132eea05565570079cb17c38`  
		Last Modified: Wed, 05 Jun 2024 06:28:49 GMT  
		Size: 307.3 KB (307303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c4739db608ffd3b9933d1078a6f304391353159f79b516964267a0448f5c6e`  
		Last Modified: Wed, 05 Jun 2024 06:28:48 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78400d29e519e86a1c1f3a22bdd8d20687db690193fa5e65e03a2d2d11fbc85a`  
		Last Modified: Wed, 05 Jun 2024 06:28:52 GMT  
		Size: 23.7 MB (23734349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f598db92475b5d6b206ffcd7ba13c02c6a3107bb13080042791c3136e73721`  
		Last Modified: Wed, 05 Jun 2024 06:30:38 GMT  
		Size: 692.2 MB (692203403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:83c8cada098357e7c08c7690bab7d76eaf6d93879cadd6bd595806273f8c44c7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.5 MB (921549166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3b5803398dce674c6354f0b7360ef78e95c2a60beec3cec58d4dc4c4aba33c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:13:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:13:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:29:03 GMT
ENV ROS_DISTRO=iron
# Wed, 05 Jun 2024 05:29:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:29:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:29:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:29:53 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:30:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:30:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:30:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:30:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:32:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f530a91a61927d0b4523bb8e4f14381cb7f7d9817c6204686d6bb5250cde836`  
		Last Modified: Wed, 05 Jun 2024 05:50:31 GMT  
		Size: 1.2 MB (1216480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a544f7ab76cc1c3437117889feb865f388e0c55099600b53c55efa34156f2fff`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 3.8 MB (3802894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f54cb7fba17b8889b6330bdd6ef5007d394b7fb9e815eb9f2af1fa6b936965`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a069ee1709898d9feb67e4cfe34cab6b60d1f4e6e228834e3605bee3deb8181`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2e13045d4af22e2a09809ec5ad219bd0e69a32734c4302f98ed338a2ae3aae`  
		Last Modified: Wed, 05 Jun 2024 05:53:14 GMT  
		Size: 121.8 MB (121755785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ad376ac5d1a80d5e0f2c80959f053279c8ed358dde21e81fc687d3c864da7d`  
		Last Modified: Wed, 05 Jun 2024 05:52:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5e7c41deb8f9091e8fa011990bd0a3b57899972d538c4f92315133e5d13329`  
		Last Modified: Wed, 05 Jun 2024 05:53:34 GMT  
		Size: 82.9 MB (82860356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3deb503a6253699d5696d173dbae99c360e2ac7fa4666593353684bcee661e`  
		Last Modified: Wed, 05 Jun 2024 05:53:25 GMT  
		Size: 307.3 KB (307309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a94888eadc41fa54800510db3a24c90d9eabee89b8c83dd3827ab70ebec4e3e`  
		Last Modified: Wed, 05 Jun 2024 05:53:25 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67a7a87e96e5242bc809c27af71b6767d1eda0469965c8ebb996ae755fd5246`  
		Last Modified: Wed, 05 Jun 2024 05:53:30 GMT  
		Size: 23.1 MB (23123653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4a1c356e28a759cd22138855e1714348c6dc76eb5b640f561e77323e86bdc0`  
		Last Modified: Wed, 05 Jun 2024 05:55:07 GMT  
		Size: 660.1 MB (660075442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-base`

```console
$ docker pull ros@sha256:0378be3497950bc286f262175e4463b50fdb7636cb9e002de58ed88710108da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:1227ae73b097a51eb8245196671eb9bf4ea87ba1b0d91e8b146f2c05ed9e0ffa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268976942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93319acb40698b522723f30da8790e735d3be23457e217eff21ae50962895ab5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:53:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:53:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:53:35 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:06:24 GMT
ENV ROS_DISTRO=iron
# Wed, 05 Jun 2024 06:07:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:07:16 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:07:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:07:16 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 06:07:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:07:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 06:07:48 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 06:08:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd8a5936f50eae12a88b5309a7de594460a6cf0c083562c45bbfaf2adc9a79f`  
		Last Modified: Wed, 05 Jun 2024 06:25:59 GMT  
		Size: 1.2 MB (1214743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa0ba2a85d3d446a820f12f96585c9af6c9ab8a6b478961fbb02d3907c0163a`  
		Last Modified: Wed, 05 Jun 2024 06:25:58 GMT  
		Size: 3.8 MB (3829597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca54b5ce5f2343afd4e77db2ceca0fcc8a71a8e5533981f969ecd86a66e9e9f8`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8030e81e3d2a09ca6a076294871304d566e86bed912d99d12e82f213fec4cc1d`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa54e95d67c63dbf0cf8f753642cfe16d08165c0ef6bd6d75b0b04dbca492494`  
		Last Modified: Wed, 05 Jun 2024 06:28:41 GMT  
		Size: 124.3 MB (124271471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e178042e3b461503d611ef9ed1a289773f1b1cc2d271d007759b4d512390717a`  
		Last Modified: Wed, 05 Jun 2024 06:28:22 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f521d7494e3239c1ec45905b8a7e715d6967d11a327a565c4b0a35c5495b3901`  
		Last Modified: Wed, 05 Jun 2024 06:28:59 GMT  
		Size: 85.2 MB (85175274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f413fb95df485200b05df4effea1b1bffced12132eea05565570079cb17c38`  
		Last Modified: Wed, 05 Jun 2024 06:28:49 GMT  
		Size: 307.3 KB (307303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c4739db608ffd3b9933d1078a6f304391353159f79b516964267a0448f5c6e`  
		Last Modified: Wed, 05 Jun 2024 06:28:48 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78400d29e519e86a1c1f3a22bdd8d20687db690193fa5e65e03a2d2d11fbc85a`  
		Last Modified: Wed, 05 Jun 2024 06:28:52 GMT  
		Size: 23.7 MB (23734349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4677fc2e545662f89a0d1db753b5c9fd6d27c026a0a81d28377e16f65f8f055d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261473724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4dbb5c04fbe23aff1e594f0ee5e6cf77e76ef0a644cf6c3cc620b8f313d138`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:13:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:13:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:29:03 GMT
ENV ROS_DISTRO=iron
# Wed, 05 Jun 2024 05:29:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:29:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:29:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:29:53 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:30:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:30:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:30:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:30:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f530a91a61927d0b4523bb8e4f14381cb7f7d9817c6204686d6bb5250cde836`  
		Last Modified: Wed, 05 Jun 2024 05:50:31 GMT  
		Size: 1.2 MB (1216480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a544f7ab76cc1c3437117889feb865f388e0c55099600b53c55efa34156f2fff`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 3.8 MB (3802894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f54cb7fba17b8889b6330bdd6ef5007d394b7fb9e815eb9f2af1fa6b936965`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a069ee1709898d9feb67e4cfe34cab6b60d1f4e6e228834e3605bee3deb8181`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2e13045d4af22e2a09809ec5ad219bd0e69a32734c4302f98ed338a2ae3aae`  
		Last Modified: Wed, 05 Jun 2024 05:53:14 GMT  
		Size: 121.8 MB (121755785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ad376ac5d1a80d5e0f2c80959f053279c8ed358dde21e81fc687d3c864da7d`  
		Last Modified: Wed, 05 Jun 2024 05:52:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5e7c41deb8f9091e8fa011990bd0a3b57899972d538c4f92315133e5d13329`  
		Last Modified: Wed, 05 Jun 2024 05:53:34 GMT  
		Size: 82.9 MB (82860356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3deb503a6253699d5696d173dbae99c360e2ac7fa4666593353684bcee661e`  
		Last Modified: Wed, 05 Jun 2024 05:53:25 GMT  
		Size: 307.3 KB (307309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a94888eadc41fa54800510db3a24c90d9eabee89b8c83dd3827ab70ebec4e3e`  
		Last Modified: Wed, 05 Jun 2024 05:53:25 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67a7a87e96e5242bc809c27af71b6767d1eda0469965c8ebb996ae755fd5246`  
		Last Modified: Wed, 05 Jun 2024 05:53:30 GMT  
		Size: 23.1 MB (23123653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:0378be3497950bc286f262175e4463b50fdb7636cb9e002de58ed88710108da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:1227ae73b097a51eb8245196671eb9bf4ea87ba1b0d91e8b146f2c05ed9e0ffa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268976942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93319acb40698b522723f30da8790e735d3be23457e217eff21ae50962895ab5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:53:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:53:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:53:35 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:06:24 GMT
ENV ROS_DISTRO=iron
# Wed, 05 Jun 2024 06:07:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:07:16 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:07:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:07:16 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 06:07:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:07:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 06:07:48 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 06:08:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd8a5936f50eae12a88b5309a7de594460a6cf0c083562c45bbfaf2adc9a79f`  
		Last Modified: Wed, 05 Jun 2024 06:25:59 GMT  
		Size: 1.2 MB (1214743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa0ba2a85d3d446a820f12f96585c9af6c9ab8a6b478961fbb02d3907c0163a`  
		Last Modified: Wed, 05 Jun 2024 06:25:58 GMT  
		Size: 3.8 MB (3829597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca54b5ce5f2343afd4e77db2ceca0fcc8a71a8e5533981f969ecd86a66e9e9f8`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8030e81e3d2a09ca6a076294871304d566e86bed912d99d12e82f213fec4cc1d`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa54e95d67c63dbf0cf8f753642cfe16d08165c0ef6bd6d75b0b04dbca492494`  
		Last Modified: Wed, 05 Jun 2024 06:28:41 GMT  
		Size: 124.3 MB (124271471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e178042e3b461503d611ef9ed1a289773f1b1cc2d271d007759b4d512390717a`  
		Last Modified: Wed, 05 Jun 2024 06:28:22 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f521d7494e3239c1ec45905b8a7e715d6967d11a327a565c4b0a35c5495b3901`  
		Last Modified: Wed, 05 Jun 2024 06:28:59 GMT  
		Size: 85.2 MB (85175274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f413fb95df485200b05df4effea1b1bffced12132eea05565570079cb17c38`  
		Last Modified: Wed, 05 Jun 2024 06:28:49 GMT  
		Size: 307.3 KB (307303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c4739db608ffd3b9933d1078a6f304391353159f79b516964267a0448f5c6e`  
		Last Modified: Wed, 05 Jun 2024 06:28:48 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78400d29e519e86a1c1f3a22bdd8d20687db690193fa5e65e03a2d2d11fbc85a`  
		Last Modified: Wed, 05 Jun 2024 06:28:52 GMT  
		Size: 23.7 MB (23734349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4677fc2e545662f89a0d1db753b5c9fd6d27c026a0a81d28377e16f65f8f055d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261473724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4dbb5c04fbe23aff1e594f0ee5e6cf77e76ef0a644cf6c3cc620b8f313d138`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:13:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:13:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:29:03 GMT
ENV ROS_DISTRO=iron
# Wed, 05 Jun 2024 05:29:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:29:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:29:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:29:53 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:30:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:30:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:30:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:30:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f530a91a61927d0b4523bb8e4f14381cb7f7d9817c6204686d6bb5250cde836`  
		Last Modified: Wed, 05 Jun 2024 05:50:31 GMT  
		Size: 1.2 MB (1216480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a544f7ab76cc1c3437117889feb865f388e0c55099600b53c55efa34156f2fff`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 3.8 MB (3802894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f54cb7fba17b8889b6330bdd6ef5007d394b7fb9e815eb9f2af1fa6b936965`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a069ee1709898d9feb67e4cfe34cab6b60d1f4e6e228834e3605bee3deb8181`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2e13045d4af22e2a09809ec5ad219bd0e69a32734c4302f98ed338a2ae3aae`  
		Last Modified: Wed, 05 Jun 2024 05:53:14 GMT  
		Size: 121.8 MB (121755785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ad376ac5d1a80d5e0f2c80959f053279c8ed358dde21e81fc687d3c864da7d`  
		Last Modified: Wed, 05 Jun 2024 05:52:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5e7c41deb8f9091e8fa011990bd0a3b57899972d538c4f92315133e5d13329`  
		Last Modified: Wed, 05 Jun 2024 05:53:34 GMT  
		Size: 82.9 MB (82860356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3deb503a6253699d5696d173dbae99c360e2ac7fa4666593353684bcee661e`  
		Last Modified: Wed, 05 Jun 2024 05:53:25 GMT  
		Size: 307.3 KB (307309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a94888eadc41fa54800510db3a24c90d9eabee89b8c83dd3827ab70ebec4e3e`  
		Last Modified: Wed, 05 Jun 2024 05:53:25 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67a7a87e96e5242bc809c27af71b6767d1eda0469965c8ebb996ae755fd5246`  
		Last Modified: Wed, 05 Jun 2024 05:53:30 GMT  
		Size: 23.1 MB (23123653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:b5aa946df59ad6a1373c9eb9a5922f2e1021c7bdd7838f913e7de0c01a1b6c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:54b9b4503b7f616afcf3e48e957afd418f08aacb6dd934af6c29fbb469dbe737
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159757578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0702e44c3057dc0490d6bdc723e1140a79f23c8d02a7869f7e10a9ac4cec9fa0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:53:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:53:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:53:35 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:06:24 GMT
ENV ROS_DISTRO=iron
# Wed, 05 Jun 2024 06:07:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:07:16 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:07:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:07:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd8a5936f50eae12a88b5309a7de594460a6cf0c083562c45bbfaf2adc9a79f`  
		Last Modified: Wed, 05 Jun 2024 06:25:59 GMT  
		Size: 1.2 MB (1214743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa0ba2a85d3d446a820f12f96585c9af6c9ab8a6b478961fbb02d3907c0163a`  
		Last Modified: Wed, 05 Jun 2024 06:25:58 GMT  
		Size: 3.8 MB (3829597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca54b5ce5f2343afd4e77db2ceca0fcc8a71a8e5533981f969ecd86a66e9e9f8`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8030e81e3d2a09ca6a076294871304d566e86bed912d99d12e82f213fec4cc1d`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa54e95d67c63dbf0cf8f753642cfe16d08165c0ef6bd6d75b0b04dbca492494`  
		Last Modified: Wed, 05 Jun 2024 06:28:41 GMT  
		Size: 124.3 MB (124271471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e178042e3b461503d611ef9ed1a289773f1b1cc2d271d007759b4d512390717a`  
		Last Modified: Wed, 05 Jun 2024 06:28:22 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f4edcd06dfd87f5ef6cee1fdb2a7894cd2e257394d249d1715e77b7ce3e81d34
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155179954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76990d93dbe0ea01669a568a80f5501b1c7eb2b6706dfc3fb11a0132a026a2c6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:13:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:13:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:29:03 GMT
ENV ROS_DISTRO=iron
# Wed, 05 Jun 2024 05:29:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:29:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:29:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:29:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f530a91a61927d0b4523bb8e4f14381cb7f7d9817c6204686d6bb5250cde836`  
		Last Modified: Wed, 05 Jun 2024 05:50:31 GMT  
		Size: 1.2 MB (1216480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a544f7ab76cc1c3437117889feb865f388e0c55099600b53c55efa34156f2fff`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 3.8 MB (3802894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f54cb7fba17b8889b6330bdd6ef5007d394b7fb9e815eb9f2af1fa6b936965`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a069ee1709898d9feb67e4cfe34cab6b60d1f4e6e228834e3605bee3deb8181`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2e13045d4af22e2a09809ec5ad219bd0e69a32734c4302f98ed338a2ae3aae`  
		Last Modified: Wed, 05 Jun 2024 05:53:14 GMT  
		Size: 121.8 MB (121755785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ad376ac5d1a80d5e0f2c80959f053279c8ed358dde21e81fc687d3c864da7d`  
		Last Modified: Wed, 05 Jun 2024 05:52:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-core-jammy`

```console
$ docker pull ros@sha256:b5aa946df59ad6a1373c9eb9a5922f2e1021c7bdd7838f913e7de0c01a1b6c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:54b9b4503b7f616afcf3e48e957afd418f08aacb6dd934af6c29fbb469dbe737
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159757578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0702e44c3057dc0490d6bdc723e1140a79f23c8d02a7869f7e10a9ac4cec9fa0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:53:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:34 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:53:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:53:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:53:35 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:53:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:06:24 GMT
ENV ROS_DISTRO=iron
# Wed, 05 Jun 2024 06:07:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:07:16 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:07:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:07:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd8a5936f50eae12a88b5309a7de594460a6cf0c083562c45bbfaf2adc9a79f`  
		Last Modified: Wed, 05 Jun 2024 06:25:59 GMT  
		Size: 1.2 MB (1214743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa0ba2a85d3d446a820f12f96585c9af6c9ab8a6b478961fbb02d3907c0163a`  
		Last Modified: Wed, 05 Jun 2024 06:25:58 GMT  
		Size: 3.8 MB (3829597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca54b5ce5f2343afd4e77db2ceca0fcc8a71a8e5533981f969ecd86a66e9e9f8`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8030e81e3d2a09ca6a076294871304d566e86bed912d99d12e82f213fec4cc1d`  
		Last Modified: Wed, 05 Jun 2024 06:25:57 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa54e95d67c63dbf0cf8f753642cfe16d08165c0ef6bd6d75b0b04dbca492494`  
		Last Modified: Wed, 05 Jun 2024 06:28:41 GMT  
		Size: 124.3 MB (124271471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e178042e3b461503d611ef9ed1a289773f1b1cc2d271d007759b4d512390717a`  
		Last Modified: Wed, 05 Jun 2024 06:28:22 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f4edcd06dfd87f5ef6cee1fdb2a7894cd2e257394d249d1715e77b7ce3e81d34
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155179954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76990d93dbe0ea01669a568a80f5501b1c7eb2b6706dfc3fb11a0132a026a2c6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:13:28 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:13:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:13:48 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:29:03 GMT
ENV ROS_DISTRO=iron
# Wed, 05 Jun 2024 05:29:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:29:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:29:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:29:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f530a91a61927d0b4523bb8e4f14381cb7f7d9817c6204686d6bb5250cde836`  
		Last Modified: Wed, 05 Jun 2024 05:50:31 GMT  
		Size: 1.2 MB (1216480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a544f7ab76cc1c3437117889feb865f388e0c55099600b53c55efa34156f2fff`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 3.8 MB (3802894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f54cb7fba17b8889b6330bdd6ef5007d394b7fb9e815eb9f2af1fa6b936965`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a069ee1709898d9feb67e4cfe34cab6b60d1f4e6e228834e3605bee3deb8181`  
		Last Modified: Wed, 05 Jun 2024 05:50:28 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2e13045d4af22e2a09809ec5ad219bd0e69a32734c4302f98ed338a2ae3aae`  
		Last Modified: Wed, 05 Jun 2024 05:53:14 GMT  
		Size: 121.8 MB (121755785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ad376ac5d1a80d5e0f2c80959f053279c8ed358dde21e81fc687d3c864da7d`  
		Last Modified: Wed, 05 Jun 2024 05:52:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy`

```console
$ docker pull ros@sha256:1c445ce6bd87d8bc884fcd40e8a9d8f7efd939e2e4d321c2c9453d1c3e3ad541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:d4eabf3df3c131b759c6781e774cc9225890984daa681a146c308e44db0bb118
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299758266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80af3343c6d36f1e6352c7a7d3c911774af876a015d371fad1c6d7d8b0eaa6c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 06:10:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV ROS_DISTRO=jazzy
# Wed, 05 Jun 2024 06:12:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:12:54 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:12:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:12:54 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 06:14:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:14:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 06:14:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 06:15:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b7b089eccbc5711efe9b5e70ebf338500c3b4261cc08c5ad96463a57a9bf1`  
		Last Modified: Wed, 05 Jun 2024 06:30:49 GMT  
		Size: 683.8 KB (683789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac994edf240e70b612dad36f314b389ed36ff1bb920412484395a0454a1d61c`  
		Last Modified: Wed, 05 Jun 2024 06:30:48 GMT  
		Size: 4.6 MB (4617771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5b36f85e72e73135bfa90830916ffb2abb10c40af616211cd07463f290a9ce`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a052403e9ecb7c5356f8463bb90b17f27010035dba5a27455ea3aa205697689f`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb5f622c1c53ac02d4c4470baf7a32907c1a1cd242fe96ddedac1656a9ab3d4`  
		Last Modified: Wed, 05 Jun 2024 06:31:05 GMT  
		Size: 122.5 MB (122450475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86d3d9063826953ab50f7a7f33047824a710fe719f16703d22dc863b0076fc4`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b96688b1efb04501ca8dfe875aeba752657cf0058f78438374d6999aeef6a53`  
		Last Modified: Wed, 05 Jun 2024 06:31:28 GMT  
		Size: 114.3 MB (114315851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33d9450ee58f63e08c1caac9e8d3756a525bb6993807a4d88647daa989b8f82`  
		Last Modified: Wed, 05 Jun 2024 06:31:13 GMT  
		Size: 312.8 KB (312755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae01f36b683cf5c4ad94c8bc0b4770b360791a539cd60152dbbf8251d154aeb`  
		Last Modified: Wed, 05 Jun 2024 06:31:13 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f27156a478f4278398d66d1c545ee847862b1899a145e56b5cfc9de8bf2baf`  
		Last Modified: Wed, 05 Jun 2024 06:31:17 GMT  
		Size: 27.7 MB (27667923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1badf5a00191973b50801c72965fed62d9cd394e275ba8f85a1d51ece2d1146e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289901220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1abcda7e1004e215f1dda94b2e26e0821a85324f8ddfa60827afa098187ac23`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:32:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:33:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV ROS_DISTRO=jazzy
# Wed, 05 Jun 2024 05:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:35:44 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:35:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:35:44 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:37:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:37:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:37:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:38:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b3822029b130a9434da04db278e695747571673f958098087aa1b0646f5e9`  
		Last Modified: Wed, 05 Jun 2024 05:55:18 GMT  
		Size: 684.9 KB (684936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b773b38eac33ca187f0b096cf08d40343b5c9d57818453f97613666eae7540`  
		Last Modified: Wed, 05 Jun 2024 05:55:16 GMT  
		Size: 4.6 MB (4612918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eed9b6478ee735e6559879b05f8a108b186e2185afbe1456b0bae55496e682`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f358deb3ce2f2d04e1ba6c224a7e7013fb4c1a6f8b1ba71583e1d609240449`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7853119aad5b9fdcc0882a2a6b18a57ce767be3e7882706171c19654acecd00a`  
		Last Modified: Wed, 05 Jun 2024 05:55:37 GMT  
		Size: 117.3 MB (117267351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03f8af49e10ce365fa194e06afda83a46f308588518527602af01fac3b7026f`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6d52f206ff0a29a3eb7519bdc04d32db2c40e16c511e7ccf45eeb792f1944`  
		Last Modified: Wed, 05 Jun 2024 05:55:58 GMT  
		Size: 111.2 MB (111160696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2c06fb4721bb4f54fc284881cc94751c3671444b26cb306c223c1d33004789`  
		Last Modified: Wed, 05 Jun 2024 05:55:45 GMT  
		Size: 312.8 KB (312756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73532281aed74c405fee3b771131841982e81415f390ec4db8c64be0e55810f`  
		Last Modified: Wed, 05 Jun 2024 05:55:45 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cda6cf897fb0f813d993a3a9006e251e903cb04b3386865697fb70974cd143c`  
		Last Modified: Wed, 05 Jun 2024 05:55:49 GMT  
		Size: 26.8 MB (26813698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:5e534893460d0c075c7b610ee304c72b931ebd19e9a055feba546c3b16761380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:51005b3911237344579acd34cb1aa9ca232770fbaff8946ef3ecfd1c9a86e68d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.7 MB (623681921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c201a80a2924b7309d556a1589c275f5fc0db0277b75c8ccee79878be6a284c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 06:10:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV ROS_DISTRO=jazzy
# Wed, 05 Jun 2024 06:12:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:12:54 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:12:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:12:54 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 06:14:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:14:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 06:14:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 06:15:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:19:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b7b089eccbc5711efe9b5e70ebf338500c3b4261cc08c5ad96463a57a9bf1`  
		Last Modified: Wed, 05 Jun 2024 06:30:49 GMT  
		Size: 683.8 KB (683789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac994edf240e70b612dad36f314b389ed36ff1bb920412484395a0454a1d61c`  
		Last Modified: Wed, 05 Jun 2024 06:30:48 GMT  
		Size: 4.6 MB (4617771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5b36f85e72e73135bfa90830916ffb2abb10c40af616211cd07463f290a9ce`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a052403e9ecb7c5356f8463bb90b17f27010035dba5a27455ea3aa205697689f`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb5f622c1c53ac02d4c4470baf7a32907c1a1cd242fe96ddedac1656a9ab3d4`  
		Last Modified: Wed, 05 Jun 2024 06:31:05 GMT  
		Size: 122.5 MB (122450475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86d3d9063826953ab50f7a7f33047824a710fe719f16703d22dc863b0076fc4`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b96688b1efb04501ca8dfe875aeba752657cf0058f78438374d6999aeef6a53`  
		Last Modified: Wed, 05 Jun 2024 06:31:28 GMT  
		Size: 114.3 MB (114315851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33d9450ee58f63e08c1caac9e8d3756a525bb6993807a4d88647daa989b8f82`  
		Last Modified: Wed, 05 Jun 2024 06:31:13 GMT  
		Size: 312.8 KB (312755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae01f36b683cf5c4ad94c8bc0b4770b360791a539cd60152dbbf8251d154aeb`  
		Last Modified: Wed, 05 Jun 2024 06:31:13 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f27156a478f4278398d66d1c545ee847862b1899a145e56b5cfc9de8bf2baf`  
		Last Modified: Wed, 05 Jun 2024 06:31:17 GMT  
		Size: 27.7 MB (27667923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629c19eda05292e16b6db22eeadc89cfeeb89587d861b14c3b09383ea7d00001`  
		Last Modified: Wed, 05 Jun 2024 06:32:25 GMT  
		Size: 323.9 MB (323923655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:390b20c52468eedf3795d854207f276aad5a30f4c0b779585b78b972b0cbe54a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.0 MB (566975386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aabe9316e914b93dcb39b7889fb4435e26a23e2cc422b542034e21acb9882bf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:32:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:33:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV ROS_DISTRO=jazzy
# Wed, 05 Jun 2024 05:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:35:44 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:35:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:35:44 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:37:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:37:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:37:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:38:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:44:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b3822029b130a9434da04db278e695747571673f958098087aa1b0646f5e9`  
		Last Modified: Wed, 05 Jun 2024 05:55:18 GMT  
		Size: 684.9 KB (684936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b773b38eac33ca187f0b096cf08d40343b5c9d57818453f97613666eae7540`  
		Last Modified: Wed, 05 Jun 2024 05:55:16 GMT  
		Size: 4.6 MB (4612918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eed9b6478ee735e6559879b05f8a108b186e2185afbe1456b0bae55496e682`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f358deb3ce2f2d04e1ba6c224a7e7013fb4c1a6f8b1ba71583e1d609240449`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7853119aad5b9fdcc0882a2a6b18a57ce767be3e7882706171c19654acecd00a`  
		Last Modified: Wed, 05 Jun 2024 05:55:37 GMT  
		Size: 117.3 MB (117267351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03f8af49e10ce365fa194e06afda83a46f308588518527602af01fac3b7026f`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6d52f206ff0a29a3eb7519bdc04d32db2c40e16c511e7ccf45eeb792f1944`  
		Last Modified: Wed, 05 Jun 2024 05:55:58 GMT  
		Size: 111.2 MB (111160696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2c06fb4721bb4f54fc284881cc94751c3671444b26cb306c223c1d33004789`  
		Last Modified: Wed, 05 Jun 2024 05:55:45 GMT  
		Size: 312.8 KB (312756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73532281aed74c405fee3b771131841982e81415f390ec4db8c64be0e55810f`  
		Last Modified: Wed, 05 Jun 2024 05:55:45 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cda6cf897fb0f813d993a3a9006e251e903cb04b3386865697fb70974cd143c`  
		Last Modified: Wed, 05 Jun 2024 05:55:49 GMT  
		Size: 26.8 MB (26813698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c09541d10f2ea7a5ec4b6c3ce632a4d7d42902768716ebac7be4bb6b6ec81f0`  
		Last Modified: Wed, 05 Jun 2024 05:56:49 GMT  
		Size: 277.1 MB (277074166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:5e534893460d0c075c7b610ee304c72b931ebd19e9a055feba546c3b16761380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:51005b3911237344579acd34cb1aa9ca232770fbaff8946ef3ecfd1c9a86e68d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.7 MB (623681921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c201a80a2924b7309d556a1589c275f5fc0db0277b75c8ccee79878be6a284c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 06:10:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV ROS_DISTRO=jazzy
# Wed, 05 Jun 2024 06:12:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:12:54 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:12:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:12:54 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 06:14:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:14:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 06:14:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 06:15:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:19:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b7b089eccbc5711efe9b5e70ebf338500c3b4261cc08c5ad96463a57a9bf1`  
		Last Modified: Wed, 05 Jun 2024 06:30:49 GMT  
		Size: 683.8 KB (683789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac994edf240e70b612dad36f314b389ed36ff1bb920412484395a0454a1d61c`  
		Last Modified: Wed, 05 Jun 2024 06:30:48 GMT  
		Size: 4.6 MB (4617771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5b36f85e72e73135bfa90830916ffb2abb10c40af616211cd07463f290a9ce`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a052403e9ecb7c5356f8463bb90b17f27010035dba5a27455ea3aa205697689f`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb5f622c1c53ac02d4c4470baf7a32907c1a1cd242fe96ddedac1656a9ab3d4`  
		Last Modified: Wed, 05 Jun 2024 06:31:05 GMT  
		Size: 122.5 MB (122450475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86d3d9063826953ab50f7a7f33047824a710fe719f16703d22dc863b0076fc4`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b96688b1efb04501ca8dfe875aeba752657cf0058f78438374d6999aeef6a53`  
		Last Modified: Wed, 05 Jun 2024 06:31:28 GMT  
		Size: 114.3 MB (114315851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33d9450ee58f63e08c1caac9e8d3756a525bb6993807a4d88647daa989b8f82`  
		Last Modified: Wed, 05 Jun 2024 06:31:13 GMT  
		Size: 312.8 KB (312755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae01f36b683cf5c4ad94c8bc0b4770b360791a539cd60152dbbf8251d154aeb`  
		Last Modified: Wed, 05 Jun 2024 06:31:13 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f27156a478f4278398d66d1c545ee847862b1899a145e56b5cfc9de8bf2baf`  
		Last Modified: Wed, 05 Jun 2024 06:31:17 GMT  
		Size: 27.7 MB (27667923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629c19eda05292e16b6db22eeadc89cfeeb89587d861b14c3b09383ea7d00001`  
		Last Modified: Wed, 05 Jun 2024 06:32:25 GMT  
		Size: 323.9 MB (323923655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:390b20c52468eedf3795d854207f276aad5a30f4c0b779585b78b972b0cbe54a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.0 MB (566975386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aabe9316e914b93dcb39b7889fb4435e26a23e2cc422b542034e21acb9882bf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:32:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:33:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV ROS_DISTRO=jazzy
# Wed, 05 Jun 2024 05:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:35:44 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:35:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:35:44 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:37:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:37:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:37:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:38:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:44:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b3822029b130a9434da04db278e695747571673f958098087aa1b0646f5e9`  
		Last Modified: Wed, 05 Jun 2024 05:55:18 GMT  
		Size: 684.9 KB (684936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b773b38eac33ca187f0b096cf08d40343b5c9d57818453f97613666eae7540`  
		Last Modified: Wed, 05 Jun 2024 05:55:16 GMT  
		Size: 4.6 MB (4612918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eed9b6478ee735e6559879b05f8a108b186e2185afbe1456b0bae55496e682`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f358deb3ce2f2d04e1ba6c224a7e7013fb4c1a6f8b1ba71583e1d609240449`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7853119aad5b9fdcc0882a2a6b18a57ce767be3e7882706171c19654acecd00a`  
		Last Modified: Wed, 05 Jun 2024 05:55:37 GMT  
		Size: 117.3 MB (117267351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03f8af49e10ce365fa194e06afda83a46f308588518527602af01fac3b7026f`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6d52f206ff0a29a3eb7519bdc04d32db2c40e16c511e7ccf45eeb792f1944`  
		Last Modified: Wed, 05 Jun 2024 05:55:58 GMT  
		Size: 111.2 MB (111160696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2c06fb4721bb4f54fc284881cc94751c3671444b26cb306c223c1d33004789`  
		Last Modified: Wed, 05 Jun 2024 05:55:45 GMT  
		Size: 312.8 KB (312756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73532281aed74c405fee3b771131841982e81415f390ec4db8c64be0e55810f`  
		Last Modified: Wed, 05 Jun 2024 05:55:45 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cda6cf897fb0f813d993a3a9006e251e903cb04b3386865697fb70974cd143c`  
		Last Modified: Wed, 05 Jun 2024 05:55:49 GMT  
		Size: 26.8 MB (26813698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c09541d10f2ea7a5ec4b6c3ce632a4d7d42902768716ebac7be4bb6b6ec81f0`  
		Last Modified: Wed, 05 Jun 2024 05:56:49 GMT  
		Size: 277.1 MB (277074166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:1c445ce6bd87d8bc884fcd40e8a9d8f7efd939e2e4d321c2c9453d1c3e3ad541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:d4eabf3df3c131b759c6781e774cc9225890984daa681a146c308e44db0bb118
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299758266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80af3343c6d36f1e6352c7a7d3c911774af876a015d371fad1c6d7d8b0eaa6c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 06:10:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV ROS_DISTRO=jazzy
# Wed, 05 Jun 2024 06:12:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:12:54 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:12:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:12:54 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 06:14:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:14:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 06:14:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 06:15:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b7b089eccbc5711efe9b5e70ebf338500c3b4261cc08c5ad96463a57a9bf1`  
		Last Modified: Wed, 05 Jun 2024 06:30:49 GMT  
		Size: 683.8 KB (683789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac994edf240e70b612dad36f314b389ed36ff1bb920412484395a0454a1d61c`  
		Last Modified: Wed, 05 Jun 2024 06:30:48 GMT  
		Size: 4.6 MB (4617771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5b36f85e72e73135bfa90830916ffb2abb10c40af616211cd07463f290a9ce`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a052403e9ecb7c5356f8463bb90b17f27010035dba5a27455ea3aa205697689f`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb5f622c1c53ac02d4c4470baf7a32907c1a1cd242fe96ddedac1656a9ab3d4`  
		Last Modified: Wed, 05 Jun 2024 06:31:05 GMT  
		Size: 122.5 MB (122450475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86d3d9063826953ab50f7a7f33047824a710fe719f16703d22dc863b0076fc4`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b96688b1efb04501ca8dfe875aeba752657cf0058f78438374d6999aeef6a53`  
		Last Modified: Wed, 05 Jun 2024 06:31:28 GMT  
		Size: 114.3 MB (114315851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33d9450ee58f63e08c1caac9e8d3756a525bb6993807a4d88647daa989b8f82`  
		Last Modified: Wed, 05 Jun 2024 06:31:13 GMT  
		Size: 312.8 KB (312755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae01f36b683cf5c4ad94c8bc0b4770b360791a539cd60152dbbf8251d154aeb`  
		Last Modified: Wed, 05 Jun 2024 06:31:13 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f27156a478f4278398d66d1c545ee847862b1899a145e56b5cfc9de8bf2baf`  
		Last Modified: Wed, 05 Jun 2024 06:31:17 GMT  
		Size: 27.7 MB (27667923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1badf5a00191973b50801c72965fed62d9cd394e275ba8f85a1d51ece2d1146e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289901220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1abcda7e1004e215f1dda94b2e26e0821a85324f8ddfa60827afa098187ac23`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:32:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:33:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV ROS_DISTRO=jazzy
# Wed, 05 Jun 2024 05:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:35:44 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:35:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:35:44 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:37:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:37:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:37:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:38:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b3822029b130a9434da04db278e695747571673f958098087aa1b0646f5e9`  
		Last Modified: Wed, 05 Jun 2024 05:55:18 GMT  
		Size: 684.9 KB (684936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b773b38eac33ca187f0b096cf08d40343b5c9d57818453f97613666eae7540`  
		Last Modified: Wed, 05 Jun 2024 05:55:16 GMT  
		Size: 4.6 MB (4612918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eed9b6478ee735e6559879b05f8a108b186e2185afbe1456b0bae55496e682`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f358deb3ce2f2d04e1ba6c224a7e7013fb4c1a6f8b1ba71583e1d609240449`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7853119aad5b9fdcc0882a2a6b18a57ce767be3e7882706171c19654acecd00a`  
		Last Modified: Wed, 05 Jun 2024 05:55:37 GMT  
		Size: 117.3 MB (117267351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03f8af49e10ce365fa194e06afda83a46f308588518527602af01fac3b7026f`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6d52f206ff0a29a3eb7519bdc04d32db2c40e16c511e7ccf45eeb792f1944`  
		Last Modified: Wed, 05 Jun 2024 05:55:58 GMT  
		Size: 111.2 MB (111160696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2c06fb4721bb4f54fc284881cc94751c3671444b26cb306c223c1d33004789`  
		Last Modified: Wed, 05 Jun 2024 05:55:45 GMT  
		Size: 312.8 KB (312756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73532281aed74c405fee3b771131841982e81415f390ec4db8c64be0e55810f`  
		Last Modified: Wed, 05 Jun 2024 05:55:45 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cda6cf897fb0f813d993a3a9006e251e903cb04b3386865697fb70974cd143c`  
		Last Modified: Wed, 05 Jun 2024 05:55:49 GMT  
		Size: 26.8 MB (26813698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:1c445ce6bd87d8bc884fcd40e8a9d8f7efd939e2e4d321c2c9453d1c3e3ad541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:d4eabf3df3c131b759c6781e774cc9225890984daa681a146c308e44db0bb118
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299758266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80af3343c6d36f1e6352c7a7d3c911774af876a015d371fad1c6d7d8b0eaa6c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 06:10:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV ROS_DISTRO=jazzy
# Wed, 05 Jun 2024 06:12:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:12:54 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:12:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:12:54 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 06:14:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:14:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 06:14:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 06:15:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b7b089eccbc5711efe9b5e70ebf338500c3b4261cc08c5ad96463a57a9bf1`  
		Last Modified: Wed, 05 Jun 2024 06:30:49 GMT  
		Size: 683.8 KB (683789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac994edf240e70b612dad36f314b389ed36ff1bb920412484395a0454a1d61c`  
		Last Modified: Wed, 05 Jun 2024 06:30:48 GMT  
		Size: 4.6 MB (4617771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5b36f85e72e73135bfa90830916ffb2abb10c40af616211cd07463f290a9ce`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a052403e9ecb7c5356f8463bb90b17f27010035dba5a27455ea3aa205697689f`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb5f622c1c53ac02d4c4470baf7a32907c1a1cd242fe96ddedac1656a9ab3d4`  
		Last Modified: Wed, 05 Jun 2024 06:31:05 GMT  
		Size: 122.5 MB (122450475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86d3d9063826953ab50f7a7f33047824a710fe719f16703d22dc863b0076fc4`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b96688b1efb04501ca8dfe875aeba752657cf0058f78438374d6999aeef6a53`  
		Last Modified: Wed, 05 Jun 2024 06:31:28 GMT  
		Size: 114.3 MB (114315851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33d9450ee58f63e08c1caac9e8d3756a525bb6993807a4d88647daa989b8f82`  
		Last Modified: Wed, 05 Jun 2024 06:31:13 GMT  
		Size: 312.8 KB (312755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae01f36b683cf5c4ad94c8bc0b4770b360791a539cd60152dbbf8251d154aeb`  
		Last Modified: Wed, 05 Jun 2024 06:31:13 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f27156a478f4278398d66d1c545ee847862b1899a145e56b5cfc9de8bf2baf`  
		Last Modified: Wed, 05 Jun 2024 06:31:17 GMT  
		Size: 27.7 MB (27667923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1badf5a00191973b50801c72965fed62d9cd394e275ba8f85a1d51ece2d1146e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289901220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1abcda7e1004e215f1dda94b2e26e0821a85324f8ddfa60827afa098187ac23`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:32:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:33:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV ROS_DISTRO=jazzy
# Wed, 05 Jun 2024 05:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:35:44 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:35:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:35:44 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:37:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:37:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:37:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:38:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b3822029b130a9434da04db278e695747571673f958098087aa1b0646f5e9`  
		Last Modified: Wed, 05 Jun 2024 05:55:18 GMT  
		Size: 684.9 KB (684936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b773b38eac33ca187f0b096cf08d40343b5c9d57818453f97613666eae7540`  
		Last Modified: Wed, 05 Jun 2024 05:55:16 GMT  
		Size: 4.6 MB (4612918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eed9b6478ee735e6559879b05f8a108b186e2185afbe1456b0bae55496e682`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f358deb3ce2f2d04e1ba6c224a7e7013fb4c1a6f8b1ba71583e1d609240449`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7853119aad5b9fdcc0882a2a6b18a57ce767be3e7882706171c19654acecd00a`  
		Last Modified: Wed, 05 Jun 2024 05:55:37 GMT  
		Size: 117.3 MB (117267351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03f8af49e10ce365fa194e06afda83a46f308588518527602af01fac3b7026f`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6d52f206ff0a29a3eb7519bdc04d32db2c40e16c511e7ccf45eeb792f1944`  
		Last Modified: Wed, 05 Jun 2024 05:55:58 GMT  
		Size: 111.2 MB (111160696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2c06fb4721bb4f54fc284881cc94751c3671444b26cb306c223c1d33004789`  
		Last Modified: Wed, 05 Jun 2024 05:55:45 GMT  
		Size: 312.8 KB (312756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73532281aed74c405fee3b771131841982e81415f390ec4db8c64be0e55810f`  
		Last Modified: Wed, 05 Jun 2024 05:55:45 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cda6cf897fb0f813d993a3a9006e251e903cb04b3386865697fb70974cd143c`  
		Last Modified: Wed, 05 Jun 2024 05:55:49 GMT  
		Size: 26.8 MB (26813698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:4977e21d0255e135eca0d146f7beb97a1ba5333997b31fbcef58b6c0a52927ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:c46bcfde6f9df1617f990578e150d3219966daad7c3d2b3367ba40f0d90f4f3a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157459298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c1f59356d8f13ff011d5cf98bfa751c5d758e69d55abf64e9c69b2224147a8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 06:10:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV ROS_DISTRO=jazzy
# Wed, 05 Jun 2024 06:12:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:12:54 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:12:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:12:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b7b089eccbc5711efe9b5e70ebf338500c3b4261cc08c5ad96463a57a9bf1`  
		Last Modified: Wed, 05 Jun 2024 06:30:49 GMT  
		Size: 683.8 KB (683789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac994edf240e70b612dad36f314b389ed36ff1bb920412484395a0454a1d61c`  
		Last Modified: Wed, 05 Jun 2024 06:30:48 GMT  
		Size: 4.6 MB (4617771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5b36f85e72e73135bfa90830916ffb2abb10c40af616211cd07463f290a9ce`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a052403e9ecb7c5356f8463bb90b17f27010035dba5a27455ea3aa205697689f`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb5f622c1c53ac02d4c4470baf7a32907c1a1cd242fe96ddedac1656a9ab3d4`  
		Last Modified: Wed, 05 Jun 2024 06:31:05 GMT  
		Size: 122.5 MB (122450475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86d3d9063826953ab50f7a7f33047824a710fe719f16703d22dc863b0076fc4`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:99c388abb370564e65ec4ae9823d6ad580fe327192c9d24180f807f29ab9ccd5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151611614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46d34d1522815ee822844042a400ff171999be5f292158a22d3eddb527678e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:32:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:33:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV ROS_DISTRO=jazzy
# Wed, 05 Jun 2024 05:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:35:44 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:35:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:35:44 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b3822029b130a9434da04db278e695747571673f958098087aa1b0646f5e9`  
		Last Modified: Wed, 05 Jun 2024 05:55:18 GMT  
		Size: 684.9 KB (684936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b773b38eac33ca187f0b096cf08d40343b5c9d57818453f97613666eae7540`  
		Last Modified: Wed, 05 Jun 2024 05:55:16 GMT  
		Size: 4.6 MB (4612918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eed9b6478ee735e6559879b05f8a108b186e2185afbe1456b0bae55496e682`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f358deb3ce2f2d04e1ba6c224a7e7013fb4c1a6f8b1ba71583e1d609240449`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7853119aad5b9fdcc0882a2a6b18a57ce767be3e7882706171c19654acecd00a`  
		Last Modified: Wed, 05 Jun 2024 05:55:37 GMT  
		Size: 117.3 MB (117267351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03f8af49e10ce365fa194e06afda83a46f308588518527602af01fac3b7026f`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:4977e21d0255e135eca0d146f7beb97a1ba5333997b31fbcef58b6c0a52927ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:c46bcfde6f9df1617f990578e150d3219966daad7c3d2b3367ba40f0d90f4f3a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157459298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c1f59356d8f13ff011d5cf98bfa751c5d758e69d55abf64e9c69b2224147a8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 06:10:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV ROS_DISTRO=jazzy
# Wed, 05 Jun 2024 06:12:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:12:54 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:12:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:12:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b7b089eccbc5711efe9b5e70ebf338500c3b4261cc08c5ad96463a57a9bf1`  
		Last Modified: Wed, 05 Jun 2024 06:30:49 GMT  
		Size: 683.8 KB (683789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac994edf240e70b612dad36f314b389ed36ff1bb920412484395a0454a1d61c`  
		Last Modified: Wed, 05 Jun 2024 06:30:48 GMT  
		Size: 4.6 MB (4617771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5b36f85e72e73135bfa90830916ffb2abb10c40af616211cd07463f290a9ce`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a052403e9ecb7c5356f8463bb90b17f27010035dba5a27455ea3aa205697689f`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb5f622c1c53ac02d4c4470baf7a32907c1a1cd242fe96ddedac1656a9ab3d4`  
		Last Modified: Wed, 05 Jun 2024 06:31:05 GMT  
		Size: 122.5 MB (122450475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86d3d9063826953ab50f7a7f33047824a710fe719f16703d22dc863b0076fc4`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:99c388abb370564e65ec4ae9823d6ad580fe327192c9d24180f807f29ab9ccd5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151611614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46d34d1522815ee822844042a400ff171999be5f292158a22d3eddb527678e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:32:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:33:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV ROS_DISTRO=jazzy
# Wed, 05 Jun 2024 05:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:35:44 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:35:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:35:44 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b3822029b130a9434da04db278e695747571673f958098087aa1b0646f5e9`  
		Last Modified: Wed, 05 Jun 2024 05:55:18 GMT  
		Size: 684.9 KB (684936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b773b38eac33ca187f0b096cf08d40343b5c9d57818453f97613666eae7540`  
		Last Modified: Wed, 05 Jun 2024 05:55:16 GMT  
		Size: 4.6 MB (4612918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eed9b6478ee735e6559879b05f8a108b186e2185afbe1456b0bae55496e682`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f358deb3ce2f2d04e1ba6c224a7e7013fb4c1a6f8b1ba71583e1d609240449`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7853119aad5b9fdcc0882a2a6b18a57ce767be3e7882706171c19654acecd00a`  
		Last Modified: Wed, 05 Jun 2024 05:55:37 GMT  
		Size: 117.3 MB (117267351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03f8af49e10ce365fa194e06afda83a46f308588518527602af01fac3b7026f`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:latest`

```console
$ docker pull ros@sha256:1c445ce6bd87d8bc884fcd40e8a9d8f7efd939e2e4d321c2c9453d1c3e3ad541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:d4eabf3df3c131b759c6781e774cc9225890984daa681a146c308e44db0bb118
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299758266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80af3343c6d36f1e6352c7a7d3c911774af876a015d371fad1c6d7d8b0eaa6c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 06:10:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV ROS_DISTRO=jazzy
# Wed, 05 Jun 2024 06:12:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:12:54 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:12:54 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:12:54 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 06:14:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:14:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 06:14:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 06:15:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b7b089eccbc5711efe9b5e70ebf338500c3b4261cc08c5ad96463a57a9bf1`  
		Last Modified: Wed, 05 Jun 2024 06:30:49 GMT  
		Size: 683.8 KB (683789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac994edf240e70b612dad36f314b389ed36ff1bb920412484395a0454a1d61c`  
		Last Modified: Wed, 05 Jun 2024 06:30:48 GMT  
		Size: 4.6 MB (4617771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5b36f85e72e73135bfa90830916ffb2abb10c40af616211cd07463f290a9ce`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a052403e9ecb7c5356f8463bb90b17f27010035dba5a27455ea3aa205697689f`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb5f622c1c53ac02d4c4470baf7a32907c1a1cd242fe96ddedac1656a9ab3d4`  
		Last Modified: Wed, 05 Jun 2024 06:31:05 GMT  
		Size: 122.5 MB (122450475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86d3d9063826953ab50f7a7f33047824a710fe719f16703d22dc863b0076fc4`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b96688b1efb04501ca8dfe875aeba752657cf0058f78438374d6999aeef6a53`  
		Last Modified: Wed, 05 Jun 2024 06:31:28 GMT  
		Size: 114.3 MB (114315851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33d9450ee58f63e08c1caac9e8d3756a525bb6993807a4d88647daa989b8f82`  
		Last Modified: Wed, 05 Jun 2024 06:31:13 GMT  
		Size: 312.8 KB (312755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae01f36b683cf5c4ad94c8bc0b4770b360791a539cd60152dbbf8251d154aeb`  
		Last Modified: Wed, 05 Jun 2024 06:31:13 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f27156a478f4278398d66d1c545ee847862b1899a145e56b5cfc9de8bf2baf`  
		Last Modified: Wed, 05 Jun 2024 06:31:17 GMT  
		Size: 27.7 MB (27667923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1badf5a00191973b50801c72965fed62d9cd394e275ba8f85a1d51ece2d1146e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289901220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1abcda7e1004e215f1dda94b2e26e0821a85324f8ddfa60827afa098187ac23`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:32:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:33:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV ROS_DISTRO=jazzy
# Wed, 05 Jun 2024 05:35:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:35:44 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:35:44 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:35:44 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:37:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:37:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:37:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:38:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b3822029b130a9434da04db278e695747571673f958098087aa1b0646f5e9`  
		Last Modified: Wed, 05 Jun 2024 05:55:18 GMT  
		Size: 684.9 KB (684936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b773b38eac33ca187f0b096cf08d40343b5c9d57818453f97613666eae7540`  
		Last Modified: Wed, 05 Jun 2024 05:55:16 GMT  
		Size: 4.6 MB (4612918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eed9b6478ee735e6559879b05f8a108b186e2185afbe1456b0bae55496e682`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f358deb3ce2f2d04e1ba6c224a7e7013fb4c1a6f8b1ba71583e1d609240449`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7853119aad5b9fdcc0882a2a6b18a57ce767be3e7882706171c19654acecd00a`  
		Last Modified: Wed, 05 Jun 2024 05:55:37 GMT  
		Size: 117.3 MB (117267351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03f8af49e10ce365fa194e06afda83a46f308588518527602af01fac3b7026f`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6d52f206ff0a29a3eb7519bdc04d32db2c40e16c511e7ccf45eeb792f1944`  
		Last Modified: Wed, 05 Jun 2024 05:55:58 GMT  
		Size: 111.2 MB (111160696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2c06fb4721bb4f54fc284881cc94751c3671444b26cb306c223c1d33004789`  
		Last Modified: Wed, 05 Jun 2024 05:55:45 GMT  
		Size: 312.8 KB (312756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73532281aed74c405fee3b771131841982e81415f390ec4db8c64be0e55810f`  
		Last Modified: Wed, 05 Jun 2024 05:55:45 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cda6cf897fb0f813d993a3a9006e251e903cb04b3386865697fb70974cd143c`  
		Last Modified: Wed, 05 Jun 2024 05:55:49 GMT  
		Size: 26.8 MB (26813698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic`

```console
$ docker pull ros@sha256:acc93816e625c953b31add8f3c209360c6e4eda9cf771f69d299e2f4141b917b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:d47940cb6d8e08ea5cbcdf9e313eeb650cf5d249f633957ff4b7365f764d3395
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264746483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d495043da1c80dc92e5e2853c7da9205887719f7e9ec8ab898d31356d5d58e0e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:35:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:36:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:45:36 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:45:36 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:45:36 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:45:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:45:36 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:46:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:46:58 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:46:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:46:59 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:47:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:47:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:47:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0b2f3debe6d753bc3abafc6b460a0a4eefe9091da70a55428112cb3b9997d0`  
		Last Modified: Wed, 05 Jun 2024 05:43:17 GMT  
		Size: 1.2 MB (1198624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d294a31ccccc8d9ba111b84126e1d1faf0694e471671e7e2e14746ac5d3053e`  
		Last Modified: Wed, 05 Jun 2024 05:43:18 GMT  
		Size: 5.6 MB (5553836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6b0882e06a01109e9d09203288aa1bad53597891b8ddaa829c49c12855c2a2`  
		Last Modified: Wed, 05 Jun 2024 06:23:20 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b2cc9d33d4188b74d5639905c35e1ae64b834ccb7d32434fd4b8837d05cfd4`  
		Last Modified: Wed, 05 Jun 2024 06:23:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d224207e0d7d191c70524deb5528af9138c432498248da8a146ef4f2ccb76522`  
		Last Modified: Wed, 05 Jun 2024 06:23:47 GMT  
		Size: 177.0 MB (177011351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a137e92617700e58635604a6f65d1484c36f3cca19e3c70c96ff77b688d60dfc`  
		Last Modified: Wed, 05 Jun 2024 06:23:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1309495ac492939fdfde58cf1da120fd01dea776ac0a3e45571a05ea16397fbf`  
		Last Modified: Wed, 05 Jun 2024 06:24:03 GMT  
		Size: 50.9 MB (50942120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78400d1f7dd7d6fa4c340c75f515ba00dd63ee35abe4412137c64f5eb2798199`  
		Last Modified: Wed, 05 Jun 2024 06:23:56 GMT  
		Size: 323.2 KB (323163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034066f6b071e6963ba4d9a67225826faeb2a36f7ab0cf1b22c3eb9ce5b50d4c`  
		Last Modified: Wed, 05 Jun 2024 06:23:56 GMT  
		Size: 1.1 MB (1130676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:165cecfb4dbf2f68f6c08eafa4858ed61352884fc120489747e15899f15348ca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229860898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316c7c6c49aa569fce41510ac70b2984c9432f081bc10e6a213ec3a3577a7daf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:12:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:12:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:12:50 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 03:12:51 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 03:12:51 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 03:12:51 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 03:12:51 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 03:16:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:16:23 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 03:16:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 03:16:23 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 03:17:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:17:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 03:17:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e858563dc379808e6dafb87d98be87a469d7eadbcf328692a93f4871b6455e1`  
		Last Modified: Wed, 05 Jun 2024 03:30:46 GMT  
		Size: 1.2 MB (1200168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edab1234b48134f83b0a8a78bf4f5ba92c3fd7169ab7bc857f88f2a379cb30c9`  
		Last Modified: Wed, 05 Jun 2024 03:30:44 GMT  
		Size: 4.7 MB (4680859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eef1562d1117fe923258ae07680e112c854d6d1460cf20b27880d3aab2b0288`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8b7cf88071311bc31839d24867f06c0215aacdd0ceed317af28071aae1ceb4`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cc5702211aa2134c20f699beae6e440479eda034ceeebfa97646b03af17f78`  
		Last Modified: Wed, 05 Jun 2024 03:31:25 GMT  
		Size: 157.5 MB (157481015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e3fc988f22240cdb1af0ce8a9135a08dd84e0c02b217c5b07783383ead3493`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81cfdc59b78354ae32bcf5b55594f95d7055d41a7dc855a9b8839be3e74546b9`  
		Last Modified: Wed, 05 Jun 2024 03:31:38 GMT  
		Size: 40.5 MB (40506614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7538f808a96d47124193d51356dff2e3ccceb60b634042d2154110232c7ea4f7`  
		Last Modified: Wed, 05 Jun 2024 03:31:33 GMT  
		Size: 323.2 KB (323163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b11dbf16d842b6f56ac3b8ece22e46a6e2358c415d73f99eb0487951c1742f`  
		Last Modified: Wed, 05 Jun 2024 03:31:33 GMT  
		Size: 1.1 MB (1062764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b2390c753cd204346f0cebad94b8475d5a430db6f800b57cf4abea0b1d9f31ee
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251988216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfecb0d5f7e93eace5ec5c6aade6cfbaf7f049199f5f69200fce6fa26b3d462`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:59:59 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:00:11 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:02:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:02:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:02:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:02:42 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:02:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:03:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:03:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ee698c21fd64dc89cbdfed5321d109a9525aeebaf898cfde7ecb7f55d0a90`  
		Last Modified: Wed, 05 Jun 2024 05:48:06 GMT  
		Size: 1.2 MB (1198556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67daca712e09cc6c6e34fb19421e400b0bc9bbf913a3b29ecd56e64e21014a0d`  
		Last Modified: Wed, 05 Jun 2024 05:48:04 GMT  
		Size: 5.5 MB (5531978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e8be46bf9534062563fa783cb360be4fc65686aca38b1df2586b3954e11b35`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1801d6616a2cd0f216d69bf6a76decd240fdeace1a5bd5a21e5c5ef31ee01f44`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8701d0e1bacd603262a548b1ca107c7eb378d56b7538d2fe69af7743dfc1fa14`  
		Last Modified: Wed, 05 Jun 2024 05:48:38 GMT  
		Size: 171.4 MB (171404678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe24a94caf00c45eb7e226d915071a9521a262a141c8006164fac3f907a66583`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6055caabb25cb3f56fdf7f72c7c835b3b1a31b20b9bbd24ae2fee4ab2a32811`  
		Last Modified: Wed, 05 Jun 2024 05:48:51 GMT  
		Size: 45.2 MB (45207269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c79a6839de6fd95d123e3a7422ff707f103d1ce1a76a5eb533428e9406735e`  
		Last Modified: Wed, 05 Jun 2024 05:48:46 GMT  
		Size: 323.2 KB (323165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387c477a284d1c9c16d5e3f1580b6ccf4b4667a94ec48b60aa971e29021b82fa`  
		Last Modified: Wed, 05 Jun 2024 05:48:46 GMT  
		Size: 1.1 MB (1114835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:c09aae48b785da56d7344f06895b02d6fedf506f1e571bd56aa786bc0d6df0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:11f498f513e2534e44d09ce467abfdf35309186dea2dddf1d6525e05c0a81a1d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.4 MB (835442875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b304e402828779989a0808fece12cb1467eb41b9f1150fbccaef5ee777ca15ee`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:35:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:36:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:45:36 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:45:36 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:45:36 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:45:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:45:36 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:46:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:46:58 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:46:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:46:59 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:47:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:47:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:47:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:52:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0b2f3debe6d753bc3abafc6b460a0a4eefe9091da70a55428112cb3b9997d0`  
		Last Modified: Wed, 05 Jun 2024 05:43:17 GMT  
		Size: 1.2 MB (1198624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d294a31ccccc8d9ba111b84126e1d1faf0694e471671e7e2e14746ac5d3053e`  
		Last Modified: Wed, 05 Jun 2024 05:43:18 GMT  
		Size: 5.6 MB (5553836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6b0882e06a01109e9d09203288aa1bad53597891b8ddaa829c49c12855c2a2`  
		Last Modified: Wed, 05 Jun 2024 06:23:20 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b2cc9d33d4188b74d5639905c35e1ae64b834ccb7d32434fd4b8837d05cfd4`  
		Last Modified: Wed, 05 Jun 2024 06:23:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d224207e0d7d191c70524deb5528af9138c432498248da8a146ef4f2ccb76522`  
		Last Modified: Wed, 05 Jun 2024 06:23:47 GMT  
		Size: 177.0 MB (177011351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a137e92617700e58635604a6f65d1484c36f3cca19e3c70c96ff77b688d60dfc`  
		Last Modified: Wed, 05 Jun 2024 06:23:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1309495ac492939fdfde58cf1da120fd01dea776ac0a3e45571a05ea16397fbf`  
		Last Modified: Wed, 05 Jun 2024 06:24:03 GMT  
		Size: 50.9 MB (50942120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78400d1f7dd7d6fa4c340c75f515ba00dd63ee35abe4412137c64f5eb2798199`  
		Last Modified: Wed, 05 Jun 2024 06:23:56 GMT  
		Size: 323.2 KB (323163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034066f6b071e6963ba4d9a67225826faeb2a36f7ab0cf1b22c3eb9ce5b50d4c`  
		Last Modified: Wed, 05 Jun 2024 06:23:56 GMT  
		Size: 1.1 MB (1130676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f8bbb2feda4a64a67d52e553f651c44b46c596aafc2576d96f5a013c213f81`  
		Last Modified: Wed, 05 Jun 2024 06:25:49 GMT  
		Size: 570.7 MB (570696392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:36c5d63c3e3503fd964b11d74458e53c2b2e48a679d495e0440e9a6d550d9266
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.4 MB (726381143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6960f2606800f20438876589aa153a9c53debd190b2030efe33b97c115e82736`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:12:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:12:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:12:50 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 03:12:51 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 03:12:51 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 03:12:51 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 03:12:51 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 03:16:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:16:23 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 03:16:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 03:16:23 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 03:17:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:17:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 03:17:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e858563dc379808e6dafb87d98be87a469d7eadbcf328692a93f4871b6455e1`  
		Last Modified: Wed, 05 Jun 2024 03:30:46 GMT  
		Size: 1.2 MB (1200168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edab1234b48134f83b0a8a78bf4f5ba92c3fd7169ab7bc857f88f2a379cb30c9`  
		Last Modified: Wed, 05 Jun 2024 03:30:44 GMT  
		Size: 4.7 MB (4680859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eef1562d1117fe923258ae07680e112c854d6d1460cf20b27880d3aab2b0288`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8b7cf88071311bc31839d24867f06c0215aacdd0ceed317af28071aae1ceb4`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cc5702211aa2134c20f699beae6e440479eda034ceeebfa97646b03af17f78`  
		Last Modified: Wed, 05 Jun 2024 03:31:25 GMT  
		Size: 157.5 MB (157481015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e3fc988f22240cdb1af0ce8a9135a08dd84e0c02b217c5b07783383ead3493`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81cfdc59b78354ae32bcf5b55594f95d7055d41a7dc855a9b8839be3e74546b9`  
		Last Modified: Wed, 05 Jun 2024 03:31:38 GMT  
		Size: 40.5 MB (40506614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7538f808a96d47124193d51356dff2e3ccceb60b634042d2154110232c7ea4f7`  
		Last Modified: Wed, 05 Jun 2024 03:31:33 GMT  
		Size: 323.2 KB (323163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b11dbf16d842b6f56ac3b8ece22e46a6e2358c415d73f99eb0487951c1742f`  
		Last Modified: Wed, 05 Jun 2024 03:31:33 GMT  
		Size: 1.1 MB (1062764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f571459483a794c9e8e8f534a0c2b226bbebc228e2ab5af766c7a27c79c84442`  
		Last Modified: Wed, 05 Jun 2024 03:33:05 GMT  
		Size: 496.5 MB (496520245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3936901dcc1fe259133babc1c556f049c38cbc96577dec5975cbb0e01d4d8454
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.6 MB (785645182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974cf60bc830169980e9b095faecb33cc29aa519d93ca6f14529311cde4dec8e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:59:59 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:00:11 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:02:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:02:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:02:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:02:42 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:02:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:03:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:03:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ee698c21fd64dc89cbdfed5321d109a9525aeebaf898cfde7ecb7f55d0a90`  
		Last Modified: Wed, 05 Jun 2024 05:48:06 GMT  
		Size: 1.2 MB (1198556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67daca712e09cc6c6e34fb19421e400b0bc9bbf913a3b29ecd56e64e21014a0d`  
		Last Modified: Wed, 05 Jun 2024 05:48:04 GMT  
		Size: 5.5 MB (5531978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e8be46bf9534062563fa783cb360be4fc65686aca38b1df2586b3954e11b35`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1801d6616a2cd0f216d69bf6a76decd240fdeace1a5bd5a21e5c5ef31ee01f44`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8701d0e1bacd603262a548b1ca107c7eb378d56b7538d2fe69af7743dfc1fa14`  
		Last Modified: Wed, 05 Jun 2024 05:48:38 GMT  
		Size: 171.4 MB (171404678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe24a94caf00c45eb7e226d915071a9521a262a141c8006164fac3f907a66583`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6055caabb25cb3f56fdf7f72c7c835b3b1a31b20b9bbd24ae2fee4ab2a32811`  
		Last Modified: Wed, 05 Jun 2024 05:48:51 GMT  
		Size: 45.2 MB (45207269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c79a6839de6fd95d123e3a7422ff707f103d1ce1a76a5eb533428e9406735e`  
		Last Modified: Wed, 05 Jun 2024 05:48:46 GMT  
		Size: 323.2 KB (323165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387c477a284d1c9c16d5e3f1580b6ccf4b4667a94ec48b60aa971e29021b82fa`  
		Last Modified: Wed, 05 Jun 2024 05:48:46 GMT  
		Size: 1.1 MB (1114835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac49e590bb5479f0b16356093f73e0f90c036c4db368b00ba0dbb8975dc79ec`  
		Last Modified: Wed, 05 Jun 2024 05:50:20 GMT  
		Size: 533.7 MB (533656966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:c09aae48b785da56d7344f06895b02d6fedf506f1e571bd56aa786bc0d6df0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:11f498f513e2534e44d09ce467abfdf35309186dea2dddf1d6525e05c0a81a1d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.4 MB (835442875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b304e402828779989a0808fece12cb1467eb41b9f1150fbccaef5ee777ca15ee`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:35:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:36:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:45:36 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:45:36 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:45:36 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:45:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:45:36 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:46:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:46:58 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:46:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:46:59 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:47:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:47:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:47:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:52:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0b2f3debe6d753bc3abafc6b460a0a4eefe9091da70a55428112cb3b9997d0`  
		Last Modified: Wed, 05 Jun 2024 05:43:17 GMT  
		Size: 1.2 MB (1198624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d294a31ccccc8d9ba111b84126e1d1faf0694e471671e7e2e14746ac5d3053e`  
		Last Modified: Wed, 05 Jun 2024 05:43:18 GMT  
		Size: 5.6 MB (5553836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6b0882e06a01109e9d09203288aa1bad53597891b8ddaa829c49c12855c2a2`  
		Last Modified: Wed, 05 Jun 2024 06:23:20 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b2cc9d33d4188b74d5639905c35e1ae64b834ccb7d32434fd4b8837d05cfd4`  
		Last Modified: Wed, 05 Jun 2024 06:23:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d224207e0d7d191c70524deb5528af9138c432498248da8a146ef4f2ccb76522`  
		Last Modified: Wed, 05 Jun 2024 06:23:47 GMT  
		Size: 177.0 MB (177011351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a137e92617700e58635604a6f65d1484c36f3cca19e3c70c96ff77b688d60dfc`  
		Last Modified: Wed, 05 Jun 2024 06:23:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1309495ac492939fdfde58cf1da120fd01dea776ac0a3e45571a05ea16397fbf`  
		Last Modified: Wed, 05 Jun 2024 06:24:03 GMT  
		Size: 50.9 MB (50942120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78400d1f7dd7d6fa4c340c75f515ba00dd63ee35abe4412137c64f5eb2798199`  
		Last Modified: Wed, 05 Jun 2024 06:23:56 GMT  
		Size: 323.2 KB (323163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034066f6b071e6963ba4d9a67225826faeb2a36f7ab0cf1b22c3eb9ce5b50d4c`  
		Last Modified: Wed, 05 Jun 2024 06:23:56 GMT  
		Size: 1.1 MB (1130676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f8bbb2feda4a64a67d52e553f651c44b46c596aafc2576d96f5a013c213f81`  
		Last Modified: Wed, 05 Jun 2024 06:25:49 GMT  
		Size: 570.7 MB (570696392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:36c5d63c3e3503fd964b11d74458e53c2b2e48a679d495e0440e9a6d550d9266
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.4 MB (726381143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6960f2606800f20438876589aa153a9c53debd190b2030efe33b97c115e82736`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:12:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:12:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:12:50 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 03:12:51 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 03:12:51 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 03:12:51 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 03:12:51 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 03:16:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:16:23 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 03:16:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 03:16:23 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 03:17:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:17:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 03:17:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e858563dc379808e6dafb87d98be87a469d7eadbcf328692a93f4871b6455e1`  
		Last Modified: Wed, 05 Jun 2024 03:30:46 GMT  
		Size: 1.2 MB (1200168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edab1234b48134f83b0a8a78bf4f5ba92c3fd7169ab7bc857f88f2a379cb30c9`  
		Last Modified: Wed, 05 Jun 2024 03:30:44 GMT  
		Size: 4.7 MB (4680859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eef1562d1117fe923258ae07680e112c854d6d1460cf20b27880d3aab2b0288`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8b7cf88071311bc31839d24867f06c0215aacdd0ceed317af28071aae1ceb4`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cc5702211aa2134c20f699beae6e440479eda034ceeebfa97646b03af17f78`  
		Last Modified: Wed, 05 Jun 2024 03:31:25 GMT  
		Size: 157.5 MB (157481015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e3fc988f22240cdb1af0ce8a9135a08dd84e0c02b217c5b07783383ead3493`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81cfdc59b78354ae32bcf5b55594f95d7055d41a7dc855a9b8839be3e74546b9`  
		Last Modified: Wed, 05 Jun 2024 03:31:38 GMT  
		Size: 40.5 MB (40506614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7538f808a96d47124193d51356dff2e3ccceb60b634042d2154110232c7ea4f7`  
		Last Modified: Wed, 05 Jun 2024 03:31:33 GMT  
		Size: 323.2 KB (323163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b11dbf16d842b6f56ac3b8ece22e46a6e2358c415d73f99eb0487951c1742f`  
		Last Modified: Wed, 05 Jun 2024 03:31:33 GMT  
		Size: 1.1 MB (1062764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f571459483a794c9e8e8f534a0c2b226bbebc228e2ab5af766c7a27c79c84442`  
		Last Modified: Wed, 05 Jun 2024 03:33:05 GMT  
		Size: 496.5 MB (496520245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3936901dcc1fe259133babc1c556f049c38cbc96577dec5975cbb0e01d4d8454
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.6 MB (785645182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974cf60bc830169980e9b095faecb33cc29aa519d93ca6f14529311cde4dec8e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:59:59 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:00:11 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:02:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:02:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:02:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:02:42 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:02:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:03:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:03:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:13:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ee698c21fd64dc89cbdfed5321d109a9525aeebaf898cfde7ecb7f55d0a90`  
		Last Modified: Wed, 05 Jun 2024 05:48:06 GMT  
		Size: 1.2 MB (1198556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67daca712e09cc6c6e34fb19421e400b0bc9bbf913a3b29ecd56e64e21014a0d`  
		Last Modified: Wed, 05 Jun 2024 05:48:04 GMT  
		Size: 5.5 MB (5531978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e8be46bf9534062563fa783cb360be4fc65686aca38b1df2586b3954e11b35`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1801d6616a2cd0f216d69bf6a76decd240fdeace1a5bd5a21e5c5ef31ee01f44`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8701d0e1bacd603262a548b1ca107c7eb378d56b7538d2fe69af7743dfc1fa14`  
		Last Modified: Wed, 05 Jun 2024 05:48:38 GMT  
		Size: 171.4 MB (171404678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe24a94caf00c45eb7e226d915071a9521a262a141c8006164fac3f907a66583`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6055caabb25cb3f56fdf7f72c7c835b3b1a31b20b9bbd24ae2fee4ab2a32811`  
		Last Modified: Wed, 05 Jun 2024 05:48:51 GMT  
		Size: 45.2 MB (45207269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c79a6839de6fd95d123e3a7422ff707f103d1ce1a76a5eb533428e9406735e`  
		Last Modified: Wed, 05 Jun 2024 05:48:46 GMT  
		Size: 323.2 KB (323165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387c477a284d1c9c16d5e3f1580b6ccf4b4667a94ec48b60aa971e29021b82fa`  
		Last Modified: Wed, 05 Jun 2024 05:48:46 GMT  
		Size: 1.1 MB (1114835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac49e590bb5479f0b16356093f73e0f90c036c4db368b00ba0dbb8975dc79ec`  
		Last Modified: Wed, 05 Jun 2024 05:50:20 GMT  
		Size: 533.7 MB (533656966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:3df8da088aa11f07d90c52a492f4194cafd3991e25c28e1a9aa06b44cdba7ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:fec57145ac32bd7a7d35964abf6da04b2f194d9ac53ed248dcbb18050bff8be2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.7 MB (281675200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a861ce36724c31493bab46152b97f57985970018126466169beef11695bfd4c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:35:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:36:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:45:36 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:45:36 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:45:36 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:45:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:45:36 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:46:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:46:58 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:46:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:46:59 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:47:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:47:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:47:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:48:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0b2f3debe6d753bc3abafc6b460a0a4eefe9091da70a55428112cb3b9997d0`  
		Last Modified: Wed, 05 Jun 2024 05:43:17 GMT  
		Size: 1.2 MB (1198624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d294a31ccccc8d9ba111b84126e1d1faf0694e471671e7e2e14746ac5d3053e`  
		Last Modified: Wed, 05 Jun 2024 05:43:18 GMT  
		Size: 5.6 MB (5553836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6b0882e06a01109e9d09203288aa1bad53597891b8ddaa829c49c12855c2a2`  
		Last Modified: Wed, 05 Jun 2024 06:23:20 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b2cc9d33d4188b74d5639905c35e1ae64b834ccb7d32434fd4b8837d05cfd4`  
		Last Modified: Wed, 05 Jun 2024 06:23:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d224207e0d7d191c70524deb5528af9138c432498248da8a146ef4f2ccb76522`  
		Last Modified: Wed, 05 Jun 2024 06:23:47 GMT  
		Size: 177.0 MB (177011351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a137e92617700e58635604a6f65d1484c36f3cca19e3c70c96ff77b688d60dfc`  
		Last Modified: Wed, 05 Jun 2024 06:23:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1309495ac492939fdfde58cf1da120fd01dea776ac0a3e45571a05ea16397fbf`  
		Last Modified: Wed, 05 Jun 2024 06:24:03 GMT  
		Size: 50.9 MB (50942120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78400d1f7dd7d6fa4c340c75f515ba00dd63ee35abe4412137c64f5eb2798199`  
		Last Modified: Wed, 05 Jun 2024 06:23:56 GMT  
		Size: 323.2 KB (323163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034066f6b071e6963ba4d9a67225826faeb2a36f7ab0cf1b22c3eb9ce5b50d4c`  
		Last Modified: Wed, 05 Jun 2024 06:23:56 GMT  
		Size: 1.1 MB (1130676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89227546201963e514197115bc817fd2fd231437c5230cc92deea20abe8f729e`  
		Last Modified: Wed, 05 Jun 2024 06:24:17 GMT  
		Size: 16.9 MB (16928717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:9524686e4eec342bcccf61e5f3cf478e5fc8ca325426c4e682bbed1f9e8f0613
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244891054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2912a93b958d3c6f8c6738c11a9eaf1509be89540af84906adeaba05830ea2cd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:12:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:12:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:12:50 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 03:12:51 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 03:12:51 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 03:12:51 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 03:12:51 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 03:16:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:16:23 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 03:16:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 03:16:23 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 03:17:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:17:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 03:17:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:18:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e858563dc379808e6dafb87d98be87a469d7eadbcf328692a93f4871b6455e1`  
		Last Modified: Wed, 05 Jun 2024 03:30:46 GMT  
		Size: 1.2 MB (1200168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edab1234b48134f83b0a8a78bf4f5ba92c3fd7169ab7bc857f88f2a379cb30c9`  
		Last Modified: Wed, 05 Jun 2024 03:30:44 GMT  
		Size: 4.7 MB (4680859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eef1562d1117fe923258ae07680e112c854d6d1460cf20b27880d3aab2b0288`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8b7cf88071311bc31839d24867f06c0215aacdd0ceed317af28071aae1ceb4`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cc5702211aa2134c20f699beae6e440479eda034ceeebfa97646b03af17f78`  
		Last Modified: Wed, 05 Jun 2024 03:31:25 GMT  
		Size: 157.5 MB (157481015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e3fc988f22240cdb1af0ce8a9135a08dd84e0c02b217c5b07783383ead3493`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81cfdc59b78354ae32bcf5b55594f95d7055d41a7dc855a9b8839be3e74546b9`  
		Last Modified: Wed, 05 Jun 2024 03:31:38 GMT  
		Size: 40.5 MB (40506614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7538f808a96d47124193d51356dff2e3ccceb60b634042d2154110232c7ea4f7`  
		Last Modified: Wed, 05 Jun 2024 03:31:33 GMT  
		Size: 323.2 KB (323163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b11dbf16d842b6f56ac3b8ece22e46a6e2358c415d73f99eb0487951c1742f`  
		Last Modified: Wed, 05 Jun 2024 03:31:33 GMT  
		Size: 1.1 MB (1062764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d73dceec9fb4fcaad37b56a30558433c3f7ea50e56f1fbab4ce3a345dca0f`  
		Last Modified: Wed, 05 Jun 2024 03:31:50 GMT  
		Size: 15.0 MB (15030156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3a671b4c28068bf5c2e42fdeda701bb9940585bdb65fe1ae28cf5fcce0cd1d34
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268518043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9508b7afb1e94eedb4b19e71c501cfacbc4fcdd755d4ccaad7514b48c28bbe79`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:59:59 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:00:11 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:02:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:02:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:02:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:02:42 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:02:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:03:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:03:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:03:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ee698c21fd64dc89cbdfed5321d109a9525aeebaf898cfde7ecb7f55d0a90`  
		Last Modified: Wed, 05 Jun 2024 05:48:06 GMT  
		Size: 1.2 MB (1198556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67daca712e09cc6c6e34fb19421e400b0bc9bbf913a3b29ecd56e64e21014a0d`  
		Last Modified: Wed, 05 Jun 2024 05:48:04 GMT  
		Size: 5.5 MB (5531978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e8be46bf9534062563fa783cb360be4fc65686aca38b1df2586b3954e11b35`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1801d6616a2cd0f216d69bf6a76decd240fdeace1a5bd5a21e5c5ef31ee01f44`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8701d0e1bacd603262a548b1ca107c7eb378d56b7538d2fe69af7743dfc1fa14`  
		Last Modified: Wed, 05 Jun 2024 05:48:38 GMT  
		Size: 171.4 MB (171404678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe24a94caf00c45eb7e226d915071a9521a262a141c8006164fac3f907a66583`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6055caabb25cb3f56fdf7f72c7c835b3b1a31b20b9bbd24ae2fee4ab2a32811`  
		Last Modified: Wed, 05 Jun 2024 05:48:51 GMT  
		Size: 45.2 MB (45207269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c79a6839de6fd95d123e3a7422ff707f103d1ce1a76a5eb533428e9406735e`  
		Last Modified: Wed, 05 Jun 2024 05:48:46 GMT  
		Size: 323.2 KB (323165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387c477a284d1c9c16d5e3f1580b6ccf4b4667a94ec48b60aa971e29021b82fa`  
		Last Modified: Wed, 05 Jun 2024 05:48:46 GMT  
		Size: 1.1 MB (1114835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebd853f08ff8e0988f316bf359278de5c7b16fd14c124c9ad074e2fd06d711f`  
		Last Modified: Wed, 05 Jun 2024 05:49:04 GMT  
		Size: 16.5 MB (16529827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:3df8da088aa11f07d90c52a492f4194cafd3991e25c28e1a9aa06b44cdba7ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:fec57145ac32bd7a7d35964abf6da04b2f194d9ac53ed248dcbb18050bff8be2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.7 MB (281675200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a861ce36724c31493bab46152b97f57985970018126466169beef11695bfd4c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:35:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:36:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:45:36 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:45:36 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:45:36 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:45:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:45:36 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:46:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:46:58 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:46:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:46:59 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:47:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:47:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:47:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:48:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0b2f3debe6d753bc3abafc6b460a0a4eefe9091da70a55428112cb3b9997d0`  
		Last Modified: Wed, 05 Jun 2024 05:43:17 GMT  
		Size: 1.2 MB (1198624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d294a31ccccc8d9ba111b84126e1d1faf0694e471671e7e2e14746ac5d3053e`  
		Last Modified: Wed, 05 Jun 2024 05:43:18 GMT  
		Size: 5.6 MB (5553836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6b0882e06a01109e9d09203288aa1bad53597891b8ddaa829c49c12855c2a2`  
		Last Modified: Wed, 05 Jun 2024 06:23:20 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b2cc9d33d4188b74d5639905c35e1ae64b834ccb7d32434fd4b8837d05cfd4`  
		Last Modified: Wed, 05 Jun 2024 06:23:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d224207e0d7d191c70524deb5528af9138c432498248da8a146ef4f2ccb76522`  
		Last Modified: Wed, 05 Jun 2024 06:23:47 GMT  
		Size: 177.0 MB (177011351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a137e92617700e58635604a6f65d1484c36f3cca19e3c70c96ff77b688d60dfc`  
		Last Modified: Wed, 05 Jun 2024 06:23:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1309495ac492939fdfde58cf1da120fd01dea776ac0a3e45571a05ea16397fbf`  
		Last Modified: Wed, 05 Jun 2024 06:24:03 GMT  
		Size: 50.9 MB (50942120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78400d1f7dd7d6fa4c340c75f515ba00dd63ee35abe4412137c64f5eb2798199`  
		Last Modified: Wed, 05 Jun 2024 06:23:56 GMT  
		Size: 323.2 KB (323163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034066f6b071e6963ba4d9a67225826faeb2a36f7ab0cf1b22c3eb9ce5b50d4c`  
		Last Modified: Wed, 05 Jun 2024 06:23:56 GMT  
		Size: 1.1 MB (1130676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89227546201963e514197115bc817fd2fd231437c5230cc92deea20abe8f729e`  
		Last Modified: Wed, 05 Jun 2024 06:24:17 GMT  
		Size: 16.9 MB (16928717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:9524686e4eec342bcccf61e5f3cf478e5fc8ca325426c4e682bbed1f9e8f0613
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244891054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2912a93b958d3c6f8c6738c11a9eaf1509be89540af84906adeaba05830ea2cd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:12:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:12:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:12:50 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 03:12:51 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 03:12:51 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 03:12:51 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 03:12:51 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 03:16:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:16:23 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 03:16:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 03:16:23 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 03:17:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:17:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 03:17:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:18:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e858563dc379808e6dafb87d98be87a469d7eadbcf328692a93f4871b6455e1`  
		Last Modified: Wed, 05 Jun 2024 03:30:46 GMT  
		Size: 1.2 MB (1200168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edab1234b48134f83b0a8a78bf4f5ba92c3fd7169ab7bc857f88f2a379cb30c9`  
		Last Modified: Wed, 05 Jun 2024 03:30:44 GMT  
		Size: 4.7 MB (4680859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eef1562d1117fe923258ae07680e112c854d6d1460cf20b27880d3aab2b0288`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8b7cf88071311bc31839d24867f06c0215aacdd0ceed317af28071aae1ceb4`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cc5702211aa2134c20f699beae6e440479eda034ceeebfa97646b03af17f78`  
		Last Modified: Wed, 05 Jun 2024 03:31:25 GMT  
		Size: 157.5 MB (157481015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e3fc988f22240cdb1af0ce8a9135a08dd84e0c02b217c5b07783383ead3493`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81cfdc59b78354ae32bcf5b55594f95d7055d41a7dc855a9b8839be3e74546b9`  
		Last Modified: Wed, 05 Jun 2024 03:31:38 GMT  
		Size: 40.5 MB (40506614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7538f808a96d47124193d51356dff2e3ccceb60b634042d2154110232c7ea4f7`  
		Last Modified: Wed, 05 Jun 2024 03:31:33 GMT  
		Size: 323.2 KB (323163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b11dbf16d842b6f56ac3b8ece22e46a6e2358c415d73f99eb0487951c1742f`  
		Last Modified: Wed, 05 Jun 2024 03:31:33 GMT  
		Size: 1.1 MB (1062764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d73dceec9fb4fcaad37b56a30558433c3f7ea50e56f1fbab4ce3a345dca0f`  
		Last Modified: Wed, 05 Jun 2024 03:31:50 GMT  
		Size: 15.0 MB (15030156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3a671b4c28068bf5c2e42fdeda701bb9940585bdb65fe1ae28cf5fcce0cd1d34
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268518043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9508b7afb1e94eedb4b19e71c501cfacbc4fcdd755d4ccaad7514b48c28bbe79`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:59:59 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:00:11 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:02:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:02:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:02:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:02:42 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:02:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:03:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:03:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:03:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ee698c21fd64dc89cbdfed5321d109a9525aeebaf898cfde7ecb7f55d0a90`  
		Last Modified: Wed, 05 Jun 2024 05:48:06 GMT  
		Size: 1.2 MB (1198556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67daca712e09cc6c6e34fb19421e400b0bc9bbf913a3b29ecd56e64e21014a0d`  
		Last Modified: Wed, 05 Jun 2024 05:48:04 GMT  
		Size: 5.5 MB (5531978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e8be46bf9534062563fa783cb360be4fc65686aca38b1df2586b3954e11b35`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1801d6616a2cd0f216d69bf6a76decd240fdeace1a5bd5a21e5c5ef31ee01f44`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8701d0e1bacd603262a548b1ca107c7eb378d56b7538d2fe69af7743dfc1fa14`  
		Last Modified: Wed, 05 Jun 2024 05:48:38 GMT  
		Size: 171.4 MB (171404678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe24a94caf00c45eb7e226d915071a9521a262a141c8006164fac3f907a66583`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6055caabb25cb3f56fdf7f72c7c835b3b1a31b20b9bbd24ae2fee4ab2a32811`  
		Last Modified: Wed, 05 Jun 2024 05:48:51 GMT  
		Size: 45.2 MB (45207269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c79a6839de6fd95d123e3a7422ff707f103d1ce1a76a5eb533428e9406735e`  
		Last Modified: Wed, 05 Jun 2024 05:48:46 GMT  
		Size: 323.2 KB (323165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387c477a284d1c9c16d5e3f1580b6ccf4b4667a94ec48b60aa971e29021b82fa`  
		Last Modified: Wed, 05 Jun 2024 05:48:46 GMT  
		Size: 1.1 MB (1114835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebd853f08ff8e0988f316bf359278de5c7b16fd14c124c9ad074e2fd06d711f`  
		Last Modified: Wed, 05 Jun 2024 05:49:04 GMT  
		Size: 16.5 MB (16529827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:acc93816e625c953b31add8f3c209360c6e4eda9cf771f69d299e2f4141b917b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:d47940cb6d8e08ea5cbcdf9e313eeb650cf5d249f633957ff4b7365f764d3395
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264746483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d495043da1c80dc92e5e2853c7da9205887719f7e9ec8ab898d31356d5d58e0e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:35:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:36:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:45:36 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:45:36 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:45:36 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:45:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:45:36 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:46:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:46:58 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:46:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:46:59 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:47:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:47:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:47:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0b2f3debe6d753bc3abafc6b460a0a4eefe9091da70a55428112cb3b9997d0`  
		Last Modified: Wed, 05 Jun 2024 05:43:17 GMT  
		Size: 1.2 MB (1198624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d294a31ccccc8d9ba111b84126e1d1faf0694e471671e7e2e14746ac5d3053e`  
		Last Modified: Wed, 05 Jun 2024 05:43:18 GMT  
		Size: 5.6 MB (5553836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6b0882e06a01109e9d09203288aa1bad53597891b8ddaa829c49c12855c2a2`  
		Last Modified: Wed, 05 Jun 2024 06:23:20 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b2cc9d33d4188b74d5639905c35e1ae64b834ccb7d32434fd4b8837d05cfd4`  
		Last Modified: Wed, 05 Jun 2024 06:23:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d224207e0d7d191c70524deb5528af9138c432498248da8a146ef4f2ccb76522`  
		Last Modified: Wed, 05 Jun 2024 06:23:47 GMT  
		Size: 177.0 MB (177011351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a137e92617700e58635604a6f65d1484c36f3cca19e3c70c96ff77b688d60dfc`  
		Last Modified: Wed, 05 Jun 2024 06:23:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1309495ac492939fdfde58cf1da120fd01dea776ac0a3e45571a05ea16397fbf`  
		Last Modified: Wed, 05 Jun 2024 06:24:03 GMT  
		Size: 50.9 MB (50942120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78400d1f7dd7d6fa4c340c75f515ba00dd63ee35abe4412137c64f5eb2798199`  
		Last Modified: Wed, 05 Jun 2024 06:23:56 GMT  
		Size: 323.2 KB (323163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034066f6b071e6963ba4d9a67225826faeb2a36f7ab0cf1b22c3eb9ce5b50d4c`  
		Last Modified: Wed, 05 Jun 2024 06:23:56 GMT  
		Size: 1.1 MB (1130676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:165cecfb4dbf2f68f6c08eafa4858ed61352884fc120489747e15899f15348ca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229860898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316c7c6c49aa569fce41510ac70b2984c9432f081bc10e6a213ec3a3577a7daf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:12:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:12:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:12:50 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 03:12:51 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 03:12:51 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 03:12:51 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 03:12:51 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 03:16:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:16:23 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 03:16:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 03:16:23 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 03:17:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:17:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 03:17:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e858563dc379808e6dafb87d98be87a469d7eadbcf328692a93f4871b6455e1`  
		Last Modified: Wed, 05 Jun 2024 03:30:46 GMT  
		Size: 1.2 MB (1200168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edab1234b48134f83b0a8a78bf4f5ba92c3fd7169ab7bc857f88f2a379cb30c9`  
		Last Modified: Wed, 05 Jun 2024 03:30:44 GMT  
		Size: 4.7 MB (4680859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eef1562d1117fe923258ae07680e112c854d6d1460cf20b27880d3aab2b0288`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8b7cf88071311bc31839d24867f06c0215aacdd0ceed317af28071aae1ceb4`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cc5702211aa2134c20f699beae6e440479eda034ceeebfa97646b03af17f78`  
		Last Modified: Wed, 05 Jun 2024 03:31:25 GMT  
		Size: 157.5 MB (157481015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e3fc988f22240cdb1af0ce8a9135a08dd84e0c02b217c5b07783383ead3493`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81cfdc59b78354ae32bcf5b55594f95d7055d41a7dc855a9b8839be3e74546b9`  
		Last Modified: Wed, 05 Jun 2024 03:31:38 GMT  
		Size: 40.5 MB (40506614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7538f808a96d47124193d51356dff2e3ccceb60b634042d2154110232c7ea4f7`  
		Last Modified: Wed, 05 Jun 2024 03:31:33 GMT  
		Size: 323.2 KB (323163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b11dbf16d842b6f56ac3b8ece22e46a6e2358c415d73f99eb0487951c1742f`  
		Last Modified: Wed, 05 Jun 2024 03:31:33 GMT  
		Size: 1.1 MB (1062764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b2390c753cd204346f0cebad94b8475d5a430db6f800b57cf4abea0b1d9f31ee
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251988216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfecb0d5f7e93eace5ec5c6aade6cfbaf7f049199f5f69200fce6fa26b3d462`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:59:59 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:00:11 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:02:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:02:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:02:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:02:42 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:02:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:03:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:03:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ee698c21fd64dc89cbdfed5321d109a9525aeebaf898cfde7ecb7f55d0a90`  
		Last Modified: Wed, 05 Jun 2024 05:48:06 GMT  
		Size: 1.2 MB (1198556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67daca712e09cc6c6e34fb19421e400b0bc9bbf913a3b29ecd56e64e21014a0d`  
		Last Modified: Wed, 05 Jun 2024 05:48:04 GMT  
		Size: 5.5 MB (5531978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e8be46bf9534062563fa783cb360be4fc65686aca38b1df2586b3954e11b35`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1801d6616a2cd0f216d69bf6a76decd240fdeace1a5bd5a21e5c5ef31ee01f44`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8701d0e1bacd603262a548b1ca107c7eb378d56b7538d2fe69af7743dfc1fa14`  
		Last Modified: Wed, 05 Jun 2024 05:48:38 GMT  
		Size: 171.4 MB (171404678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe24a94caf00c45eb7e226d915071a9521a262a141c8006164fac3f907a66583`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6055caabb25cb3f56fdf7f72c7c835b3b1a31b20b9bbd24ae2fee4ab2a32811`  
		Last Modified: Wed, 05 Jun 2024 05:48:51 GMT  
		Size: 45.2 MB (45207269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c79a6839de6fd95d123e3a7422ff707f103d1ce1a76a5eb533428e9406735e`  
		Last Modified: Wed, 05 Jun 2024 05:48:46 GMT  
		Size: 323.2 KB (323165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387c477a284d1c9c16d5e3f1580b6ccf4b4667a94ec48b60aa971e29021b82fa`  
		Last Modified: Wed, 05 Jun 2024 05:48:46 GMT  
		Size: 1.1 MB (1114835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:acc93816e625c953b31add8f3c209360c6e4eda9cf771f69d299e2f4141b917b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:d47940cb6d8e08ea5cbcdf9e313eeb650cf5d249f633957ff4b7365f764d3395
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264746483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d495043da1c80dc92e5e2853c7da9205887719f7e9ec8ab898d31356d5d58e0e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:35:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:36:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:45:36 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:45:36 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:45:36 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:45:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:45:36 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:46:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:46:58 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:46:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:46:59 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:47:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:47:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:47:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0b2f3debe6d753bc3abafc6b460a0a4eefe9091da70a55428112cb3b9997d0`  
		Last Modified: Wed, 05 Jun 2024 05:43:17 GMT  
		Size: 1.2 MB (1198624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d294a31ccccc8d9ba111b84126e1d1faf0694e471671e7e2e14746ac5d3053e`  
		Last Modified: Wed, 05 Jun 2024 05:43:18 GMT  
		Size: 5.6 MB (5553836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6b0882e06a01109e9d09203288aa1bad53597891b8ddaa829c49c12855c2a2`  
		Last Modified: Wed, 05 Jun 2024 06:23:20 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b2cc9d33d4188b74d5639905c35e1ae64b834ccb7d32434fd4b8837d05cfd4`  
		Last Modified: Wed, 05 Jun 2024 06:23:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d224207e0d7d191c70524deb5528af9138c432498248da8a146ef4f2ccb76522`  
		Last Modified: Wed, 05 Jun 2024 06:23:47 GMT  
		Size: 177.0 MB (177011351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a137e92617700e58635604a6f65d1484c36f3cca19e3c70c96ff77b688d60dfc`  
		Last Modified: Wed, 05 Jun 2024 06:23:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1309495ac492939fdfde58cf1da120fd01dea776ac0a3e45571a05ea16397fbf`  
		Last Modified: Wed, 05 Jun 2024 06:24:03 GMT  
		Size: 50.9 MB (50942120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78400d1f7dd7d6fa4c340c75f515ba00dd63ee35abe4412137c64f5eb2798199`  
		Last Modified: Wed, 05 Jun 2024 06:23:56 GMT  
		Size: 323.2 KB (323163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034066f6b071e6963ba4d9a67225826faeb2a36f7ab0cf1b22c3eb9ce5b50d4c`  
		Last Modified: Wed, 05 Jun 2024 06:23:56 GMT  
		Size: 1.1 MB (1130676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:165cecfb4dbf2f68f6c08eafa4858ed61352884fc120489747e15899f15348ca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229860898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316c7c6c49aa569fce41510ac70b2984c9432f081bc10e6a213ec3a3577a7daf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:12:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:12:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:12:50 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 03:12:51 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 03:12:51 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 03:12:51 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 03:12:51 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 03:16:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:16:23 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 03:16:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 03:16:23 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 03:17:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:17:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 03:17:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e858563dc379808e6dafb87d98be87a469d7eadbcf328692a93f4871b6455e1`  
		Last Modified: Wed, 05 Jun 2024 03:30:46 GMT  
		Size: 1.2 MB (1200168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edab1234b48134f83b0a8a78bf4f5ba92c3fd7169ab7bc857f88f2a379cb30c9`  
		Last Modified: Wed, 05 Jun 2024 03:30:44 GMT  
		Size: 4.7 MB (4680859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eef1562d1117fe923258ae07680e112c854d6d1460cf20b27880d3aab2b0288`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8b7cf88071311bc31839d24867f06c0215aacdd0ceed317af28071aae1ceb4`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cc5702211aa2134c20f699beae6e440479eda034ceeebfa97646b03af17f78`  
		Last Modified: Wed, 05 Jun 2024 03:31:25 GMT  
		Size: 157.5 MB (157481015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e3fc988f22240cdb1af0ce8a9135a08dd84e0c02b217c5b07783383ead3493`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81cfdc59b78354ae32bcf5b55594f95d7055d41a7dc855a9b8839be3e74546b9`  
		Last Modified: Wed, 05 Jun 2024 03:31:38 GMT  
		Size: 40.5 MB (40506614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7538f808a96d47124193d51356dff2e3ccceb60b634042d2154110232c7ea4f7`  
		Last Modified: Wed, 05 Jun 2024 03:31:33 GMT  
		Size: 323.2 KB (323163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b11dbf16d842b6f56ac3b8ece22e46a6e2358c415d73f99eb0487951c1742f`  
		Last Modified: Wed, 05 Jun 2024 03:31:33 GMT  
		Size: 1.1 MB (1062764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b2390c753cd204346f0cebad94b8475d5a430db6f800b57cf4abea0b1d9f31ee
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251988216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfecb0d5f7e93eace5ec5c6aade6cfbaf7f049199f5f69200fce6fa26b3d462`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:59:59 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:00:11 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:02:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:02:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:02:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:02:42 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:02:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:03:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:03:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ee698c21fd64dc89cbdfed5321d109a9525aeebaf898cfde7ecb7f55d0a90`  
		Last Modified: Wed, 05 Jun 2024 05:48:06 GMT  
		Size: 1.2 MB (1198556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67daca712e09cc6c6e34fb19421e400b0bc9bbf913a3b29ecd56e64e21014a0d`  
		Last Modified: Wed, 05 Jun 2024 05:48:04 GMT  
		Size: 5.5 MB (5531978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e8be46bf9534062563fa783cb360be4fc65686aca38b1df2586b3954e11b35`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1801d6616a2cd0f216d69bf6a76decd240fdeace1a5bd5a21e5c5ef31ee01f44`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8701d0e1bacd603262a548b1ca107c7eb378d56b7538d2fe69af7743dfc1fa14`  
		Last Modified: Wed, 05 Jun 2024 05:48:38 GMT  
		Size: 171.4 MB (171404678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe24a94caf00c45eb7e226d915071a9521a262a141c8006164fac3f907a66583`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6055caabb25cb3f56fdf7f72c7c835b3b1a31b20b9bbd24ae2fee4ab2a32811`  
		Last Modified: Wed, 05 Jun 2024 05:48:51 GMT  
		Size: 45.2 MB (45207269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c79a6839de6fd95d123e3a7422ff707f103d1ce1a76a5eb533428e9406735e`  
		Last Modified: Wed, 05 Jun 2024 05:48:46 GMT  
		Size: 323.2 KB (323165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387c477a284d1c9c16d5e3f1580b6ccf4b4667a94ec48b60aa971e29021b82fa`  
		Last Modified: Wed, 05 Jun 2024 05:48:46 GMT  
		Size: 1.1 MB (1114835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:86a20463b4db39800af4f86a55dea7e21336d3e54a10670e53aadf4a74d8a164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:d06ff3c3b27e9bccef03577c38a1467893130dd68a1fa2c6b17e29154d0b2e20
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212350524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1030feebccda0104be30c5d9aa9d0c1baec82db0e30bd8215fc352f36f8b66c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:35:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:36:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:45:36 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:45:36 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:45:36 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:45:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:45:36 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:46:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:46:58 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:46:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:46:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0b2f3debe6d753bc3abafc6b460a0a4eefe9091da70a55428112cb3b9997d0`  
		Last Modified: Wed, 05 Jun 2024 05:43:17 GMT  
		Size: 1.2 MB (1198624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d294a31ccccc8d9ba111b84126e1d1faf0694e471671e7e2e14746ac5d3053e`  
		Last Modified: Wed, 05 Jun 2024 05:43:18 GMT  
		Size: 5.6 MB (5553836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6b0882e06a01109e9d09203288aa1bad53597891b8ddaa829c49c12855c2a2`  
		Last Modified: Wed, 05 Jun 2024 06:23:20 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b2cc9d33d4188b74d5639905c35e1ae64b834ccb7d32434fd4b8837d05cfd4`  
		Last Modified: Wed, 05 Jun 2024 06:23:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d224207e0d7d191c70524deb5528af9138c432498248da8a146ef4f2ccb76522`  
		Last Modified: Wed, 05 Jun 2024 06:23:47 GMT  
		Size: 177.0 MB (177011351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a137e92617700e58635604a6f65d1484c36f3cca19e3c70c96ff77b688d60dfc`  
		Last Modified: Wed, 05 Jun 2024 06:23:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:9a0531b6d7cf92629b284677cfd2f9ef67ebc35bc12a8bd0c8cdae8f9b7e390f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187968357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a2b5bf6900795dc6cab29ca5c3fdc5dfa6944dcbfa84510972bfc77688b5852`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:12:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:12:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:12:50 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 03:12:51 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 03:12:51 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 03:12:51 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 03:12:51 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 03:16:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:16:23 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 03:16:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 03:16:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e858563dc379808e6dafb87d98be87a469d7eadbcf328692a93f4871b6455e1`  
		Last Modified: Wed, 05 Jun 2024 03:30:46 GMT  
		Size: 1.2 MB (1200168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edab1234b48134f83b0a8a78bf4f5ba92c3fd7169ab7bc857f88f2a379cb30c9`  
		Last Modified: Wed, 05 Jun 2024 03:30:44 GMT  
		Size: 4.7 MB (4680859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eef1562d1117fe923258ae07680e112c854d6d1460cf20b27880d3aab2b0288`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8b7cf88071311bc31839d24867f06c0215aacdd0ceed317af28071aae1ceb4`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cc5702211aa2134c20f699beae6e440479eda034ceeebfa97646b03af17f78`  
		Last Modified: Wed, 05 Jun 2024 03:31:25 GMT  
		Size: 157.5 MB (157481015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e3fc988f22240cdb1af0ce8a9135a08dd84e0c02b217c5b07783383ead3493`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3b3f3091c2a307515fe9cfeb70961bf8b51fb50d2271a0124d1794c9200d83d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205342947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbcdda2db64e31d27975630f071ef7c4c16c8bc08ced9807c40f62a51ed8d41e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:59:59 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:00:11 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:02:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:02:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:02:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:02:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ee698c21fd64dc89cbdfed5321d109a9525aeebaf898cfde7ecb7f55d0a90`  
		Last Modified: Wed, 05 Jun 2024 05:48:06 GMT  
		Size: 1.2 MB (1198556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67daca712e09cc6c6e34fb19421e400b0bc9bbf913a3b29ecd56e64e21014a0d`  
		Last Modified: Wed, 05 Jun 2024 05:48:04 GMT  
		Size: 5.5 MB (5531978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e8be46bf9534062563fa783cb360be4fc65686aca38b1df2586b3954e11b35`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1801d6616a2cd0f216d69bf6a76decd240fdeace1a5bd5a21e5c5ef31ee01f44`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8701d0e1bacd603262a548b1ca107c7eb378d56b7538d2fe69af7743dfc1fa14`  
		Last Modified: Wed, 05 Jun 2024 05:48:38 GMT  
		Size: 171.4 MB (171404678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe24a94caf00c45eb7e226d915071a9521a262a141c8006164fac3f907a66583`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:86a20463b4db39800af4f86a55dea7e21336d3e54a10670e53aadf4a74d8a164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:d06ff3c3b27e9bccef03577c38a1467893130dd68a1fa2c6b17e29154d0b2e20
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212350524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1030feebccda0104be30c5d9aa9d0c1baec82db0e30bd8215fc352f36f8b66c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:35:58 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:36:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:45:36 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:45:36 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:45:36 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:45:36 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:45:36 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:46:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:46:58 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:46:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:46:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0b2f3debe6d753bc3abafc6b460a0a4eefe9091da70a55428112cb3b9997d0`  
		Last Modified: Wed, 05 Jun 2024 05:43:17 GMT  
		Size: 1.2 MB (1198624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d294a31ccccc8d9ba111b84126e1d1faf0694e471671e7e2e14746ac5d3053e`  
		Last Modified: Wed, 05 Jun 2024 05:43:18 GMT  
		Size: 5.6 MB (5553836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6b0882e06a01109e9d09203288aa1bad53597891b8ddaa829c49c12855c2a2`  
		Last Modified: Wed, 05 Jun 2024 06:23:20 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b2cc9d33d4188b74d5639905c35e1ae64b834ccb7d32434fd4b8837d05cfd4`  
		Last Modified: Wed, 05 Jun 2024 06:23:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d224207e0d7d191c70524deb5528af9138c432498248da8a146ef4f2ccb76522`  
		Last Modified: Wed, 05 Jun 2024 06:23:47 GMT  
		Size: 177.0 MB (177011351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a137e92617700e58635604a6f65d1484c36f3cca19e3c70c96ff77b688d60dfc`  
		Last Modified: Wed, 05 Jun 2024 06:23:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:9a0531b6d7cf92629b284677cfd2f9ef67ebc35bc12a8bd0c8cdae8f9b7e390f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187968357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a2b5bf6900795dc6cab29ca5c3fdc5dfa6944dcbfa84510972bfc77688b5852`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:12:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:12:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:12:50 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 03:12:51 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 03:12:51 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 03:12:51 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 03:12:51 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 03:16:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:16:23 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 03:16:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 03:16:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e858563dc379808e6dafb87d98be87a469d7eadbcf328692a93f4871b6455e1`  
		Last Modified: Wed, 05 Jun 2024 03:30:46 GMT  
		Size: 1.2 MB (1200168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edab1234b48134f83b0a8a78bf4f5ba92c3fd7169ab7bc857f88f2a379cb30c9`  
		Last Modified: Wed, 05 Jun 2024 03:30:44 GMT  
		Size: 4.7 MB (4680859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eef1562d1117fe923258ae07680e112c854d6d1460cf20b27880d3aab2b0288`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8b7cf88071311bc31839d24867f06c0215aacdd0ceed317af28071aae1ceb4`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cc5702211aa2134c20f699beae6e440479eda034ceeebfa97646b03af17f78`  
		Last Modified: Wed, 05 Jun 2024 03:31:25 GMT  
		Size: 157.5 MB (157481015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e3fc988f22240cdb1af0ce8a9135a08dd84e0c02b217c5b07783383ead3493`  
		Last Modified: Wed, 05 Jun 2024 03:30:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3b3f3091c2a307515fe9cfeb70961bf8b51fb50d2271a0124d1794c9200d83d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205342947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbcdda2db64e31d27975630f071ef7c4c16c8bc08ced9807c40f62a51ed8d41e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:59:59 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:00:11 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:00:11 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:00:11 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Jun 2024 05:02:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:02:41 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Jun 2024 05:02:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:02:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1ee698c21fd64dc89cbdfed5321d109a9525aeebaf898cfde7ecb7f55d0a90`  
		Last Modified: Wed, 05 Jun 2024 05:48:06 GMT  
		Size: 1.2 MB (1198556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67daca712e09cc6c6e34fb19421e400b0bc9bbf913a3b29ecd56e64e21014a0d`  
		Last Modified: Wed, 05 Jun 2024 05:48:04 GMT  
		Size: 5.5 MB (5531978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e8be46bf9534062563fa783cb360be4fc65686aca38b1df2586b3954e11b35`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 2.0 KB (2024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1801d6616a2cd0f216d69bf6a76decd240fdeace1a5bd5a21e5c5ef31ee01f44`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8701d0e1bacd603262a548b1ca107c7eb378d56b7538d2fe69af7743dfc1fa14`  
		Last Modified: Wed, 05 Jun 2024 05:48:38 GMT  
		Size: 171.4 MB (171404678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe24a94caf00c45eb7e226d915071a9521a262a141c8006164fac3f907a66583`  
		Last Modified: Wed, 05 Jun 2024 05:48:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling`

```console
$ docker pull ros@sha256:5f04661331f7f5b8436131e062823706575533b394b56891bd9666ca5d878c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:6c30cecf18841ec4493fc206d8c63906980801503e2a88911db49035b3a70f64
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299756307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd504a35a414a0fff6a3a3cfdb872ff6eb158c969708d6d01da21b59681c2a9e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 06:10:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:20:19 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Jun 2024 06:21:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:21:04 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:21:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:21:04 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 06:21:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:21:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 06:21:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 06:21:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b7b089eccbc5711efe9b5e70ebf338500c3b4261cc08c5ad96463a57a9bf1`  
		Last Modified: Wed, 05 Jun 2024 06:30:49 GMT  
		Size: 683.8 KB (683789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac994edf240e70b612dad36f314b389ed36ff1bb920412484395a0454a1d61c`  
		Last Modified: Wed, 05 Jun 2024 06:30:48 GMT  
		Size: 4.6 MB (4617771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5b36f85e72e73135bfa90830916ffb2abb10c40af616211cd07463f290a9ce`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a052403e9ecb7c5356f8463bb90b17f27010035dba5a27455ea3aa205697689f`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4875ea069f77ccb9390426ba9a3add0497f8d4eff08001ddf9c0d16a327f7514`  
		Last Modified: Wed, 05 Jun 2024 06:32:51 GMT  
		Size: 122.5 MB (122451283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a253df8ece8660676ec84b140af57ae9d1e1102d6d00de41ef255dc4be2ec92`  
		Last Modified: Wed, 05 Jun 2024 06:32:33 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2662c619c85291f1c5373990ce67dd656732b1713e6a2e530dc4c7e919aa4d`  
		Last Modified: Wed, 05 Jun 2024 06:33:14 GMT  
		Size: 114.3 MB (114315856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46788892d21f6a27a3146a33bf193d36045bf80d7ccf46b31b7f81aa48ac2dd`  
		Last Modified: Wed, 05 Jun 2024 06:32:59 GMT  
		Size: 311.9 KB (311937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599c02e1aaa8a27726480aeda8f420f4d510c18c033236710719593a3a8683d2`  
		Last Modified: Wed, 05 Jun 2024 06:32:59 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8af64f7b4bca9f0f94faee8b3e77e6898cede65a278230955cd65948cd5998b`  
		Last Modified: Wed, 05 Jun 2024 06:33:03 GMT  
		Size: 27.7 MB (27665965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b3629b8ac343fec82ab34bdc012524b9511e1e196b7462730fc5b004b76cca46
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289897896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1849614724cd139a7faf4d210dc57321d0d2b243b7225b34b617987364d58c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:32:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:33:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:45:14 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Jun 2024 05:45:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:45:58 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:45:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:45:58 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:46:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:46:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:46:27 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:46:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b3822029b130a9434da04db278e695747571673f958098087aa1b0646f5e9`  
		Last Modified: Wed, 05 Jun 2024 05:55:18 GMT  
		Size: 684.9 KB (684936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b773b38eac33ca187f0b096cf08d40343b5c9d57818453f97613666eae7540`  
		Last Modified: Wed, 05 Jun 2024 05:55:16 GMT  
		Size: 4.6 MB (4612918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eed9b6478ee735e6559879b05f8a108b186e2185afbe1456b0bae55496e682`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f358deb3ce2f2d04e1ba6c224a7e7013fb4c1a6f8b1ba71583e1d609240449`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d3fc7f96a756b58b15da57d532f1288c13a4cbe173e9b8f7e894858ec6be1b`  
		Last Modified: Wed, 05 Jun 2024 05:57:21 GMT  
		Size: 117.3 MB (117266227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc15b5f12b05ed813b347aaa018910667314fe42cca600e7aceced207f800c69`  
		Last Modified: Wed, 05 Jun 2024 05:56:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4662d32b5079aa867b80b3da7b6aeff46fe9e17b6fe2259eb511f34086c06b`  
		Last Modified: Wed, 05 Jun 2024 05:57:42 GMT  
		Size: 111.2 MB (111160874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ed15ebbe5e1e631506250b6c996ae37c7ba07d31ab8d1319367c8c5e46d97a`  
		Last Modified: Wed, 05 Jun 2024 05:57:30 GMT  
		Size: 311.9 KB (311946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1ea445888bf5410c54c8096c7c8479ddbf15fcc0cf7cb3f86625b4c08264bd`  
		Last Modified: Wed, 05 Jun 2024 05:57:29 GMT  
		Size: 2.4 KB (2417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1c1854b7a8c4003cdbef2894a590e165775f3bbceaf4e101c38f11718d434e`  
		Last Modified: Wed, 05 Jun 2024 05:57:34 GMT  
		Size: 26.8 MB (26812168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:a87b57ce7b0bb0fcfe5faa58c8648fc08da53b1e46f0a8ac81ddc44798d65104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:0053f85471614952280cde2359dc1c0deaab4fae8f40a99b33d0d559c0ba0cc3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.8 MB (623792612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4c4910ed4c4015b001c54618ef1a9fe9877fc030ea0b4b8116a70679318521`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 06:10:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:20:19 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Jun 2024 06:21:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:21:04 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:21:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:21:04 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 06:21:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:21:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 06:21:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 06:21:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:22:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b7b089eccbc5711efe9b5e70ebf338500c3b4261cc08c5ad96463a57a9bf1`  
		Last Modified: Wed, 05 Jun 2024 06:30:49 GMT  
		Size: 683.8 KB (683789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac994edf240e70b612dad36f314b389ed36ff1bb920412484395a0454a1d61c`  
		Last Modified: Wed, 05 Jun 2024 06:30:48 GMT  
		Size: 4.6 MB (4617771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5b36f85e72e73135bfa90830916ffb2abb10c40af616211cd07463f290a9ce`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a052403e9ecb7c5356f8463bb90b17f27010035dba5a27455ea3aa205697689f`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4875ea069f77ccb9390426ba9a3add0497f8d4eff08001ddf9c0d16a327f7514`  
		Last Modified: Wed, 05 Jun 2024 06:32:51 GMT  
		Size: 122.5 MB (122451283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a253df8ece8660676ec84b140af57ae9d1e1102d6d00de41ef255dc4be2ec92`  
		Last Modified: Wed, 05 Jun 2024 06:32:33 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2662c619c85291f1c5373990ce67dd656732b1713e6a2e530dc4c7e919aa4d`  
		Last Modified: Wed, 05 Jun 2024 06:33:14 GMT  
		Size: 114.3 MB (114315856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46788892d21f6a27a3146a33bf193d36045bf80d7ccf46b31b7f81aa48ac2dd`  
		Last Modified: Wed, 05 Jun 2024 06:32:59 GMT  
		Size: 311.9 KB (311937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599c02e1aaa8a27726480aeda8f420f4d510c18c033236710719593a3a8683d2`  
		Last Modified: Wed, 05 Jun 2024 06:32:59 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8af64f7b4bca9f0f94faee8b3e77e6898cede65a278230955cd65948cd5998b`  
		Last Modified: Wed, 05 Jun 2024 06:33:03 GMT  
		Size: 27.7 MB (27665965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233c80f73d0c2e06cdb00c9a9bcb097849a63205c42a690e13e2e9232d81f0e1`  
		Last Modified: Wed, 05 Jun 2024 06:34:08 GMT  
		Size: 324.0 MB (324036305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8b8333dc9f646b8dcf5e6c4a81b72697cab9d98f30fd7efed33ac55f6ba74ae7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.1 MB (567076760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc5cbe0c1533dd13f1f4e6e74c0f8f83ea5601b9b648a7451f073d6592a5654`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:32:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:33:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:45:14 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Jun 2024 05:45:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:45:58 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:45:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:45:58 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:46:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:46:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:46:27 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:46:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:47:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b3822029b130a9434da04db278e695747571673f958098087aa1b0646f5e9`  
		Last Modified: Wed, 05 Jun 2024 05:55:18 GMT  
		Size: 684.9 KB (684936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b773b38eac33ca187f0b096cf08d40343b5c9d57818453f97613666eae7540`  
		Last Modified: Wed, 05 Jun 2024 05:55:16 GMT  
		Size: 4.6 MB (4612918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eed9b6478ee735e6559879b05f8a108b186e2185afbe1456b0bae55496e682`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f358deb3ce2f2d04e1ba6c224a7e7013fb4c1a6f8b1ba71583e1d609240449`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d3fc7f96a756b58b15da57d532f1288c13a4cbe173e9b8f7e894858ec6be1b`  
		Last Modified: Wed, 05 Jun 2024 05:57:21 GMT  
		Size: 117.3 MB (117266227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc15b5f12b05ed813b347aaa018910667314fe42cca600e7aceced207f800c69`  
		Last Modified: Wed, 05 Jun 2024 05:56:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4662d32b5079aa867b80b3da7b6aeff46fe9e17b6fe2259eb511f34086c06b`  
		Last Modified: Wed, 05 Jun 2024 05:57:42 GMT  
		Size: 111.2 MB (111160874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ed15ebbe5e1e631506250b6c996ae37c7ba07d31ab8d1319367c8c5e46d97a`  
		Last Modified: Wed, 05 Jun 2024 05:57:30 GMT  
		Size: 311.9 KB (311946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1ea445888bf5410c54c8096c7c8479ddbf15fcc0cf7cb3f86625b4c08264bd`  
		Last Modified: Wed, 05 Jun 2024 05:57:29 GMT  
		Size: 2.4 KB (2417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1c1854b7a8c4003cdbef2894a590e165775f3bbceaf4e101c38f11718d434e`  
		Last Modified: Wed, 05 Jun 2024 05:57:34 GMT  
		Size: 26.8 MB (26812168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90942491ec1b68370835207f8dd15452a1d2cb857546a5b4ae549cdfacfd0835`  
		Last Modified: Wed, 05 Jun 2024 05:58:31 GMT  
		Size: 277.2 MB (277178864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:a87b57ce7b0bb0fcfe5faa58c8648fc08da53b1e46f0a8ac81ddc44798d65104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:0053f85471614952280cde2359dc1c0deaab4fae8f40a99b33d0d559c0ba0cc3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.8 MB (623792612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4c4910ed4c4015b001c54618ef1a9fe9877fc030ea0b4b8116a70679318521`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 06:10:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:20:19 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Jun 2024 06:21:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:21:04 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:21:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:21:04 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 06:21:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:21:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 06:21:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 06:21:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:22:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b7b089eccbc5711efe9b5e70ebf338500c3b4261cc08c5ad96463a57a9bf1`  
		Last Modified: Wed, 05 Jun 2024 06:30:49 GMT  
		Size: 683.8 KB (683789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac994edf240e70b612dad36f314b389ed36ff1bb920412484395a0454a1d61c`  
		Last Modified: Wed, 05 Jun 2024 06:30:48 GMT  
		Size: 4.6 MB (4617771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5b36f85e72e73135bfa90830916ffb2abb10c40af616211cd07463f290a9ce`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a052403e9ecb7c5356f8463bb90b17f27010035dba5a27455ea3aa205697689f`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4875ea069f77ccb9390426ba9a3add0497f8d4eff08001ddf9c0d16a327f7514`  
		Last Modified: Wed, 05 Jun 2024 06:32:51 GMT  
		Size: 122.5 MB (122451283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a253df8ece8660676ec84b140af57ae9d1e1102d6d00de41ef255dc4be2ec92`  
		Last Modified: Wed, 05 Jun 2024 06:32:33 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2662c619c85291f1c5373990ce67dd656732b1713e6a2e530dc4c7e919aa4d`  
		Last Modified: Wed, 05 Jun 2024 06:33:14 GMT  
		Size: 114.3 MB (114315856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46788892d21f6a27a3146a33bf193d36045bf80d7ccf46b31b7f81aa48ac2dd`  
		Last Modified: Wed, 05 Jun 2024 06:32:59 GMT  
		Size: 311.9 KB (311937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599c02e1aaa8a27726480aeda8f420f4d510c18c033236710719593a3a8683d2`  
		Last Modified: Wed, 05 Jun 2024 06:32:59 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8af64f7b4bca9f0f94faee8b3e77e6898cede65a278230955cd65948cd5998b`  
		Last Modified: Wed, 05 Jun 2024 06:33:03 GMT  
		Size: 27.7 MB (27665965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233c80f73d0c2e06cdb00c9a9bcb097849a63205c42a690e13e2e9232d81f0e1`  
		Last Modified: Wed, 05 Jun 2024 06:34:08 GMT  
		Size: 324.0 MB (324036305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8b8333dc9f646b8dcf5e6c4a81b72697cab9d98f30fd7efed33ac55f6ba74ae7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.1 MB (567076760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc5cbe0c1533dd13f1f4e6e74c0f8f83ea5601b9b648a7451f073d6592a5654`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:32:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:33:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:45:14 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Jun 2024 05:45:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:45:58 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:45:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:45:58 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:46:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:46:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:46:27 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:46:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:47:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b3822029b130a9434da04db278e695747571673f958098087aa1b0646f5e9`  
		Last Modified: Wed, 05 Jun 2024 05:55:18 GMT  
		Size: 684.9 KB (684936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b773b38eac33ca187f0b096cf08d40343b5c9d57818453f97613666eae7540`  
		Last Modified: Wed, 05 Jun 2024 05:55:16 GMT  
		Size: 4.6 MB (4612918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eed9b6478ee735e6559879b05f8a108b186e2185afbe1456b0bae55496e682`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f358deb3ce2f2d04e1ba6c224a7e7013fb4c1a6f8b1ba71583e1d609240449`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d3fc7f96a756b58b15da57d532f1288c13a4cbe173e9b8f7e894858ec6be1b`  
		Last Modified: Wed, 05 Jun 2024 05:57:21 GMT  
		Size: 117.3 MB (117266227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc15b5f12b05ed813b347aaa018910667314fe42cca600e7aceced207f800c69`  
		Last Modified: Wed, 05 Jun 2024 05:56:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4662d32b5079aa867b80b3da7b6aeff46fe9e17b6fe2259eb511f34086c06b`  
		Last Modified: Wed, 05 Jun 2024 05:57:42 GMT  
		Size: 111.2 MB (111160874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ed15ebbe5e1e631506250b6c996ae37c7ba07d31ab8d1319367c8c5e46d97a`  
		Last Modified: Wed, 05 Jun 2024 05:57:30 GMT  
		Size: 311.9 KB (311946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1ea445888bf5410c54c8096c7c8479ddbf15fcc0cf7cb3f86625b4c08264bd`  
		Last Modified: Wed, 05 Jun 2024 05:57:29 GMT  
		Size: 2.4 KB (2417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1c1854b7a8c4003cdbef2894a590e165775f3bbceaf4e101c38f11718d434e`  
		Last Modified: Wed, 05 Jun 2024 05:57:34 GMT  
		Size: 26.8 MB (26812168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90942491ec1b68370835207f8dd15452a1d2cb857546a5b4ae549cdfacfd0835`  
		Last Modified: Wed, 05 Jun 2024 05:58:31 GMT  
		Size: 277.2 MB (277178864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:5f04661331f7f5b8436131e062823706575533b394b56891bd9666ca5d878c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:6c30cecf18841ec4493fc206d8c63906980801503e2a88911db49035b3a70f64
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299756307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd504a35a414a0fff6a3a3cfdb872ff6eb158c969708d6d01da21b59681c2a9e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 06:10:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:20:19 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Jun 2024 06:21:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:21:04 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:21:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:21:04 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 06:21:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:21:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 06:21:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 06:21:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b7b089eccbc5711efe9b5e70ebf338500c3b4261cc08c5ad96463a57a9bf1`  
		Last Modified: Wed, 05 Jun 2024 06:30:49 GMT  
		Size: 683.8 KB (683789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac994edf240e70b612dad36f314b389ed36ff1bb920412484395a0454a1d61c`  
		Last Modified: Wed, 05 Jun 2024 06:30:48 GMT  
		Size: 4.6 MB (4617771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5b36f85e72e73135bfa90830916ffb2abb10c40af616211cd07463f290a9ce`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a052403e9ecb7c5356f8463bb90b17f27010035dba5a27455ea3aa205697689f`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4875ea069f77ccb9390426ba9a3add0497f8d4eff08001ddf9c0d16a327f7514`  
		Last Modified: Wed, 05 Jun 2024 06:32:51 GMT  
		Size: 122.5 MB (122451283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a253df8ece8660676ec84b140af57ae9d1e1102d6d00de41ef255dc4be2ec92`  
		Last Modified: Wed, 05 Jun 2024 06:32:33 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2662c619c85291f1c5373990ce67dd656732b1713e6a2e530dc4c7e919aa4d`  
		Last Modified: Wed, 05 Jun 2024 06:33:14 GMT  
		Size: 114.3 MB (114315856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46788892d21f6a27a3146a33bf193d36045bf80d7ccf46b31b7f81aa48ac2dd`  
		Last Modified: Wed, 05 Jun 2024 06:32:59 GMT  
		Size: 311.9 KB (311937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599c02e1aaa8a27726480aeda8f420f4d510c18c033236710719593a3a8683d2`  
		Last Modified: Wed, 05 Jun 2024 06:32:59 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8af64f7b4bca9f0f94faee8b3e77e6898cede65a278230955cd65948cd5998b`  
		Last Modified: Wed, 05 Jun 2024 06:33:03 GMT  
		Size: 27.7 MB (27665965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b3629b8ac343fec82ab34bdc012524b9511e1e196b7462730fc5b004b76cca46
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289897896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1849614724cd139a7faf4d210dc57321d0d2b243b7225b34b617987364d58c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:32:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:33:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:45:14 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Jun 2024 05:45:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:45:58 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:45:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:45:58 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:46:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:46:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:46:27 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:46:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b3822029b130a9434da04db278e695747571673f958098087aa1b0646f5e9`  
		Last Modified: Wed, 05 Jun 2024 05:55:18 GMT  
		Size: 684.9 KB (684936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b773b38eac33ca187f0b096cf08d40343b5c9d57818453f97613666eae7540`  
		Last Modified: Wed, 05 Jun 2024 05:55:16 GMT  
		Size: 4.6 MB (4612918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eed9b6478ee735e6559879b05f8a108b186e2185afbe1456b0bae55496e682`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f358deb3ce2f2d04e1ba6c224a7e7013fb4c1a6f8b1ba71583e1d609240449`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d3fc7f96a756b58b15da57d532f1288c13a4cbe173e9b8f7e894858ec6be1b`  
		Last Modified: Wed, 05 Jun 2024 05:57:21 GMT  
		Size: 117.3 MB (117266227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc15b5f12b05ed813b347aaa018910667314fe42cca600e7aceced207f800c69`  
		Last Modified: Wed, 05 Jun 2024 05:56:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4662d32b5079aa867b80b3da7b6aeff46fe9e17b6fe2259eb511f34086c06b`  
		Last Modified: Wed, 05 Jun 2024 05:57:42 GMT  
		Size: 111.2 MB (111160874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ed15ebbe5e1e631506250b6c996ae37c7ba07d31ab8d1319367c8c5e46d97a`  
		Last Modified: Wed, 05 Jun 2024 05:57:30 GMT  
		Size: 311.9 KB (311946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1ea445888bf5410c54c8096c7c8479ddbf15fcc0cf7cb3f86625b4c08264bd`  
		Last Modified: Wed, 05 Jun 2024 05:57:29 GMT  
		Size: 2.4 KB (2417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1c1854b7a8c4003cdbef2894a590e165775f3bbceaf4e101c38f11718d434e`  
		Last Modified: Wed, 05 Jun 2024 05:57:34 GMT  
		Size: 26.8 MB (26812168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:5f04661331f7f5b8436131e062823706575533b394b56891bd9666ca5d878c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:6c30cecf18841ec4493fc206d8c63906980801503e2a88911db49035b3a70f64
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299756307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd504a35a414a0fff6a3a3cfdb872ff6eb158c969708d6d01da21b59681c2a9e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 06:10:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:20:19 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Jun 2024 06:21:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:21:04 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:21:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:21:04 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 06:21:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:21:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 06:21:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 06:21:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b7b089eccbc5711efe9b5e70ebf338500c3b4261cc08c5ad96463a57a9bf1`  
		Last Modified: Wed, 05 Jun 2024 06:30:49 GMT  
		Size: 683.8 KB (683789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac994edf240e70b612dad36f314b389ed36ff1bb920412484395a0454a1d61c`  
		Last Modified: Wed, 05 Jun 2024 06:30:48 GMT  
		Size: 4.6 MB (4617771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5b36f85e72e73135bfa90830916ffb2abb10c40af616211cd07463f290a9ce`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a052403e9ecb7c5356f8463bb90b17f27010035dba5a27455ea3aa205697689f`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4875ea069f77ccb9390426ba9a3add0497f8d4eff08001ddf9c0d16a327f7514`  
		Last Modified: Wed, 05 Jun 2024 06:32:51 GMT  
		Size: 122.5 MB (122451283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a253df8ece8660676ec84b140af57ae9d1e1102d6d00de41ef255dc4be2ec92`  
		Last Modified: Wed, 05 Jun 2024 06:32:33 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2662c619c85291f1c5373990ce67dd656732b1713e6a2e530dc4c7e919aa4d`  
		Last Modified: Wed, 05 Jun 2024 06:33:14 GMT  
		Size: 114.3 MB (114315856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46788892d21f6a27a3146a33bf193d36045bf80d7ccf46b31b7f81aa48ac2dd`  
		Last Modified: Wed, 05 Jun 2024 06:32:59 GMT  
		Size: 311.9 KB (311937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599c02e1aaa8a27726480aeda8f420f4d510c18c033236710719593a3a8683d2`  
		Last Modified: Wed, 05 Jun 2024 06:32:59 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8af64f7b4bca9f0f94faee8b3e77e6898cede65a278230955cd65948cd5998b`  
		Last Modified: Wed, 05 Jun 2024 06:33:03 GMT  
		Size: 27.7 MB (27665965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b3629b8ac343fec82ab34bdc012524b9511e1e196b7462730fc5b004b76cca46
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289897896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1849614724cd139a7faf4d210dc57321d0d2b243b7225b34b617987364d58c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:32:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:33:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:45:14 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Jun 2024 05:45:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:45:58 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:45:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:45:58 GMT
CMD ["bash"]
# Wed, 05 Jun 2024 05:46:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:46:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Jun 2024 05:46:27 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Jun 2024 05:46:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b3822029b130a9434da04db278e695747571673f958098087aa1b0646f5e9`  
		Last Modified: Wed, 05 Jun 2024 05:55:18 GMT  
		Size: 684.9 KB (684936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b773b38eac33ca187f0b096cf08d40343b5c9d57818453f97613666eae7540`  
		Last Modified: Wed, 05 Jun 2024 05:55:16 GMT  
		Size: 4.6 MB (4612918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eed9b6478ee735e6559879b05f8a108b186e2185afbe1456b0bae55496e682`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f358deb3ce2f2d04e1ba6c224a7e7013fb4c1a6f8b1ba71583e1d609240449`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d3fc7f96a756b58b15da57d532f1288c13a4cbe173e9b8f7e894858ec6be1b`  
		Last Modified: Wed, 05 Jun 2024 05:57:21 GMT  
		Size: 117.3 MB (117266227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc15b5f12b05ed813b347aaa018910667314fe42cca600e7aceced207f800c69`  
		Last Modified: Wed, 05 Jun 2024 05:56:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4662d32b5079aa867b80b3da7b6aeff46fe9e17b6fe2259eb511f34086c06b`  
		Last Modified: Wed, 05 Jun 2024 05:57:42 GMT  
		Size: 111.2 MB (111160874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ed15ebbe5e1e631506250b6c996ae37c7ba07d31ab8d1319367c8c5e46d97a`  
		Last Modified: Wed, 05 Jun 2024 05:57:30 GMT  
		Size: 311.9 KB (311946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1ea445888bf5410c54c8096c7c8479ddbf15fcc0cf7cb3f86625b4c08264bd`  
		Last Modified: Wed, 05 Jun 2024 05:57:29 GMT  
		Size: 2.4 KB (2417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1c1854b7a8c4003cdbef2894a590e165775f3bbceaf4e101c38f11718d434e`  
		Last Modified: Wed, 05 Jun 2024 05:57:34 GMT  
		Size: 26.8 MB (26812168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:5a625fb6e0fc52fa035bad3c7440b9343b1b16a3584e1806d598ff3be732d092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:e4955227787fd2b5f3b929bcab486d9eeb9a4d22e8efbd970d7741691ceb97ff
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157460105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53081cfdd3e9eb8edfe207684980b6a0dc468158d027969eda62a320559d8490`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 06:10:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:20:19 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Jun 2024 06:21:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:21:04 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:21:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:21:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b7b089eccbc5711efe9b5e70ebf338500c3b4261cc08c5ad96463a57a9bf1`  
		Last Modified: Wed, 05 Jun 2024 06:30:49 GMT  
		Size: 683.8 KB (683789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac994edf240e70b612dad36f314b389ed36ff1bb920412484395a0454a1d61c`  
		Last Modified: Wed, 05 Jun 2024 06:30:48 GMT  
		Size: 4.6 MB (4617771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5b36f85e72e73135bfa90830916ffb2abb10c40af616211cd07463f290a9ce`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a052403e9ecb7c5356f8463bb90b17f27010035dba5a27455ea3aa205697689f`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4875ea069f77ccb9390426ba9a3add0497f8d4eff08001ddf9c0d16a327f7514`  
		Last Modified: Wed, 05 Jun 2024 06:32:51 GMT  
		Size: 122.5 MB (122451283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a253df8ece8660676ec84b140af57ae9d1e1102d6d00de41ef255dc4be2ec92`  
		Last Modified: Wed, 05 Jun 2024 06:32:33 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:560290b12a23bee21f016f412c7d2d38e17958b21b24d4d0f24dd2886e6b11ca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151610491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2d8d0bb52bd82301c1646050a8510ff088205d61cfc118059492d325f973f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:32:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:33:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:45:14 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Jun 2024 05:45:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:45:58 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:45:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:45:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b3822029b130a9434da04db278e695747571673f958098087aa1b0646f5e9`  
		Last Modified: Wed, 05 Jun 2024 05:55:18 GMT  
		Size: 684.9 KB (684936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b773b38eac33ca187f0b096cf08d40343b5c9d57818453f97613666eae7540`  
		Last Modified: Wed, 05 Jun 2024 05:55:16 GMT  
		Size: 4.6 MB (4612918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eed9b6478ee735e6559879b05f8a108b186e2185afbe1456b0bae55496e682`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f358deb3ce2f2d04e1ba6c224a7e7013fb4c1a6f8b1ba71583e1d609240449`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d3fc7f96a756b58b15da57d532f1288c13a4cbe173e9b8f7e894858ec6be1b`  
		Last Modified: Wed, 05 Jun 2024 05:57:21 GMT  
		Size: 117.3 MB (117266227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc15b5f12b05ed813b347aaa018910667314fe42cca600e7aceced207f800c69`  
		Last Modified: Wed, 05 Jun 2024 05:56:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:5a625fb6e0fc52fa035bad3c7440b9343b1b16a3584e1806d598ff3be732d092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:e4955227787fd2b5f3b929bcab486d9eeb9a4d22e8efbd970d7741691ceb97ff
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157460105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53081cfdd3e9eb8edfe207684980b6a0dc468158d027969eda62a320559d8490`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:10:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:10:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 06:10:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 06:10:38 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 06:20:19 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Jun 2024 06:21:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:21:04 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 06:21:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 06:21:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:076fc1534bee31ee29b2f08c23f1b5d4d040c9863d04d8b7b79f0cf8dbdaeb7c`  
		Last Modified: Fri, 31 May 2024 11:14:11 GMT  
		Size: 29.7 MB (29704776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b7b089eccbc5711efe9b5e70ebf338500c3b4261cc08c5ad96463a57a9bf1`  
		Last Modified: Wed, 05 Jun 2024 06:30:49 GMT  
		Size: 683.8 KB (683789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac994edf240e70b612dad36f314b389ed36ff1bb920412484395a0454a1d61c`  
		Last Modified: Wed, 05 Jun 2024 06:30:48 GMT  
		Size: 4.6 MB (4617771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5b36f85e72e73135bfa90830916ffb2abb10c40af616211cd07463f290a9ce`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a052403e9ecb7c5356f8463bb90b17f27010035dba5a27455ea3aa205697689f`  
		Last Modified: Wed, 05 Jun 2024 06:30:47 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4875ea069f77ccb9390426ba9a3add0497f8d4eff08001ddf9c0d16a327f7514`  
		Last Modified: Wed, 05 Jun 2024 06:32:51 GMT  
		Size: 122.5 MB (122451283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a253df8ece8660676ec84b140af57ae9d1e1102d6d00de41ef255dc4be2ec92`  
		Last Modified: Wed, 05 Jun 2024 06:32:33 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:560290b12a23bee21f016f412c7d2d38e17958b21b24d4d0f24dd2886e6b11ca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151610491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2d8d0bb52bd82301c1646050a8510ff088205d61cfc118059492d325f973f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:32:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:15 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:33:16 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Wed, 05 Jun 2024 05:33:17 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 05:33:17 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Jun 2024 05:45:14 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Jun 2024 05:45:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:45:58 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Jun 2024 05:45:58 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Jun 2024 05:45:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b3822029b130a9434da04db278e695747571673f958098087aa1b0646f5e9`  
		Last Modified: Wed, 05 Jun 2024 05:55:18 GMT  
		Size: 684.9 KB (684936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b773b38eac33ca187f0b096cf08d40343b5c9d57818453f97613666eae7540`  
		Last Modified: Wed, 05 Jun 2024 05:55:16 GMT  
		Size: 4.6 MB (4612918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12eed9b6478ee735e6559879b05f8a108b186e2185afbe1456b0bae55496e682`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f358deb3ce2f2d04e1ba6c224a7e7013fb4c1a6f8b1ba71583e1d609240449`  
		Last Modified: Wed, 05 Jun 2024 05:55:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d3fc7f96a756b58b15da57d532f1288c13a4cbe173e9b8f7e894858ec6be1b`  
		Last Modified: Wed, 05 Jun 2024 05:57:21 GMT  
		Size: 117.3 MB (117266227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc15b5f12b05ed813b347aaa018910667314fe42cca600e7aceced207f800c69`  
		Last Modified: Wed, 05 Jun 2024 05:56:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
