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
-	[`ros:rolling-perception-noble`](#rosrolling-perception-noble)
-	[`ros:rolling-ros-base`](#rosrolling-ros-base)
-	[`ros:rolling-ros-base-noble`](#rosrolling-ros-base-noble)
-	[`ros:rolling-ros-core`](#rosrolling-ros-core)
-	[`ros:rolling-ros-core-noble`](#rosrolling-ros-core-noble)

## `ros:humble`

```console
$ docker pull ros@sha256:ca92c95cdf8a49f9df4954457d8c722c71f1162183019bdc598555d5ec72be69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:48f600bd2320f83d5f883b6bf556241d20f0fc61fa0e6c2dccc9596ad7fc16ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268724756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e61c24be13c923514bca2d9633d30daf5e988b20fdf513bc1ce93d246d0586`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:46:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:46:15 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV ROS_DISTRO=humble
# Thu, 25 Apr 2024 23:47:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:47:50 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:47:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:47:50 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:48:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:48:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:48:46 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 25 Apr 2024 23:49:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c55c47f6c73f60c344ac909c8ce0f12556b25eb765ed1f930fd5119119fa8`  
		Last Modified: Fri, 26 Apr 2024 00:10:13 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea1bb9a1cbe1070a649d11146b0737587115408731b3aaafc4369bf8fa8ec5`  
		Last Modified: Fri, 26 Apr 2024 00:10:12 GMT  
		Size: 3.8 MB (3829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fcfe8f75de0eb6b7aa0353aa2da1b14a8e59971d76b2aaa765db2fbcd3646d`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613a8d5a300a55d99cc495b072be31797992ae61ee123425443a8e057f213d22`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e613eafee0b5c3d693725fcd8aee80138fa0b98e7bac50db0c98a01e5d8db657`  
		Last Modified: Fri, 26 Apr 2024 00:11:20 GMT  
		Size: 111.7 MB (111670901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd4eb513578eec2e5735951fb45bb003578d15385dd1543f44cbce4337eeba1`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2566fd61ac60a9b3080af079366caf626ff1a80b331ef4d6db464b110cf1668`  
		Last Modified: Fri, 26 Apr 2024 00:11:42 GMT  
		Size: 98.1 MB (98144643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0743914e27de4c58dbb07d421fc77800a8e84159462620a31145ad84dc4d6e25`  
		Last Modified: Fri, 26 Apr 2024 00:11:29 GMT  
		Size: 318.6 KB (318577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8e0f05e85575ca00e3a6def93ae68aea67031e70c294807ba3d2296c24f3a6`  
		Last Modified: Fri, 26 Apr 2024 00:11:29 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33f8167f8092660bad0dbe0b83a8eaa60de68fc721873903c266beb36f28eb8`  
		Last Modified: Fri, 26 Apr 2024 00:11:33 GMT  
		Size: 23.1 MB (23101532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e8ba2693933a33857ef428044e4922f6cb7e5a0e4b93ac09eab65239c8ca1bdb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260252435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea97f2abef7148e115ec2fe03ebcd28e1116b42712465753d5302e845f5c58a4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:15:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:26 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:15:27 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV ROS_DISTRO=humble
# Thu, 25 Apr 2024 23:17:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:17:03 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:17:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:17:03 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:18:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:18:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:18:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 25 Apr 2024 23:18:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8742e7f1cdee93cb67c00da995274c6e0ba604195faecabb78406165bda44c8`  
		Last Modified: Thu, 25 Apr 2024 23:48:53 GMT  
		Size: 1.2 MB (1215061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb0c9474a61e99af61afdbd9b14569fd8665a46861ca9152a5ee8bce5949b92`  
		Last Modified: Thu, 25 Apr 2024 23:48:51 GMT  
		Size: 3.8 MB (3801439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22805c294de7be40a069d9239ec8d1faa88dd167cec6bc905f2563ad0924efb0`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47453fc6a62dcd9926ec5ec79224f57fee1b8c82a80e42cd77cb74f79429db13`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9041c054936e39ecd00eb1e5d8f68751ff7c88ac3305bc02f2980938a41609a8`  
		Last Modified: Thu, 25 Apr 2024 23:49:08 GMT  
		Size: 108.3 MB (108301385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfea731d72343f3e24f5cc55f8b6719d51b80736bbeb51f38e3ef6db5eb640b9`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091f9d9649c87b52ff226fc85a91b595a37923baa5399ad60a8de5b67bffb0cc`  
		Last Modified: Thu, 25 Apr 2024 23:49:28 GMT  
		Size: 95.7 MB (95689323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130fa34a155f4df6a8d3f6505f55730d3c0d63d79dfa43382ba1b779cf89e428`  
		Last Modified: Thu, 25 Apr 2024 23:49:17 GMT  
		Size: 318.6 KB (318573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c7a38f9f8bc099380ed9c7686469ca38adccc4d03281f06706e02b57a2736d`  
		Last Modified: Thu, 25 Apr 2024 23:49:17 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8075d42472813ac5f7cc2bf03f077a9dae00912f0fb50fafea6a799bf9e39df`  
		Last Modified: Thu, 25 Apr 2024 23:49:21 GMT  
		Size: 22.5 MB (22520687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception`

```console
$ docker pull ros@sha256:6cfe60b123976dd87ff58edee9f6343f2778bf4e554582db8330a2f4814e46a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:97c303c5176d8aae89f42ce811e6568fd8779c3477b33f66e46d14ec9342f72c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **960.2 MB (960241668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7595e8f5b300cc0a92650308282332262e62c664116d345e85a4644cae118765`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:46:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:46:15 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV ROS_DISTRO=humble
# Thu, 25 Apr 2024 23:47:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:47:50 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:47:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:47:50 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:48:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:48:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:48:46 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 25 Apr 2024 23:49:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:58:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c55c47f6c73f60c344ac909c8ce0f12556b25eb765ed1f930fd5119119fa8`  
		Last Modified: Fri, 26 Apr 2024 00:10:13 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea1bb9a1cbe1070a649d11146b0737587115408731b3aaafc4369bf8fa8ec5`  
		Last Modified: Fri, 26 Apr 2024 00:10:12 GMT  
		Size: 3.8 MB (3829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fcfe8f75de0eb6b7aa0353aa2da1b14a8e59971d76b2aaa765db2fbcd3646d`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613a8d5a300a55d99cc495b072be31797992ae61ee123425443a8e057f213d22`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e613eafee0b5c3d693725fcd8aee80138fa0b98e7bac50db0c98a01e5d8db657`  
		Last Modified: Fri, 26 Apr 2024 00:11:20 GMT  
		Size: 111.7 MB (111670901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd4eb513578eec2e5735951fb45bb003578d15385dd1543f44cbce4337eeba1`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2566fd61ac60a9b3080af079366caf626ff1a80b331ef4d6db464b110cf1668`  
		Last Modified: Fri, 26 Apr 2024 00:11:42 GMT  
		Size: 98.1 MB (98144643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0743914e27de4c58dbb07d421fc77800a8e84159462620a31145ad84dc4d6e25`  
		Last Modified: Fri, 26 Apr 2024 00:11:29 GMT  
		Size: 318.6 KB (318577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8e0f05e85575ca00e3a6def93ae68aea67031e70c294807ba3d2296c24f3a6`  
		Last Modified: Fri, 26 Apr 2024 00:11:29 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33f8167f8092660bad0dbe0b83a8eaa60de68fc721873903c266beb36f28eb8`  
		Last Modified: Fri, 26 Apr 2024 00:11:33 GMT  
		Size: 23.1 MB (23101532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcce2ebf2152ebefbbdd95b3844a1cc58eb99ba1e99f061e1c129941633dee5e`  
		Last Modified: Fri, 26 Apr 2024 00:13:24 GMT  
		Size: 691.5 MB (691516912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:34083b799b2b47a91ac9708de2384b9e52ac81afe0fa541f50df9ed7159c9c1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **919.7 MB (919716234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a41bf69055951b647e04ea740bf44c951466ed4041309a741ce71755e54e08`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:15:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:26 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:15:27 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV ROS_DISTRO=humble
# Thu, 25 Apr 2024 23:17:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:17:03 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:17:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:17:03 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:18:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:18:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:18:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 25 Apr 2024 23:18:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:35:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8742e7f1cdee93cb67c00da995274c6e0ba604195faecabb78406165bda44c8`  
		Last Modified: Thu, 25 Apr 2024 23:48:53 GMT  
		Size: 1.2 MB (1215061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb0c9474a61e99af61afdbd9b14569fd8665a46861ca9152a5ee8bce5949b92`  
		Last Modified: Thu, 25 Apr 2024 23:48:51 GMT  
		Size: 3.8 MB (3801439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22805c294de7be40a069d9239ec8d1faa88dd167cec6bc905f2563ad0924efb0`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47453fc6a62dcd9926ec5ec79224f57fee1b8c82a80e42cd77cb74f79429db13`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9041c054936e39ecd00eb1e5d8f68751ff7c88ac3305bc02f2980938a41609a8`  
		Last Modified: Thu, 25 Apr 2024 23:49:08 GMT  
		Size: 108.3 MB (108301385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfea731d72343f3e24f5cc55f8b6719d51b80736bbeb51f38e3ef6db5eb640b9`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091f9d9649c87b52ff226fc85a91b595a37923baa5399ad60a8de5b67bffb0cc`  
		Last Modified: Thu, 25 Apr 2024 23:49:28 GMT  
		Size: 95.7 MB (95689323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130fa34a155f4df6a8d3f6505f55730d3c0d63d79dfa43382ba1b779cf89e428`  
		Last Modified: Thu, 25 Apr 2024 23:49:17 GMT  
		Size: 318.6 KB (318573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c7a38f9f8bc099380ed9c7686469ca38adccc4d03281f06706e02b57a2736d`  
		Last Modified: Thu, 25 Apr 2024 23:49:17 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8075d42472813ac5f7cc2bf03f077a9dae00912f0fb50fafea6a799bf9e39df`  
		Last Modified: Thu, 25 Apr 2024 23:49:21 GMT  
		Size: 22.5 MB (22520687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb9e7ee2e75ad658b95297689258c7dc8156e3a49c99ea727fb41ea9fd0f0ce`  
		Last Modified: Thu, 25 Apr 2024 23:51:04 GMT  
		Size: 659.5 MB (659463799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:6cfe60b123976dd87ff58edee9f6343f2778bf4e554582db8330a2f4814e46a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:97c303c5176d8aae89f42ce811e6568fd8779c3477b33f66e46d14ec9342f72c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **960.2 MB (960241668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7595e8f5b300cc0a92650308282332262e62c664116d345e85a4644cae118765`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:46:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:46:15 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV ROS_DISTRO=humble
# Thu, 25 Apr 2024 23:47:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:47:50 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:47:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:47:50 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:48:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:48:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:48:46 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 25 Apr 2024 23:49:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:58:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c55c47f6c73f60c344ac909c8ce0f12556b25eb765ed1f930fd5119119fa8`  
		Last Modified: Fri, 26 Apr 2024 00:10:13 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea1bb9a1cbe1070a649d11146b0737587115408731b3aaafc4369bf8fa8ec5`  
		Last Modified: Fri, 26 Apr 2024 00:10:12 GMT  
		Size: 3.8 MB (3829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fcfe8f75de0eb6b7aa0353aa2da1b14a8e59971d76b2aaa765db2fbcd3646d`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613a8d5a300a55d99cc495b072be31797992ae61ee123425443a8e057f213d22`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e613eafee0b5c3d693725fcd8aee80138fa0b98e7bac50db0c98a01e5d8db657`  
		Last Modified: Fri, 26 Apr 2024 00:11:20 GMT  
		Size: 111.7 MB (111670901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd4eb513578eec2e5735951fb45bb003578d15385dd1543f44cbce4337eeba1`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2566fd61ac60a9b3080af079366caf626ff1a80b331ef4d6db464b110cf1668`  
		Last Modified: Fri, 26 Apr 2024 00:11:42 GMT  
		Size: 98.1 MB (98144643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0743914e27de4c58dbb07d421fc77800a8e84159462620a31145ad84dc4d6e25`  
		Last Modified: Fri, 26 Apr 2024 00:11:29 GMT  
		Size: 318.6 KB (318577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8e0f05e85575ca00e3a6def93ae68aea67031e70c294807ba3d2296c24f3a6`  
		Last Modified: Fri, 26 Apr 2024 00:11:29 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33f8167f8092660bad0dbe0b83a8eaa60de68fc721873903c266beb36f28eb8`  
		Last Modified: Fri, 26 Apr 2024 00:11:33 GMT  
		Size: 23.1 MB (23101532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcce2ebf2152ebefbbdd95b3844a1cc58eb99ba1e99f061e1c129941633dee5e`  
		Last Modified: Fri, 26 Apr 2024 00:13:24 GMT  
		Size: 691.5 MB (691516912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:34083b799b2b47a91ac9708de2384b9e52ac81afe0fa541f50df9ed7159c9c1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **919.7 MB (919716234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a41bf69055951b647e04ea740bf44c951466ed4041309a741ce71755e54e08`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:15:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:26 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:15:27 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV ROS_DISTRO=humble
# Thu, 25 Apr 2024 23:17:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:17:03 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:17:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:17:03 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:18:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:18:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:18:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 25 Apr 2024 23:18:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:35:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8742e7f1cdee93cb67c00da995274c6e0ba604195faecabb78406165bda44c8`  
		Last Modified: Thu, 25 Apr 2024 23:48:53 GMT  
		Size: 1.2 MB (1215061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb0c9474a61e99af61afdbd9b14569fd8665a46861ca9152a5ee8bce5949b92`  
		Last Modified: Thu, 25 Apr 2024 23:48:51 GMT  
		Size: 3.8 MB (3801439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22805c294de7be40a069d9239ec8d1faa88dd167cec6bc905f2563ad0924efb0`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47453fc6a62dcd9926ec5ec79224f57fee1b8c82a80e42cd77cb74f79429db13`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9041c054936e39ecd00eb1e5d8f68751ff7c88ac3305bc02f2980938a41609a8`  
		Last Modified: Thu, 25 Apr 2024 23:49:08 GMT  
		Size: 108.3 MB (108301385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfea731d72343f3e24f5cc55f8b6719d51b80736bbeb51f38e3ef6db5eb640b9`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091f9d9649c87b52ff226fc85a91b595a37923baa5399ad60a8de5b67bffb0cc`  
		Last Modified: Thu, 25 Apr 2024 23:49:28 GMT  
		Size: 95.7 MB (95689323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130fa34a155f4df6a8d3f6505f55730d3c0d63d79dfa43382ba1b779cf89e428`  
		Last Modified: Thu, 25 Apr 2024 23:49:17 GMT  
		Size: 318.6 KB (318573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c7a38f9f8bc099380ed9c7686469ca38adccc4d03281f06706e02b57a2736d`  
		Last Modified: Thu, 25 Apr 2024 23:49:17 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8075d42472813ac5f7cc2bf03f077a9dae00912f0fb50fafea6a799bf9e39df`  
		Last Modified: Thu, 25 Apr 2024 23:49:21 GMT  
		Size: 22.5 MB (22520687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb9e7ee2e75ad658b95297689258c7dc8156e3a49c99ea727fb41ea9fd0f0ce`  
		Last Modified: Thu, 25 Apr 2024 23:51:04 GMT  
		Size: 659.5 MB (659463799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:ca92c95cdf8a49f9df4954457d8c722c71f1162183019bdc598555d5ec72be69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:48f600bd2320f83d5f883b6bf556241d20f0fc61fa0e6c2dccc9596ad7fc16ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268724756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e61c24be13c923514bca2d9633d30daf5e988b20fdf513bc1ce93d246d0586`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:46:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:46:15 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV ROS_DISTRO=humble
# Thu, 25 Apr 2024 23:47:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:47:50 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:47:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:47:50 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:48:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:48:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:48:46 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 25 Apr 2024 23:49:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c55c47f6c73f60c344ac909c8ce0f12556b25eb765ed1f930fd5119119fa8`  
		Last Modified: Fri, 26 Apr 2024 00:10:13 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea1bb9a1cbe1070a649d11146b0737587115408731b3aaafc4369bf8fa8ec5`  
		Last Modified: Fri, 26 Apr 2024 00:10:12 GMT  
		Size: 3.8 MB (3829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fcfe8f75de0eb6b7aa0353aa2da1b14a8e59971d76b2aaa765db2fbcd3646d`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613a8d5a300a55d99cc495b072be31797992ae61ee123425443a8e057f213d22`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e613eafee0b5c3d693725fcd8aee80138fa0b98e7bac50db0c98a01e5d8db657`  
		Last Modified: Fri, 26 Apr 2024 00:11:20 GMT  
		Size: 111.7 MB (111670901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd4eb513578eec2e5735951fb45bb003578d15385dd1543f44cbce4337eeba1`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2566fd61ac60a9b3080af079366caf626ff1a80b331ef4d6db464b110cf1668`  
		Last Modified: Fri, 26 Apr 2024 00:11:42 GMT  
		Size: 98.1 MB (98144643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0743914e27de4c58dbb07d421fc77800a8e84159462620a31145ad84dc4d6e25`  
		Last Modified: Fri, 26 Apr 2024 00:11:29 GMT  
		Size: 318.6 KB (318577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8e0f05e85575ca00e3a6def93ae68aea67031e70c294807ba3d2296c24f3a6`  
		Last Modified: Fri, 26 Apr 2024 00:11:29 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33f8167f8092660bad0dbe0b83a8eaa60de68fc721873903c266beb36f28eb8`  
		Last Modified: Fri, 26 Apr 2024 00:11:33 GMT  
		Size: 23.1 MB (23101532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e8ba2693933a33857ef428044e4922f6cb7e5a0e4b93ac09eab65239c8ca1bdb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260252435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea97f2abef7148e115ec2fe03ebcd28e1116b42712465753d5302e845f5c58a4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:15:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:26 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:15:27 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV ROS_DISTRO=humble
# Thu, 25 Apr 2024 23:17:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:17:03 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:17:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:17:03 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:18:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:18:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:18:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 25 Apr 2024 23:18:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8742e7f1cdee93cb67c00da995274c6e0ba604195faecabb78406165bda44c8`  
		Last Modified: Thu, 25 Apr 2024 23:48:53 GMT  
		Size: 1.2 MB (1215061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb0c9474a61e99af61afdbd9b14569fd8665a46861ca9152a5ee8bce5949b92`  
		Last Modified: Thu, 25 Apr 2024 23:48:51 GMT  
		Size: 3.8 MB (3801439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22805c294de7be40a069d9239ec8d1faa88dd167cec6bc905f2563ad0924efb0`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47453fc6a62dcd9926ec5ec79224f57fee1b8c82a80e42cd77cb74f79429db13`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9041c054936e39ecd00eb1e5d8f68751ff7c88ac3305bc02f2980938a41609a8`  
		Last Modified: Thu, 25 Apr 2024 23:49:08 GMT  
		Size: 108.3 MB (108301385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfea731d72343f3e24f5cc55f8b6719d51b80736bbeb51f38e3ef6db5eb640b9`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091f9d9649c87b52ff226fc85a91b595a37923baa5399ad60a8de5b67bffb0cc`  
		Last Modified: Thu, 25 Apr 2024 23:49:28 GMT  
		Size: 95.7 MB (95689323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130fa34a155f4df6a8d3f6505f55730d3c0d63d79dfa43382ba1b779cf89e428`  
		Last Modified: Thu, 25 Apr 2024 23:49:17 GMT  
		Size: 318.6 KB (318573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c7a38f9f8bc099380ed9c7686469ca38adccc4d03281f06706e02b57a2736d`  
		Last Modified: Thu, 25 Apr 2024 23:49:17 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8075d42472813ac5f7cc2bf03f077a9dae00912f0fb50fafea6a799bf9e39df`  
		Last Modified: Thu, 25 Apr 2024 23:49:21 GMT  
		Size: 22.5 MB (22520687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:ca92c95cdf8a49f9df4954457d8c722c71f1162183019bdc598555d5ec72be69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:48f600bd2320f83d5f883b6bf556241d20f0fc61fa0e6c2dccc9596ad7fc16ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268724756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e61c24be13c923514bca2d9633d30daf5e988b20fdf513bc1ce93d246d0586`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:46:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:46:15 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV ROS_DISTRO=humble
# Thu, 25 Apr 2024 23:47:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:47:50 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:47:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:47:50 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:48:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:48:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:48:46 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 25 Apr 2024 23:49:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c55c47f6c73f60c344ac909c8ce0f12556b25eb765ed1f930fd5119119fa8`  
		Last Modified: Fri, 26 Apr 2024 00:10:13 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea1bb9a1cbe1070a649d11146b0737587115408731b3aaafc4369bf8fa8ec5`  
		Last Modified: Fri, 26 Apr 2024 00:10:12 GMT  
		Size: 3.8 MB (3829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fcfe8f75de0eb6b7aa0353aa2da1b14a8e59971d76b2aaa765db2fbcd3646d`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613a8d5a300a55d99cc495b072be31797992ae61ee123425443a8e057f213d22`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e613eafee0b5c3d693725fcd8aee80138fa0b98e7bac50db0c98a01e5d8db657`  
		Last Modified: Fri, 26 Apr 2024 00:11:20 GMT  
		Size: 111.7 MB (111670901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd4eb513578eec2e5735951fb45bb003578d15385dd1543f44cbce4337eeba1`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2566fd61ac60a9b3080af079366caf626ff1a80b331ef4d6db464b110cf1668`  
		Last Modified: Fri, 26 Apr 2024 00:11:42 GMT  
		Size: 98.1 MB (98144643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0743914e27de4c58dbb07d421fc77800a8e84159462620a31145ad84dc4d6e25`  
		Last Modified: Fri, 26 Apr 2024 00:11:29 GMT  
		Size: 318.6 KB (318577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8e0f05e85575ca00e3a6def93ae68aea67031e70c294807ba3d2296c24f3a6`  
		Last Modified: Fri, 26 Apr 2024 00:11:29 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33f8167f8092660bad0dbe0b83a8eaa60de68fc721873903c266beb36f28eb8`  
		Last Modified: Fri, 26 Apr 2024 00:11:33 GMT  
		Size: 23.1 MB (23101532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e8ba2693933a33857ef428044e4922f6cb7e5a0e4b93ac09eab65239c8ca1bdb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260252435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea97f2abef7148e115ec2fe03ebcd28e1116b42712465753d5302e845f5c58a4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:15:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:26 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:15:27 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV ROS_DISTRO=humble
# Thu, 25 Apr 2024 23:17:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:17:03 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:17:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:17:03 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:18:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:18:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:18:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 25 Apr 2024 23:18:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8742e7f1cdee93cb67c00da995274c6e0ba604195faecabb78406165bda44c8`  
		Last Modified: Thu, 25 Apr 2024 23:48:53 GMT  
		Size: 1.2 MB (1215061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb0c9474a61e99af61afdbd9b14569fd8665a46861ca9152a5ee8bce5949b92`  
		Last Modified: Thu, 25 Apr 2024 23:48:51 GMT  
		Size: 3.8 MB (3801439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22805c294de7be40a069d9239ec8d1faa88dd167cec6bc905f2563ad0924efb0`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47453fc6a62dcd9926ec5ec79224f57fee1b8c82a80e42cd77cb74f79429db13`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9041c054936e39ecd00eb1e5d8f68751ff7c88ac3305bc02f2980938a41609a8`  
		Last Modified: Thu, 25 Apr 2024 23:49:08 GMT  
		Size: 108.3 MB (108301385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfea731d72343f3e24f5cc55f8b6719d51b80736bbeb51f38e3ef6db5eb640b9`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091f9d9649c87b52ff226fc85a91b595a37923baa5399ad60a8de5b67bffb0cc`  
		Last Modified: Thu, 25 Apr 2024 23:49:28 GMT  
		Size: 95.7 MB (95689323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130fa34a155f4df6a8d3f6505f55730d3c0d63d79dfa43382ba1b779cf89e428`  
		Last Modified: Thu, 25 Apr 2024 23:49:17 GMT  
		Size: 318.6 KB (318573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c7a38f9f8bc099380ed9c7686469ca38adccc4d03281f06706e02b57a2736d`  
		Last Modified: Thu, 25 Apr 2024 23:49:17 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8075d42472813ac5f7cc2bf03f077a9dae00912f0fb50fafea6a799bf9e39df`  
		Last Modified: Thu, 25 Apr 2024 23:49:21 GMT  
		Size: 22.5 MB (22520687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:5e1f1789c2d963246cb93020672ae57dbfc3a3dbaac57f1319d8cd4b1de59bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:2dbb0a1f7d21ce9b7235242cf7fc85d1bd7e598b293f5bba856523981144a8ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147157534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c8118ed8bd24ca40db916cc29649031004c8a1c63e4ee70dc712023733cd6c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:46:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:46:15 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV ROS_DISTRO=humble
# Thu, 25 Apr 2024 23:47:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:47:50 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:47:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:47:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c55c47f6c73f60c344ac909c8ce0f12556b25eb765ed1f930fd5119119fa8`  
		Last Modified: Fri, 26 Apr 2024 00:10:13 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea1bb9a1cbe1070a649d11146b0737587115408731b3aaafc4369bf8fa8ec5`  
		Last Modified: Fri, 26 Apr 2024 00:10:12 GMT  
		Size: 3.8 MB (3829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fcfe8f75de0eb6b7aa0353aa2da1b14a8e59971d76b2aaa765db2fbcd3646d`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613a8d5a300a55d99cc495b072be31797992ae61ee123425443a8e057f213d22`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e613eafee0b5c3d693725fcd8aee80138fa0b98e7bac50db0c98a01e5d8db657`  
		Last Modified: Fri, 26 Apr 2024 00:11:20 GMT  
		Size: 111.7 MB (111670901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd4eb513578eec2e5735951fb45bb003578d15385dd1543f44cbce4337eeba1`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eddc3c5f7180b6bf9ab2128cf3231c74367a99f019f8e8b42e09941e79b56cbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141721375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70735918669b34ff60aa8774f233b61761fc3ab444ee21fdc83e61b84be2fee6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:15:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:26 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:15:27 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV ROS_DISTRO=humble
# Thu, 25 Apr 2024 23:17:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:17:03 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:17:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:17:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8742e7f1cdee93cb67c00da995274c6e0ba604195faecabb78406165bda44c8`  
		Last Modified: Thu, 25 Apr 2024 23:48:53 GMT  
		Size: 1.2 MB (1215061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb0c9474a61e99af61afdbd9b14569fd8665a46861ca9152a5ee8bce5949b92`  
		Last Modified: Thu, 25 Apr 2024 23:48:51 GMT  
		Size: 3.8 MB (3801439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22805c294de7be40a069d9239ec8d1faa88dd167cec6bc905f2563ad0924efb0`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47453fc6a62dcd9926ec5ec79224f57fee1b8c82a80e42cd77cb74f79429db13`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9041c054936e39ecd00eb1e5d8f68751ff7c88ac3305bc02f2980938a41609a8`  
		Last Modified: Thu, 25 Apr 2024 23:49:08 GMT  
		Size: 108.3 MB (108301385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfea731d72343f3e24f5cc55f8b6719d51b80736bbeb51f38e3ef6db5eb640b9`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:5e1f1789c2d963246cb93020672ae57dbfc3a3dbaac57f1319d8cd4b1de59bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:2dbb0a1f7d21ce9b7235242cf7fc85d1bd7e598b293f5bba856523981144a8ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147157534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c8118ed8bd24ca40db916cc29649031004c8a1c63e4ee70dc712023733cd6c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:46:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:46:15 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV ROS_DISTRO=humble
# Thu, 25 Apr 2024 23:47:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:47:50 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:47:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:47:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c55c47f6c73f60c344ac909c8ce0f12556b25eb765ed1f930fd5119119fa8`  
		Last Modified: Fri, 26 Apr 2024 00:10:13 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea1bb9a1cbe1070a649d11146b0737587115408731b3aaafc4369bf8fa8ec5`  
		Last Modified: Fri, 26 Apr 2024 00:10:12 GMT  
		Size: 3.8 MB (3829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fcfe8f75de0eb6b7aa0353aa2da1b14a8e59971d76b2aaa765db2fbcd3646d`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613a8d5a300a55d99cc495b072be31797992ae61ee123425443a8e057f213d22`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e613eafee0b5c3d693725fcd8aee80138fa0b98e7bac50db0c98a01e5d8db657`  
		Last Modified: Fri, 26 Apr 2024 00:11:20 GMT  
		Size: 111.7 MB (111670901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd4eb513578eec2e5735951fb45bb003578d15385dd1543f44cbce4337eeba1`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eddc3c5f7180b6bf9ab2128cf3231c74367a99f019f8e8b42e09941e79b56cbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141721375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70735918669b34ff60aa8774f233b61761fc3ab444ee21fdc83e61b84be2fee6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:15:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:26 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:15:27 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV ROS_DISTRO=humble
# Thu, 25 Apr 2024 23:17:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:17:03 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:17:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:17:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8742e7f1cdee93cb67c00da995274c6e0ba604195faecabb78406165bda44c8`  
		Last Modified: Thu, 25 Apr 2024 23:48:53 GMT  
		Size: 1.2 MB (1215061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb0c9474a61e99af61afdbd9b14569fd8665a46861ca9152a5ee8bce5949b92`  
		Last Modified: Thu, 25 Apr 2024 23:48:51 GMT  
		Size: 3.8 MB (3801439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22805c294de7be40a069d9239ec8d1faa88dd167cec6bc905f2563ad0924efb0`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47453fc6a62dcd9926ec5ec79224f57fee1b8c82a80e42cd77cb74f79429db13`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9041c054936e39ecd00eb1e5d8f68751ff7c88ac3305bc02f2980938a41609a8`  
		Last Modified: Thu, 25 Apr 2024 23:49:08 GMT  
		Size: 108.3 MB (108301385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfea731d72343f3e24f5cc55f8b6719d51b80736bbeb51f38e3ef6db5eb640b9`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron`

```console
$ docker pull ros@sha256:793761f4b910a035da9873fd3b962024f8b429c4ae1f20e46864e5eaf409dd58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron` - linux; amd64

```console
$ docker pull ros@sha256:a573f950575377c4263e57957c6d6dcc02a1d2071d604d0ebcb23355ac9b273b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274138940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55aaef701db462fed2147281c3ab669d7a2d1cba703b326934ea30fcae6df9fb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:46:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:46:15 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:58:29 GMT
ENV ROS_DISTRO=iron
# Thu, 25 Apr 2024 23:59:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:59:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:59:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:59:19 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:59:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:59:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:59:52 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 26 Apr 2024 00:00:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c55c47f6c73f60c344ac909c8ce0f12556b25eb765ed1f930fd5119119fa8`  
		Last Modified: Fri, 26 Apr 2024 00:10:13 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea1bb9a1cbe1070a649d11146b0737587115408731b3aaafc4369bf8fa8ec5`  
		Last Modified: Fri, 26 Apr 2024 00:10:12 GMT  
		Size: 3.8 MB (3829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fcfe8f75de0eb6b7aa0353aa2da1b14a8e59971d76b2aaa765db2fbcd3646d`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613a8d5a300a55d99cc495b072be31797992ae61ee123425443a8e057f213d22`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09746b27f422485d8473855067a57c2a5b382bd7af77d2e57bb03135fe53726a`  
		Last Modified: Fri, 26 Apr 2024 00:13:54 GMT  
		Size: 129.4 MB (129439340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b0dd01d830d6f7a02dcff390bd7e6dca8c567f47dde423deb2d8d9cc213b27`  
		Last Modified: Fri, 26 Apr 2024 00:13:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c788bbf8906d323dabf78fd02984454611c7f0813ee03ad13ada9a7e7d7a3df`  
		Last Modified: Fri, 26 Apr 2024 00:14:13 GMT  
		Size: 85.2 MB (85172231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb115de4a4f2dc14fc51329a24630087a98d316d3e34534d3fdcdfca83612c2`  
		Last Modified: Fri, 26 Apr 2024 00:14:03 GMT  
		Size: 304.0 KB (303969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02b4458aff6bfe760b18d725f3435ff9d4921931e29c56a4fbf863a2574495c`  
		Last Modified: Fri, 26 Apr 2024 00:14:03 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fc2f00f0169936bfde19063cdd5b052261b4ccb752cf391cf4e5e0aacbd756`  
		Last Modified: Fri, 26 Apr 2024 00:14:07 GMT  
		Size: 23.7 MB (23734288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bcccef72adf805fec11a65c7ace7cf4055750edd226286b126a43bd908b458c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265514511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd4684ba7c242f227d61d054c0eacf3b617c7430d6eaad6a1e61ad346c1cff6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:15:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:26 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:15:27 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:35:50 GMT
ENV ROS_DISTRO=iron
# Thu, 25 Apr 2024 23:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:36:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:36:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:36:51 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:37:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:37:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:37:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 25 Apr 2024 23:37:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8742e7f1cdee93cb67c00da995274c6e0ba604195faecabb78406165bda44c8`  
		Last Modified: Thu, 25 Apr 2024 23:48:53 GMT  
		Size: 1.2 MB (1215061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb0c9474a61e99af61afdbd9b14569fd8665a46861ca9152a5ee8bce5949b92`  
		Last Modified: Thu, 25 Apr 2024 23:48:51 GMT  
		Size: 3.8 MB (3801439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22805c294de7be40a069d9239ec8d1faa88dd167cec6bc905f2563ad0924efb0`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47453fc6a62dcd9926ec5ec79224f57fee1b8c82a80e42cd77cb74f79429db13`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba50c5e8c063dd02d5262b7ac93a158b4818e0636449c9aeec4f35b4f358c40`  
		Last Modified: Thu, 25 Apr 2024 23:51:32 GMT  
		Size: 125.8 MB (125818097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7519a5ce24ec95ec84e069ac80bf61aa9eff8e1d536ff3ac2b1344cc081cfaeb`  
		Last Modified: Thu, 25 Apr 2024 23:51:13 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c444202310a3b295657f00e13d43fb34e0e1b7e5a4fcc3c5f00a6bf1c58dc02b`  
		Last Modified: Thu, 25 Apr 2024 23:51:49 GMT  
		Size: 82.8 MB (82848125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c1d250e67d2a6b488b18a2854e800a47b2fc648e6c1c90120e344b0d728e4f`  
		Last Modified: Thu, 25 Apr 2024 23:51:41 GMT  
		Size: 304.0 KB (303966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d54974e2af3e22412efba3d867427f335016c5fec75318bfd2c3350c059ba81`  
		Last Modified: Thu, 25 Apr 2024 23:51:40 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fdd964bb98502b1d29d5fba037733eccaac0ac56a70526e08f4568cee71d52`  
		Last Modified: Thu, 25 Apr 2024 23:51:44 GMT  
		Size: 23.1 MB (23121829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-perception`

```console
$ docker pull ros@sha256:aaa475bd27f8becd9d1a951133a3164c1a01c1e332b2e5105869db4a04f517c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception` - linux; amd64

```console
$ docker pull ros@sha256:de02ff945d3f2b4db5f5d54135acde26508a706b9ee0c42bec3698551e055879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **966.3 MB (966322722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e750ce4df840d87ba41230398c45c5ceac4cc40a9cbbbe4289f04ae7187c5347`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:46:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:46:15 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:58:29 GMT
ENV ROS_DISTRO=iron
# Thu, 25 Apr 2024 23:59:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:59:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:59:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:59:19 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:59:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:59:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:59:52 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 26 Apr 2024 00:00:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 00:01:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c55c47f6c73f60c344ac909c8ce0f12556b25eb765ed1f930fd5119119fa8`  
		Last Modified: Fri, 26 Apr 2024 00:10:13 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea1bb9a1cbe1070a649d11146b0737587115408731b3aaafc4369bf8fa8ec5`  
		Last Modified: Fri, 26 Apr 2024 00:10:12 GMT  
		Size: 3.8 MB (3829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fcfe8f75de0eb6b7aa0353aa2da1b14a8e59971d76b2aaa765db2fbcd3646d`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613a8d5a300a55d99cc495b072be31797992ae61ee123425443a8e057f213d22`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09746b27f422485d8473855067a57c2a5b382bd7af77d2e57bb03135fe53726a`  
		Last Modified: Fri, 26 Apr 2024 00:13:54 GMT  
		Size: 129.4 MB (129439340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b0dd01d830d6f7a02dcff390bd7e6dca8c567f47dde423deb2d8d9cc213b27`  
		Last Modified: Fri, 26 Apr 2024 00:13:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c788bbf8906d323dabf78fd02984454611c7f0813ee03ad13ada9a7e7d7a3df`  
		Last Modified: Fri, 26 Apr 2024 00:14:13 GMT  
		Size: 85.2 MB (85172231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb115de4a4f2dc14fc51329a24630087a98d316d3e34534d3fdcdfca83612c2`  
		Last Modified: Fri, 26 Apr 2024 00:14:03 GMT  
		Size: 304.0 KB (303969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02b4458aff6bfe760b18d725f3435ff9d4921931e29c56a4fbf863a2574495c`  
		Last Modified: Fri, 26 Apr 2024 00:14:03 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fc2f00f0169936bfde19063cdd5b052261b4ccb752cf391cf4e5e0aacbd756`  
		Last Modified: Fri, 26 Apr 2024 00:14:07 GMT  
		Size: 23.7 MB (23734288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34d769359b16a2f33d4653d5e347275386689b248c7bcb333be46e61784259c`  
		Last Modified: Fri, 26 Apr 2024 00:15:54 GMT  
		Size: 692.2 MB (692183782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5e19b81bc2e84c3435f4bfde199633f765f151ea2234e30ad1a040b472f59fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **925.6 MB (925604355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f1b8dd17144535b1c5f0e61d8051ea6a7ce8dc1f51ff1e019ddbe77d07d65b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:15:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:26 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:15:27 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:35:50 GMT
ENV ROS_DISTRO=iron
# Thu, 25 Apr 2024 23:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:36:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:36:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:36:51 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:37:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:37:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:37:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 25 Apr 2024 23:37:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:39:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8742e7f1cdee93cb67c00da995274c6e0ba604195faecabb78406165bda44c8`  
		Last Modified: Thu, 25 Apr 2024 23:48:53 GMT  
		Size: 1.2 MB (1215061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb0c9474a61e99af61afdbd9b14569fd8665a46861ca9152a5ee8bce5949b92`  
		Last Modified: Thu, 25 Apr 2024 23:48:51 GMT  
		Size: 3.8 MB (3801439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22805c294de7be40a069d9239ec8d1faa88dd167cec6bc905f2563ad0924efb0`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47453fc6a62dcd9926ec5ec79224f57fee1b8c82a80e42cd77cb74f79429db13`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba50c5e8c063dd02d5262b7ac93a158b4818e0636449c9aeec4f35b4f358c40`  
		Last Modified: Thu, 25 Apr 2024 23:51:32 GMT  
		Size: 125.8 MB (125818097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7519a5ce24ec95ec84e069ac80bf61aa9eff8e1d536ff3ac2b1344cc081cfaeb`  
		Last Modified: Thu, 25 Apr 2024 23:51:13 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c444202310a3b295657f00e13d43fb34e0e1b7e5a4fcc3c5f00a6bf1c58dc02b`  
		Last Modified: Thu, 25 Apr 2024 23:51:49 GMT  
		Size: 82.8 MB (82848125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c1d250e67d2a6b488b18a2854e800a47b2fc648e6c1c90120e344b0d728e4f`  
		Last Modified: Thu, 25 Apr 2024 23:51:41 GMT  
		Size: 304.0 KB (303966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d54974e2af3e22412efba3d867427f335016c5fec75318bfd2c3350c059ba81`  
		Last Modified: Thu, 25 Apr 2024 23:51:40 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fdd964bb98502b1d29d5fba037733eccaac0ac56a70526e08f4568cee71d52`  
		Last Modified: Thu, 25 Apr 2024 23:51:44 GMT  
		Size: 23.1 MB (23121829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8c8f7b80d3d8d15be275e89ee85469f66662427031114ab3b0978f19368f44`  
		Last Modified: Thu, 25 Apr 2024 23:53:15 GMT  
		Size: 660.1 MB (660089844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:aaa475bd27f8becd9d1a951133a3164c1a01c1e332b2e5105869db4a04f517c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:de02ff945d3f2b4db5f5d54135acde26508a706b9ee0c42bec3698551e055879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **966.3 MB (966322722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e750ce4df840d87ba41230398c45c5ceac4cc40a9cbbbe4289f04ae7187c5347`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:46:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:46:15 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:58:29 GMT
ENV ROS_DISTRO=iron
# Thu, 25 Apr 2024 23:59:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:59:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:59:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:59:19 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:59:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:59:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:59:52 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 26 Apr 2024 00:00:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 00:01:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c55c47f6c73f60c344ac909c8ce0f12556b25eb765ed1f930fd5119119fa8`  
		Last Modified: Fri, 26 Apr 2024 00:10:13 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea1bb9a1cbe1070a649d11146b0737587115408731b3aaafc4369bf8fa8ec5`  
		Last Modified: Fri, 26 Apr 2024 00:10:12 GMT  
		Size: 3.8 MB (3829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fcfe8f75de0eb6b7aa0353aa2da1b14a8e59971d76b2aaa765db2fbcd3646d`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613a8d5a300a55d99cc495b072be31797992ae61ee123425443a8e057f213d22`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09746b27f422485d8473855067a57c2a5b382bd7af77d2e57bb03135fe53726a`  
		Last Modified: Fri, 26 Apr 2024 00:13:54 GMT  
		Size: 129.4 MB (129439340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b0dd01d830d6f7a02dcff390bd7e6dca8c567f47dde423deb2d8d9cc213b27`  
		Last Modified: Fri, 26 Apr 2024 00:13:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c788bbf8906d323dabf78fd02984454611c7f0813ee03ad13ada9a7e7d7a3df`  
		Last Modified: Fri, 26 Apr 2024 00:14:13 GMT  
		Size: 85.2 MB (85172231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb115de4a4f2dc14fc51329a24630087a98d316d3e34534d3fdcdfca83612c2`  
		Last Modified: Fri, 26 Apr 2024 00:14:03 GMT  
		Size: 304.0 KB (303969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02b4458aff6bfe760b18d725f3435ff9d4921931e29c56a4fbf863a2574495c`  
		Last Modified: Fri, 26 Apr 2024 00:14:03 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fc2f00f0169936bfde19063cdd5b052261b4ccb752cf391cf4e5e0aacbd756`  
		Last Modified: Fri, 26 Apr 2024 00:14:07 GMT  
		Size: 23.7 MB (23734288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34d769359b16a2f33d4653d5e347275386689b248c7bcb333be46e61784259c`  
		Last Modified: Fri, 26 Apr 2024 00:15:54 GMT  
		Size: 692.2 MB (692183782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5e19b81bc2e84c3435f4bfde199633f765f151ea2234e30ad1a040b472f59fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **925.6 MB (925604355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f1b8dd17144535b1c5f0e61d8051ea6a7ce8dc1f51ff1e019ddbe77d07d65b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:15:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:26 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:15:27 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:35:50 GMT
ENV ROS_DISTRO=iron
# Thu, 25 Apr 2024 23:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:36:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:36:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:36:51 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:37:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:37:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:37:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 25 Apr 2024 23:37:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:39:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8742e7f1cdee93cb67c00da995274c6e0ba604195faecabb78406165bda44c8`  
		Last Modified: Thu, 25 Apr 2024 23:48:53 GMT  
		Size: 1.2 MB (1215061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb0c9474a61e99af61afdbd9b14569fd8665a46861ca9152a5ee8bce5949b92`  
		Last Modified: Thu, 25 Apr 2024 23:48:51 GMT  
		Size: 3.8 MB (3801439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22805c294de7be40a069d9239ec8d1faa88dd167cec6bc905f2563ad0924efb0`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47453fc6a62dcd9926ec5ec79224f57fee1b8c82a80e42cd77cb74f79429db13`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba50c5e8c063dd02d5262b7ac93a158b4818e0636449c9aeec4f35b4f358c40`  
		Last Modified: Thu, 25 Apr 2024 23:51:32 GMT  
		Size: 125.8 MB (125818097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7519a5ce24ec95ec84e069ac80bf61aa9eff8e1d536ff3ac2b1344cc081cfaeb`  
		Last Modified: Thu, 25 Apr 2024 23:51:13 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c444202310a3b295657f00e13d43fb34e0e1b7e5a4fcc3c5f00a6bf1c58dc02b`  
		Last Modified: Thu, 25 Apr 2024 23:51:49 GMT  
		Size: 82.8 MB (82848125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c1d250e67d2a6b488b18a2854e800a47b2fc648e6c1c90120e344b0d728e4f`  
		Last Modified: Thu, 25 Apr 2024 23:51:41 GMT  
		Size: 304.0 KB (303966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d54974e2af3e22412efba3d867427f335016c5fec75318bfd2c3350c059ba81`  
		Last Modified: Thu, 25 Apr 2024 23:51:40 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fdd964bb98502b1d29d5fba037733eccaac0ac56a70526e08f4568cee71d52`  
		Last Modified: Thu, 25 Apr 2024 23:51:44 GMT  
		Size: 23.1 MB (23121829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8c8f7b80d3d8d15be275e89ee85469f66662427031114ab3b0978f19368f44`  
		Last Modified: Thu, 25 Apr 2024 23:53:15 GMT  
		Size: 660.1 MB (660089844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-base`

```console
$ docker pull ros@sha256:793761f4b910a035da9873fd3b962024f8b429c4ae1f20e46864e5eaf409dd58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:a573f950575377c4263e57957c6d6dcc02a1d2071d604d0ebcb23355ac9b273b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274138940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55aaef701db462fed2147281c3ab669d7a2d1cba703b326934ea30fcae6df9fb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:46:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:46:15 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:58:29 GMT
ENV ROS_DISTRO=iron
# Thu, 25 Apr 2024 23:59:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:59:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:59:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:59:19 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:59:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:59:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:59:52 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 26 Apr 2024 00:00:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c55c47f6c73f60c344ac909c8ce0f12556b25eb765ed1f930fd5119119fa8`  
		Last Modified: Fri, 26 Apr 2024 00:10:13 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea1bb9a1cbe1070a649d11146b0737587115408731b3aaafc4369bf8fa8ec5`  
		Last Modified: Fri, 26 Apr 2024 00:10:12 GMT  
		Size: 3.8 MB (3829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fcfe8f75de0eb6b7aa0353aa2da1b14a8e59971d76b2aaa765db2fbcd3646d`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613a8d5a300a55d99cc495b072be31797992ae61ee123425443a8e057f213d22`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09746b27f422485d8473855067a57c2a5b382bd7af77d2e57bb03135fe53726a`  
		Last Modified: Fri, 26 Apr 2024 00:13:54 GMT  
		Size: 129.4 MB (129439340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b0dd01d830d6f7a02dcff390bd7e6dca8c567f47dde423deb2d8d9cc213b27`  
		Last Modified: Fri, 26 Apr 2024 00:13:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c788bbf8906d323dabf78fd02984454611c7f0813ee03ad13ada9a7e7d7a3df`  
		Last Modified: Fri, 26 Apr 2024 00:14:13 GMT  
		Size: 85.2 MB (85172231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb115de4a4f2dc14fc51329a24630087a98d316d3e34534d3fdcdfca83612c2`  
		Last Modified: Fri, 26 Apr 2024 00:14:03 GMT  
		Size: 304.0 KB (303969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02b4458aff6bfe760b18d725f3435ff9d4921931e29c56a4fbf863a2574495c`  
		Last Modified: Fri, 26 Apr 2024 00:14:03 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fc2f00f0169936bfde19063cdd5b052261b4ccb752cf391cf4e5e0aacbd756`  
		Last Modified: Fri, 26 Apr 2024 00:14:07 GMT  
		Size: 23.7 MB (23734288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bcccef72adf805fec11a65c7ace7cf4055750edd226286b126a43bd908b458c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265514511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd4684ba7c242f227d61d054c0eacf3b617c7430d6eaad6a1e61ad346c1cff6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:15:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:26 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:15:27 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:35:50 GMT
ENV ROS_DISTRO=iron
# Thu, 25 Apr 2024 23:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:36:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:36:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:36:51 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:37:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:37:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:37:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 25 Apr 2024 23:37:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8742e7f1cdee93cb67c00da995274c6e0ba604195faecabb78406165bda44c8`  
		Last Modified: Thu, 25 Apr 2024 23:48:53 GMT  
		Size: 1.2 MB (1215061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb0c9474a61e99af61afdbd9b14569fd8665a46861ca9152a5ee8bce5949b92`  
		Last Modified: Thu, 25 Apr 2024 23:48:51 GMT  
		Size: 3.8 MB (3801439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22805c294de7be40a069d9239ec8d1faa88dd167cec6bc905f2563ad0924efb0`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47453fc6a62dcd9926ec5ec79224f57fee1b8c82a80e42cd77cb74f79429db13`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba50c5e8c063dd02d5262b7ac93a158b4818e0636449c9aeec4f35b4f358c40`  
		Last Modified: Thu, 25 Apr 2024 23:51:32 GMT  
		Size: 125.8 MB (125818097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7519a5ce24ec95ec84e069ac80bf61aa9eff8e1d536ff3ac2b1344cc081cfaeb`  
		Last Modified: Thu, 25 Apr 2024 23:51:13 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c444202310a3b295657f00e13d43fb34e0e1b7e5a4fcc3c5f00a6bf1c58dc02b`  
		Last Modified: Thu, 25 Apr 2024 23:51:49 GMT  
		Size: 82.8 MB (82848125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c1d250e67d2a6b488b18a2854e800a47b2fc648e6c1c90120e344b0d728e4f`  
		Last Modified: Thu, 25 Apr 2024 23:51:41 GMT  
		Size: 304.0 KB (303966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d54974e2af3e22412efba3d867427f335016c5fec75318bfd2c3350c059ba81`  
		Last Modified: Thu, 25 Apr 2024 23:51:40 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fdd964bb98502b1d29d5fba037733eccaac0ac56a70526e08f4568cee71d52`  
		Last Modified: Thu, 25 Apr 2024 23:51:44 GMT  
		Size: 23.1 MB (23121829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:793761f4b910a035da9873fd3b962024f8b429c4ae1f20e46864e5eaf409dd58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:a573f950575377c4263e57957c6d6dcc02a1d2071d604d0ebcb23355ac9b273b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274138940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55aaef701db462fed2147281c3ab669d7a2d1cba703b326934ea30fcae6df9fb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:46:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:46:15 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:58:29 GMT
ENV ROS_DISTRO=iron
# Thu, 25 Apr 2024 23:59:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:59:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:59:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:59:19 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:59:42 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:59:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:59:52 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 26 Apr 2024 00:00:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c55c47f6c73f60c344ac909c8ce0f12556b25eb765ed1f930fd5119119fa8`  
		Last Modified: Fri, 26 Apr 2024 00:10:13 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea1bb9a1cbe1070a649d11146b0737587115408731b3aaafc4369bf8fa8ec5`  
		Last Modified: Fri, 26 Apr 2024 00:10:12 GMT  
		Size: 3.8 MB (3829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fcfe8f75de0eb6b7aa0353aa2da1b14a8e59971d76b2aaa765db2fbcd3646d`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613a8d5a300a55d99cc495b072be31797992ae61ee123425443a8e057f213d22`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09746b27f422485d8473855067a57c2a5b382bd7af77d2e57bb03135fe53726a`  
		Last Modified: Fri, 26 Apr 2024 00:13:54 GMT  
		Size: 129.4 MB (129439340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b0dd01d830d6f7a02dcff390bd7e6dca8c567f47dde423deb2d8d9cc213b27`  
		Last Modified: Fri, 26 Apr 2024 00:13:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c788bbf8906d323dabf78fd02984454611c7f0813ee03ad13ada9a7e7d7a3df`  
		Last Modified: Fri, 26 Apr 2024 00:14:13 GMT  
		Size: 85.2 MB (85172231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb115de4a4f2dc14fc51329a24630087a98d316d3e34534d3fdcdfca83612c2`  
		Last Modified: Fri, 26 Apr 2024 00:14:03 GMT  
		Size: 304.0 KB (303969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02b4458aff6bfe760b18d725f3435ff9d4921931e29c56a4fbf863a2574495c`  
		Last Modified: Fri, 26 Apr 2024 00:14:03 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fc2f00f0169936bfde19063cdd5b052261b4ccb752cf391cf4e5e0aacbd756`  
		Last Modified: Fri, 26 Apr 2024 00:14:07 GMT  
		Size: 23.7 MB (23734288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bcccef72adf805fec11a65c7ace7cf4055750edd226286b126a43bd908b458c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265514511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd4684ba7c242f227d61d054c0eacf3b617c7430d6eaad6a1e61ad346c1cff6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:15:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:26 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:15:27 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:35:50 GMT
ENV ROS_DISTRO=iron
# Thu, 25 Apr 2024 23:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:36:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:36:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:36:51 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:37:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:37:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:37:21 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 25 Apr 2024 23:37:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8742e7f1cdee93cb67c00da995274c6e0ba604195faecabb78406165bda44c8`  
		Last Modified: Thu, 25 Apr 2024 23:48:53 GMT  
		Size: 1.2 MB (1215061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb0c9474a61e99af61afdbd9b14569fd8665a46861ca9152a5ee8bce5949b92`  
		Last Modified: Thu, 25 Apr 2024 23:48:51 GMT  
		Size: 3.8 MB (3801439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22805c294de7be40a069d9239ec8d1faa88dd167cec6bc905f2563ad0924efb0`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47453fc6a62dcd9926ec5ec79224f57fee1b8c82a80e42cd77cb74f79429db13`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba50c5e8c063dd02d5262b7ac93a158b4818e0636449c9aeec4f35b4f358c40`  
		Last Modified: Thu, 25 Apr 2024 23:51:32 GMT  
		Size: 125.8 MB (125818097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7519a5ce24ec95ec84e069ac80bf61aa9eff8e1d536ff3ac2b1344cc081cfaeb`  
		Last Modified: Thu, 25 Apr 2024 23:51:13 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c444202310a3b295657f00e13d43fb34e0e1b7e5a4fcc3c5f00a6bf1c58dc02b`  
		Last Modified: Thu, 25 Apr 2024 23:51:49 GMT  
		Size: 82.8 MB (82848125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c1d250e67d2a6b488b18a2854e800a47b2fc648e6c1c90120e344b0d728e4f`  
		Last Modified: Thu, 25 Apr 2024 23:51:41 GMT  
		Size: 304.0 KB (303966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d54974e2af3e22412efba3d867427f335016c5fec75318bfd2c3350c059ba81`  
		Last Modified: Thu, 25 Apr 2024 23:51:40 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fdd964bb98502b1d29d5fba037733eccaac0ac56a70526e08f4568cee71d52`  
		Last Modified: Thu, 25 Apr 2024 23:51:44 GMT  
		Size: 23.1 MB (23121829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:b0cca1f90a209e566c22bc41c2009e9f9878dae62a446571bf8f50c0df10a0f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:82afa105fd5960e606049c48abc17b393cc46f2e75916a3202c4587c3f4266b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.9 MB (164925973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dce5789cec82361f3b13b231a7c8da5e639d18eb434c00322eb73c50f840222`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:46:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:46:15 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:58:29 GMT
ENV ROS_DISTRO=iron
# Thu, 25 Apr 2024 23:59:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:59:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:59:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:59:19 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c55c47f6c73f60c344ac909c8ce0f12556b25eb765ed1f930fd5119119fa8`  
		Last Modified: Fri, 26 Apr 2024 00:10:13 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea1bb9a1cbe1070a649d11146b0737587115408731b3aaafc4369bf8fa8ec5`  
		Last Modified: Fri, 26 Apr 2024 00:10:12 GMT  
		Size: 3.8 MB (3829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fcfe8f75de0eb6b7aa0353aa2da1b14a8e59971d76b2aaa765db2fbcd3646d`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613a8d5a300a55d99cc495b072be31797992ae61ee123425443a8e057f213d22`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09746b27f422485d8473855067a57c2a5b382bd7af77d2e57bb03135fe53726a`  
		Last Modified: Fri, 26 Apr 2024 00:13:54 GMT  
		Size: 129.4 MB (129439340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b0dd01d830d6f7a02dcff390bd7e6dca8c567f47dde423deb2d8d9cc213b27`  
		Last Modified: Fri, 26 Apr 2024 00:13:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f27b86933276108e1ed30766cc81f45d1743c38dee3fb60c1b65bc4ecbadcfff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159238087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833b3f505d30fc60bded99f8da4fb5c1cec23919d07d6e7ca125dde8a707e576`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:15:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:26 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:15:27 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:35:50 GMT
ENV ROS_DISTRO=iron
# Thu, 25 Apr 2024 23:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:36:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:36:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:36:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8742e7f1cdee93cb67c00da995274c6e0ba604195faecabb78406165bda44c8`  
		Last Modified: Thu, 25 Apr 2024 23:48:53 GMT  
		Size: 1.2 MB (1215061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb0c9474a61e99af61afdbd9b14569fd8665a46861ca9152a5ee8bce5949b92`  
		Last Modified: Thu, 25 Apr 2024 23:48:51 GMT  
		Size: 3.8 MB (3801439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22805c294de7be40a069d9239ec8d1faa88dd167cec6bc905f2563ad0924efb0`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47453fc6a62dcd9926ec5ec79224f57fee1b8c82a80e42cd77cb74f79429db13`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba50c5e8c063dd02d5262b7ac93a158b4818e0636449c9aeec4f35b4f358c40`  
		Last Modified: Thu, 25 Apr 2024 23:51:32 GMT  
		Size: 125.8 MB (125818097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7519a5ce24ec95ec84e069ac80bf61aa9eff8e1d536ff3ac2b1344cc081cfaeb`  
		Last Modified: Thu, 25 Apr 2024 23:51:13 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-core-jammy`

```console
$ docker pull ros@sha256:b0cca1f90a209e566c22bc41c2009e9f9878dae62a446571bf8f50c0df10a0f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:82afa105fd5960e606049c48abc17b393cc46f2e75916a3202c4587c3f4266b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.9 MB (164925973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dce5789cec82361f3b13b231a7c8da5e639d18eb434c00322eb73c50f840222`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:46:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:46:15 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:58:29 GMT
ENV ROS_DISTRO=iron
# Thu, 25 Apr 2024 23:59:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:59:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:59:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:59:19 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c55c47f6c73f60c344ac909c8ce0f12556b25eb765ed1f930fd5119119fa8`  
		Last Modified: Fri, 26 Apr 2024 00:10:13 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea1bb9a1cbe1070a649d11146b0737587115408731b3aaafc4369bf8fa8ec5`  
		Last Modified: Fri, 26 Apr 2024 00:10:12 GMT  
		Size: 3.8 MB (3829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fcfe8f75de0eb6b7aa0353aa2da1b14a8e59971d76b2aaa765db2fbcd3646d`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613a8d5a300a55d99cc495b072be31797992ae61ee123425443a8e057f213d22`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09746b27f422485d8473855067a57c2a5b382bd7af77d2e57bb03135fe53726a`  
		Last Modified: Fri, 26 Apr 2024 00:13:54 GMT  
		Size: 129.4 MB (129439340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b0dd01d830d6f7a02dcff390bd7e6dca8c567f47dde423deb2d8d9cc213b27`  
		Last Modified: Fri, 26 Apr 2024 00:13:34 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f27b86933276108e1ed30766cc81f45d1743c38dee3fb60c1b65bc4ecbadcfff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159238087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833b3f505d30fc60bded99f8da4fb5c1cec23919d07d6e7ca125dde8a707e576`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:15:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:26 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:15:27 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:35:50 GMT
ENV ROS_DISTRO=iron
# Thu, 25 Apr 2024 23:36:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:36:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:36:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:36:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8742e7f1cdee93cb67c00da995274c6e0ba604195faecabb78406165bda44c8`  
		Last Modified: Thu, 25 Apr 2024 23:48:53 GMT  
		Size: 1.2 MB (1215061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb0c9474a61e99af61afdbd9b14569fd8665a46861ca9152a5ee8bce5949b92`  
		Last Modified: Thu, 25 Apr 2024 23:48:51 GMT  
		Size: 3.8 MB (3801439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22805c294de7be40a069d9239ec8d1faa88dd167cec6bc905f2563ad0924efb0`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47453fc6a62dcd9926ec5ec79224f57fee1b8c82a80e42cd77cb74f79429db13`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba50c5e8c063dd02d5262b7ac93a158b4818e0636449c9aeec4f35b4f358c40`  
		Last Modified: Thu, 25 Apr 2024 23:51:32 GMT  
		Size: 125.8 MB (125818097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7519a5ce24ec95ec84e069ac80bf61aa9eff8e1d536ff3ac2b1344cc081cfaeb`  
		Last Modified: Thu, 25 Apr 2024 23:51:13 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:latest`

```console
$ docker pull ros@sha256:ca92c95cdf8a49f9df4954457d8c722c71f1162183019bdc598555d5ec72be69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:48f600bd2320f83d5f883b6bf556241d20f0fc61fa0e6c2dccc9596ad7fc16ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268724756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e61c24be13c923514bca2d9633d30daf5e988b20fdf513bc1ce93d246d0586`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:46:07 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:13 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:46:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:46:15 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:46:15 GMT
ENV ROS_DISTRO=humble
# Thu, 25 Apr 2024 23:47:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:47:50 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:47:50 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:47:50 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:48:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:48:44 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:48:46 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 25 Apr 2024 23:49:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c55c47f6c73f60c344ac909c8ce0f12556b25eb765ed1f930fd5119119fa8`  
		Last Modified: Fri, 26 Apr 2024 00:10:13 GMT  
		Size: 1.2 MB (1214738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea1bb9a1cbe1070a649d11146b0737587115408731b3aaafc4369bf8fa8ec5`  
		Last Modified: Fri, 26 Apr 2024 00:10:12 GMT  
		Size: 3.8 MB (3829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fcfe8f75de0eb6b7aa0353aa2da1b14a8e59971d76b2aaa765db2fbcd3646d`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613a8d5a300a55d99cc495b072be31797992ae61ee123425443a8e057f213d22`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e613eafee0b5c3d693725fcd8aee80138fa0b98e7bac50db0c98a01e5d8db657`  
		Last Modified: Fri, 26 Apr 2024 00:11:20 GMT  
		Size: 111.7 MB (111670901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd4eb513578eec2e5735951fb45bb003578d15385dd1543f44cbce4337eeba1`  
		Last Modified: Fri, 26 Apr 2024 00:10:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2566fd61ac60a9b3080af079366caf626ff1a80b331ef4d6db464b110cf1668`  
		Last Modified: Fri, 26 Apr 2024 00:11:42 GMT  
		Size: 98.1 MB (98144643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0743914e27de4c58dbb07d421fc77800a8e84159462620a31145ad84dc4d6e25`  
		Last Modified: Fri, 26 Apr 2024 00:11:29 GMT  
		Size: 318.6 KB (318577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8e0f05e85575ca00e3a6def93ae68aea67031e70c294807ba3d2296c24f3a6`  
		Last Modified: Fri, 26 Apr 2024 00:11:29 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33f8167f8092660bad0dbe0b83a8eaa60de68fc721873903c266beb36f28eb8`  
		Last Modified: Fri, 26 Apr 2024 00:11:33 GMT  
		Size: 23.1 MB (23101532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e8ba2693933a33857ef428044e4922f6cb7e5a0e4b93ac09eab65239c8ca1bdb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260252435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea97f2abef7148e115ec2fe03ebcd28e1116b42712465753d5302e845f5c58a4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:15:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:26 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:15:27 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:15:27 GMT
ENV ROS_DISTRO=humble
# Thu, 25 Apr 2024 23:17:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:17:03 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:17:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:17:03 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:18:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:18:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:18:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 25 Apr 2024 23:18:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8742e7f1cdee93cb67c00da995274c6e0ba604195faecabb78406165bda44c8`  
		Last Modified: Thu, 25 Apr 2024 23:48:53 GMT  
		Size: 1.2 MB (1215061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb0c9474a61e99af61afdbd9b14569fd8665a46861ca9152a5ee8bce5949b92`  
		Last Modified: Thu, 25 Apr 2024 23:48:51 GMT  
		Size: 3.8 MB (3801439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22805c294de7be40a069d9239ec8d1faa88dd167cec6bc905f2563ad0924efb0`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47453fc6a62dcd9926ec5ec79224f57fee1b8c82a80e42cd77cb74f79429db13`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9041c054936e39ecd00eb1e5d8f68751ff7c88ac3305bc02f2980938a41609a8`  
		Last Modified: Thu, 25 Apr 2024 23:49:08 GMT  
		Size: 108.3 MB (108301385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfea731d72343f3e24f5cc55f8b6719d51b80736bbeb51f38e3ef6db5eb640b9`  
		Last Modified: Thu, 25 Apr 2024 23:48:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091f9d9649c87b52ff226fc85a91b595a37923baa5399ad60a8de5b67bffb0cc`  
		Last Modified: Thu, 25 Apr 2024 23:49:28 GMT  
		Size: 95.7 MB (95689323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130fa34a155f4df6a8d3f6505f55730d3c0d63d79dfa43382ba1b779cf89e428`  
		Last Modified: Thu, 25 Apr 2024 23:49:17 GMT  
		Size: 318.6 KB (318573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c7a38f9f8bc099380ed9c7686469ca38adccc4d03281f06706e02b57a2736d`  
		Last Modified: Thu, 25 Apr 2024 23:49:17 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8075d42472813ac5f7cc2bf03f077a9dae00912f0fb50fafea6a799bf9e39df`  
		Last Modified: Thu, 25 Apr 2024 23:49:21 GMT  
		Size: 22.5 MB (22520687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic`

```console
$ docker pull ros@sha256:b1b54754a3b0ab5c5fcb2bab22af22a76cec3a610669db310b90522d64437197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:19da7f9b9cdd8f1c74e7e85bd1c489c5cf44d5a07a9103fa6e03ed22e19d7452
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269855614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c2655d647e16dab430a4ab3e0fd88a0ff4d48d749c9fc095b92ced2cf84cfa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:23:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:23:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:23:33 GMT
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
# Wed, 17 Apr 2024 18:23:33 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:46:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:46:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:34:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:34:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 23:34:52 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:34:53 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:34:53 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 23:37:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:37:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 23:37:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:37:39 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:38:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:38:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:38:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:60cc0dcff74033c96380df2ca2f1381aa68602df27d53aa1bbf2bbe4ba703158`  
		Last Modified: Wed, 17 Apr 2024 23:03:46 GMT  
		Size: 28.6 MB (28584597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d5a8b38971aa00006472ba6e15b3d63812d5be3b6ea5d0934a10a9c5eff4f2`  
		Last Modified: Thu, 25 Apr 2024 21:58:11 GMT  
		Size: 1.2 MB (1198651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8bdba8db8e4ab0c862f77320974371c1676dc95c1446f27833f85847318046`  
		Last Modified: Thu, 25 Apr 2024 21:58:10 GMT  
		Size: 5.6 MB (5553903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c80ca07639219bf407e128fe8caa52302b4292bbe474c1ab1832eb72aec9c2`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328f9b72b1ffdadcda11bef8fe51610c9edd40f3808de9b55a1f3544f935246b`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9fc3a1fbfc1da703dfe0a7eebc525c436ecb136099c7b093223f63a53a88cf`  
		Last Modified: Fri, 26 Apr 2024 00:08:04 GMT  
		Size: 182.1 MB (182121227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1d60a891782a0a32e458132ad27a7f52858a04eb4e454cee7a157277c91dc`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2042a043f80758c28a5085cc32b1b95a7ca2b058c0cafd51cab3a38f6c90abd9`  
		Last Modified: Fri, 26 Apr 2024 00:08:20 GMT  
		Size: 50.9 MB (50942523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed89c27bd2976f63a3b389c2abca113a81e69f65764d0cd0b29bf8d6c15e2048`  
		Last Modified: Fri, 26 Apr 2024 00:08:13 GMT  
		Size: 321.3 KB (321272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739fa1e6ce1a27dcd30dbe9247ecd6e46e3ab63e942aed8b10426f25b5ca4617`  
		Last Modified: Fri, 26 Apr 2024 00:08:13 GMT  
		Size: 1.1 MB (1130946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:bb6a6d98c3c87304529ba58c0bd3552bedb2d340eb7f25a9a01645271b667e8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234219895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458ab54c0bf134242e1fb27512203ae482be46b731ee02315d6e2eeb41632079`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:58:26 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:58:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:58:28 GMT
ADD file:648705eca6ad0949d4722f06be77e38518c38195f6aa605ceb301e2b576583a6 in / 
# Wed, 17 Apr 2024 17:58:29 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:23:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:23:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:23:39 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 21:23:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 21:23:40 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 21:23:40 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 21:23:40 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 21:28:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:28:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 21:28:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 21:28:05 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 21:28:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:28:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 21:28:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43be25f0e2861789d9988ebf21e9e09ed9fc29e4a0a9fcff186988c12198eb72`  
		Last Modified: Thu, 25 Apr 2024 20:32:27 GMT  
		Size: 24.6 MB (24603299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57c7c6b0d95dbfe3cdbfca2f13d363127a75593233feee79392b8bdc04c578f`  
		Last Modified: Thu, 25 Apr 2024 21:49:18 GMT  
		Size: 1.2 MB (1199826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e539bd992a697f1fe8600e12c926d29000edb31bd2a48e7ef2b1246c8b6b17ee`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 4.7 MB (4680560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af33f8ee12b49adbb11a4303ea26d144b4c9d91f1f73dede2a2697078e34c6ab`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73760fd1ba70cccc5f6b2efce867d27db17bdb15016a88dec04eea8aa5806495`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1234195d2e5c75a9c262290994f16cc1ad58c8359272cfa7a800c1f5b101b4c3`  
		Last Modified: Thu, 25 Apr 2024 21:49:44 GMT  
		Size: 161.8 MB (161843399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4d243b7fe65f370eb5fb5f9321d972d35280ebd7433f8a330366d8dc0ab708`  
		Last Modified: Thu, 25 Apr 2024 21:49:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2816939926a122bd358038de82d4cfab0e8f0c93b2314bd6255b3714e16ce3`  
		Last Modified: Thu, 25 Apr 2024 21:49:58 GMT  
		Size: 40.5 MB (40506317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc2d4fd3276529e1d6a7750cfeed0babd5a9715ad7f05f84265931aa73ed916`  
		Last Modified: Thu, 25 Apr 2024 21:49:53 GMT  
		Size: 321.3 KB (321270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b41cf2f29b6ef786b1f9bb11f48d1a06b36d458954f8e8e7fea76e3417bd029`  
		Last Modified: Thu, 25 Apr 2024 21:49:53 GMT  
		Size: 1.1 MB (1062732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5865307a4a1cc6f0107c987374732bb7439d634829c17d52b2e4e2f485b4a099
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256234064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee4042e70495fb72a82455992f83cb31483c7ba66e016ad7e28347669434a9b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:57:12 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:57:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:57:14 GMT
ADD file:14fd903d8c1e98bd6a8c31b38182fa528e5277243e3b7ea9f682a57a9e7a3e60 in / 
# Wed, 17 Apr 2024 17:57:14 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:52:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:52:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:53:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 22:53:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 22:53:01 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 22:53:01 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 22:53:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 22:57:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:57:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 22:57:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 22:57:11 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 22:57:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:57:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 22:58:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:11686d3c3279d285321ad7d2bd863c8436ee583c2e454390121bee791f83f4f0`  
		Last Modified: Fri, 19 Apr 2024 07:58:29 GMT  
		Size: 27.2 MB (27207009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d906abf37f94562dad4628e21edd4799f5b7ad35968b61e15ac75c2cdd6a03`  
		Last Modified: Thu, 25 Apr 2024 23:46:27 GMT  
		Size: 1.2 MB (1199790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c05ed3567f843faffdfe34cd1e0c2129c935c1a173f0f4340766ed2d7ea43c`  
		Last Modified: Thu, 25 Apr 2024 23:46:25 GMT  
		Size: 5.5 MB (5533359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2594a6c8a02cb8f624261bc1605dcc0a74febf3f99680383df74b1080f57db`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8db85d1386e4c9fbd8b44e416a226d866066b3cc601c33438b92f7e1f6b224c`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7191c39f47ff99af771f395f002e176589449dcee4a37ad63b334ccfad4b2b9`  
		Last Modified: Thu, 25 Apr 2024 23:46:59 GMT  
		Size: 175.6 MB (175645026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd936626e6ae7df788c5427a537008cb4d013834a4f47679b073a0be77f83eb`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b8e1dda62c86776ddde10c811ef285d3c93bb5e555a2bc77c86d47b7a8eae2`  
		Last Modified: Thu, 25 Apr 2024 23:47:13 GMT  
		Size: 45.2 MB (45208883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe611b97ee16439882986c4db27e03bd4a744413b106139077698f89e94f066c`  
		Last Modified: Thu, 25 Apr 2024 23:47:08 GMT  
		Size: 321.3 KB (321275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57e83a2db4356c8df2eba1a0d044a5b944d95996fcad3f50882dd8ecb50b9d`  
		Last Modified: Thu, 25 Apr 2024 23:47:08 GMT  
		Size: 1.1 MB (1116233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:1c75db4d44d416097ec52eb3b6ba7dfce7ea0600f936f213477b93bdf29d1f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:8da562734df8c3a461f2934b2d49713c70bc58403cc1945f0696cce8b205928b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.5 MB (840529615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f6479d04bc3c94470ba86f69a476f37d79a93a5d6463a84c9b6ed6d6c1b624`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:23:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:23:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:23:33 GMT
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
# Wed, 17 Apr 2024 18:23:33 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:46:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:46:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:34:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:34:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 23:34:52 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:34:53 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:34:53 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 23:37:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:37:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 23:37:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:37:39 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:38:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:38:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:38:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:45:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:60cc0dcff74033c96380df2ca2f1381aa68602df27d53aa1bbf2bbe4ba703158`  
		Last Modified: Wed, 17 Apr 2024 23:03:46 GMT  
		Size: 28.6 MB (28584597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d5a8b38971aa00006472ba6e15b3d63812d5be3b6ea5d0934a10a9c5eff4f2`  
		Last Modified: Thu, 25 Apr 2024 21:58:11 GMT  
		Size: 1.2 MB (1198651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8bdba8db8e4ab0c862f77320974371c1676dc95c1446f27833f85847318046`  
		Last Modified: Thu, 25 Apr 2024 21:58:10 GMT  
		Size: 5.6 MB (5553903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c80ca07639219bf407e128fe8caa52302b4292bbe474c1ab1832eb72aec9c2`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328f9b72b1ffdadcda11bef8fe51610c9edd40f3808de9b55a1f3544f935246b`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9fc3a1fbfc1da703dfe0a7eebc525c436ecb136099c7b093223f63a53a88cf`  
		Last Modified: Fri, 26 Apr 2024 00:08:04 GMT  
		Size: 182.1 MB (182121227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1d60a891782a0a32e458132ad27a7f52858a04eb4e454cee7a157277c91dc`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2042a043f80758c28a5085cc32b1b95a7ca2b058c0cafd51cab3a38f6c90abd9`  
		Last Modified: Fri, 26 Apr 2024 00:08:20 GMT  
		Size: 50.9 MB (50942523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed89c27bd2976f63a3b389c2abca113a81e69f65764d0cd0b29bf8d6c15e2048`  
		Last Modified: Fri, 26 Apr 2024 00:08:13 GMT  
		Size: 321.3 KB (321272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739fa1e6ce1a27dcd30dbe9247ecd6e46e3ab63e942aed8b10426f25b5ca4617`  
		Last Modified: Fri, 26 Apr 2024 00:08:13 GMT  
		Size: 1.1 MB (1130946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b75b46386e23032b66cbf7822b7a854a3be6f89124ec693ab386259442116f`  
		Last Modified: Fri, 26 Apr 2024 00:10:01 GMT  
		Size: 570.7 MB (570674001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:24b363b3f0afa0594079f769e4a2f9ad595b7699fb12386f79ea76f1d6061139
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.7 MB (730741016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71259b9d424129594b2dbd6199c1548e4cda8523248e56d985160e77cda88d50`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:58:26 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:58:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:58:28 GMT
ADD file:648705eca6ad0949d4722f06be77e38518c38195f6aa605ceb301e2b576583a6 in / 
# Wed, 17 Apr 2024 17:58:29 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:23:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:23:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:23:39 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 21:23:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 21:23:40 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 21:23:40 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 21:23:40 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 21:28:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:28:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 21:28:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 21:28:05 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 21:28:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:28:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 21:28:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:48:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43be25f0e2861789d9988ebf21e9e09ed9fc29e4a0a9fcff186988c12198eb72`  
		Last Modified: Thu, 25 Apr 2024 20:32:27 GMT  
		Size: 24.6 MB (24603299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57c7c6b0d95dbfe3cdbfca2f13d363127a75593233feee79392b8bdc04c578f`  
		Last Modified: Thu, 25 Apr 2024 21:49:18 GMT  
		Size: 1.2 MB (1199826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e539bd992a697f1fe8600e12c926d29000edb31bd2a48e7ef2b1246c8b6b17ee`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 4.7 MB (4680560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af33f8ee12b49adbb11a4303ea26d144b4c9d91f1f73dede2a2697078e34c6ab`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73760fd1ba70cccc5f6b2efce867d27db17bdb15016a88dec04eea8aa5806495`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1234195d2e5c75a9c262290994f16cc1ad58c8359272cfa7a800c1f5b101b4c3`  
		Last Modified: Thu, 25 Apr 2024 21:49:44 GMT  
		Size: 161.8 MB (161843399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4d243b7fe65f370eb5fb5f9321d972d35280ebd7433f8a330366d8dc0ab708`  
		Last Modified: Thu, 25 Apr 2024 21:49:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2816939926a122bd358038de82d4cfab0e8f0c93b2314bd6255b3714e16ce3`  
		Last Modified: Thu, 25 Apr 2024 21:49:58 GMT  
		Size: 40.5 MB (40506317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc2d4fd3276529e1d6a7750cfeed0babd5a9715ad7f05f84265931aa73ed916`  
		Last Modified: Thu, 25 Apr 2024 21:49:53 GMT  
		Size: 321.3 KB (321270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b41cf2f29b6ef786b1f9bb11f48d1a06b36d458954f8e8e7fea76e3417bd029`  
		Last Modified: Thu, 25 Apr 2024 21:49:53 GMT  
		Size: 1.1 MB (1062732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a890070a65f31ffd4461eeb161999179f8006289a9d3d8b6d5f88fe4eb520727`  
		Last Modified: Thu, 25 Apr 2024 21:51:28 GMT  
		Size: 496.5 MB (496521121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dc6426450630d5729e91078ac701bf4b4cbae6d2dac03068e99f77b53f5fc56e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **789.9 MB (789874441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256ec6c2ad4925b69e365723c222d588968b21452ab16f8823b40d4285d407cb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:57:12 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:57:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:57:14 GMT
ADD file:14fd903d8c1e98bd6a8c31b38182fa528e5277243e3b7ea9f682a57a9e7a3e60 in / 
# Wed, 17 Apr 2024 17:57:14 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:52:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:52:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:53:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 22:53:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 22:53:01 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 22:53:01 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 22:53:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 22:57:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:57:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 22:57:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 22:57:11 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 22:57:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:57:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 22:58:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:11686d3c3279d285321ad7d2bd863c8436ee583c2e454390121bee791f83f4f0`  
		Last Modified: Fri, 19 Apr 2024 07:58:29 GMT  
		Size: 27.2 MB (27207009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d906abf37f94562dad4628e21edd4799f5b7ad35968b61e15ac75c2cdd6a03`  
		Last Modified: Thu, 25 Apr 2024 23:46:27 GMT  
		Size: 1.2 MB (1199790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c05ed3567f843faffdfe34cd1e0c2129c935c1a173f0f4340766ed2d7ea43c`  
		Last Modified: Thu, 25 Apr 2024 23:46:25 GMT  
		Size: 5.5 MB (5533359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2594a6c8a02cb8f624261bc1605dcc0a74febf3f99680383df74b1080f57db`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8db85d1386e4c9fbd8b44e416a226d866066b3cc601c33438b92f7e1f6b224c`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7191c39f47ff99af771f395f002e176589449dcee4a37ad63b334ccfad4b2b9`  
		Last Modified: Thu, 25 Apr 2024 23:46:59 GMT  
		Size: 175.6 MB (175645026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd936626e6ae7df788c5427a537008cb4d013834a4f47679b073a0be77f83eb`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b8e1dda62c86776ddde10c811ef285d3c93bb5e555a2bc77c86d47b7a8eae2`  
		Last Modified: Thu, 25 Apr 2024 23:47:13 GMT  
		Size: 45.2 MB (45208883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe611b97ee16439882986c4db27e03bd4a744413b106139077698f89e94f066c`  
		Last Modified: Thu, 25 Apr 2024 23:47:08 GMT  
		Size: 321.3 KB (321275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57e83a2db4356c8df2eba1a0d044a5b944d95996fcad3f50882dd8ecb50b9d`  
		Last Modified: Thu, 25 Apr 2024 23:47:08 GMT  
		Size: 1.1 MB (1116233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cffb7118714ebff6eef992d85a49777651085cd578f5dee16226dfbae7e29b`  
		Last Modified: Thu, 25 Apr 2024 23:48:41 GMT  
		Size: 533.6 MB (533640377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:1c75db4d44d416097ec52eb3b6ba7dfce7ea0600f936f213477b93bdf29d1f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:8da562734df8c3a461f2934b2d49713c70bc58403cc1945f0696cce8b205928b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.5 MB (840529615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f6479d04bc3c94470ba86f69a476f37d79a93a5d6463a84c9b6ed6d6c1b624`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:23:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:23:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:23:33 GMT
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
# Wed, 17 Apr 2024 18:23:33 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:46:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:46:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:34:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:34:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 23:34:52 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:34:53 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:34:53 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 23:37:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:37:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 23:37:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:37:39 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:38:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:38:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:38:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:45:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:60cc0dcff74033c96380df2ca2f1381aa68602df27d53aa1bbf2bbe4ba703158`  
		Last Modified: Wed, 17 Apr 2024 23:03:46 GMT  
		Size: 28.6 MB (28584597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d5a8b38971aa00006472ba6e15b3d63812d5be3b6ea5d0934a10a9c5eff4f2`  
		Last Modified: Thu, 25 Apr 2024 21:58:11 GMT  
		Size: 1.2 MB (1198651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8bdba8db8e4ab0c862f77320974371c1676dc95c1446f27833f85847318046`  
		Last Modified: Thu, 25 Apr 2024 21:58:10 GMT  
		Size: 5.6 MB (5553903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c80ca07639219bf407e128fe8caa52302b4292bbe474c1ab1832eb72aec9c2`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328f9b72b1ffdadcda11bef8fe51610c9edd40f3808de9b55a1f3544f935246b`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9fc3a1fbfc1da703dfe0a7eebc525c436ecb136099c7b093223f63a53a88cf`  
		Last Modified: Fri, 26 Apr 2024 00:08:04 GMT  
		Size: 182.1 MB (182121227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1d60a891782a0a32e458132ad27a7f52858a04eb4e454cee7a157277c91dc`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2042a043f80758c28a5085cc32b1b95a7ca2b058c0cafd51cab3a38f6c90abd9`  
		Last Modified: Fri, 26 Apr 2024 00:08:20 GMT  
		Size: 50.9 MB (50942523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed89c27bd2976f63a3b389c2abca113a81e69f65764d0cd0b29bf8d6c15e2048`  
		Last Modified: Fri, 26 Apr 2024 00:08:13 GMT  
		Size: 321.3 KB (321272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739fa1e6ce1a27dcd30dbe9247ecd6e46e3ab63e942aed8b10426f25b5ca4617`  
		Last Modified: Fri, 26 Apr 2024 00:08:13 GMT  
		Size: 1.1 MB (1130946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b75b46386e23032b66cbf7822b7a854a3be6f89124ec693ab386259442116f`  
		Last Modified: Fri, 26 Apr 2024 00:10:01 GMT  
		Size: 570.7 MB (570674001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:24b363b3f0afa0594079f769e4a2f9ad595b7699fb12386f79ea76f1d6061139
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.7 MB (730741016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71259b9d424129594b2dbd6199c1548e4cda8523248e56d985160e77cda88d50`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:58:26 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:58:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:58:28 GMT
ADD file:648705eca6ad0949d4722f06be77e38518c38195f6aa605ceb301e2b576583a6 in / 
# Wed, 17 Apr 2024 17:58:29 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:23:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:23:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:23:39 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 21:23:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 21:23:40 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 21:23:40 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 21:23:40 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 21:28:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:28:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 21:28:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 21:28:05 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 21:28:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:28:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 21:28:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:48:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43be25f0e2861789d9988ebf21e9e09ed9fc29e4a0a9fcff186988c12198eb72`  
		Last Modified: Thu, 25 Apr 2024 20:32:27 GMT  
		Size: 24.6 MB (24603299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57c7c6b0d95dbfe3cdbfca2f13d363127a75593233feee79392b8bdc04c578f`  
		Last Modified: Thu, 25 Apr 2024 21:49:18 GMT  
		Size: 1.2 MB (1199826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e539bd992a697f1fe8600e12c926d29000edb31bd2a48e7ef2b1246c8b6b17ee`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 4.7 MB (4680560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af33f8ee12b49adbb11a4303ea26d144b4c9d91f1f73dede2a2697078e34c6ab`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73760fd1ba70cccc5f6b2efce867d27db17bdb15016a88dec04eea8aa5806495`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1234195d2e5c75a9c262290994f16cc1ad58c8359272cfa7a800c1f5b101b4c3`  
		Last Modified: Thu, 25 Apr 2024 21:49:44 GMT  
		Size: 161.8 MB (161843399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4d243b7fe65f370eb5fb5f9321d972d35280ebd7433f8a330366d8dc0ab708`  
		Last Modified: Thu, 25 Apr 2024 21:49:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2816939926a122bd358038de82d4cfab0e8f0c93b2314bd6255b3714e16ce3`  
		Last Modified: Thu, 25 Apr 2024 21:49:58 GMT  
		Size: 40.5 MB (40506317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc2d4fd3276529e1d6a7750cfeed0babd5a9715ad7f05f84265931aa73ed916`  
		Last Modified: Thu, 25 Apr 2024 21:49:53 GMT  
		Size: 321.3 KB (321270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b41cf2f29b6ef786b1f9bb11f48d1a06b36d458954f8e8e7fea76e3417bd029`  
		Last Modified: Thu, 25 Apr 2024 21:49:53 GMT  
		Size: 1.1 MB (1062732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a890070a65f31ffd4461eeb161999179f8006289a9d3d8b6d5f88fe4eb520727`  
		Last Modified: Thu, 25 Apr 2024 21:51:28 GMT  
		Size: 496.5 MB (496521121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dc6426450630d5729e91078ac701bf4b4cbae6d2dac03068e99f77b53f5fc56e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **789.9 MB (789874441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256ec6c2ad4925b69e365723c222d588968b21452ab16f8823b40d4285d407cb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:57:12 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:57:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:57:14 GMT
ADD file:14fd903d8c1e98bd6a8c31b38182fa528e5277243e3b7ea9f682a57a9e7a3e60 in / 
# Wed, 17 Apr 2024 17:57:14 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:52:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:52:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:53:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 22:53:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 22:53:01 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 22:53:01 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 22:53:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 22:57:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:57:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 22:57:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 22:57:11 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 22:57:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:57:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 22:58:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:15:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:11686d3c3279d285321ad7d2bd863c8436ee583c2e454390121bee791f83f4f0`  
		Last Modified: Fri, 19 Apr 2024 07:58:29 GMT  
		Size: 27.2 MB (27207009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d906abf37f94562dad4628e21edd4799f5b7ad35968b61e15ac75c2cdd6a03`  
		Last Modified: Thu, 25 Apr 2024 23:46:27 GMT  
		Size: 1.2 MB (1199790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c05ed3567f843faffdfe34cd1e0c2129c935c1a173f0f4340766ed2d7ea43c`  
		Last Modified: Thu, 25 Apr 2024 23:46:25 GMT  
		Size: 5.5 MB (5533359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2594a6c8a02cb8f624261bc1605dcc0a74febf3f99680383df74b1080f57db`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8db85d1386e4c9fbd8b44e416a226d866066b3cc601c33438b92f7e1f6b224c`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7191c39f47ff99af771f395f002e176589449dcee4a37ad63b334ccfad4b2b9`  
		Last Modified: Thu, 25 Apr 2024 23:46:59 GMT  
		Size: 175.6 MB (175645026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd936626e6ae7df788c5427a537008cb4d013834a4f47679b073a0be77f83eb`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b8e1dda62c86776ddde10c811ef285d3c93bb5e555a2bc77c86d47b7a8eae2`  
		Last Modified: Thu, 25 Apr 2024 23:47:13 GMT  
		Size: 45.2 MB (45208883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe611b97ee16439882986c4db27e03bd4a744413b106139077698f89e94f066c`  
		Last Modified: Thu, 25 Apr 2024 23:47:08 GMT  
		Size: 321.3 KB (321275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57e83a2db4356c8df2eba1a0d044a5b944d95996fcad3f50882dd8ecb50b9d`  
		Last Modified: Thu, 25 Apr 2024 23:47:08 GMT  
		Size: 1.1 MB (1116233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cffb7118714ebff6eef992d85a49777651085cd578f5dee16226dfbae7e29b`  
		Last Modified: Thu, 25 Apr 2024 23:48:41 GMT  
		Size: 533.6 MB (533640377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:fe5abc605da5afd638b0ba872a0898014f795eb7b0b5200d21508ae89ba39ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:b5042b4213cff7a9dc56b504215427c56adc475c8b91941179c67bd34356e92a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286784773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15c94e7694692829cda4da3854d63ba43a821915f58e756c072cff9c8ebba7b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:23:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:23:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:23:33 GMT
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
# Wed, 17 Apr 2024 18:23:33 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:46:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:46:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:34:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:34:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 23:34:52 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:34:53 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:34:53 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 23:37:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:37:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 23:37:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:37:39 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:38:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:38:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:38:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:39:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:60cc0dcff74033c96380df2ca2f1381aa68602df27d53aa1bbf2bbe4ba703158`  
		Last Modified: Wed, 17 Apr 2024 23:03:46 GMT  
		Size: 28.6 MB (28584597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d5a8b38971aa00006472ba6e15b3d63812d5be3b6ea5d0934a10a9c5eff4f2`  
		Last Modified: Thu, 25 Apr 2024 21:58:11 GMT  
		Size: 1.2 MB (1198651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8bdba8db8e4ab0c862f77320974371c1676dc95c1446f27833f85847318046`  
		Last Modified: Thu, 25 Apr 2024 21:58:10 GMT  
		Size: 5.6 MB (5553903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c80ca07639219bf407e128fe8caa52302b4292bbe474c1ab1832eb72aec9c2`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328f9b72b1ffdadcda11bef8fe51610c9edd40f3808de9b55a1f3544f935246b`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9fc3a1fbfc1da703dfe0a7eebc525c436ecb136099c7b093223f63a53a88cf`  
		Last Modified: Fri, 26 Apr 2024 00:08:04 GMT  
		Size: 182.1 MB (182121227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1d60a891782a0a32e458132ad27a7f52858a04eb4e454cee7a157277c91dc`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2042a043f80758c28a5085cc32b1b95a7ca2b058c0cafd51cab3a38f6c90abd9`  
		Last Modified: Fri, 26 Apr 2024 00:08:20 GMT  
		Size: 50.9 MB (50942523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed89c27bd2976f63a3b389c2abca113a81e69f65764d0cd0b29bf8d6c15e2048`  
		Last Modified: Fri, 26 Apr 2024 00:08:13 GMT  
		Size: 321.3 KB (321272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739fa1e6ce1a27dcd30dbe9247ecd6e46e3ab63e942aed8b10426f25b5ca4617`  
		Last Modified: Fri, 26 Apr 2024 00:08:13 GMT  
		Size: 1.1 MB (1130946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e3db20e63d979149296bbc750f00e8f864ed040c855f9e34c51d3c79119a04`  
		Last Modified: Fri, 26 Apr 2024 00:08:34 GMT  
		Size: 16.9 MB (16929159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:c9eb3355b18b1e0ed15ef8471f5215b18f8bda154d61de93bd1bfaea14a0e53c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249250039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc24ea5c0690fc95521d6aa258314a8accef98937eda1de041b2ba4efdd945a8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:58:26 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:58:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:58:28 GMT
ADD file:648705eca6ad0949d4722f06be77e38518c38195f6aa605ceb301e2b576583a6 in / 
# Wed, 17 Apr 2024 17:58:29 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:23:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:23:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:23:39 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 21:23:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 21:23:40 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 21:23:40 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 21:23:40 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 21:28:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:28:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 21:28:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 21:28:05 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 21:28:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:28:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 21:28:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:30:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43be25f0e2861789d9988ebf21e9e09ed9fc29e4a0a9fcff186988c12198eb72`  
		Last Modified: Thu, 25 Apr 2024 20:32:27 GMT  
		Size: 24.6 MB (24603299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57c7c6b0d95dbfe3cdbfca2f13d363127a75593233feee79392b8bdc04c578f`  
		Last Modified: Thu, 25 Apr 2024 21:49:18 GMT  
		Size: 1.2 MB (1199826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e539bd992a697f1fe8600e12c926d29000edb31bd2a48e7ef2b1246c8b6b17ee`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 4.7 MB (4680560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af33f8ee12b49adbb11a4303ea26d144b4c9d91f1f73dede2a2697078e34c6ab`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73760fd1ba70cccc5f6b2efce867d27db17bdb15016a88dec04eea8aa5806495`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1234195d2e5c75a9c262290994f16cc1ad58c8359272cfa7a800c1f5b101b4c3`  
		Last Modified: Thu, 25 Apr 2024 21:49:44 GMT  
		Size: 161.8 MB (161843399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4d243b7fe65f370eb5fb5f9321d972d35280ebd7433f8a330366d8dc0ab708`  
		Last Modified: Thu, 25 Apr 2024 21:49:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2816939926a122bd358038de82d4cfab0e8f0c93b2314bd6255b3714e16ce3`  
		Last Modified: Thu, 25 Apr 2024 21:49:58 GMT  
		Size: 40.5 MB (40506317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc2d4fd3276529e1d6a7750cfeed0babd5a9715ad7f05f84265931aa73ed916`  
		Last Modified: Thu, 25 Apr 2024 21:49:53 GMT  
		Size: 321.3 KB (321270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b41cf2f29b6ef786b1f9bb11f48d1a06b36d458954f8e8e7fea76e3417bd029`  
		Last Modified: Thu, 25 Apr 2024 21:49:53 GMT  
		Size: 1.1 MB (1062732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2bd1a3fefb6624d4580897c55b76059a1f27df12c1492382eea214faf7da29`  
		Last Modified: Thu, 25 Apr 2024 21:50:12 GMT  
		Size: 15.0 MB (15030144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5588687265eb7415a8e568b4c008df9cd47ee7afd3266166f363da599ca23d69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272765567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad54962939ce01b9491dc1c1c549a179d78efe236c38f3842fd483687cd2252f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:57:12 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:57:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:57:14 GMT
ADD file:14fd903d8c1e98bd6a8c31b38182fa528e5277243e3b7ea9f682a57a9e7a3e60 in / 
# Wed, 17 Apr 2024 17:57:14 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:52:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:52:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:53:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 22:53:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 22:53:01 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 22:53:01 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 22:53:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 22:57:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:57:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 22:57:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 22:57:11 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 22:57:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:57:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 22:58:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:59:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:11686d3c3279d285321ad7d2bd863c8436ee583c2e454390121bee791f83f4f0`  
		Last Modified: Fri, 19 Apr 2024 07:58:29 GMT  
		Size: 27.2 MB (27207009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d906abf37f94562dad4628e21edd4799f5b7ad35968b61e15ac75c2cdd6a03`  
		Last Modified: Thu, 25 Apr 2024 23:46:27 GMT  
		Size: 1.2 MB (1199790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c05ed3567f843faffdfe34cd1e0c2129c935c1a173f0f4340766ed2d7ea43c`  
		Last Modified: Thu, 25 Apr 2024 23:46:25 GMT  
		Size: 5.5 MB (5533359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2594a6c8a02cb8f624261bc1605dcc0a74febf3f99680383df74b1080f57db`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8db85d1386e4c9fbd8b44e416a226d866066b3cc601c33438b92f7e1f6b224c`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7191c39f47ff99af771f395f002e176589449dcee4a37ad63b334ccfad4b2b9`  
		Last Modified: Thu, 25 Apr 2024 23:46:59 GMT  
		Size: 175.6 MB (175645026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd936626e6ae7df788c5427a537008cb4d013834a4f47679b073a0be77f83eb`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b8e1dda62c86776ddde10c811ef285d3c93bb5e555a2bc77c86d47b7a8eae2`  
		Last Modified: Thu, 25 Apr 2024 23:47:13 GMT  
		Size: 45.2 MB (45208883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe611b97ee16439882986c4db27e03bd4a744413b106139077698f89e94f066c`  
		Last Modified: Thu, 25 Apr 2024 23:47:08 GMT  
		Size: 321.3 KB (321275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57e83a2db4356c8df2eba1a0d044a5b944d95996fcad3f50882dd8ecb50b9d`  
		Last Modified: Thu, 25 Apr 2024 23:47:08 GMT  
		Size: 1.1 MB (1116233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d705c1bee9e1a12dac5e27f15b47c425e3a5e9c144c20c4a22972a3048bb3358`  
		Last Modified: Thu, 25 Apr 2024 23:47:26 GMT  
		Size: 16.5 MB (16531503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:fe5abc605da5afd638b0ba872a0898014f795eb7b0b5200d21508ae89ba39ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:b5042b4213cff7a9dc56b504215427c56adc475c8b91941179c67bd34356e92a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286784773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15c94e7694692829cda4da3854d63ba43a821915f58e756c072cff9c8ebba7b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:23:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:23:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:23:33 GMT
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
# Wed, 17 Apr 2024 18:23:33 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:46:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:46:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:34:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:34:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 23:34:52 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:34:53 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:34:53 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 23:37:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:37:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 23:37:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:37:39 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:38:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:38:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:38:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:39:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:60cc0dcff74033c96380df2ca2f1381aa68602df27d53aa1bbf2bbe4ba703158`  
		Last Modified: Wed, 17 Apr 2024 23:03:46 GMT  
		Size: 28.6 MB (28584597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d5a8b38971aa00006472ba6e15b3d63812d5be3b6ea5d0934a10a9c5eff4f2`  
		Last Modified: Thu, 25 Apr 2024 21:58:11 GMT  
		Size: 1.2 MB (1198651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8bdba8db8e4ab0c862f77320974371c1676dc95c1446f27833f85847318046`  
		Last Modified: Thu, 25 Apr 2024 21:58:10 GMT  
		Size: 5.6 MB (5553903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c80ca07639219bf407e128fe8caa52302b4292bbe474c1ab1832eb72aec9c2`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328f9b72b1ffdadcda11bef8fe51610c9edd40f3808de9b55a1f3544f935246b`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9fc3a1fbfc1da703dfe0a7eebc525c436ecb136099c7b093223f63a53a88cf`  
		Last Modified: Fri, 26 Apr 2024 00:08:04 GMT  
		Size: 182.1 MB (182121227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1d60a891782a0a32e458132ad27a7f52858a04eb4e454cee7a157277c91dc`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2042a043f80758c28a5085cc32b1b95a7ca2b058c0cafd51cab3a38f6c90abd9`  
		Last Modified: Fri, 26 Apr 2024 00:08:20 GMT  
		Size: 50.9 MB (50942523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed89c27bd2976f63a3b389c2abca113a81e69f65764d0cd0b29bf8d6c15e2048`  
		Last Modified: Fri, 26 Apr 2024 00:08:13 GMT  
		Size: 321.3 KB (321272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739fa1e6ce1a27dcd30dbe9247ecd6e46e3ab63e942aed8b10426f25b5ca4617`  
		Last Modified: Fri, 26 Apr 2024 00:08:13 GMT  
		Size: 1.1 MB (1130946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e3db20e63d979149296bbc750f00e8f864ed040c855f9e34c51d3c79119a04`  
		Last Modified: Fri, 26 Apr 2024 00:08:34 GMT  
		Size: 16.9 MB (16929159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:c9eb3355b18b1e0ed15ef8471f5215b18f8bda154d61de93bd1bfaea14a0e53c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249250039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc24ea5c0690fc95521d6aa258314a8accef98937eda1de041b2ba4efdd945a8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:58:26 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:58:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:58:28 GMT
ADD file:648705eca6ad0949d4722f06be77e38518c38195f6aa605ceb301e2b576583a6 in / 
# Wed, 17 Apr 2024 17:58:29 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:23:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:23:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:23:39 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 21:23:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 21:23:40 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 21:23:40 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 21:23:40 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 21:28:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:28:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 21:28:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 21:28:05 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 21:28:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:28:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 21:28:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:30:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43be25f0e2861789d9988ebf21e9e09ed9fc29e4a0a9fcff186988c12198eb72`  
		Last Modified: Thu, 25 Apr 2024 20:32:27 GMT  
		Size: 24.6 MB (24603299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57c7c6b0d95dbfe3cdbfca2f13d363127a75593233feee79392b8bdc04c578f`  
		Last Modified: Thu, 25 Apr 2024 21:49:18 GMT  
		Size: 1.2 MB (1199826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e539bd992a697f1fe8600e12c926d29000edb31bd2a48e7ef2b1246c8b6b17ee`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 4.7 MB (4680560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af33f8ee12b49adbb11a4303ea26d144b4c9d91f1f73dede2a2697078e34c6ab`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73760fd1ba70cccc5f6b2efce867d27db17bdb15016a88dec04eea8aa5806495`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1234195d2e5c75a9c262290994f16cc1ad58c8359272cfa7a800c1f5b101b4c3`  
		Last Modified: Thu, 25 Apr 2024 21:49:44 GMT  
		Size: 161.8 MB (161843399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4d243b7fe65f370eb5fb5f9321d972d35280ebd7433f8a330366d8dc0ab708`  
		Last Modified: Thu, 25 Apr 2024 21:49:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2816939926a122bd358038de82d4cfab0e8f0c93b2314bd6255b3714e16ce3`  
		Last Modified: Thu, 25 Apr 2024 21:49:58 GMT  
		Size: 40.5 MB (40506317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc2d4fd3276529e1d6a7750cfeed0babd5a9715ad7f05f84265931aa73ed916`  
		Last Modified: Thu, 25 Apr 2024 21:49:53 GMT  
		Size: 321.3 KB (321270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b41cf2f29b6ef786b1f9bb11f48d1a06b36d458954f8e8e7fea76e3417bd029`  
		Last Modified: Thu, 25 Apr 2024 21:49:53 GMT  
		Size: 1.1 MB (1062732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2bd1a3fefb6624d4580897c55b76059a1f27df12c1492382eea214faf7da29`  
		Last Modified: Thu, 25 Apr 2024 21:50:12 GMT  
		Size: 15.0 MB (15030144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5588687265eb7415a8e568b4c008df9cd47ee7afd3266166f363da599ca23d69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272765567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad54962939ce01b9491dc1c1c549a179d78efe236c38f3842fd483687cd2252f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:57:12 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:57:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:57:14 GMT
ADD file:14fd903d8c1e98bd6a8c31b38182fa528e5277243e3b7ea9f682a57a9e7a3e60 in / 
# Wed, 17 Apr 2024 17:57:14 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:52:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:52:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:53:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 22:53:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 22:53:01 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 22:53:01 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 22:53:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 22:57:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:57:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 22:57:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 22:57:11 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 22:57:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:57:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 22:58:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:59:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:11686d3c3279d285321ad7d2bd863c8436ee583c2e454390121bee791f83f4f0`  
		Last Modified: Fri, 19 Apr 2024 07:58:29 GMT  
		Size: 27.2 MB (27207009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d906abf37f94562dad4628e21edd4799f5b7ad35968b61e15ac75c2cdd6a03`  
		Last Modified: Thu, 25 Apr 2024 23:46:27 GMT  
		Size: 1.2 MB (1199790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c05ed3567f843faffdfe34cd1e0c2129c935c1a173f0f4340766ed2d7ea43c`  
		Last Modified: Thu, 25 Apr 2024 23:46:25 GMT  
		Size: 5.5 MB (5533359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2594a6c8a02cb8f624261bc1605dcc0a74febf3f99680383df74b1080f57db`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8db85d1386e4c9fbd8b44e416a226d866066b3cc601c33438b92f7e1f6b224c`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7191c39f47ff99af771f395f002e176589449dcee4a37ad63b334ccfad4b2b9`  
		Last Modified: Thu, 25 Apr 2024 23:46:59 GMT  
		Size: 175.6 MB (175645026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd936626e6ae7df788c5427a537008cb4d013834a4f47679b073a0be77f83eb`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b8e1dda62c86776ddde10c811ef285d3c93bb5e555a2bc77c86d47b7a8eae2`  
		Last Modified: Thu, 25 Apr 2024 23:47:13 GMT  
		Size: 45.2 MB (45208883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe611b97ee16439882986c4db27e03bd4a744413b106139077698f89e94f066c`  
		Last Modified: Thu, 25 Apr 2024 23:47:08 GMT  
		Size: 321.3 KB (321275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57e83a2db4356c8df2eba1a0d044a5b944d95996fcad3f50882dd8ecb50b9d`  
		Last Modified: Thu, 25 Apr 2024 23:47:08 GMT  
		Size: 1.1 MB (1116233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d705c1bee9e1a12dac5e27f15b47c425e3a5e9c144c20c4a22972a3048bb3358`  
		Last Modified: Thu, 25 Apr 2024 23:47:26 GMT  
		Size: 16.5 MB (16531503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:b1b54754a3b0ab5c5fcb2bab22af22a76cec3a610669db310b90522d64437197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:19da7f9b9cdd8f1c74e7e85bd1c489c5cf44d5a07a9103fa6e03ed22e19d7452
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269855614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c2655d647e16dab430a4ab3e0fd88a0ff4d48d749c9fc095b92ced2cf84cfa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:23:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:23:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:23:33 GMT
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
# Wed, 17 Apr 2024 18:23:33 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:46:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:46:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:34:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:34:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 23:34:52 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:34:53 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:34:53 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 23:37:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:37:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 23:37:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:37:39 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:38:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:38:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:38:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:60cc0dcff74033c96380df2ca2f1381aa68602df27d53aa1bbf2bbe4ba703158`  
		Last Modified: Wed, 17 Apr 2024 23:03:46 GMT  
		Size: 28.6 MB (28584597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d5a8b38971aa00006472ba6e15b3d63812d5be3b6ea5d0934a10a9c5eff4f2`  
		Last Modified: Thu, 25 Apr 2024 21:58:11 GMT  
		Size: 1.2 MB (1198651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8bdba8db8e4ab0c862f77320974371c1676dc95c1446f27833f85847318046`  
		Last Modified: Thu, 25 Apr 2024 21:58:10 GMT  
		Size: 5.6 MB (5553903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c80ca07639219bf407e128fe8caa52302b4292bbe474c1ab1832eb72aec9c2`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328f9b72b1ffdadcda11bef8fe51610c9edd40f3808de9b55a1f3544f935246b`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9fc3a1fbfc1da703dfe0a7eebc525c436ecb136099c7b093223f63a53a88cf`  
		Last Modified: Fri, 26 Apr 2024 00:08:04 GMT  
		Size: 182.1 MB (182121227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1d60a891782a0a32e458132ad27a7f52858a04eb4e454cee7a157277c91dc`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2042a043f80758c28a5085cc32b1b95a7ca2b058c0cafd51cab3a38f6c90abd9`  
		Last Modified: Fri, 26 Apr 2024 00:08:20 GMT  
		Size: 50.9 MB (50942523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed89c27bd2976f63a3b389c2abca113a81e69f65764d0cd0b29bf8d6c15e2048`  
		Last Modified: Fri, 26 Apr 2024 00:08:13 GMT  
		Size: 321.3 KB (321272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739fa1e6ce1a27dcd30dbe9247ecd6e46e3ab63e942aed8b10426f25b5ca4617`  
		Last Modified: Fri, 26 Apr 2024 00:08:13 GMT  
		Size: 1.1 MB (1130946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:bb6a6d98c3c87304529ba58c0bd3552bedb2d340eb7f25a9a01645271b667e8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234219895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458ab54c0bf134242e1fb27512203ae482be46b731ee02315d6e2eeb41632079`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:58:26 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:58:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:58:28 GMT
ADD file:648705eca6ad0949d4722f06be77e38518c38195f6aa605ceb301e2b576583a6 in / 
# Wed, 17 Apr 2024 17:58:29 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:23:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:23:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:23:39 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 21:23:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 21:23:40 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 21:23:40 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 21:23:40 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 21:28:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:28:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 21:28:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 21:28:05 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 21:28:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:28:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 21:28:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43be25f0e2861789d9988ebf21e9e09ed9fc29e4a0a9fcff186988c12198eb72`  
		Last Modified: Thu, 25 Apr 2024 20:32:27 GMT  
		Size: 24.6 MB (24603299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57c7c6b0d95dbfe3cdbfca2f13d363127a75593233feee79392b8bdc04c578f`  
		Last Modified: Thu, 25 Apr 2024 21:49:18 GMT  
		Size: 1.2 MB (1199826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e539bd992a697f1fe8600e12c926d29000edb31bd2a48e7ef2b1246c8b6b17ee`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 4.7 MB (4680560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af33f8ee12b49adbb11a4303ea26d144b4c9d91f1f73dede2a2697078e34c6ab`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73760fd1ba70cccc5f6b2efce867d27db17bdb15016a88dec04eea8aa5806495`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1234195d2e5c75a9c262290994f16cc1ad58c8359272cfa7a800c1f5b101b4c3`  
		Last Modified: Thu, 25 Apr 2024 21:49:44 GMT  
		Size: 161.8 MB (161843399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4d243b7fe65f370eb5fb5f9321d972d35280ebd7433f8a330366d8dc0ab708`  
		Last Modified: Thu, 25 Apr 2024 21:49:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2816939926a122bd358038de82d4cfab0e8f0c93b2314bd6255b3714e16ce3`  
		Last Modified: Thu, 25 Apr 2024 21:49:58 GMT  
		Size: 40.5 MB (40506317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc2d4fd3276529e1d6a7750cfeed0babd5a9715ad7f05f84265931aa73ed916`  
		Last Modified: Thu, 25 Apr 2024 21:49:53 GMT  
		Size: 321.3 KB (321270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b41cf2f29b6ef786b1f9bb11f48d1a06b36d458954f8e8e7fea76e3417bd029`  
		Last Modified: Thu, 25 Apr 2024 21:49:53 GMT  
		Size: 1.1 MB (1062732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5865307a4a1cc6f0107c987374732bb7439d634829c17d52b2e4e2f485b4a099
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256234064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee4042e70495fb72a82455992f83cb31483c7ba66e016ad7e28347669434a9b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:57:12 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:57:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:57:14 GMT
ADD file:14fd903d8c1e98bd6a8c31b38182fa528e5277243e3b7ea9f682a57a9e7a3e60 in / 
# Wed, 17 Apr 2024 17:57:14 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:52:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:52:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:53:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 22:53:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 22:53:01 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 22:53:01 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 22:53:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 22:57:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:57:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 22:57:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 22:57:11 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 22:57:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:57:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 22:58:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:11686d3c3279d285321ad7d2bd863c8436ee583c2e454390121bee791f83f4f0`  
		Last Modified: Fri, 19 Apr 2024 07:58:29 GMT  
		Size: 27.2 MB (27207009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d906abf37f94562dad4628e21edd4799f5b7ad35968b61e15ac75c2cdd6a03`  
		Last Modified: Thu, 25 Apr 2024 23:46:27 GMT  
		Size: 1.2 MB (1199790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c05ed3567f843faffdfe34cd1e0c2129c935c1a173f0f4340766ed2d7ea43c`  
		Last Modified: Thu, 25 Apr 2024 23:46:25 GMT  
		Size: 5.5 MB (5533359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2594a6c8a02cb8f624261bc1605dcc0a74febf3f99680383df74b1080f57db`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8db85d1386e4c9fbd8b44e416a226d866066b3cc601c33438b92f7e1f6b224c`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7191c39f47ff99af771f395f002e176589449dcee4a37ad63b334ccfad4b2b9`  
		Last Modified: Thu, 25 Apr 2024 23:46:59 GMT  
		Size: 175.6 MB (175645026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd936626e6ae7df788c5427a537008cb4d013834a4f47679b073a0be77f83eb`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b8e1dda62c86776ddde10c811ef285d3c93bb5e555a2bc77c86d47b7a8eae2`  
		Last Modified: Thu, 25 Apr 2024 23:47:13 GMT  
		Size: 45.2 MB (45208883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe611b97ee16439882986c4db27e03bd4a744413b106139077698f89e94f066c`  
		Last Modified: Thu, 25 Apr 2024 23:47:08 GMT  
		Size: 321.3 KB (321275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57e83a2db4356c8df2eba1a0d044a5b944d95996fcad3f50882dd8ecb50b9d`  
		Last Modified: Thu, 25 Apr 2024 23:47:08 GMT  
		Size: 1.1 MB (1116233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:b1b54754a3b0ab5c5fcb2bab22af22a76cec3a610669db310b90522d64437197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:19da7f9b9cdd8f1c74e7e85bd1c489c5cf44d5a07a9103fa6e03ed22e19d7452
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269855614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c2655d647e16dab430a4ab3e0fd88a0ff4d48d749c9fc095b92ced2cf84cfa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:23:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:23:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:23:33 GMT
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
# Wed, 17 Apr 2024 18:23:33 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:46:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:46:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:34:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:34:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 23:34:52 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:34:53 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:34:53 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 23:37:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:37:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 23:37:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:37:39 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:38:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:38:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:38:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:60cc0dcff74033c96380df2ca2f1381aa68602df27d53aa1bbf2bbe4ba703158`  
		Last Modified: Wed, 17 Apr 2024 23:03:46 GMT  
		Size: 28.6 MB (28584597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d5a8b38971aa00006472ba6e15b3d63812d5be3b6ea5d0934a10a9c5eff4f2`  
		Last Modified: Thu, 25 Apr 2024 21:58:11 GMT  
		Size: 1.2 MB (1198651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8bdba8db8e4ab0c862f77320974371c1676dc95c1446f27833f85847318046`  
		Last Modified: Thu, 25 Apr 2024 21:58:10 GMT  
		Size: 5.6 MB (5553903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c80ca07639219bf407e128fe8caa52302b4292bbe474c1ab1832eb72aec9c2`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328f9b72b1ffdadcda11bef8fe51610c9edd40f3808de9b55a1f3544f935246b`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9fc3a1fbfc1da703dfe0a7eebc525c436ecb136099c7b093223f63a53a88cf`  
		Last Modified: Fri, 26 Apr 2024 00:08:04 GMT  
		Size: 182.1 MB (182121227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1d60a891782a0a32e458132ad27a7f52858a04eb4e454cee7a157277c91dc`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2042a043f80758c28a5085cc32b1b95a7ca2b058c0cafd51cab3a38f6c90abd9`  
		Last Modified: Fri, 26 Apr 2024 00:08:20 GMT  
		Size: 50.9 MB (50942523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed89c27bd2976f63a3b389c2abca113a81e69f65764d0cd0b29bf8d6c15e2048`  
		Last Modified: Fri, 26 Apr 2024 00:08:13 GMT  
		Size: 321.3 KB (321272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739fa1e6ce1a27dcd30dbe9247ecd6e46e3ab63e942aed8b10426f25b5ca4617`  
		Last Modified: Fri, 26 Apr 2024 00:08:13 GMT  
		Size: 1.1 MB (1130946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:bb6a6d98c3c87304529ba58c0bd3552bedb2d340eb7f25a9a01645271b667e8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234219895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458ab54c0bf134242e1fb27512203ae482be46b731ee02315d6e2eeb41632079`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:58:26 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:58:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:58:28 GMT
ADD file:648705eca6ad0949d4722f06be77e38518c38195f6aa605ceb301e2b576583a6 in / 
# Wed, 17 Apr 2024 17:58:29 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:23:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:23:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:23:39 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 21:23:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 21:23:40 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 21:23:40 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 21:23:40 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 21:28:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:28:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 21:28:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 21:28:05 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 21:28:31 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:28:37 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 21:28:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43be25f0e2861789d9988ebf21e9e09ed9fc29e4a0a9fcff186988c12198eb72`  
		Last Modified: Thu, 25 Apr 2024 20:32:27 GMT  
		Size: 24.6 MB (24603299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57c7c6b0d95dbfe3cdbfca2f13d363127a75593233feee79392b8bdc04c578f`  
		Last Modified: Thu, 25 Apr 2024 21:49:18 GMT  
		Size: 1.2 MB (1199826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e539bd992a697f1fe8600e12c926d29000edb31bd2a48e7ef2b1246c8b6b17ee`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 4.7 MB (4680560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af33f8ee12b49adbb11a4303ea26d144b4c9d91f1f73dede2a2697078e34c6ab`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73760fd1ba70cccc5f6b2efce867d27db17bdb15016a88dec04eea8aa5806495`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1234195d2e5c75a9c262290994f16cc1ad58c8359272cfa7a800c1f5b101b4c3`  
		Last Modified: Thu, 25 Apr 2024 21:49:44 GMT  
		Size: 161.8 MB (161843399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4d243b7fe65f370eb5fb5f9321d972d35280ebd7433f8a330366d8dc0ab708`  
		Last Modified: Thu, 25 Apr 2024 21:49:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2816939926a122bd358038de82d4cfab0e8f0c93b2314bd6255b3714e16ce3`  
		Last Modified: Thu, 25 Apr 2024 21:49:58 GMT  
		Size: 40.5 MB (40506317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc2d4fd3276529e1d6a7750cfeed0babd5a9715ad7f05f84265931aa73ed916`  
		Last Modified: Thu, 25 Apr 2024 21:49:53 GMT  
		Size: 321.3 KB (321270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b41cf2f29b6ef786b1f9bb11f48d1a06b36d458954f8e8e7fea76e3417bd029`  
		Last Modified: Thu, 25 Apr 2024 21:49:53 GMT  
		Size: 1.1 MB (1062732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5865307a4a1cc6f0107c987374732bb7439d634829c17d52b2e4e2f485b4a099
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256234064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee4042e70495fb72a82455992f83cb31483c7ba66e016ad7e28347669434a9b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:57:12 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:57:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:57:14 GMT
ADD file:14fd903d8c1e98bd6a8c31b38182fa528e5277243e3b7ea9f682a57a9e7a3e60 in / 
# Wed, 17 Apr 2024 17:57:14 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:52:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:52:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:53:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 22:53:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 22:53:01 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 22:53:01 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 22:53:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 22:57:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:57:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 22:57:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 22:57:11 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 22:57:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:57:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 22:58:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:11686d3c3279d285321ad7d2bd863c8436ee583c2e454390121bee791f83f4f0`  
		Last Modified: Fri, 19 Apr 2024 07:58:29 GMT  
		Size: 27.2 MB (27207009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d906abf37f94562dad4628e21edd4799f5b7ad35968b61e15ac75c2cdd6a03`  
		Last Modified: Thu, 25 Apr 2024 23:46:27 GMT  
		Size: 1.2 MB (1199790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c05ed3567f843faffdfe34cd1e0c2129c935c1a173f0f4340766ed2d7ea43c`  
		Last Modified: Thu, 25 Apr 2024 23:46:25 GMT  
		Size: 5.5 MB (5533359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2594a6c8a02cb8f624261bc1605dcc0a74febf3f99680383df74b1080f57db`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8db85d1386e4c9fbd8b44e416a226d866066b3cc601c33438b92f7e1f6b224c`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7191c39f47ff99af771f395f002e176589449dcee4a37ad63b334ccfad4b2b9`  
		Last Modified: Thu, 25 Apr 2024 23:46:59 GMT  
		Size: 175.6 MB (175645026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd936626e6ae7df788c5427a537008cb4d013834a4f47679b073a0be77f83eb`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b8e1dda62c86776ddde10c811ef285d3c93bb5e555a2bc77c86d47b7a8eae2`  
		Last Modified: Thu, 25 Apr 2024 23:47:13 GMT  
		Size: 45.2 MB (45208883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe611b97ee16439882986c4db27e03bd4a744413b106139077698f89e94f066c`  
		Last Modified: Thu, 25 Apr 2024 23:47:08 GMT  
		Size: 321.3 KB (321275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57e83a2db4356c8df2eba1a0d044a5b944d95996fcad3f50882dd8ecb50b9d`  
		Last Modified: Thu, 25 Apr 2024 23:47:08 GMT  
		Size: 1.1 MB (1116233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:91ed9c5abfe6115e5fccfee312adff9f944126d7a7b17f17e6e4d2808475a6e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:14cacd59d3cc55cf0b2c7e0a9557666f25a8d0b247ec0246360dd8b68fd2b737
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217460873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe932093ca95aa479905eec4196c695e2124a068ac5ae760bd340d945db419a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:23:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:23:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:23:33 GMT
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
# Wed, 17 Apr 2024 18:23:33 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:46:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:46:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:34:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:34:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 23:34:52 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:34:53 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:34:53 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 23:37:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:37:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 23:37:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:37:39 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:60cc0dcff74033c96380df2ca2f1381aa68602df27d53aa1bbf2bbe4ba703158`  
		Last Modified: Wed, 17 Apr 2024 23:03:46 GMT  
		Size: 28.6 MB (28584597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d5a8b38971aa00006472ba6e15b3d63812d5be3b6ea5d0934a10a9c5eff4f2`  
		Last Modified: Thu, 25 Apr 2024 21:58:11 GMT  
		Size: 1.2 MB (1198651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8bdba8db8e4ab0c862f77320974371c1676dc95c1446f27833f85847318046`  
		Last Modified: Thu, 25 Apr 2024 21:58:10 GMT  
		Size: 5.6 MB (5553903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c80ca07639219bf407e128fe8caa52302b4292bbe474c1ab1832eb72aec9c2`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328f9b72b1ffdadcda11bef8fe51610c9edd40f3808de9b55a1f3544f935246b`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9fc3a1fbfc1da703dfe0a7eebc525c436ecb136099c7b093223f63a53a88cf`  
		Last Modified: Fri, 26 Apr 2024 00:08:04 GMT  
		Size: 182.1 MB (182121227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1d60a891782a0a32e458132ad27a7f52858a04eb4e454cee7a157277c91dc`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:5be4bd88b4dd0f8435cc575a96faac5ec52d9735e31fada395d357100e1a5065
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192329576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7273443bffe70cbded19b90d9298804a0e57327d4f5859bab0bdb34c6d94f58`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:58:26 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:58:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:58:28 GMT
ADD file:648705eca6ad0949d4722f06be77e38518c38195f6aa605ceb301e2b576583a6 in / 
# Wed, 17 Apr 2024 17:58:29 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:23:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:23:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:23:39 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 21:23:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 21:23:40 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 21:23:40 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 21:23:40 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 21:28:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:28:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 21:28:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 21:28:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:43be25f0e2861789d9988ebf21e9e09ed9fc29e4a0a9fcff186988c12198eb72`  
		Last Modified: Thu, 25 Apr 2024 20:32:27 GMT  
		Size: 24.6 MB (24603299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57c7c6b0d95dbfe3cdbfca2f13d363127a75593233feee79392b8bdc04c578f`  
		Last Modified: Thu, 25 Apr 2024 21:49:18 GMT  
		Size: 1.2 MB (1199826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e539bd992a697f1fe8600e12c926d29000edb31bd2a48e7ef2b1246c8b6b17ee`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 4.7 MB (4680560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af33f8ee12b49adbb11a4303ea26d144b4c9d91f1f73dede2a2697078e34c6ab`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73760fd1ba70cccc5f6b2efce867d27db17bdb15016a88dec04eea8aa5806495`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1234195d2e5c75a9c262290994f16cc1ad58c8359272cfa7a800c1f5b101b4c3`  
		Last Modified: Thu, 25 Apr 2024 21:49:44 GMT  
		Size: 161.8 MB (161843399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4d243b7fe65f370eb5fb5f9321d972d35280ebd7433f8a330366d8dc0ab708`  
		Last Modified: Thu, 25 Apr 2024 21:49:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1aabd4532484e4a75b8e86b2cd9cee1ea5e5b3a672aef0d422d51fccb6b6c1f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 MB (209587673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3b5dc90679ce32604eb3bb8987f70e8da04000dda0e491db54b597f38b1f9f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:57:12 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:57:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:57:14 GMT
ADD file:14fd903d8c1e98bd6a8c31b38182fa528e5277243e3b7ea9f682a57a9e7a3e60 in / 
# Wed, 17 Apr 2024 17:57:14 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:52:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:52:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:53:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 22:53:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 22:53:01 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 22:53:01 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 22:53:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 22:57:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:57:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 22:57:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 22:57:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:11686d3c3279d285321ad7d2bd863c8436ee583c2e454390121bee791f83f4f0`  
		Last Modified: Fri, 19 Apr 2024 07:58:29 GMT  
		Size: 27.2 MB (27207009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d906abf37f94562dad4628e21edd4799f5b7ad35968b61e15ac75c2cdd6a03`  
		Last Modified: Thu, 25 Apr 2024 23:46:27 GMT  
		Size: 1.2 MB (1199790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c05ed3567f843faffdfe34cd1e0c2129c935c1a173f0f4340766ed2d7ea43c`  
		Last Modified: Thu, 25 Apr 2024 23:46:25 GMT  
		Size: 5.5 MB (5533359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2594a6c8a02cb8f624261bc1605dcc0a74febf3f99680383df74b1080f57db`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8db85d1386e4c9fbd8b44e416a226d866066b3cc601c33438b92f7e1f6b224c`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7191c39f47ff99af771f395f002e176589449dcee4a37ad63b334ccfad4b2b9`  
		Last Modified: Thu, 25 Apr 2024 23:46:59 GMT  
		Size: 175.6 MB (175645026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd936626e6ae7df788c5427a537008cb4d013834a4f47679b073a0be77f83eb`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:91ed9c5abfe6115e5fccfee312adff9f944126d7a7b17f17e6e4d2808475a6e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:14cacd59d3cc55cf0b2c7e0a9557666f25a8d0b247ec0246360dd8b68fd2b737
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217460873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe932093ca95aa479905eec4196c695e2124a068ac5ae760bd340d945db419a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:23:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:23:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:23:33 GMT
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
# Wed, 17 Apr 2024 18:23:33 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:46:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:46:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:34:52 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:34:52 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 23:34:52 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:34:53 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:34:53 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 23:37:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:37:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 23:37:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:37:39 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:60cc0dcff74033c96380df2ca2f1381aa68602df27d53aa1bbf2bbe4ba703158`  
		Last Modified: Wed, 17 Apr 2024 23:03:46 GMT  
		Size: 28.6 MB (28584597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d5a8b38971aa00006472ba6e15b3d63812d5be3b6ea5d0934a10a9c5eff4f2`  
		Last Modified: Thu, 25 Apr 2024 21:58:11 GMT  
		Size: 1.2 MB (1198651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8bdba8db8e4ab0c862f77320974371c1676dc95c1446f27833f85847318046`  
		Last Modified: Thu, 25 Apr 2024 21:58:10 GMT  
		Size: 5.6 MB (5553903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c80ca07639219bf407e128fe8caa52302b4292bbe474c1ab1832eb72aec9c2`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 2.0 KB (2025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328f9b72b1ffdadcda11bef8fe51610c9edd40f3808de9b55a1f3544f935246b`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9fc3a1fbfc1da703dfe0a7eebc525c436ecb136099c7b093223f63a53a88cf`  
		Last Modified: Fri, 26 Apr 2024 00:08:04 GMT  
		Size: 182.1 MB (182121227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c1d60a891782a0a32e458132ad27a7f52858a04eb4e454cee7a157277c91dc`  
		Last Modified: Fri, 26 Apr 2024 00:07:35 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:5be4bd88b4dd0f8435cc575a96faac5ec52d9735e31fada395d357100e1a5065
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192329576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7273443bffe70cbded19b90d9298804a0e57327d4f5859bab0bdb34c6d94f58`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:58:26 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:58:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:58:28 GMT
ADD file:648705eca6ad0949d4722f06be77e38518c38195f6aa605ceb301e2b576583a6 in / 
# Wed, 17 Apr 2024 17:58:29 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:23:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:23:38 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:23:39 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 21:23:40 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 21:23:40 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 21:23:40 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 21:23:40 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 21:28:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:28:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 21:28:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 21:28:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:43be25f0e2861789d9988ebf21e9e09ed9fc29e4a0a9fcff186988c12198eb72`  
		Last Modified: Thu, 25 Apr 2024 20:32:27 GMT  
		Size: 24.6 MB (24603299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57c7c6b0d95dbfe3cdbfca2f13d363127a75593233feee79392b8bdc04c578f`  
		Last Modified: Thu, 25 Apr 2024 21:49:18 GMT  
		Size: 1.2 MB (1199826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e539bd992a697f1fe8600e12c926d29000edb31bd2a48e7ef2b1246c8b6b17ee`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 4.7 MB (4680560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af33f8ee12b49adbb11a4303ea26d144b4c9d91f1f73dede2a2697078e34c6ab`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73760fd1ba70cccc5f6b2efce867d27db17bdb15016a88dec04eea8aa5806495`  
		Last Modified: Thu, 25 Apr 2024 21:49:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1234195d2e5c75a9c262290994f16cc1ad58c8359272cfa7a800c1f5b101b4c3`  
		Last Modified: Thu, 25 Apr 2024 21:49:44 GMT  
		Size: 161.8 MB (161843399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4d243b7fe65f370eb5fb5f9321d972d35280ebd7433f8a330366d8dc0ab708`  
		Last Modified: Thu, 25 Apr 2024 21:49:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1aabd4532484e4a75b8e86b2cd9cee1ea5e5b3a672aef0d422d51fccb6b6c1f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 MB (209587673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3b5dc90679ce32604eb3bb8987f70e8da04000dda0e491db54b597f38b1f9f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:57:12 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:57:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:57:14 GMT
ADD file:14fd903d8c1e98bd6a8c31b38182fa528e5277243e3b7ea9f682a57a9e7a3e60 in / 
# Wed, 17 Apr 2024 17:57:14 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:52:53 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:52:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:53:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 22:53:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 25 Apr 2024 22:53:01 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 22:53:01 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 22:53:01 GMT
ENV ROS_DISTRO=noetic
# Thu, 25 Apr 2024 22:57:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:57:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 25 Apr 2024 22:57:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 22:57:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:11686d3c3279d285321ad7d2bd863c8436ee583c2e454390121bee791f83f4f0`  
		Last Modified: Fri, 19 Apr 2024 07:58:29 GMT  
		Size: 27.2 MB (27207009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d906abf37f94562dad4628e21edd4799f5b7ad35968b61e15ac75c2cdd6a03`  
		Last Modified: Thu, 25 Apr 2024 23:46:27 GMT  
		Size: 1.2 MB (1199790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c05ed3567f843faffdfe34cd1e0c2129c935c1a173f0f4340766ed2d7ea43c`  
		Last Modified: Thu, 25 Apr 2024 23:46:25 GMT  
		Size: 5.5 MB (5533359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2594a6c8a02cb8f624261bc1605dcc0a74febf3f99680383df74b1080f57db`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8db85d1386e4c9fbd8b44e416a226d866066b3cc601c33438b92f7e1f6b224c`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7191c39f47ff99af771f395f002e176589449dcee4a37ad63b334ccfad4b2b9`  
		Last Modified: Thu, 25 Apr 2024 23:46:59 GMT  
		Size: 175.6 MB (175645026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd936626e6ae7df788c5427a537008cb4d013834a4f47679b073a0be77f83eb`  
		Last Modified: Thu, 25 Apr 2024 23:46:24 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling`

```console
$ docker pull ros@sha256:aac0381b54e368a27aa78f67996b34c3c246a5703d42415614f8d75d0b7d392f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:4f692bd459b8c069c95b1161b70c7012b6bd6d3f03d8da71d8fa0f36731ac630
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299699712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4feba4c47c41fdc1d74bf02589c7f5c8ad628bab02a9f507c9047c481a94a1e0`
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
# Fri, 26 Apr 2024 00:02:43 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 26 Apr 2024 00:02:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 26 Apr 2024 00:02:43 GMT
ENV LANG=C.UTF-8
# Fri, 26 Apr 2024 00:02:43 GMT
ENV LC_ALL=C.UTF-8
# Fri, 26 Apr 2024 00:02:44 GMT
ENV ROS_DISTRO=rolling
# Fri, 26 Apr 2024 00:04:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 00:04:33 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 26 Apr 2024 00:04:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Apr 2024 00:04:33 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 00:05:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 00:05:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 26 Apr 2024 00:05:55 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 26 Apr 2024 00:06:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a4d1f96a582d77e142a9372c219837cfe0f63629329a255baa7d24c420180aa8`  
		Last Modified: Fri, 26 Apr 2024 00:16:04 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5d59efebd94c99ec9df4d45496b0da2a6cf7b2c0cdf5d25b454fcb2e658edb`  
		Last Modified: Fri, 26 Apr 2024 00:16:04 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58520ddab8eb418ed7f39a6254a49b4bcfd80de215fa34ce34a9225fda76cfa1`  
		Last Modified: Fri, 26 Apr 2024 00:16:23 GMT  
		Size: 122.4 MB (122419667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d901e24f0b5da18df9a9856ebd15b74d91636de5681425f96f796b0b33eee6fa`  
		Last Modified: Fri, 26 Apr 2024 00:16:04 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0f6d3a4fe977861e43b66af02f2cb05ddf4dc2f1077710ce94e3e725465777`  
		Last Modified: Fri, 26 Apr 2024 00:16:48 GMT  
		Size: 114.3 MB (114304236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edda434a4d5818268d4c619a9bc04730867294dd2019473d6caddd71e839979`  
		Last Modified: Fri, 26 Apr 2024 00:16:32 GMT  
		Size: 308.4 KB (308383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74118983417a907cbd593804ea5005eac2b24de69f5a15beba9c617db19c4308`  
		Last Modified: Fri, 26 Apr 2024 00:16:32 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a05c6e33bf42de738f5c7251416ca858af547a21401340c42c8b7f81140638e`  
		Last Modified: Fri, 26 Apr 2024 00:16:36 GMT  
		Size: 27.7 MB (27664162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b5485704c32bf60c31f0ec40d821853c6ed2b02611b3e3a360191a7158bf4c4a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289834728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb6cb328d62b21ab96c04e4cd291c9db0394c18acf4b095a96ced1c229159b6`
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
# Thu, 25 Apr 2024 23:40:24 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:40:24 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:40:24 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:40:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:40:24 GMT
ENV ROS_DISTRO=rolling
# Thu, 25 Apr 2024 23:42:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:42:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:42:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:42:42 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:44:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:44:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:44:46 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 25 Apr 2024 23:45:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:e67f27bf0eb8d01126489b229cc3de66eaf05114f0e8b097ec3cc1f82c7323d3`  
		Last Modified: Thu, 25 Apr 2024 23:53:23 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96db453f945716348ca0ce9b78ef87efa36506cc0eb304b6a721f8c3f7546e5b`  
		Last Modified: Thu, 25 Apr 2024 23:53:24 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1aaa8c881c7ea864f1ba79d24492f21979b6f4ef00bd8cb560a7c8d1cf24429`  
		Last Modified: Thu, 25 Apr 2024 23:53:47 GMT  
		Size: 117.2 MB (117220954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef1a74238ed8c5ca9164c6237a3de769a1ae331f532e3238a73422d516ed5d0`  
		Last Modified: Thu, 25 Apr 2024 23:53:24 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d434bce647868d8c266b6795f1cf576c146632ec85d73151d57000a28c38e7d`  
		Last Modified: Thu, 25 Apr 2024 23:54:09 GMT  
		Size: 111.2 MB (111162364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faa2b1bdd0240ea2225a565cd568f6b9835fbed9898f687ec5448aa3d49c16e`  
		Last Modified: Thu, 25 Apr 2024 23:53:56 GMT  
		Size: 308.4 KB (308378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d7a7b9b224d77d659618adfdcda742e0be04485cc3a45df8fd75f0d487c6ed`  
		Last Modified: Thu, 25 Apr 2024 23:53:56 GMT  
		Size: 2.5 KB (2481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3f10187114ee79588a9e9161a26e3460e17b8e07d0f53cc9917f0887077936`  
		Last Modified: Thu, 25 Apr 2024 23:54:00 GMT  
		Size: 26.8 MB (26809287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:83e35c16711e1aeca1d751b1d44f59e6ceee3100b6699e233c8b78b3a63093d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:2b4095ccbaa7b360055d1e33f65605db23a23b4c5c63d13667878b802f1e4063
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1033040266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ebe5f2366c7a7fd00ab88d976e433afc37e0f6112cfba9f9aaba137b9aee01`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:12:58 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:12:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:13:00 GMT
ADD file:86e27cbcb9656cd837a2abb01bc5989043c00e9d687476bf5efddfd851228eaf in / 
# Sun, 07 Apr 2024 17:13:00 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 06:11:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:11:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:11:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 06:11:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 06:11:35 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 06:11:36 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 06:11:36 GMT
ENV ROS_DISTRO=rolling
# Tue, 16 Apr 2024 06:13:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:13:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 06:13:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 06:13:26 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 06:14:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:14:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 06:14:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 06:15:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:22:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6174c5967d452dad6f4d36aaa2a180582ea28ff9feba01d4cb8e451d3b3cf9a5`  
		Last Modified: Tue, 16 Apr 2024 03:17:32 GMT  
		Size: 29.7 MB (29706077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b44e467bacfb7e6664cb54b2be8b2bb0e28cee3fee76f4508585354522b55a`  
		Last Modified: Tue, 16 Apr 2024 06:31:22 GMT  
		Size: 680.5 KB (680550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b23b4e90351e0ff53e0f246eb18f111157b19cd9e0227d3a7fd31c8a1a6a97`  
		Last Modified: Tue, 16 Apr 2024 06:31:20 GMT  
		Size: 4.6 MB (4615259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f53ffd1138587b21bb7b0292d1f849469294ce7c37501746ea72511888875a1`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c8044662d106608fa49367eba1c6cb3b733befde6e3d90252404ddeb605105`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92c225ad89dfb7994b629d899d0659840118a9df3f88d6f90833728df55f8da`  
		Last Modified: Tue, 16 Apr 2024 06:31:38 GMT  
		Size: 123.2 MB (123218612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc76761a117e06aab729b9d28f67024b4728da9f2d627f871fb96c606e657567`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b6f4b1b2354371c3b3662f463dc6cea88bf654b1fcbfb21b79391736e633de`  
		Last Modified: Tue, 16 Apr 2024 06:32:02 GMT  
		Size: 114.4 MB (114384650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660034266ff49dea642e331c01516c78c452605d29ea904978898465cba6c041`  
		Last Modified: Tue, 16 Apr 2024 06:31:47 GMT  
		Size: 308.3 KB (308319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf5f31453040c4a6ec4d9aa45f377ca84e64ab9aadc50bb0f5bf265e4a50ec7`  
		Last Modified: Tue, 16 Apr 2024 06:31:47 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cac77dcdb816a2bf142cc9fd94c312e1e1aaacf48147b55c853774c1c62d40`  
		Last Modified: Tue, 16 Apr 2024 06:31:50 GMT  
		Size: 24.4 MB (24443788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4e69740ba09b1706be29844449e22b0006825b2ef9afcb606ca9c37d7ac125`  
		Last Modified: Tue, 16 Apr 2024 06:33:48 GMT  
		Size: 735.7 MB (735678045 bytes)  
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

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:f6f5745c356ea8c451fd1ae323968d7840a1301092164eb691980d188c632c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:2b4095ccbaa7b360055d1e33f65605db23a23b4c5c63d13667878b802f1e4063
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1033040266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ebe5f2366c7a7fd00ab88d976e433afc37e0f6112cfba9f9aaba137b9aee01`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:12:58 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:12:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:13:00 GMT
ADD file:86e27cbcb9656cd837a2abb01bc5989043c00e9d687476bf5efddfd851228eaf in / 
# Sun, 07 Apr 2024 17:13:00 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 06:11:17 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:11:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:11:35 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Tue, 16 Apr 2024 06:11:35 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 16 Apr 2024 06:11:35 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 06:11:36 GMT
ENV LC_ALL=C.UTF-8
# Tue, 16 Apr 2024 06:11:36 GMT
ENV ROS_DISTRO=rolling
# Tue, 16 Apr 2024 06:13:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:13:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 16 Apr 2024 06:13:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 16 Apr 2024 06:13:26 GMT
CMD ["bash"]
# Tue, 16 Apr 2024 06:14:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:14:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 16 Apr 2024 06:14:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 16 Apr 2024 06:15:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:22:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6174c5967d452dad6f4d36aaa2a180582ea28ff9feba01d4cb8e451d3b3cf9a5`  
		Last Modified: Tue, 16 Apr 2024 03:17:32 GMT  
		Size: 29.7 MB (29706077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b44e467bacfb7e6664cb54b2be8b2bb0e28cee3fee76f4508585354522b55a`  
		Last Modified: Tue, 16 Apr 2024 06:31:22 GMT  
		Size: 680.5 KB (680550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b23b4e90351e0ff53e0f246eb18f111157b19cd9e0227d3a7fd31c8a1a6a97`  
		Last Modified: Tue, 16 Apr 2024 06:31:20 GMT  
		Size: 4.6 MB (4615259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f53ffd1138587b21bb7b0292d1f849469294ce7c37501746ea72511888875a1`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c8044662d106608fa49367eba1c6cb3b733befde6e3d90252404ddeb605105`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92c225ad89dfb7994b629d899d0659840118a9df3f88d6f90833728df55f8da`  
		Last Modified: Tue, 16 Apr 2024 06:31:38 GMT  
		Size: 123.2 MB (123218612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc76761a117e06aab729b9d28f67024b4728da9f2d627f871fb96c606e657567`  
		Last Modified: Tue, 16 Apr 2024 06:31:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b6f4b1b2354371c3b3662f463dc6cea88bf654b1fcbfb21b79391736e633de`  
		Last Modified: Tue, 16 Apr 2024 06:32:02 GMT  
		Size: 114.4 MB (114384650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660034266ff49dea642e331c01516c78c452605d29ea904978898465cba6c041`  
		Last Modified: Tue, 16 Apr 2024 06:31:47 GMT  
		Size: 308.3 KB (308319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf5f31453040c4a6ec4d9aa45f377ca84e64ab9aadc50bb0f5bf265e4a50ec7`  
		Last Modified: Tue, 16 Apr 2024 06:31:47 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cac77dcdb816a2bf142cc9fd94c312e1e1aaacf48147b55c853774c1c62d40`  
		Last Modified: Tue, 16 Apr 2024 06:31:50 GMT  
		Size: 24.4 MB (24443788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4e69740ba09b1706be29844449e22b0006825b2ef9afcb606ca9c37d7ac125`  
		Last Modified: Tue, 16 Apr 2024 06:33:48 GMT  
		Size: 735.7 MB (735678045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:aac0381b54e368a27aa78f67996b34c3c246a5703d42415614f8d75d0b7d392f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:4f692bd459b8c069c95b1161b70c7012b6bd6d3f03d8da71d8fa0f36731ac630
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299699712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4feba4c47c41fdc1d74bf02589c7f5c8ad628bab02a9f507c9047c481a94a1e0`
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
# Fri, 26 Apr 2024 00:02:43 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 26 Apr 2024 00:02:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 26 Apr 2024 00:02:43 GMT
ENV LANG=C.UTF-8
# Fri, 26 Apr 2024 00:02:43 GMT
ENV LC_ALL=C.UTF-8
# Fri, 26 Apr 2024 00:02:44 GMT
ENV ROS_DISTRO=rolling
# Fri, 26 Apr 2024 00:04:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 00:04:33 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 26 Apr 2024 00:04:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Apr 2024 00:04:33 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 00:05:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 00:05:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 26 Apr 2024 00:05:55 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 26 Apr 2024 00:06:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a4d1f96a582d77e142a9372c219837cfe0f63629329a255baa7d24c420180aa8`  
		Last Modified: Fri, 26 Apr 2024 00:16:04 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5d59efebd94c99ec9df4d45496b0da2a6cf7b2c0cdf5d25b454fcb2e658edb`  
		Last Modified: Fri, 26 Apr 2024 00:16:04 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58520ddab8eb418ed7f39a6254a49b4bcfd80de215fa34ce34a9225fda76cfa1`  
		Last Modified: Fri, 26 Apr 2024 00:16:23 GMT  
		Size: 122.4 MB (122419667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d901e24f0b5da18df9a9856ebd15b74d91636de5681425f96f796b0b33eee6fa`  
		Last Modified: Fri, 26 Apr 2024 00:16:04 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0f6d3a4fe977861e43b66af02f2cb05ddf4dc2f1077710ce94e3e725465777`  
		Last Modified: Fri, 26 Apr 2024 00:16:48 GMT  
		Size: 114.3 MB (114304236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edda434a4d5818268d4c619a9bc04730867294dd2019473d6caddd71e839979`  
		Last Modified: Fri, 26 Apr 2024 00:16:32 GMT  
		Size: 308.4 KB (308383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74118983417a907cbd593804ea5005eac2b24de69f5a15beba9c617db19c4308`  
		Last Modified: Fri, 26 Apr 2024 00:16:32 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a05c6e33bf42de738f5c7251416ca858af547a21401340c42c8b7f81140638e`  
		Last Modified: Fri, 26 Apr 2024 00:16:36 GMT  
		Size: 27.7 MB (27664162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b5485704c32bf60c31f0ec40d821853c6ed2b02611b3e3a360191a7158bf4c4a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289834728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb6cb328d62b21ab96c04e4cd291c9db0394c18acf4b095a96ced1c229159b6`
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
# Thu, 25 Apr 2024 23:40:24 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:40:24 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:40:24 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:40:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:40:24 GMT
ENV ROS_DISTRO=rolling
# Thu, 25 Apr 2024 23:42:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:42:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:42:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:42:42 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:44:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:44:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:44:46 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 25 Apr 2024 23:45:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:e67f27bf0eb8d01126489b229cc3de66eaf05114f0e8b097ec3cc1f82c7323d3`  
		Last Modified: Thu, 25 Apr 2024 23:53:23 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96db453f945716348ca0ce9b78ef87efa36506cc0eb304b6a721f8c3f7546e5b`  
		Last Modified: Thu, 25 Apr 2024 23:53:24 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1aaa8c881c7ea864f1ba79d24492f21979b6f4ef00bd8cb560a7c8d1cf24429`  
		Last Modified: Thu, 25 Apr 2024 23:53:47 GMT  
		Size: 117.2 MB (117220954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef1a74238ed8c5ca9164c6237a3de769a1ae331f532e3238a73422d516ed5d0`  
		Last Modified: Thu, 25 Apr 2024 23:53:24 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d434bce647868d8c266b6795f1cf576c146632ec85d73151d57000a28c38e7d`  
		Last Modified: Thu, 25 Apr 2024 23:54:09 GMT  
		Size: 111.2 MB (111162364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faa2b1bdd0240ea2225a565cd568f6b9835fbed9898f687ec5448aa3d49c16e`  
		Last Modified: Thu, 25 Apr 2024 23:53:56 GMT  
		Size: 308.4 KB (308378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d7a7b9b224d77d659618adfdcda742e0be04485cc3a45df8fd75f0d487c6ed`  
		Last Modified: Thu, 25 Apr 2024 23:53:56 GMT  
		Size: 2.5 KB (2481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3f10187114ee79588a9e9161a26e3460e17b8e07d0f53cc9917f0887077936`  
		Last Modified: Thu, 25 Apr 2024 23:54:00 GMT  
		Size: 26.8 MB (26809287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:aac0381b54e368a27aa78f67996b34c3c246a5703d42415614f8d75d0b7d392f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:4f692bd459b8c069c95b1161b70c7012b6bd6d3f03d8da71d8fa0f36731ac630
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299699712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4feba4c47c41fdc1d74bf02589c7f5c8ad628bab02a9f507c9047c481a94a1e0`
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
# Fri, 26 Apr 2024 00:02:43 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 26 Apr 2024 00:02:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 26 Apr 2024 00:02:43 GMT
ENV LANG=C.UTF-8
# Fri, 26 Apr 2024 00:02:43 GMT
ENV LC_ALL=C.UTF-8
# Fri, 26 Apr 2024 00:02:44 GMT
ENV ROS_DISTRO=rolling
# Fri, 26 Apr 2024 00:04:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 00:04:33 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 26 Apr 2024 00:04:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Apr 2024 00:04:33 GMT
CMD ["bash"]
# Fri, 26 Apr 2024 00:05:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 00:05:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 26 Apr 2024 00:05:55 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 26 Apr 2024 00:06:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a4d1f96a582d77e142a9372c219837cfe0f63629329a255baa7d24c420180aa8`  
		Last Modified: Fri, 26 Apr 2024 00:16:04 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5d59efebd94c99ec9df4d45496b0da2a6cf7b2c0cdf5d25b454fcb2e658edb`  
		Last Modified: Fri, 26 Apr 2024 00:16:04 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58520ddab8eb418ed7f39a6254a49b4bcfd80de215fa34ce34a9225fda76cfa1`  
		Last Modified: Fri, 26 Apr 2024 00:16:23 GMT  
		Size: 122.4 MB (122419667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d901e24f0b5da18df9a9856ebd15b74d91636de5681425f96f796b0b33eee6fa`  
		Last Modified: Fri, 26 Apr 2024 00:16:04 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0f6d3a4fe977861e43b66af02f2cb05ddf4dc2f1077710ce94e3e725465777`  
		Last Modified: Fri, 26 Apr 2024 00:16:48 GMT  
		Size: 114.3 MB (114304236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edda434a4d5818268d4c619a9bc04730867294dd2019473d6caddd71e839979`  
		Last Modified: Fri, 26 Apr 2024 00:16:32 GMT  
		Size: 308.4 KB (308383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74118983417a907cbd593804ea5005eac2b24de69f5a15beba9c617db19c4308`  
		Last Modified: Fri, 26 Apr 2024 00:16:32 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a05c6e33bf42de738f5c7251416ca858af547a21401340c42c8b7f81140638e`  
		Last Modified: Fri, 26 Apr 2024 00:16:36 GMT  
		Size: 27.7 MB (27664162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b5485704c32bf60c31f0ec40d821853c6ed2b02611b3e3a360191a7158bf4c4a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289834728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb6cb328d62b21ab96c04e4cd291c9db0394c18acf4b095a96ced1c229159b6`
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
# Thu, 25 Apr 2024 23:40:24 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:40:24 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:40:24 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:40:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:40:24 GMT
ENV ROS_DISTRO=rolling
# Thu, 25 Apr 2024 23:42:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:42:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:42:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:42:42 GMT
CMD ["bash"]
# Thu, 25 Apr 2024 23:44:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:44:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 25 Apr 2024 23:44:46 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 25 Apr 2024 23:45:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:e67f27bf0eb8d01126489b229cc3de66eaf05114f0e8b097ec3cc1f82c7323d3`  
		Last Modified: Thu, 25 Apr 2024 23:53:23 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96db453f945716348ca0ce9b78ef87efa36506cc0eb304b6a721f8c3f7546e5b`  
		Last Modified: Thu, 25 Apr 2024 23:53:24 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1aaa8c881c7ea864f1ba79d24492f21979b6f4ef00bd8cb560a7c8d1cf24429`  
		Last Modified: Thu, 25 Apr 2024 23:53:47 GMT  
		Size: 117.2 MB (117220954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef1a74238ed8c5ca9164c6237a3de769a1ae331f532e3238a73422d516ed5d0`  
		Last Modified: Thu, 25 Apr 2024 23:53:24 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d434bce647868d8c266b6795f1cf576c146632ec85d73151d57000a28c38e7d`  
		Last Modified: Thu, 25 Apr 2024 23:54:09 GMT  
		Size: 111.2 MB (111162364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faa2b1bdd0240ea2225a565cd568f6b9835fbed9898f687ec5448aa3d49c16e`  
		Last Modified: Thu, 25 Apr 2024 23:53:56 GMT  
		Size: 308.4 KB (308378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d7a7b9b224d77d659618adfdcda742e0be04485cc3a45df8fd75f0d487c6ed`  
		Last Modified: Thu, 25 Apr 2024 23:53:56 GMT  
		Size: 2.5 KB (2481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3f10187114ee79588a9e9161a26e3460e17b8e07d0f53cc9917f0887077936`  
		Last Modified: Thu, 25 Apr 2024 23:54:00 GMT  
		Size: 26.8 MB (26809287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:49da26992fa549a1c9c581154076dbd6618c3d5d5475e1a0f6e6841b16a5a08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:8cea41e8048594171cd9ab0cc251c2d833d12657f45a7805740fa040a7d413d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157420423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8bb42ad1c8296633e0e30c976eb63cf011f02dee00b78954d7ba47ee6e5c948`
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
# Fri, 26 Apr 2024 00:02:43 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 26 Apr 2024 00:02:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 26 Apr 2024 00:02:43 GMT
ENV LANG=C.UTF-8
# Fri, 26 Apr 2024 00:02:43 GMT
ENV LC_ALL=C.UTF-8
# Fri, 26 Apr 2024 00:02:44 GMT
ENV ROS_DISTRO=rolling
# Fri, 26 Apr 2024 00:04:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 00:04:33 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 26 Apr 2024 00:04:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Apr 2024 00:04:33 GMT
CMD ["bash"]
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
	-	`sha256:a4d1f96a582d77e142a9372c219837cfe0f63629329a255baa7d24c420180aa8`  
		Last Modified: Fri, 26 Apr 2024 00:16:04 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5d59efebd94c99ec9df4d45496b0da2a6cf7b2c0cdf5d25b454fcb2e658edb`  
		Last Modified: Fri, 26 Apr 2024 00:16:04 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58520ddab8eb418ed7f39a6254a49b4bcfd80de215fa34ce34a9225fda76cfa1`  
		Last Modified: Fri, 26 Apr 2024 00:16:23 GMT  
		Size: 122.4 MB (122419667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d901e24f0b5da18df9a9856ebd15b74d91636de5681425f96f796b0b33eee6fa`  
		Last Modified: Fri, 26 Apr 2024 00:16:04 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:63f344d05e550961278e70af7c29c97ff452ea87660ed3c4cadb3870d8c3c318
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151552218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa575920bfdae9831d632e9c4e14a0a459f078417924d08a34395c7f665933e3`
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
# Thu, 25 Apr 2024 23:40:24 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:40:24 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:40:24 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:40:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:40:24 GMT
ENV ROS_DISTRO=rolling
# Thu, 25 Apr 2024 23:42:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:42:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:42:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:42:42 GMT
CMD ["bash"]
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
	-	`sha256:e67f27bf0eb8d01126489b229cc3de66eaf05114f0e8b097ec3cc1f82c7323d3`  
		Last Modified: Thu, 25 Apr 2024 23:53:23 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96db453f945716348ca0ce9b78ef87efa36506cc0eb304b6a721f8c3f7546e5b`  
		Last Modified: Thu, 25 Apr 2024 23:53:24 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1aaa8c881c7ea864f1ba79d24492f21979b6f4ef00bd8cb560a7c8d1cf24429`  
		Last Modified: Thu, 25 Apr 2024 23:53:47 GMT  
		Size: 117.2 MB (117220954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef1a74238ed8c5ca9164c6237a3de769a1ae331f532e3238a73422d516ed5d0`  
		Last Modified: Thu, 25 Apr 2024 23:53:24 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:49da26992fa549a1c9c581154076dbd6618c3d5d5475e1a0f6e6841b16a5a08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:8cea41e8048594171cd9ab0cc251c2d833d12657f45a7805740fa040a7d413d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157420423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8bb42ad1c8296633e0e30c976eb63cf011f02dee00b78954d7ba47ee6e5c948`
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
# Fri, 26 Apr 2024 00:02:43 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 26 Apr 2024 00:02:43 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 26 Apr 2024 00:02:43 GMT
ENV LANG=C.UTF-8
# Fri, 26 Apr 2024 00:02:43 GMT
ENV LC_ALL=C.UTF-8
# Fri, 26 Apr 2024 00:02:44 GMT
ENV ROS_DISTRO=rolling
# Fri, 26 Apr 2024 00:04:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 00:04:33 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 26 Apr 2024 00:04:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 26 Apr 2024 00:04:33 GMT
CMD ["bash"]
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
	-	`sha256:a4d1f96a582d77e142a9372c219837cfe0f63629329a255baa7d24c420180aa8`  
		Last Modified: Fri, 26 Apr 2024 00:16:04 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5d59efebd94c99ec9df4d45496b0da2a6cf7b2c0cdf5d25b454fcb2e658edb`  
		Last Modified: Fri, 26 Apr 2024 00:16:04 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58520ddab8eb418ed7f39a6254a49b4bcfd80de215fa34ce34a9225fda76cfa1`  
		Last Modified: Fri, 26 Apr 2024 00:16:23 GMT  
		Size: 122.4 MB (122419667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d901e24f0b5da18df9a9856ebd15b74d91636de5681425f96f796b0b33eee6fa`  
		Last Modified: Fri, 26 Apr 2024 00:16:04 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:63f344d05e550961278e70af7c29c97ff452ea87660ed3c4cadb3870d8c3c318
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151552218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa575920bfdae9831d632e9c4e14a0a459f078417924d08a34395c7f665933e3`
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
# Thu, 25 Apr 2024 23:40:24 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 25 Apr 2024 23:40:24 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 25 Apr 2024 23:40:24 GMT
ENV LANG=C.UTF-8
# Thu, 25 Apr 2024 23:40:24 GMT
ENV LC_ALL=C.UTF-8
# Thu, 25 Apr 2024 23:40:24 GMT
ENV ROS_DISTRO=rolling
# Thu, 25 Apr 2024 23:42:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:42:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 25 Apr 2024 23:42:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 25 Apr 2024 23:42:42 GMT
CMD ["bash"]
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
	-	`sha256:e67f27bf0eb8d01126489b229cc3de66eaf05114f0e8b097ec3cc1f82c7323d3`  
		Last Modified: Thu, 25 Apr 2024 23:53:23 GMT  
		Size: 2.0 KB (2023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96db453f945716348ca0ce9b78ef87efa36506cc0eb304b6a721f8c3f7546e5b`  
		Last Modified: Thu, 25 Apr 2024 23:53:24 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1aaa8c881c7ea864f1ba79d24492f21979b6f4ef00bd8cb560a7c8d1cf24429`  
		Last Modified: Thu, 25 Apr 2024 23:53:47 GMT  
		Size: 117.2 MB (117220954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef1a74238ed8c5ca9164c6237a3de769a1ae331f532e3238a73422d516ed5d0`  
		Last Modified: Thu, 25 Apr 2024 23:53:24 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
