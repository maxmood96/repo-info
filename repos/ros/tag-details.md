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
$ docker pull ros@sha256:d254bb722b9b490d3b71723dc2a55591170daad2851ad45e367114c211889120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:b5873864423bb6f669f32e4df4996e8647aeec3418ddec1ca4b440202ba2bb58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263557808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a28846ad48b383d0c7619dc85bdf0d956629acc770989a79c865fea416650bb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV ROS_DISTRO=humble
# Fri, 16 Feb 2024 02:32:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:32:21 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:32:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:32:21 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 02:33:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:33:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 02:33:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 02:34:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd46df5b586152474291f517cc5304c420d8f7f52e5604ceecb4f9f5ca2f73b5`  
		Last Modified: Fri, 16 Feb 2024 02:50:11 GMT  
		Size: 106.5 MB (106493044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06479915931fcc3b2eac705bbb368afe26bf9b7079ee628b10d388eb13cebd14`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6b578444c314f4183a82a2470575f2f6b399491d63e2059853bf6e7062c0f7`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 98.1 MB (98137779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0f945a0b34607bf2bb40053ff1689acf2902add4b2a1f3710126f236f08f4f`  
		Last Modified: Fri, 16 Feb 2024 02:50:19 GMT  
		Size: 328.8 KB (328773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac53ad1c8b6a3ed726b1c4ce440cb2e6ec03ea9c7567d839b434eb2189c3fdb`  
		Last Modified: Fri, 16 Feb 2024 02:50:19 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a94d8a09e4a010d92764ffd2d8ded04c3227ea1847236e217399bffb9329c26`  
		Last Modified: Fri, 16 Feb 2024 02:50:23 GMT  
		Size: 23.1 MB (23097854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5b530b78b01b3429d086b49a776dc4f5e6240677122d723b8211e6b46d73c471
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256170722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73b7994e5284da433bbaf5270f0a53664605479b33a7301cf7d3f9689d778a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV ROS_DISTRO=humble
# Fri, 16 Feb 2024 05:20:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:21:00 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:21:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:21:00 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 05:21:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:21:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 05:21:50 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 05:22:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4911c0776f2ae7fe89cd66c93d0756d78612a13c99e608d2d93c7e831c7e9e`  
		Last Modified: Fri, 16 Feb 2024 05:40:14 GMT  
		Size: 104.2 MB (104217966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b39b7ccfac9f954cfc61d6e781869a803f4824048f7d6672687e545e673a49`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e4f660e2ab4b30e946b77496f8b67fb109bbc6aa0dd1c153e3858e775535da`  
		Last Modified: Fri, 16 Feb 2024 05:40:35 GMT  
		Size: 95.7 MB (95684460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd33ff5103ddc8d8e2639b35aa6fdd477b18c2b6b7d47ec633524ebaefe79ed4`  
		Last Modified: Fri, 16 Feb 2024 05:40:23 GMT  
		Size: 328.8 KB (328775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779051c6b69728da04857f95ad57e73f3daacf073e2d9fa103e10ec2837f0465`  
		Last Modified: Fri, 16 Feb 2024 05:40:23 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0a04bef770df3e0e27ace254b6e3b47b7204042f28fe2a7bb975c5acf66bec`  
		Last Modified: Fri, 16 Feb 2024 05:40:27 GMT  
		Size: 22.5 MB (22517283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception`

```console
$ docker pull ros@sha256:8680d5b7d6d49f5276d1f999d759ebb6eacc1a6eff313b1d54c37b61537ddaf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:ba8a19ef1d06f526d73d34c16fea8e10eef62a419303560392d906d8699c815e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.7 MB (954733165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16b441586fd013fff7e9962ddfbe37be46ef99ac0a6b5407fddd828a79e95a1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV ROS_DISTRO=humble
# Fri, 16 Feb 2024 02:32:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:32:21 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:32:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:32:21 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 02:33:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:33:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 02:33:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 02:34:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:41:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd46df5b586152474291f517cc5304c420d8f7f52e5604ceecb4f9f5ca2f73b5`  
		Last Modified: Fri, 16 Feb 2024 02:50:11 GMT  
		Size: 106.5 MB (106493044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06479915931fcc3b2eac705bbb368afe26bf9b7079ee628b10d388eb13cebd14`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6b578444c314f4183a82a2470575f2f6b399491d63e2059853bf6e7062c0f7`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 98.1 MB (98137779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0f945a0b34607bf2bb40053ff1689acf2902add4b2a1f3710126f236f08f4f`  
		Last Modified: Fri, 16 Feb 2024 02:50:19 GMT  
		Size: 328.8 KB (328773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac53ad1c8b6a3ed726b1c4ce440cb2e6ec03ea9c7567d839b434eb2189c3fdb`  
		Last Modified: Fri, 16 Feb 2024 02:50:19 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a94d8a09e4a010d92764ffd2d8ded04c3227ea1847236e217399bffb9329c26`  
		Last Modified: Fri, 16 Feb 2024 02:50:23 GMT  
		Size: 23.1 MB (23097854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e7f6cd7c375e12f72fce012e71e2941b0af29d184ed6d78b942c9979d14dc0`  
		Last Modified: Fri, 16 Feb 2024 02:52:19 GMT  
		Size: 691.2 MB (691175357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5cd9796eb83ae11261bf4399ff122ea58469489eca7e58c9c0b4c0a2ea8744a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.3 MB (915255968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ad51b10dfd0201fff7233512760010cfb4e95b6497110ea2e5d7d12f8a90c0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV ROS_DISTRO=humble
# Fri, 16 Feb 2024 05:20:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:21:00 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:21:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:21:00 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 05:21:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:21:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 05:21:50 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 05:22:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:32:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4911c0776f2ae7fe89cd66c93d0756d78612a13c99e608d2d93c7e831c7e9e`  
		Last Modified: Fri, 16 Feb 2024 05:40:14 GMT  
		Size: 104.2 MB (104217966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b39b7ccfac9f954cfc61d6e781869a803f4824048f7d6672687e545e673a49`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e4f660e2ab4b30e946b77496f8b67fb109bbc6aa0dd1c153e3858e775535da`  
		Last Modified: Fri, 16 Feb 2024 05:40:35 GMT  
		Size: 95.7 MB (95684460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd33ff5103ddc8d8e2639b35aa6fdd477b18c2b6b7d47ec633524ebaefe79ed4`  
		Last Modified: Fri, 16 Feb 2024 05:40:23 GMT  
		Size: 328.8 KB (328775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779051c6b69728da04857f95ad57e73f3daacf073e2d9fa103e10ec2837f0465`  
		Last Modified: Fri, 16 Feb 2024 05:40:23 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0a04bef770df3e0e27ace254b6e3b47b7204042f28fe2a7bb975c5acf66bec`  
		Last Modified: Fri, 16 Feb 2024 05:40:27 GMT  
		Size: 22.5 MB (22517283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1e9c7f576a3f227b1bd51cc470bcc029eb6e80a8b033e00f51a0b42e5dd921`  
		Last Modified: Fri, 16 Feb 2024 05:42:11 GMT  
		Size: 659.1 MB (659085246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:8680d5b7d6d49f5276d1f999d759ebb6eacc1a6eff313b1d54c37b61537ddaf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:ba8a19ef1d06f526d73d34c16fea8e10eef62a419303560392d906d8699c815e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.7 MB (954733165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16b441586fd013fff7e9962ddfbe37be46ef99ac0a6b5407fddd828a79e95a1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV ROS_DISTRO=humble
# Fri, 16 Feb 2024 02:32:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:32:21 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:32:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:32:21 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 02:33:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:33:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 02:33:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 02:34:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:41:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd46df5b586152474291f517cc5304c420d8f7f52e5604ceecb4f9f5ca2f73b5`  
		Last Modified: Fri, 16 Feb 2024 02:50:11 GMT  
		Size: 106.5 MB (106493044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06479915931fcc3b2eac705bbb368afe26bf9b7079ee628b10d388eb13cebd14`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6b578444c314f4183a82a2470575f2f6b399491d63e2059853bf6e7062c0f7`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 98.1 MB (98137779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0f945a0b34607bf2bb40053ff1689acf2902add4b2a1f3710126f236f08f4f`  
		Last Modified: Fri, 16 Feb 2024 02:50:19 GMT  
		Size: 328.8 KB (328773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac53ad1c8b6a3ed726b1c4ce440cb2e6ec03ea9c7567d839b434eb2189c3fdb`  
		Last Modified: Fri, 16 Feb 2024 02:50:19 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a94d8a09e4a010d92764ffd2d8ded04c3227ea1847236e217399bffb9329c26`  
		Last Modified: Fri, 16 Feb 2024 02:50:23 GMT  
		Size: 23.1 MB (23097854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e7f6cd7c375e12f72fce012e71e2941b0af29d184ed6d78b942c9979d14dc0`  
		Last Modified: Fri, 16 Feb 2024 02:52:19 GMT  
		Size: 691.2 MB (691175357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5cd9796eb83ae11261bf4399ff122ea58469489eca7e58c9c0b4c0a2ea8744a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.3 MB (915255968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ad51b10dfd0201fff7233512760010cfb4e95b6497110ea2e5d7d12f8a90c0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV ROS_DISTRO=humble
# Fri, 16 Feb 2024 05:20:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:21:00 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:21:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:21:00 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 05:21:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:21:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 05:21:50 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 05:22:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:32:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4911c0776f2ae7fe89cd66c93d0756d78612a13c99e608d2d93c7e831c7e9e`  
		Last Modified: Fri, 16 Feb 2024 05:40:14 GMT  
		Size: 104.2 MB (104217966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b39b7ccfac9f954cfc61d6e781869a803f4824048f7d6672687e545e673a49`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e4f660e2ab4b30e946b77496f8b67fb109bbc6aa0dd1c153e3858e775535da`  
		Last Modified: Fri, 16 Feb 2024 05:40:35 GMT  
		Size: 95.7 MB (95684460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd33ff5103ddc8d8e2639b35aa6fdd477b18c2b6b7d47ec633524ebaefe79ed4`  
		Last Modified: Fri, 16 Feb 2024 05:40:23 GMT  
		Size: 328.8 KB (328775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779051c6b69728da04857f95ad57e73f3daacf073e2d9fa103e10ec2837f0465`  
		Last Modified: Fri, 16 Feb 2024 05:40:23 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0a04bef770df3e0e27ace254b6e3b47b7204042f28fe2a7bb975c5acf66bec`  
		Last Modified: Fri, 16 Feb 2024 05:40:27 GMT  
		Size: 22.5 MB (22517283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1e9c7f576a3f227b1bd51cc470bcc029eb6e80a8b033e00f51a0b42e5dd921`  
		Last Modified: Fri, 16 Feb 2024 05:42:11 GMT  
		Size: 659.1 MB (659085246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:d254bb722b9b490d3b71723dc2a55591170daad2851ad45e367114c211889120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:b5873864423bb6f669f32e4df4996e8647aeec3418ddec1ca4b440202ba2bb58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263557808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a28846ad48b383d0c7619dc85bdf0d956629acc770989a79c865fea416650bb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV ROS_DISTRO=humble
# Fri, 16 Feb 2024 02:32:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:32:21 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:32:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:32:21 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 02:33:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:33:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 02:33:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 02:34:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd46df5b586152474291f517cc5304c420d8f7f52e5604ceecb4f9f5ca2f73b5`  
		Last Modified: Fri, 16 Feb 2024 02:50:11 GMT  
		Size: 106.5 MB (106493044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06479915931fcc3b2eac705bbb368afe26bf9b7079ee628b10d388eb13cebd14`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6b578444c314f4183a82a2470575f2f6b399491d63e2059853bf6e7062c0f7`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 98.1 MB (98137779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0f945a0b34607bf2bb40053ff1689acf2902add4b2a1f3710126f236f08f4f`  
		Last Modified: Fri, 16 Feb 2024 02:50:19 GMT  
		Size: 328.8 KB (328773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac53ad1c8b6a3ed726b1c4ce440cb2e6ec03ea9c7567d839b434eb2189c3fdb`  
		Last Modified: Fri, 16 Feb 2024 02:50:19 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a94d8a09e4a010d92764ffd2d8ded04c3227ea1847236e217399bffb9329c26`  
		Last Modified: Fri, 16 Feb 2024 02:50:23 GMT  
		Size: 23.1 MB (23097854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5b530b78b01b3429d086b49a776dc4f5e6240677122d723b8211e6b46d73c471
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256170722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73b7994e5284da433bbaf5270f0a53664605479b33a7301cf7d3f9689d778a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV ROS_DISTRO=humble
# Fri, 16 Feb 2024 05:20:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:21:00 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:21:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:21:00 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 05:21:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:21:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 05:21:50 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 05:22:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4911c0776f2ae7fe89cd66c93d0756d78612a13c99e608d2d93c7e831c7e9e`  
		Last Modified: Fri, 16 Feb 2024 05:40:14 GMT  
		Size: 104.2 MB (104217966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b39b7ccfac9f954cfc61d6e781869a803f4824048f7d6672687e545e673a49`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e4f660e2ab4b30e946b77496f8b67fb109bbc6aa0dd1c153e3858e775535da`  
		Last Modified: Fri, 16 Feb 2024 05:40:35 GMT  
		Size: 95.7 MB (95684460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd33ff5103ddc8d8e2639b35aa6fdd477b18c2b6b7d47ec633524ebaefe79ed4`  
		Last Modified: Fri, 16 Feb 2024 05:40:23 GMT  
		Size: 328.8 KB (328775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779051c6b69728da04857f95ad57e73f3daacf073e2d9fa103e10ec2837f0465`  
		Last Modified: Fri, 16 Feb 2024 05:40:23 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0a04bef770df3e0e27ace254b6e3b47b7204042f28fe2a7bb975c5acf66bec`  
		Last Modified: Fri, 16 Feb 2024 05:40:27 GMT  
		Size: 22.5 MB (22517283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:d254bb722b9b490d3b71723dc2a55591170daad2851ad45e367114c211889120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:b5873864423bb6f669f32e4df4996e8647aeec3418ddec1ca4b440202ba2bb58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263557808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a28846ad48b383d0c7619dc85bdf0d956629acc770989a79c865fea416650bb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV ROS_DISTRO=humble
# Fri, 16 Feb 2024 02:32:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:32:21 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:32:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:32:21 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 02:33:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:33:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 02:33:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 02:34:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd46df5b586152474291f517cc5304c420d8f7f52e5604ceecb4f9f5ca2f73b5`  
		Last Modified: Fri, 16 Feb 2024 02:50:11 GMT  
		Size: 106.5 MB (106493044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06479915931fcc3b2eac705bbb368afe26bf9b7079ee628b10d388eb13cebd14`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6b578444c314f4183a82a2470575f2f6b399491d63e2059853bf6e7062c0f7`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 98.1 MB (98137779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0f945a0b34607bf2bb40053ff1689acf2902add4b2a1f3710126f236f08f4f`  
		Last Modified: Fri, 16 Feb 2024 02:50:19 GMT  
		Size: 328.8 KB (328773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac53ad1c8b6a3ed726b1c4ce440cb2e6ec03ea9c7567d839b434eb2189c3fdb`  
		Last Modified: Fri, 16 Feb 2024 02:50:19 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a94d8a09e4a010d92764ffd2d8ded04c3227ea1847236e217399bffb9329c26`  
		Last Modified: Fri, 16 Feb 2024 02:50:23 GMT  
		Size: 23.1 MB (23097854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5b530b78b01b3429d086b49a776dc4f5e6240677122d723b8211e6b46d73c471
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256170722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73b7994e5284da433bbaf5270f0a53664605479b33a7301cf7d3f9689d778a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV ROS_DISTRO=humble
# Fri, 16 Feb 2024 05:20:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:21:00 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:21:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:21:00 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 05:21:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:21:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 05:21:50 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 05:22:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4911c0776f2ae7fe89cd66c93d0756d78612a13c99e608d2d93c7e831c7e9e`  
		Last Modified: Fri, 16 Feb 2024 05:40:14 GMT  
		Size: 104.2 MB (104217966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b39b7ccfac9f954cfc61d6e781869a803f4824048f7d6672687e545e673a49`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e4f660e2ab4b30e946b77496f8b67fb109bbc6aa0dd1c153e3858e775535da`  
		Last Modified: Fri, 16 Feb 2024 05:40:35 GMT  
		Size: 95.7 MB (95684460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd33ff5103ddc8d8e2639b35aa6fdd477b18c2b6b7d47ec633524ebaefe79ed4`  
		Last Modified: Fri, 16 Feb 2024 05:40:23 GMT  
		Size: 328.8 KB (328775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779051c6b69728da04857f95ad57e73f3daacf073e2d9fa103e10ec2837f0465`  
		Last Modified: Fri, 16 Feb 2024 05:40:23 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0a04bef770df3e0e27ace254b6e3b47b7204042f28fe2a7bb975c5acf66bec`  
		Last Modified: Fri, 16 Feb 2024 05:40:27 GMT  
		Size: 22.5 MB (22517283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:474a2f02dc9e7a8cebd7bc85df96d41f3ecd91b301a694520bef519f18e86f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:f5911f0eb55091cfb2c2b217f335ee53d23ed05668454613b61bb635c5cc3b42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141990895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50272922e891659ea068ed97a247c4292688734ed04791bbf18c42fa82195ec`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV ROS_DISTRO=humble
# Fri, 16 Feb 2024 02:32:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:32:21 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:32:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:32:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd46df5b586152474291f517cc5304c420d8f7f52e5604ceecb4f9f5ca2f73b5`  
		Last Modified: Fri, 16 Feb 2024 02:50:11 GMT  
		Size: 106.5 MB (106493044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06479915931fcc3b2eac705bbb368afe26bf9b7079ee628b10d388eb13cebd14`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:647bea6d596533e9c6082289bb3d6af2ba33e61754c416f960d7e77c0f4e986a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137637702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f11146ddab35d6653e9884d95b73a03ac5ea938a4e0ce7f9d52c41fdc22d15`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV ROS_DISTRO=humble
# Fri, 16 Feb 2024 05:20:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:21:00 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:21:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:21:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4911c0776f2ae7fe89cd66c93d0756d78612a13c99e608d2d93c7e831c7e9e`  
		Last Modified: Fri, 16 Feb 2024 05:40:14 GMT  
		Size: 104.2 MB (104217966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b39b7ccfac9f954cfc61d6e781869a803f4824048f7d6672687e545e673a49`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:474a2f02dc9e7a8cebd7bc85df96d41f3ecd91b301a694520bef519f18e86f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:f5911f0eb55091cfb2c2b217f335ee53d23ed05668454613b61bb635c5cc3b42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141990895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50272922e891659ea068ed97a247c4292688734ed04791bbf18c42fa82195ec`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV ROS_DISTRO=humble
# Fri, 16 Feb 2024 02:32:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:32:21 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:32:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:32:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd46df5b586152474291f517cc5304c420d8f7f52e5604ceecb4f9f5ca2f73b5`  
		Last Modified: Fri, 16 Feb 2024 02:50:11 GMT  
		Size: 106.5 MB (106493044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06479915931fcc3b2eac705bbb368afe26bf9b7079ee628b10d388eb13cebd14`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:647bea6d596533e9c6082289bb3d6af2ba33e61754c416f960d7e77c0f4e986a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137637702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f11146ddab35d6653e9884d95b73a03ac5ea938a4e0ce7f9d52c41fdc22d15`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV ROS_DISTRO=humble
# Fri, 16 Feb 2024 05:20:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:21:00 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:21:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:21:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4911c0776f2ae7fe89cd66c93d0756d78612a13c99e608d2d93c7e831c7e9e`  
		Last Modified: Fri, 16 Feb 2024 05:40:14 GMT  
		Size: 104.2 MB (104217966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b39b7ccfac9f954cfc61d6e781869a803f4824048f7d6672687e545e673a49`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron`

```console
$ docker pull ros@sha256:085753761dc1376498dccfd95f97ff31fb76878726451e9a5ef27d7b741f8567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron` - linux; amd64

```console
$ docker pull ros@sha256:3b35abb12383053d56d083c71a79a00008591aba52e3244f07ac48c5b9c5bb3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268962226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b8b248050243f7430ea86fe37ebb761450a9a8e3f84d781ea05ef08c76411b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:42:07 GMT
ENV ROS_DISTRO=iron
# Fri, 16 Feb 2024 02:42:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:43:01 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:43:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:43:01 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 02:43:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:43:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 02:43:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 02:43:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64116f613b23c02909000a42e67e9be2cd684886af17a609ab67bc5d1a8190b8`  
		Last Modified: Fri, 16 Feb 2024 02:52:48 GMT  
		Size: 124.3 MB (124264870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943b642bdfd3e9e1483069ffba4a7090e364f2d29606904fbb9a26d3925c2964`  
		Last Modified: Fri, 16 Feb 2024 02:52:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177e592df8efe0984926f743e834f7746effd90d514f3d3851abe3044c8a61c0`  
		Last Modified: Fri, 16 Feb 2024 02:53:07 GMT  
		Size: 85.2 MB (85170370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82907e5ee200d3fc665288fc89fc9cf64841db34917726251c720cd2178de28`  
		Last Modified: Fri, 16 Feb 2024 02:52:57 GMT  
		Size: 295.4 KB (295426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62501b0855f8ce6c24c8e4011b811b0a788aa94b6bf9a2a64c672fb2dee59828`  
		Last Modified: Fri, 16 Feb 2024 02:52:57 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6846f1670ef3d1bc2c2f4ac35db04c584f6230744c631aac1531732b9eb6b3`  
		Last Modified: Fri, 16 Feb 2024 02:53:01 GMT  
		Size: 23.7 MB (23731179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eb5628c8ab3a85248456a3734cac09a58a7ffb8c1a1e0ed9e91b6744e540ab23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261398601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713e809b449bab3b6047d6d25eb24413f9742d43210d613868bd812ef74ece18`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:32:32 GMT
ENV ROS_DISTRO=iron
# Fri, 16 Feb 2024 05:33:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:33:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:33:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:33:26 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 05:33:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:33:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 05:33:58 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 05:34:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e207bf6d488de8bf4729e007d8eb9410b4b3a38a7c721829786658d178204f07`  
		Last Modified: Fri, 16 Feb 2024 05:42:41 GMT  
		Size: 121.7 MB (121717451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb71cb6cd71fe8fa2e2596589682998757cfdec8fc8da02644abb2d765f0252`  
		Last Modified: Fri, 16 Feb 2024 05:42:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bc779048061a71f1468d53a6c163fdfe916bb3394178b935cd72b13b5cfbf0`  
		Last Modified: Fri, 16 Feb 2024 05:42:58 GMT  
		Size: 82.8 MB (82844209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25527e451a1fe313ae426757e1658152f1cff6a3d0d8099e5b419bd5c9771452`  
		Last Modified: Fri, 16 Feb 2024 05:42:50 GMT  
		Size: 295.4 KB (295426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94efc4c25e34e2e5a67ab27e06262274ba4466c2f0f2c5e79436943fe6cfa0e0`  
		Last Modified: Fri, 16 Feb 2024 05:42:50 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234f1eff56417c7838f77bc1df18e31fe55a3588ebdef5395b13f3fcdeb61300`  
		Last Modified: Fri, 16 Feb 2024 05:42:53 GMT  
		Size: 23.1 MB (23119281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-perception`

```console
$ docker pull ros@sha256:37a589d8b29165533eb9b365a22f7cc6a02048dfbf6e5bbf943f6db35a3889d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception` - linux; amd64

```console
$ docker pull ros@sha256:b89df97dd9e57f60e44c3ed8e0555afbf2764d3323051784cb31c2535743c3f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.0 MB (961034771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34638ebbb65a9ff4294af75873c0076a46a3e6c0ab4defe346df6de3495ae411`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:42:07 GMT
ENV ROS_DISTRO=iron
# Fri, 16 Feb 2024 02:42:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:43:01 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:43:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:43:01 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 02:43:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:43:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 02:43:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 02:43:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:45:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64116f613b23c02909000a42e67e9be2cd684886af17a609ab67bc5d1a8190b8`  
		Last Modified: Fri, 16 Feb 2024 02:52:48 GMT  
		Size: 124.3 MB (124264870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943b642bdfd3e9e1483069ffba4a7090e364f2d29606904fbb9a26d3925c2964`  
		Last Modified: Fri, 16 Feb 2024 02:52:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177e592df8efe0984926f743e834f7746effd90d514f3d3851abe3044c8a61c0`  
		Last Modified: Fri, 16 Feb 2024 02:53:07 GMT  
		Size: 85.2 MB (85170370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82907e5ee200d3fc665288fc89fc9cf64841db34917726251c720cd2178de28`  
		Last Modified: Fri, 16 Feb 2024 02:52:57 GMT  
		Size: 295.4 KB (295426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62501b0855f8ce6c24c8e4011b811b0a788aa94b6bf9a2a64c672fb2dee59828`  
		Last Modified: Fri, 16 Feb 2024 02:52:57 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6846f1670ef3d1bc2c2f4ac35db04c584f6230744c631aac1531732b9eb6b3`  
		Last Modified: Fri, 16 Feb 2024 02:53:01 GMT  
		Size: 23.7 MB (23731179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b87fc794a6250d680bd9b7b58667af4784b595b7ff1a5911281ff89f9d5bad`  
		Last Modified: Fri, 16 Feb 2024 02:54:51 GMT  
		Size: 692.1 MB (692072545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d3f78400a14896ff5a2805afc40472c40ba3d882a6fca7d99982a6fb2bcce0b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.4 MB (921354929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0f5150263e592dc4d373e2693757906e86844edd536f4deb50785e7d67bfdc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:32:32 GMT
ENV ROS_DISTRO=iron
# Fri, 16 Feb 2024 05:33:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:33:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:33:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:33:26 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 05:33:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:33:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 05:33:58 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 05:34:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:35:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e207bf6d488de8bf4729e007d8eb9410b4b3a38a7c721829786658d178204f07`  
		Last Modified: Fri, 16 Feb 2024 05:42:41 GMT  
		Size: 121.7 MB (121717451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb71cb6cd71fe8fa2e2596589682998757cfdec8fc8da02644abb2d765f0252`  
		Last Modified: Fri, 16 Feb 2024 05:42:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bc779048061a71f1468d53a6c163fdfe916bb3394178b935cd72b13b5cfbf0`  
		Last Modified: Fri, 16 Feb 2024 05:42:58 GMT  
		Size: 82.8 MB (82844209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25527e451a1fe313ae426757e1658152f1cff6a3d0d8099e5b419bd5c9771452`  
		Last Modified: Fri, 16 Feb 2024 05:42:50 GMT  
		Size: 295.4 KB (295426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94efc4c25e34e2e5a67ab27e06262274ba4466c2f0f2c5e79436943fe6cfa0e0`  
		Last Modified: Fri, 16 Feb 2024 05:42:50 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234f1eff56417c7838f77bc1df18e31fe55a3588ebdef5395b13f3fcdeb61300`  
		Last Modified: Fri, 16 Feb 2024 05:42:53 GMT  
		Size: 23.1 MB (23119281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca27c0b368e44e2e47a4108ec308ac6773c88e26d409d337ba04f823d38759c7`  
		Last Modified: Fri, 16 Feb 2024 05:44:26 GMT  
		Size: 660.0 MB (659956328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:37a589d8b29165533eb9b365a22f7cc6a02048dfbf6e5bbf943f6db35a3889d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:b89df97dd9e57f60e44c3ed8e0555afbf2764d3323051784cb31c2535743c3f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.0 MB (961034771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34638ebbb65a9ff4294af75873c0076a46a3e6c0ab4defe346df6de3495ae411`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:42:07 GMT
ENV ROS_DISTRO=iron
# Fri, 16 Feb 2024 02:42:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:43:01 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:43:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:43:01 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 02:43:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:43:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 02:43:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 02:43:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:45:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64116f613b23c02909000a42e67e9be2cd684886af17a609ab67bc5d1a8190b8`  
		Last Modified: Fri, 16 Feb 2024 02:52:48 GMT  
		Size: 124.3 MB (124264870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943b642bdfd3e9e1483069ffba4a7090e364f2d29606904fbb9a26d3925c2964`  
		Last Modified: Fri, 16 Feb 2024 02:52:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177e592df8efe0984926f743e834f7746effd90d514f3d3851abe3044c8a61c0`  
		Last Modified: Fri, 16 Feb 2024 02:53:07 GMT  
		Size: 85.2 MB (85170370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82907e5ee200d3fc665288fc89fc9cf64841db34917726251c720cd2178de28`  
		Last Modified: Fri, 16 Feb 2024 02:52:57 GMT  
		Size: 295.4 KB (295426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62501b0855f8ce6c24c8e4011b811b0a788aa94b6bf9a2a64c672fb2dee59828`  
		Last Modified: Fri, 16 Feb 2024 02:52:57 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6846f1670ef3d1bc2c2f4ac35db04c584f6230744c631aac1531732b9eb6b3`  
		Last Modified: Fri, 16 Feb 2024 02:53:01 GMT  
		Size: 23.7 MB (23731179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b87fc794a6250d680bd9b7b58667af4784b595b7ff1a5911281ff89f9d5bad`  
		Last Modified: Fri, 16 Feb 2024 02:54:51 GMT  
		Size: 692.1 MB (692072545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d3f78400a14896ff5a2805afc40472c40ba3d882a6fca7d99982a6fb2bcce0b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.4 MB (921354929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0f5150263e592dc4d373e2693757906e86844edd536f4deb50785e7d67bfdc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:32:32 GMT
ENV ROS_DISTRO=iron
# Fri, 16 Feb 2024 05:33:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:33:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:33:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:33:26 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 05:33:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:33:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 05:33:58 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 05:34:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:35:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e207bf6d488de8bf4729e007d8eb9410b4b3a38a7c721829786658d178204f07`  
		Last Modified: Fri, 16 Feb 2024 05:42:41 GMT  
		Size: 121.7 MB (121717451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb71cb6cd71fe8fa2e2596589682998757cfdec8fc8da02644abb2d765f0252`  
		Last Modified: Fri, 16 Feb 2024 05:42:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bc779048061a71f1468d53a6c163fdfe916bb3394178b935cd72b13b5cfbf0`  
		Last Modified: Fri, 16 Feb 2024 05:42:58 GMT  
		Size: 82.8 MB (82844209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25527e451a1fe313ae426757e1658152f1cff6a3d0d8099e5b419bd5c9771452`  
		Last Modified: Fri, 16 Feb 2024 05:42:50 GMT  
		Size: 295.4 KB (295426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94efc4c25e34e2e5a67ab27e06262274ba4466c2f0f2c5e79436943fe6cfa0e0`  
		Last Modified: Fri, 16 Feb 2024 05:42:50 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234f1eff56417c7838f77bc1df18e31fe55a3588ebdef5395b13f3fcdeb61300`  
		Last Modified: Fri, 16 Feb 2024 05:42:53 GMT  
		Size: 23.1 MB (23119281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca27c0b368e44e2e47a4108ec308ac6773c88e26d409d337ba04f823d38759c7`  
		Last Modified: Fri, 16 Feb 2024 05:44:26 GMT  
		Size: 660.0 MB (659956328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-base`

```console
$ docker pull ros@sha256:085753761dc1376498dccfd95f97ff31fb76878726451e9a5ef27d7b741f8567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:3b35abb12383053d56d083c71a79a00008591aba52e3244f07ac48c5b9c5bb3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268962226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b8b248050243f7430ea86fe37ebb761450a9a8e3f84d781ea05ef08c76411b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:42:07 GMT
ENV ROS_DISTRO=iron
# Fri, 16 Feb 2024 02:42:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:43:01 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:43:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:43:01 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 02:43:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:43:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 02:43:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 02:43:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64116f613b23c02909000a42e67e9be2cd684886af17a609ab67bc5d1a8190b8`  
		Last Modified: Fri, 16 Feb 2024 02:52:48 GMT  
		Size: 124.3 MB (124264870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943b642bdfd3e9e1483069ffba4a7090e364f2d29606904fbb9a26d3925c2964`  
		Last Modified: Fri, 16 Feb 2024 02:52:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177e592df8efe0984926f743e834f7746effd90d514f3d3851abe3044c8a61c0`  
		Last Modified: Fri, 16 Feb 2024 02:53:07 GMT  
		Size: 85.2 MB (85170370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82907e5ee200d3fc665288fc89fc9cf64841db34917726251c720cd2178de28`  
		Last Modified: Fri, 16 Feb 2024 02:52:57 GMT  
		Size: 295.4 KB (295426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62501b0855f8ce6c24c8e4011b811b0a788aa94b6bf9a2a64c672fb2dee59828`  
		Last Modified: Fri, 16 Feb 2024 02:52:57 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6846f1670ef3d1bc2c2f4ac35db04c584f6230744c631aac1531732b9eb6b3`  
		Last Modified: Fri, 16 Feb 2024 02:53:01 GMT  
		Size: 23.7 MB (23731179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eb5628c8ab3a85248456a3734cac09a58a7ffb8c1a1e0ed9e91b6744e540ab23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261398601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713e809b449bab3b6047d6d25eb24413f9742d43210d613868bd812ef74ece18`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:32:32 GMT
ENV ROS_DISTRO=iron
# Fri, 16 Feb 2024 05:33:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:33:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:33:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:33:26 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 05:33:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:33:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 05:33:58 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 05:34:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e207bf6d488de8bf4729e007d8eb9410b4b3a38a7c721829786658d178204f07`  
		Last Modified: Fri, 16 Feb 2024 05:42:41 GMT  
		Size: 121.7 MB (121717451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb71cb6cd71fe8fa2e2596589682998757cfdec8fc8da02644abb2d765f0252`  
		Last Modified: Fri, 16 Feb 2024 05:42:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bc779048061a71f1468d53a6c163fdfe916bb3394178b935cd72b13b5cfbf0`  
		Last Modified: Fri, 16 Feb 2024 05:42:58 GMT  
		Size: 82.8 MB (82844209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25527e451a1fe313ae426757e1658152f1cff6a3d0d8099e5b419bd5c9771452`  
		Last Modified: Fri, 16 Feb 2024 05:42:50 GMT  
		Size: 295.4 KB (295426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94efc4c25e34e2e5a67ab27e06262274ba4466c2f0f2c5e79436943fe6cfa0e0`  
		Last Modified: Fri, 16 Feb 2024 05:42:50 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234f1eff56417c7838f77bc1df18e31fe55a3588ebdef5395b13f3fcdeb61300`  
		Last Modified: Fri, 16 Feb 2024 05:42:53 GMT  
		Size: 23.1 MB (23119281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:085753761dc1376498dccfd95f97ff31fb76878726451e9a5ef27d7b741f8567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:3b35abb12383053d56d083c71a79a00008591aba52e3244f07ac48c5b9c5bb3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268962226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b8b248050243f7430ea86fe37ebb761450a9a8e3f84d781ea05ef08c76411b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:42:07 GMT
ENV ROS_DISTRO=iron
# Fri, 16 Feb 2024 02:42:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:43:01 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:43:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:43:01 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 02:43:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:43:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 02:43:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 02:43:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64116f613b23c02909000a42e67e9be2cd684886af17a609ab67bc5d1a8190b8`  
		Last Modified: Fri, 16 Feb 2024 02:52:48 GMT  
		Size: 124.3 MB (124264870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943b642bdfd3e9e1483069ffba4a7090e364f2d29606904fbb9a26d3925c2964`  
		Last Modified: Fri, 16 Feb 2024 02:52:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177e592df8efe0984926f743e834f7746effd90d514f3d3851abe3044c8a61c0`  
		Last Modified: Fri, 16 Feb 2024 02:53:07 GMT  
		Size: 85.2 MB (85170370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82907e5ee200d3fc665288fc89fc9cf64841db34917726251c720cd2178de28`  
		Last Modified: Fri, 16 Feb 2024 02:52:57 GMT  
		Size: 295.4 KB (295426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62501b0855f8ce6c24c8e4011b811b0a788aa94b6bf9a2a64c672fb2dee59828`  
		Last Modified: Fri, 16 Feb 2024 02:52:57 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6846f1670ef3d1bc2c2f4ac35db04c584f6230744c631aac1531732b9eb6b3`  
		Last Modified: Fri, 16 Feb 2024 02:53:01 GMT  
		Size: 23.7 MB (23731179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eb5628c8ab3a85248456a3734cac09a58a7ffb8c1a1e0ed9e91b6744e540ab23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261398601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713e809b449bab3b6047d6d25eb24413f9742d43210d613868bd812ef74ece18`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:32:32 GMT
ENV ROS_DISTRO=iron
# Fri, 16 Feb 2024 05:33:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:33:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:33:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:33:26 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 05:33:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:33:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 05:33:58 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 05:34:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e207bf6d488de8bf4729e007d8eb9410b4b3a38a7c721829786658d178204f07`  
		Last Modified: Fri, 16 Feb 2024 05:42:41 GMT  
		Size: 121.7 MB (121717451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb71cb6cd71fe8fa2e2596589682998757cfdec8fc8da02644abb2d765f0252`  
		Last Modified: Fri, 16 Feb 2024 05:42:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bc779048061a71f1468d53a6c163fdfe916bb3394178b935cd72b13b5cfbf0`  
		Last Modified: Fri, 16 Feb 2024 05:42:58 GMT  
		Size: 82.8 MB (82844209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25527e451a1fe313ae426757e1658152f1cff6a3d0d8099e5b419bd5c9771452`  
		Last Modified: Fri, 16 Feb 2024 05:42:50 GMT  
		Size: 295.4 KB (295426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94efc4c25e34e2e5a67ab27e06262274ba4466c2f0f2c5e79436943fe6cfa0e0`  
		Last Modified: Fri, 16 Feb 2024 05:42:50 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234f1eff56417c7838f77bc1df18e31fe55a3588ebdef5395b13f3fcdeb61300`  
		Last Modified: Fri, 16 Feb 2024 05:42:53 GMT  
		Size: 23.1 MB (23119281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:248d07fd92c42fc52a06c531b3da6f53a99369b840c8672524a95c0d1d988174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:71f4ef9c9d6a965ff1dec8ce2a33ca5e28883bd7a3904f77f0cfd23b139bb47c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159762720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb784a6a0e1ec07db33d34a932ab18279bb4d7ae0744bc18364a9a99324255e6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:42:07 GMT
ENV ROS_DISTRO=iron
# Fri, 16 Feb 2024 02:42:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:43:01 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:43:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:43:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64116f613b23c02909000a42e67e9be2cd684886af17a609ab67bc5d1a8190b8`  
		Last Modified: Fri, 16 Feb 2024 02:52:48 GMT  
		Size: 124.3 MB (124264870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943b642bdfd3e9e1483069ffba4a7090e364f2d29606904fbb9a26d3925c2964`  
		Last Modified: Fri, 16 Feb 2024 02:52:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:88c6ac71500727b61fc002f004078bff1512b059f3caf3dc2a6f86fd01872973
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155137186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326c8cfea7c02414de6b67437a2bf2c01df8bfeb28070e270188f0b5e05396b7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:32:32 GMT
ENV ROS_DISTRO=iron
# Fri, 16 Feb 2024 05:33:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:33:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:33:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:33:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e207bf6d488de8bf4729e007d8eb9410b4b3a38a7c721829786658d178204f07`  
		Last Modified: Fri, 16 Feb 2024 05:42:41 GMT  
		Size: 121.7 MB (121717451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb71cb6cd71fe8fa2e2596589682998757cfdec8fc8da02644abb2d765f0252`  
		Last Modified: Fri, 16 Feb 2024 05:42:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-core-jammy`

```console
$ docker pull ros@sha256:248d07fd92c42fc52a06c531b3da6f53a99369b840c8672524a95c0d1d988174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:71f4ef9c9d6a965ff1dec8ce2a33ca5e28883bd7a3904f77f0cfd23b139bb47c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159762720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb784a6a0e1ec07db33d34a932ab18279bb4d7ae0744bc18364a9a99324255e6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:42:07 GMT
ENV ROS_DISTRO=iron
# Fri, 16 Feb 2024 02:42:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:43:01 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:43:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:43:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64116f613b23c02909000a42e67e9be2cd684886af17a609ab67bc5d1a8190b8`  
		Last Modified: Fri, 16 Feb 2024 02:52:48 GMT  
		Size: 124.3 MB (124264870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943b642bdfd3e9e1483069ffba4a7090e364f2d29606904fbb9a26d3925c2964`  
		Last Modified: Fri, 16 Feb 2024 02:52:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:88c6ac71500727b61fc002f004078bff1512b059f3caf3dc2a6f86fd01872973
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155137186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326c8cfea7c02414de6b67437a2bf2c01df8bfeb28070e270188f0b5e05396b7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:32:32 GMT
ENV ROS_DISTRO=iron
# Fri, 16 Feb 2024 05:33:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:33:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:33:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:33:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e207bf6d488de8bf4729e007d8eb9410b4b3a38a7c721829786658d178204f07`  
		Last Modified: Fri, 16 Feb 2024 05:42:41 GMT  
		Size: 121.7 MB (121717451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb71cb6cd71fe8fa2e2596589682998757cfdec8fc8da02644abb2d765f0252`  
		Last Modified: Fri, 16 Feb 2024 05:42:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:latest`

```console
$ docker pull ros@sha256:d254bb722b9b490d3b71723dc2a55591170daad2851ad45e367114c211889120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:b5873864423bb6f669f32e4df4996e8647aeec3418ddec1ca4b440202ba2bb58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263557808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a28846ad48b383d0c7619dc85bdf0d956629acc770989a79c865fea416650bb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV ROS_DISTRO=humble
# Fri, 16 Feb 2024 02:32:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:32:21 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:32:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:32:21 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 02:33:00 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:33:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 02:33:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 02:34:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd46df5b586152474291f517cc5304c420d8f7f52e5604ceecb4f9f5ca2f73b5`  
		Last Modified: Fri, 16 Feb 2024 02:50:11 GMT  
		Size: 106.5 MB (106493044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06479915931fcc3b2eac705bbb368afe26bf9b7079ee628b10d388eb13cebd14`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6b578444c314f4183a82a2470575f2f6b399491d63e2059853bf6e7062c0f7`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 98.1 MB (98137779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0f945a0b34607bf2bb40053ff1689acf2902add4b2a1f3710126f236f08f4f`  
		Last Modified: Fri, 16 Feb 2024 02:50:19 GMT  
		Size: 328.8 KB (328773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac53ad1c8b6a3ed726b1c4ce440cb2e6ec03ea9c7567d839b434eb2189c3fdb`  
		Last Modified: Fri, 16 Feb 2024 02:50:19 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a94d8a09e4a010d92764ffd2d8ded04c3227ea1847236e217399bffb9329c26`  
		Last Modified: Fri, 16 Feb 2024 02:50:23 GMT  
		Size: 23.1 MB (23097854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5b530b78b01b3429d086b49a776dc4f5e6240677122d723b8211e6b46d73c471
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256170722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73b7994e5284da433bbaf5270f0a53664605479b33a7301cf7d3f9689d778a7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV ROS_DISTRO=humble
# Fri, 16 Feb 2024 05:20:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:21:00 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:21:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:21:00 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 05:21:39 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:21:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 05:21:50 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 05:22:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4911c0776f2ae7fe89cd66c93d0756d78612a13c99e608d2d93c7e831c7e9e`  
		Last Modified: Fri, 16 Feb 2024 05:40:14 GMT  
		Size: 104.2 MB (104217966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b39b7ccfac9f954cfc61d6e781869a803f4824048f7d6672687e545e673a49`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e4f660e2ab4b30e946b77496f8b67fb109bbc6aa0dd1c153e3858e775535da`  
		Last Modified: Fri, 16 Feb 2024 05:40:35 GMT  
		Size: 95.7 MB (95684460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd33ff5103ddc8d8e2639b35aa6fdd477b18c2b6b7d47ec633524ebaefe79ed4`  
		Last Modified: Fri, 16 Feb 2024 05:40:23 GMT  
		Size: 328.8 KB (328775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779051c6b69728da04857f95ad57e73f3daacf073e2d9fa103e10ec2837f0465`  
		Last Modified: Fri, 16 Feb 2024 05:40:23 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0a04bef770df3e0e27ace254b6e3b47b7204042f28fe2a7bb975c5acf66bec`  
		Last Modified: Fri, 16 Feb 2024 05:40:27 GMT  
		Size: 22.5 MB (22517283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic`

```console
$ docker pull ros@sha256:0e9073076550b1deffe45dc34b1baba0780e0778c5d0d053603951773dc12f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:41a0aad743d47e08bec68cf48005706c27a3d7aad10632d204cada99ef3642b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264703234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01ea3953302a6e2a2f91d97e3176d5d13cf3f90bee0b275851f6ac905a51480`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:47:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:47:22 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 02:47:22 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:47:22 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 02:47:22 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 02:49:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:49:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 02:49:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 02:49:43 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:50:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:50:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 02:50:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a0eff542a051aae29e565a80741d3a7b4cd98c32b2ee71ee5e65db2ea8339`  
		Last Modified: Fri, 02 Feb 2024 03:17:20 GMT  
		Size: 1.2 MB (1201927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3571ddcbb373955cce83c06caec6194bba015787cf70532a40f372ad0cfc4909`  
		Last Modified: Fri, 02 Feb 2024 03:17:19 GMT  
		Size: 5.6 MB (5553822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e738e3b521cc9f5634c723d391d85a3a5b9569b3d553421368380ec4b0582e`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5112e8bfde9264cec5c34ecd6175fa4701bc99b5ff0aebeb55286a24376bf0a7`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04476a0b14995e64a377f43280d3fc9f658e1f4005cd08626ea0bd7b8d76a151`  
		Last Modified: Fri, 02 Feb 2024 03:17:45 GMT  
		Size: 177.0 MB (176973755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aabb9a5c8e0fca47efaaf6ca15b59dee3873ec14b91c8ddd10726f63a82f48`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024be12c4ffd4a149d28e31d958bc58069c42db5afb0cd99622d76e3e567d07d`  
		Last Modified: Fri, 02 Feb 2024 03:18:01 GMT  
		Size: 50.9 MB (50942122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc791a8924c8665d0f658cbb906ef7da28971a46346f6e0506615abbbf4f10f5`  
		Last Modified: Fri, 02 Feb 2024 03:17:54 GMT  
		Size: 313.9 KB (313919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4e64ce06ce76c1990596e84ebbdb5bd709437b2d9d8bd557617c4b324a27b6`  
		Last Modified: Fri, 02 Feb 2024 03:17:54 GMT  
		Size: 1.1 MB (1130740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:26ec5db8714303c05d81e84567def32b1f7a41259b032af2ef9ed24d36caa222
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229825558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077a1be6f057e887d3741768be12841f0ff517475725c4fa447087fca8861d33`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:13:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:13:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:13:49 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 00:13:50 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 00:13:50 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 00:13:50 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 00:13:50 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 00:16:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:16:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 00:16:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 00:16:05 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:16:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:16:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 00:16:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93eb4c358a70eb4dc4f48209013d08987bf6c1a559df5adba7fc713ba9fc0bf7`  
		Last Modified: Thu, 25 Jan 2024 21:04:32 GMT  
		Size: 24.6 MB (24602341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b7f4d695b13df91b2e25dfb78289b3e42569d62b0797c47d012e7b28a4272f`  
		Last Modified: Fri, 02 Feb 2024 00:26:00 GMT  
		Size: 1.2 MB (1201866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7a566271693a24f462f1117821fdcc4a23cc64f686c845f89a05db132f75aa`  
		Last Modified: Fri, 02 Feb 2024 00:25:59 GMT  
		Size: 4.7 MB (4679249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d909a7e301dd4ccde1c83536b0c3894584dddb57bb4bba6c4aebea359488481`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2ce71c763b5dba0bb0f09e80c70a9430e62efee12ea01c91b900c82cf1de54`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1990aaec86a85bea7c5dab838a1699738f59db5b330181a2539eb7d3d6da4829`  
		Last Modified: Fri, 02 Feb 2024 00:26:26 GMT  
		Size: 157.5 MB (157460405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207b3e1bcaf5adbee8554fece6a2e8e149fbb2bac7a0e144ab02ccf9b7579e3`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f14aa3c10e2086f72ed556eda8d19460fc5d82b83b1907928a09f36a4164d5`  
		Last Modified: Fri, 02 Feb 2024 00:26:41 GMT  
		Size: 40.5 MB (40504147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb38a6164e77c6851bc201aaeccf8c3fb2232a434cc5c76191bdc9d9220925c`  
		Last Modified: Fri, 02 Feb 2024 00:26:35 GMT  
		Size: 313.9 KB (313921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f1f3a607ddd355114411ed00b9b5d84628f9b5d9983316fdd11cf697833b61`  
		Last Modified: Fri, 02 Feb 2024 00:26:35 GMT  
		Size: 1.1 MB (1061142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ea77a409e77dc685cc6f7afce25cc7d0c9d1b13dc4b7b34afaeb7867a15ee646
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251988690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d439934e28b7cd08d1dd54db338ce1cb0cf22971131b27801cf6440d8265a7c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:38:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:38:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:38:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:38:47 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 02:38:47 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:38:47 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 02:38:48 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 02:41:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:41:26 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 02:41:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 02:41:26 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:41:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:42:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 02:42:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438b6b7c23286db8dea96cdf7072080a74f406ba4a7410eef9c9f9641523383b`  
		Last Modified: Fri, 02 Feb 2024 03:11:58 GMT  
		Size: 1.2 MB (1201863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a1f0f6848253a24ff4febd2c0b176fbbd1da89e23ec1a09694ebe3cba1cb98`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 5.5 MB (5532029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e614d2391d60a20ea55e27fc4757f6bf1feab494316071f49ab45c581638cb50`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807e86654c3f9af8fbc24df5a78c74fe5269aad2fd964c5428210f0cb4234b38`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cdec50b2982f5dbf33f29c7fb41a1400458bb10cf566abe5c73ba9857b3b50`  
		Last Modified: Fri, 02 Feb 2024 03:12:30 GMT  
		Size: 171.4 MB (171411451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddde60dd4677c9a8031ea604fe475f07800a88ff8dd76656c7424482ff09cc9d`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c611c5a97cbf0cdf9e83341151f6e4e327d36f5f1ec0a3ffffca3ad32b90b6`  
		Last Modified: Fri, 02 Feb 2024 03:12:44 GMT  
		Size: 45.2 MB (45207021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9018935407b2aa0321010be3e88629c37577aca47c2cc6fa04fbcee72458f4`  
		Last Modified: Fri, 02 Feb 2024 03:12:39 GMT  
		Size: 313.9 KB (313926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df260141e23ac900edc232c7425584d8b241f1d4a8e53d7db1c3ddbc57ab044`  
		Last Modified: Fri, 02 Feb 2024 03:12:39 GMT  
		Size: 1.1 MB (1114853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:2c148353584102ee7991e9e5b00480c64549b3861704569466e89505cce4fe02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:bd001e6c1caade1e9e6c9b113b27c8cf357ef9521e4f07c03bc3193768f70f5f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.2 MB (835191775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3094361c2b747dfde1632ee2f4628bfad5c2998162e6900fa9598c48993a50`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:47:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:47:22 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 02:47:22 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:47:22 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 02:47:22 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 02:49:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:49:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 02:49:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 02:49:43 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:50:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:50:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 02:50:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:58:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a0eff542a051aae29e565a80741d3a7b4cd98c32b2ee71ee5e65db2ea8339`  
		Last Modified: Fri, 02 Feb 2024 03:17:20 GMT  
		Size: 1.2 MB (1201927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3571ddcbb373955cce83c06caec6194bba015787cf70532a40f372ad0cfc4909`  
		Last Modified: Fri, 02 Feb 2024 03:17:19 GMT  
		Size: 5.6 MB (5553822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e738e3b521cc9f5634c723d391d85a3a5b9569b3d553421368380ec4b0582e`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5112e8bfde9264cec5c34ecd6175fa4701bc99b5ff0aebeb55286a24376bf0a7`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04476a0b14995e64a377f43280d3fc9f658e1f4005cd08626ea0bd7b8d76a151`  
		Last Modified: Fri, 02 Feb 2024 03:17:45 GMT  
		Size: 177.0 MB (176973755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aabb9a5c8e0fca47efaaf6ca15b59dee3873ec14b91c8ddd10726f63a82f48`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024be12c4ffd4a149d28e31d958bc58069c42db5afb0cd99622d76e3e567d07d`  
		Last Modified: Fri, 02 Feb 2024 03:18:01 GMT  
		Size: 50.9 MB (50942122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc791a8924c8665d0f658cbb906ef7da28971a46346f6e0506615abbbf4f10f5`  
		Last Modified: Fri, 02 Feb 2024 03:17:54 GMT  
		Size: 313.9 KB (313919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4e64ce06ce76c1990596e84ebbdb5bd709437b2d9d8bd557617c4b324a27b6`  
		Last Modified: Fri, 02 Feb 2024 03:17:54 GMT  
		Size: 1.1 MB (1130740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d296db1c4147b052044e176bc981e70533ef30f7d4fb898c04660e4c4b70c8`  
		Last Modified: Fri, 02 Feb 2024 03:19:42 GMT  
		Size: 570.5 MB (570488541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:8116a2ec3393b0b10dca954cedda9f8365cc5fb9337a2e99ddb9b4039c06325a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.2 MB (726198513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b01c33a81a2eb5710e8e3b8733ca3f43835f6c7860dc7cb64ffd4a99051b65`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:13:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:13:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:13:49 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 00:13:50 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 00:13:50 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 00:13:50 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 00:13:50 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 00:16:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:16:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 00:16:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 00:16:05 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:16:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:16:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 00:16:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:25:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93eb4c358a70eb4dc4f48209013d08987bf6c1a559df5adba7fc713ba9fc0bf7`  
		Last Modified: Thu, 25 Jan 2024 21:04:32 GMT  
		Size: 24.6 MB (24602341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b7f4d695b13df91b2e25dfb78289b3e42569d62b0797c47d012e7b28a4272f`  
		Last Modified: Fri, 02 Feb 2024 00:26:00 GMT  
		Size: 1.2 MB (1201866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7a566271693a24f462f1117821fdcc4a23cc64f686c845f89a05db132f75aa`  
		Last Modified: Fri, 02 Feb 2024 00:25:59 GMT  
		Size: 4.7 MB (4679249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d909a7e301dd4ccde1c83536b0c3894584dddb57bb4bba6c4aebea359488481`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2ce71c763b5dba0bb0f09e80c70a9430e62efee12ea01c91b900c82cf1de54`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1990aaec86a85bea7c5dab838a1699738f59db5b330181a2539eb7d3d6da4829`  
		Last Modified: Fri, 02 Feb 2024 00:26:26 GMT  
		Size: 157.5 MB (157460405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207b3e1bcaf5adbee8554fece6a2e8e149fbb2bac7a0e144ab02ccf9b7579e3`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f14aa3c10e2086f72ed556eda8d19460fc5d82b83b1907928a09f36a4164d5`  
		Last Modified: Fri, 02 Feb 2024 00:26:41 GMT  
		Size: 40.5 MB (40504147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb38a6164e77c6851bc201aaeccf8c3fb2232a434cc5c76191bdc9d9220925c`  
		Last Modified: Fri, 02 Feb 2024 00:26:35 GMT  
		Size: 313.9 KB (313921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f1f3a607ddd355114411ed00b9b5d84628f9b5d9983316fdd11cf697833b61`  
		Last Modified: Fri, 02 Feb 2024 00:26:35 GMT  
		Size: 1.1 MB (1061142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1055a8b31ee9456fbc9755c48f94ce23fc267bf488bc15ea829546c767aa0281`  
		Last Modified: Fri, 02 Feb 2024 00:28:12 GMT  
		Size: 496.4 MB (496372955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:592dc254833f8aca88a2637371bf3761c4803aa4a293694c9645ae7c78d9ce47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.5 MB (785478217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e8a46d9370a9f5bbe88a2218ed403e1b81b69516011699c34e2fe8df54191b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:38:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:38:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:38:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:38:47 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 02:38:47 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:38:47 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 02:38:48 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 02:41:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:41:26 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 02:41:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 02:41:26 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:41:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:42:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 02:42:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:51:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438b6b7c23286db8dea96cdf7072080a74f406ba4a7410eef9c9f9641523383b`  
		Last Modified: Fri, 02 Feb 2024 03:11:58 GMT  
		Size: 1.2 MB (1201863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a1f0f6848253a24ff4febd2c0b176fbbd1da89e23ec1a09694ebe3cba1cb98`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 5.5 MB (5532029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e614d2391d60a20ea55e27fc4757f6bf1feab494316071f49ab45c581638cb50`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807e86654c3f9af8fbc24df5a78c74fe5269aad2fd964c5428210f0cb4234b38`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cdec50b2982f5dbf33f29c7fb41a1400458bb10cf566abe5c73ba9857b3b50`  
		Last Modified: Fri, 02 Feb 2024 03:12:30 GMT  
		Size: 171.4 MB (171411451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddde60dd4677c9a8031ea604fe475f07800a88ff8dd76656c7424482ff09cc9d`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c611c5a97cbf0cdf9e83341151f6e4e327d36f5f1ec0a3ffffca3ad32b90b6`  
		Last Modified: Fri, 02 Feb 2024 03:12:44 GMT  
		Size: 45.2 MB (45207021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9018935407b2aa0321010be3e88629c37577aca47c2cc6fa04fbcee72458f4`  
		Last Modified: Fri, 02 Feb 2024 03:12:39 GMT  
		Size: 313.9 KB (313926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df260141e23ac900edc232c7425584d8b241f1d4a8e53d7db1c3ddbc57ab044`  
		Last Modified: Fri, 02 Feb 2024 03:12:39 GMT  
		Size: 1.1 MB (1114853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367843c93cc0c093c415056cd200d5951983cdf6a6f6b157323718a00d486498`  
		Last Modified: Fri, 02 Feb 2024 03:14:17 GMT  
		Size: 533.5 MB (533489527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:2c148353584102ee7991e9e5b00480c64549b3861704569466e89505cce4fe02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:bd001e6c1caade1e9e6c9b113b27c8cf357ef9521e4f07c03bc3193768f70f5f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.2 MB (835191775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3094361c2b747dfde1632ee2f4628bfad5c2998162e6900fa9598c48993a50`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:47:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:47:22 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 02:47:22 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:47:22 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 02:47:22 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 02:49:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:49:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 02:49:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 02:49:43 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:50:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:50:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 02:50:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:58:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a0eff542a051aae29e565a80741d3a7b4cd98c32b2ee71ee5e65db2ea8339`  
		Last Modified: Fri, 02 Feb 2024 03:17:20 GMT  
		Size: 1.2 MB (1201927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3571ddcbb373955cce83c06caec6194bba015787cf70532a40f372ad0cfc4909`  
		Last Modified: Fri, 02 Feb 2024 03:17:19 GMT  
		Size: 5.6 MB (5553822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e738e3b521cc9f5634c723d391d85a3a5b9569b3d553421368380ec4b0582e`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5112e8bfde9264cec5c34ecd6175fa4701bc99b5ff0aebeb55286a24376bf0a7`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04476a0b14995e64a377f43280d3fc9f658e1f4005cd08626ea0bd7b8d76a151`  
		Last Modified: Fri, 02 Feb 2024 03:17:45 GMT  
		Size: 177.0 MB (176973755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aabb9a5c8e0fca47efaaf6ca15b59dee3873ec14b91c8ddd10726f63a82f48`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024be12c4ffd4a149d28e31d958bc58069c42db5afb0cd99622d76e3e567d07d`  
		Last Modified: Fri, 02 Feb 2024 03:18:01 GMT  
		Size: 50.9 MB (50942122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc791a8924c8665d0f658cbb906ef7da28971a46346f6e0506615abbbf4f10f5`  
		Last Modified: Fri, 02 Feb 2024 03:17:54 GMT  
		Size: 313.9 KB (313919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4e64ce06ce76c1990596e84ebbdb5bd709437b2d9d8bd557617c4b324a27b6`  
		Last Modified: Fri, 02 Feb 2024 03:17:54 GMT  
		Size: 1.1 MB (1130740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d296db1c4147b052044e176bc981e70533ef30f7d4fb898c04660e4c4b70c8`  
		Last Modified: Fri, 02 Feb 2024 03:19:42 GMT  
		Size: 570.5 MB (570488541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:8116a2ec3393b0b10dca954cedda9f8365cc5fb9337a2e99ddb9b4039c06325a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.2 MB (726198513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b01c33a81a2eb5710e8e3b8733ca3f43835f6c7860dc7cb64ffd4a99051b65`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:13:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:13:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:13:49 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 00:13:50 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 00:13:50 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 00:13:50 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 00:13:50 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 00:16:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:16:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 00:16:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 00:16:05 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:16:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:16:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 00:16:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:25:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93eb4c358a70eb4dc4f48209013d08987bf6c1a559df5adba7fc713ba9fc0bf7`  
		Last Modified: Thu, 25 Jan 2024 21:04:32 GMT  
		Size: 24.6 MB (24602341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b7f4d695b13df91b2e25dfb78289b3e42569d62b0797c47d012e7b28a4272f`  
		Last Modified: Fri, 02 Feb 2024 00:26:00 GMT  
		Size: 1.2 MB (1201866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7a566271693a24f462f1117821fdcc4a23cc64f686c845f89a05db132f75aa`  
		Last Modified: Fri, 02 Feb 2024 00:25:59 GMT  
		Size: 4.7 MB (4679249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d909a7e301dd4ccde1c83536b0c3894584dddb57bb4bba6c4aebea359488481`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2ce71c763b5dba0bb0f09e80c70a9430e62efee12ea01c91b900c82cf1de54`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1990aaec86a85bea7c5dab838a1699738f59db5b330181a2539eb7d3d6da4829`  
		Last Modified: Fri, 02 Feb 2024 00:26:26 GMT  
		Size: 157.5 MB (157460405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207b3e1bcaf5adbee8554fece6a2e8e149fbb2bac7a0e144ab02ccf9b7579e3`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f14aa3c10e2086f72ed556eda8d19460fc5d82b83b1907928a09f36a4164d5`  
		Last Modified: Fri, 02 Feb 2024 00:26:41 GMT  
		Size: 40.5 MB (40504147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb38a6164e77c6851bc201aaeccf8c3fb2232a434cc5c76191bdc9d9220925c`  
		Last Modified: Fri, 02 Feb 2024 00:26:35 GMT  
		Size: 313.9 KB (313921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f1f3a607ddd355114411ed00b9b5d84628f9b5d9983316fdd11cf697833b61`  
		Last Modified: Fri, 02 Feb 2024 00:26:35 GMT  
		Size: 1.1 MB (1061142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1055a8b31ee9456fbc9755c48f94ce23fc267bf488bc15ea829546c767aa0281`  
		Last Modified: Fri, 02 Feb 2024 00:28:12 GMT  
		Size: 496.4 MB (496372955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:592dc254833f8aca88a2637371bf3761c4803aa4a293694c9645ae7c78d9ce47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.5 MB (785478217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e8a46d9370a9f5bbe88a2218ed403e1b81b69516011699c34e2fe8df54191b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:38:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:38:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:38:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:38:47 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 02:38:47 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:38:47 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 02:38:48 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 02:41:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:41:26 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 02:41:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 02:41:26 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:41:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:42:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 02:42:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:51:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438b6b7c23286db8dea96cdf7072080a74f406ba4a7410eef9c9f9641523383b`  
		Last Modified: Fri, 02 Feb 2024 03:11:58 GMT  
		Size: 1.2 MB (1201863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a1f0f6848253a24ff4febd2c0b176fbbd1da89e23ec1a09694ebe3cba1cb98`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 5.5 MB (5532029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e614d2391d60a20ea55e27fc4757f6bf1feab494316071f49ab45c581638cb50`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807e86654c3f9af8fbc24df5a78c74fe5269aad2fd964c5428210f0cb4234b38`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cdec50b2982f5dbf33f29c7fb41a1400458bb10cf566abe5c73ba9857b3b50`  
		Last Modified: Fri, 02 Feb 2024 03:12:30 GMT  
		Size: 171.4 MB (171411451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddde60dd4677c9a8031ea604fe475f07800a88ff8dd76656c7424482ff09cc9d`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c611c5a97cbf0cdf9e83341151f6e4e327d36f5f1ec0a3ffffca3ad32b90b6`  
		Last Modified: Fri, 02 Feb 2024 03:12:44 GMT  
		Size: 45.2 MB (45207021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9018935407b2aa0321010be3e88629c37577aca47c2cc6fa04fbcee72458f4`  
		Last Modified: Fri, 02 Feb 2024 03:12:39 GMT  
		Size: 313.9 KB (313926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df260141e23ac900edc232c7425584d8b241f1d4a8e53d7db1c3ddbc57ab044`  
		Last Modified: Fri, 02 Feb 2024 03:12:39 GMT  
		Size: 1.1 MB (1114853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367843c93cc0c093c415056cd200d5951983cdf6a6f6b157323718a00d486498`  
		Last Modified: Fri, 02 Feb 2024 03:14:17 GMT  
		Size: 533.5 MB (533489527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:de3dc326117a3eca9117edd4dd6f21f1c0526ba4f32cb16639d1bda3658d642e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:ef2048f51c9ad41f63bd602ab45cc5df3d4f1e9f3712998a5499d0616dbabc1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 MB (281631198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec0e78e4fec2361652ced4378f8694705e81f3089c1dd608fceb4fd97903a57`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:47:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:47:22 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 02:47:22 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:47:22 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 02:47:22 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 02:49:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:49:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 02:49:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 02:49:43 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:50:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:50:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 02:50:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:51:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a0eff542a051aae29e565a80741d3a7b4cd98c32b2ee71ee5e65db2ea8339`  
		Last Modified: Fri, 02 Feb 2024 03:17:20 GMT  
		Size: 1.2 MB (1201927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3571ddcbb373955cce83c06caec6194bba015787cf70532a40f372ad0cfc4909`  
		Last Modified: Fri, 02 Feb 2024 03:17:19 GMT  
		Size: 5.6 MB (5553822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e738e3b521cc9f5634c723d391d85a3a5b9569b3d553421368380ec4b0582e`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5112e8bfde9264cec5c34ecd6175fa4701bc99b5ff0aebeb55286a24376bf0a7`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04476a0b14995e64a377f43280d3fc9f658e1f4005cd08626ea0bd7b8d76a151`  
		Last Modified: Fri, 02 Feb 2024 03:17:45 GMT  
		Size: 177.0 MB (176973755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aabb9a5c8e0fca47efaaf6ca15b59dee3873ec14b91c8ddd10726f63a82f48`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024be12c4ffd4a149d28e31d958bc58069c42db5afb0cd99622d76e3e567d07d`  
		Last Modified: Fri, 02 Feb 2024 03:18:01 GMT  
		Size: 50.9 MB (50942122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc791a8924c8665d0f658cbb906ef7da28971a46346f6e0506615abbbf4f10f5`  
		Last Modified: Fri, 02 Feb 2024 03:17:54 GMT  
		Size: 313.9 KB (313919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4e64ce06ce76c1990596e84ebbdb5bd709437b2d9d8bd557617c4b324a27b6`  
		Last Modified: Fri, 02 Feb 2024 03:17:54 GMT  
		Size: 1.1 MB (1130740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d7f8770389fdfdc6a9ce1f2094d5715c4ba077a9ef4096ef4405527ac24b31`  
		Last Modified: Fri, 02 Feb 2024 03:18:14 GMT  
		Size: 16.9 MB (16927964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:7915e1e2e3d91c401bb0559f07796a7a350495c4e98010b7a0202f3e364c1f3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244852955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d6909c09e92421146fe22857fc6d972fe314878d35d8c5fdc0208785bb1399`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:13:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:13:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:13:49 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 00:13:50 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 00:13:50 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 00:13:50 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 00:13:50 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 00:16:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:16:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 00:16:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 00:16:05 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:16:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:16:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 00:16:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:17:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93eb4c358a70eb4dc4f48209013d08987bf6c1a559df5adba7fc713ba9fc0bf7`  
		Last Modified: Thu, 25 Jan 2024 21:04:32 GMT  
		Size: 24.6 MB (24602341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b7f4d695b13df91b2e25dfb78289b3e42569d62b0797c47d012e7b28a4272f`  
		Last Modified: Fri, 02 Feb 2024 00:26:00 GMT  
		Size: 1.2 MB (1201866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7a566271693a24f462f1117821fdcc4a23cc64f686c845f89a05db132f75aa`  
		Last Modified: Fri, 02 Feb 2024 00:25:59 GMT  
		Size: 4.7 MB (4679249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d909a7e301dd4ccde1c83536b0c3894584dddb57bb4bba6c4aebea359488481`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2ce71c763b5dba0bb0f09e80c70a9430e62efee12ea01c91b900c82cf1de54`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1990aaec86a85bea7c5dab838a1699738f59db5b330181a2539eb7d3d6da4829`  
		Last Modified: Fri, 02 Feb 2024 00:26:26 GMT  
		Size: 157.5 MB (157460405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207b3e1bcaf5adbee8554fece6a2e8e149fbb2bac7a0e144ab02ccf9b7579e3`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f14aa3c10e2086f72ed556eda8d19460fc5d82b83b1907928a09f36a4164d5`  
		Last Modified: Fri, 02 Feb 2024 00:26:41 GMT  
		Size: 40.5 MB (40504147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb38a6164e77c6851bc201aaeccf8c3fb2232a434cc5c76191bdc9d9220925c`  
		Last Modified: Fri, 02 Feb 2024 00:26:35 GMT  
		Size: 313.9 KB (313921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f1f3a607ddd355114411ed00b9b5d84628f9b5d9983316fdd11cf697833b61`  
		Last Modified: Fri, 02 Feb 2024 00:26:35 GMT  
		Size: 1.1 MB (1061142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11de08eced2c70ae2d6581306d24c98598343c157f94fde56483aa08338aea9`  
		Last Modified: Fri, 02 Feb 2024 00:26:56 GMT  
		Size: 15.0 MB (15027397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:47c24a6a1002dd46b05fbce38f18bbcde4f8236fd3fdceaa2f1c2abae9015f75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268518733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48545a915f79f53e140fc9833c2f716863ca59fb19432ca0170d6762aa254a4f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:38:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:38:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:38:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:38:47 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 02:38:47 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:38:47 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 02:38:48 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 02:41:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:41:26 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 02:41:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 02:41:26 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:41:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:42:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 02:42:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:42:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438b6b7c23286db8dea96cdf7072080a74f406ba4a7410eef9c9f9641523383b`  
		Last Modified: Fri, 02 Feb 2024 03:11:58 GMT  
		Size: 1.2 MB (1201863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a1f0f6848253a24ff4febd2c0b176fbbd1da89e23ec1a09694ebe3cba1cb98`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 5.5 MB (5532029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e614d2391d60a20ea55e27fc4757f6bf1feab494316071f49ab45c581638cb50`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807e86654c3f9af8fbc24df5a78c74fe5269aad2fd964c5428210f0cb4234b38`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cdec50b2982f5dbf33f29c7fb41a1400458bb10cf566abe5c73ba9857b3b50`  
		Last Modified: Fri, 02 Feb 2024 03:12:30 GMT  
		Size: 171.4 MB (171411451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddde60dd4677c9a8031ea604fe475f07800a88ff8dd76656c7424482ff09cc9d`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c611c5a97cbf0cdf9e83341151f6e4e327d36f5f1ec0a3ffffca3ad32b90b6`  
		Last Modified: Fri, 02 Feb 2024 03:12:44 GMT  
		Size: 45.2 MB (45207021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9018935407b2aa0321010be3e88629c37577aca47c2cc6fa04fbcee72458f4`  
		Last Modified: Fri, 02 Feb 2024 03:12:39 GMT  
		Size: 313.9 KB (313926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df260141e23ac900edc232c7425584d8b241f1d4a8e53d7db1c3ddbc57ab044`  
		Last Modified: Fri, 02 Feb 2024 03:12:39 GMT  
		Size: 1.1 MB (1114853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4be71dd2839851daf476ddba70b4b313ccc02433c6be56a0e5d1a108c0c961`  
		Last Modified: Fri, 02 Feb 2024 03:12:59 GMT  
		Size: 16.5 MB (16530043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:de3dc326117a3eca9117edd4dd6f21f1c0526ba4f32cb16639d1bda3658d642e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:ef2048f51c9ad41f63bd602ab45cc5df3d4f1e9f3712998a5499d0616dbabc1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 MB (281631198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec0e78e4fec2361652ced4378f8694705e81f3089c1dd608fceb4fd97903a57`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:47:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:47:22 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 02:47:22 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:47:22 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 02:47:22 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 02:49:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:49:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 02:49:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 02:49:43 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:50:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:50:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 02:50:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:51:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a0eff542a051aae29e565a80741d3a7b4cd98c32b2ee71ee5e65db2ea8339`  
		Last Modified: Fri, 02 Feb 2024 03:17:20 GMT  
		Size: 1.2 MB (1201927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3571ddcbb373955cce83c06caec6194bba015787cf70532a40f372ad0cfc4909`  
		Last Modified: Fri, 02 Feb 2024 03:17:19 GMT  
		Size: 5.6 MB (5553822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e738e3b521cc9f5634c723d391d85a3a5b9569b3d553421368380ec4b0582e`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5112e8bfde9264cec5c34ecd6175fa4701bc99b5ff0aebeb55286a24376bf0a7`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04476a0b14995e64a377f43280d3fc9f658e1f4005cd08626ea0bd7b8d76a151`  
		Last Modified: Fri, 02 Feb 2024 03:17:45 GMT  
		Size: 177.0 MB (176973755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aabb9a5c8e0fca47efaaf6ca15b59dee3873ec14b91c8ddd10726f63a82f48`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024be12c4ffd4a149d28e31d958bc58069c42db5afb0cd99622d76e3e567d07d`  
		Last Modified: Fri, 02 Feb 2024 03:18:01 GMT  
		Size: 50.9 MB (50942122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc791a8924c8665d0f658cbb906ef7da28971a46346f6e0506615abbbf4f10f5`  
		Last Modified: Fri, 02 Feb 2024 03:17:54 GMT  
		Size: 313.9 KB (313919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4e64ce06ce76c1990596e84ebbdb5bd709437b2d9d8bd557617c4b324a27b6`  
		Last Modified: Fri, 02 Feb 2024 03:17:54 GMT  
		Size: 1.1 MB (1130740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d7f8770389fdfdc6a9ce1f2094d5715c4ba077a9ef4096ef4405527ac24b31`  
		Last Modified: Fri, 02 Feb 2024 03:18:14 GMT  
		Size: 16.9 MB (16927964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:7915e1e2e3d91c401bb0559f07796a7a350495c4e98010b7a0202f3e364c1f3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244852955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d6909c09e92421146fe22857fc6d972fe314878d35d8c5fdc0208785bb1399`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:13:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:13:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:13:49 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 00:13:50 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 00:13:50 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 00:13:50 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 00:13:50 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 00:16:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:16:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 00:16:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 00:16:05 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:16:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:16:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 00:16:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:17:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93eb4c358a70eb4dc4f48209013d08987bf6c1a559df5adba7fc713ba9fc0bf7`  
		Last Modified: Thu, 25 Jan 2024 21:04:32 GMT  
		Size: 24.6 MB (24602341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b7f4d695b13df91b2e25dfb78289b3e42569d62b0797c47d012e7b28a4272f`  
		Last Modified: Fri, 02 Feb 2024 00:26:00 GMT  
		Size: 1.2 MB (1201866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7a566271693a24f462f1117821fdcc4a23cc64f686c845f89a05db132f75aa`  
		Last Modified: Fri, 02 Feb 2024 00:25:59 GMT  
		Size: 4.7 MB (4679249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d909a7e301dd4ccde1c83536b0c3894584dddb57bb4bba6c4aebea359488481`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2ce71c763b5dba0bb0f09e80c70a9430e62efee12ea01c91b900c82cf1de54`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1990aaec86a85bea7c5dab838a1699738f59db5b330181a2539eb7d3d6da4829`  
		Last Modified: Fri, 02 Feb 2024 00:26:26 GMT  
		Size: 157.5 MB (157460405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207b3e1bcaf5adbee8554fece6a2e8e149fbb2bac7a0e144ab02ccf9b7579e3`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f14aa3c10e2086f72ed556eda8d19460fc5d82b83b1907928a09f36a4164d5`  
		Last Modified: Fri, 02 Feb 2024 00:26:41 GMT  
		Size: 40.5 MB (40504147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb38a6164e77c6851bc201aaeccf8c3fb2232a434cc5c76191bdc9d9220925c`  
		Last Modified: Fri, 02 Feb 2024 00:26:35 GMT  
		Size: 313.9 KB (313921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f1f3a607ddd355114411ed00b9b5d84628f9b5d9983316fdd11cf697833b61`  
		Last Modified: Fri, 02 Feb 2024 00:26:35 GMT  
		Size: 1.1 MB (1061142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11de08eced2c70ae2d6581306d24c98598343c157f94fde56483aa08338aea9`  
		Last Modified: Fri, 02 Feb 2024 00:26:56 GMT  
		Size: 15.0 MB (15027397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:47c24a6a1002dd46b05fbce38f18bbcde4f8236fd3fdceaa2f1c2abae9015f75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268518733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48545a915f79f53e140fc9833c2f716863ca59fb19432ca0170d6762aa254a4f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:38:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:38:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:38:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:38:47 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 02:38:47 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:38:47 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 02:38:48 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 02:41:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:41:26 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 02:41:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 02:41:26 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:41:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:42:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 02:42:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:42:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438b6b7c23286db8dea96cdf7072080a74f406ba4a7410eef9c9f9641523383b`  
		Last Modified: Fri, 02 Feb 2024 03:11:58 GMT  
		Size: 1.2 MB (1201863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a1f0f6848253a24ff4febd2c0b176fbbd1da89e23ec1a09694ebe3cba1cb98`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 5.5 MB (5532029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e614d2391d60a20ea55e27fc4757f6bf1feab494316071f49ab45c581638cb50`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807e86654c3f9af8fbc24df5a78c74fe5269aad2fd964c5428210f0cb4234b38`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cdec50b2982f5dbf33f29c7fb41a1400458bb10cf566abe5c73ba9857b3b50`  
		Last Modified: Fri, 02 Feb 2024 03:12:30 GMT  
		Size: 171.4 MB (171411451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddde60dd4677c9a8031ea604fe475f07800a88ff8dd76656c7424482ff09cc9d`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c611c5a97cbf0cdf9e83341151f6e4e327d36f5f1ec0a3ffffca3ad32b90b6`  
		Last Modified: Fri, 02 Feb 2024 03:12:44 GMT  
		Size: 45.2 MB (45207021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9018935407b2aa0321010be3e88629c37577aca47c2cc6fa04fbcee72458f4`  
		Last Modified: Fri, 02 Feb 2024 03:12:39 GMT  
		Size: 313.9 KB (313926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df260141e23ac900edc232c7425584d8b241f1d4a8e53d7db1c3ddbc57ab044`  
		Last Modified: Fri, 02 Feb 2024 03:12:39 GMT  
		Size: 1.1 MB (1114853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4be71dd2839851daf476ddba70b4b313ccc02433c6be56a0e5d1a108c0c961`  
		Last Modified: Fri, 02 Feb 2024 03:12:59 GMT  
		Size: 16.5 MB (16530043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:0e9073076550b1deffe45dc34b1baba0780e0778c5d0d053603951773dc12f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:41a0aad743d47e08bec68cf48005706c27a3d7aad10632d204cada99ef3642b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264703234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01ea3953302a6e2a2f91d97e3176d5d13cf3f90bee0b275851f6ac905a51480`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:47:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:47:22 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 02:47:22 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:47:22 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 02:47:22 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 02:49:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:49:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 02:49:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 02:49:43 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:50:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:50:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 02:50:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a0eff542a051aae29e565a80741d3a7b4cd98c32b2ee71ee5e65db2ea8339`  
		Last Modified: Fri, 02 Feb 2024 03:17:20 GMT  
		Size: 1.2 MB (1201927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3571ddcbb373955cce83c06caec6194bba015787cf70532a40f372ad0cfc4909`  
		Last Modified: Fri, 02 Feb 2024 03:17:19 GMT  
		Size: 5.6 MB (5553822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e738e3b521cc9f5634c723d391d85a3a5b9569b3d553421368380ec4b0582e`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5112e8bfde9264cec5c34ecd6175fa4701bc99b5ff0aebeb55286a24376bf0a7`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04476a0b14995e64a377f43280d3fc9f658e1f4005cd08626ea0bd7b8d76a151`  
		Last Modified: Fri, 02 Feb 2024 03:17:45 GMT  
		Size: 177.0 MB (176973755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aabb9a5c8e0fca47efaaf6ca15b59dee3873ec14b91c8ddd10726f63a82f48`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024be12c4ffd4a149d28e31d958bc58069c42db5afb0cd99622d76e3e567d07d`  
		Last Modified: Fri, 02 Feb 2024 03:18:01 GMT  
		Size: 50.9 MB (50942122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc791a8924c8665d0f658cbb906ef7da28971a46346f6e0506615abbbf4f10f5`  
		Last Modified: Fri, 02 Feb 2024 03:17:54 GMT  
		Size: 313.9 KB (313919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4e64ce06ce76c1990596e84ebbdb5bd709437b2d9d8bd557617c4b324a27b6`  
		Last Modified: Fri, 02 Feb 2024 03:17:54 GMT  
		Size: 1.1 MB (1130740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:26ec5db8714303c05d81e84567def32b1f7a41259b032af2ef9ed24d36caa222
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229825558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077a1be6f057e887d3741768be12841f0ff517475725c4fa447087fca8861d33`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:13:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:13:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:13:49 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 00:13:50 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 00:13:50 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 00:13:50 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 00:13:50 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 00:16:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:16:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 00:16:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 00:16:05 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:16:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:16:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 00:16:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93eb4c358a70eb4dc4f48209013d08987bf6c1a559df5adba7fc713ba9fc0bf7`  
		Last Modified: Thu, 25 Jan 2024 21:04:32 GMT  
		Size: 24.6 MB (24602341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b7f4d695b13df91b2e25dfb78289b3e42569d62b0797c47d012e7b28a4272f`  
		Last Modified: Fri, 02 Feb 2024 00:26:00 GMT  
		Size: 1.2 MB (1201866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7a566271693a24f462f1117821fdcc4a23cc64f686c845f89a05db132f75aa`  
		Last Modified: Fri, 02 Feb 2024 00:25:59 GMT  
		Size: 4.7 MB (4679249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d909a7e301dd4ccde1c83536b0c3894584dddb57bb4bba6c4aebea359488481`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2ce71c763b5dba0bb0f09e80c70a9430e62efee12ea01c91b900c82cf1de54`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1990aaec86a85bea7c5dab838a1699738f59db5b330181a2539eb7d3d6da4829`  
		Last Modified: Fri, 02 Feb 2024 00:26:26 GMT  
		Size: 157.5 MB (157460405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207b3e1bcaf5adbee8554fece6a2e8e149fbb2bac7a0e144ab02ccf9b7579e3`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f14aa3c10e2086f72ed556eda8d19460fc5d82b83b1907928a09f36a4164d5`  
		Last Modified: Fri, 02 Feb 2024 00:26:41 GMT  
		Size: 40.5 MB (40504147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb38a6164e77c6851bc201aaeccf8c3fb2232a434cc5c76191bdc9d9220925c`  
		Last Modified: Fri, 02 Feb 2024 00:26:35 GMT  
		Size: 313.9 KB (313921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f1f3a607ddd355114411ed00b9b5d84628f9b5d9983316fdd11cf697833b61`  
		Last Modified: Fri, 02 Feb 2024 00:26:35 GMT  
		Size: 1.1 MB (1061142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ea77a409e77dc685cc6f7afce25cc7d0c9d1b13dc4b7b34afaeb7867a15ee646
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251988690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d439934e28b7cd08d1dd54db338ce1cb0cf22971131b27801cf6440d8265a7c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:38:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:38:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:38:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:38:47 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 02:38:47 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:38:47 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 02:38:48 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 02:41:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:41:26 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 02:41:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 02:41:26 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:41:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:42:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 02:42:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438b6b7c23286db8dea96cdf7072080a74f406ba4a7410eef9c9f9641523383b`  
		Last Modified: Fri, 02 Feb 2024 03:11:58 GMT  
		Size: 1.2 MB (1201863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a1f0f6848253a24ff4febd2c0b176fbbd1da89e23ec1a09694ebe3cba1cb98`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 5.5 MB (5532029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e614d2391d60a20ea55e27fc4757f6bf1feab494316071f49ab45c581638cb50`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807e86654c3f9af8fbc24df5a78c74fe5269aad2fd964c5428210f0cb4234b38`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cdec50b2982f5dbf33f29c7fb41a1400458bb10cf566abe5c73ba9857b3b50`  
		Last Modified: Fri, 02 Feb 2024 03:12:30 GMT  
		Size: 171.4 MB (171411451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddde60dd4677c9a8031ea604fe475f07800a88ff8dd76656c7424482ff09cc9d`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c611c5a97cbf0cdf9e83341151f6e4e327d36f5f1ec0a3ffffca3ad32b90b6`  
		Last Modified: Fri, 02 Feb 2024 03:12:44 GMT  
		Size: 45.2 MB (45207021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9018935407b2aa0321010be3e88629c37577aca47c2cc6fa04fbcee72458f4`  
		Last Modified: Fri, 02 Feb 2024 03:12:39 GMT  
		Size: 313.9 KB (313926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df260141e23ac900edc232c7425584d8b241f1d4a8e53d7db1c3ddbc57ab044`  
		Last Modified: Fri, 02 Feb 2024 03:12:39 GMT  
		Size: 1.1 MB (1114853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:0e9073076550b1deffe45dc34b1baba0780e0778c5d0d053603951773dc12f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:41a0aad743d47e08bec68cf48005706c27a3d7aad10632d204cada99ef3642b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264703234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01ea3953302a6e2a2f91d97e3176d5d13cf3f90bee0b275851f6ac905a51480`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:47:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:47:22 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 02:47:22 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:47:22 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 02:47:22 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 02:49:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:49:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 02:49:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 02:49:43 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:50:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:50:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 02:50:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a0eff542a051aae29e565a80741d3a7b4cd98c32b2ee71ee5e65db2ea8339`  
		Last Modified: Fri, 02 Feb 2024 03:17:20 GMT  
		Size: 1.2 MB (1201927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3571ddcbb373955cce83c06caec6194bba015787cf70532a40f372ad0cfc4909`  
		Last Modified: Fri, 02 Feb 2024 03:17:19 GMT  
		Size: 5.6 MB (5553822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e738e3b521cc9f5634c723d391d85a3a5b9569b3d553421368380ec4b0582e`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5112e8bfde9264cec5c34ecd6175fa4701bc99b5ff0aebeb55286a24376bf0a7`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04476a0b14995e64a377f43280d3fc9f658e1f4005cd08626ea0bd7b8d76a151`  
		Last Modified: Fri, 02 Feb 2024 03:17:45 GMT  
		Size: 177.0 MB (176973755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aabb9a5c8e0fca47efaaf6ca15b59dee3873ec14b91c8ddd10726f63a82f48`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024be12c4ffd4a149d28e31d958bc58069c42db5afb0cd99622d76e3e567d07d`  
		Last Modified: Fri, 02 Feb 2024 03:18:01 GMT  
		Size: 50.9 MB (50942122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc791a8924c8665d0f658cbb906ef7da28971a46346f6e0506615abbbf4f10f5`  
		Last Modified: Fri, 02 Feb 2024 03:17:54 GMT  
		Size: 313.9 KB (313919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4e64ce06ce76c1990596e84ebbdb5bd709437b2d9d8bd557617c4b324a27b6`  
		Last Modified: Fri, 02 Feb 2024 03:17:54 GMT  
		Size: 1.1 MB (1130740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:26ec5db8714303c05d81e84567def32b1f7a41259b032af2ef9ed24d36caa222
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229825558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077a1be6f057e887d3741768be12841f0ff517475725c4fa447087fca8861d33`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:13:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:13:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:13:49 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 00:13:50 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 00:13:50 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 00:13:50 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 00:13:50 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 00:16:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:16:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 00:16:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 00:16:05 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 00:16:26 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:16:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 00:16:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93eb4c358a70eb4dc4f48209013d08987bf6c1a559df5adba7fc713ba9fc0bf7`  
		Last Modified: Thu, 25 Jan 2024 21:04:32 GMT  
		Size: 24.6 MB (24602341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b7f4d695b13df91b2e25dfb78289b3e42569d62b0797c47d012e7b28a4272f`  
		Last Modified: Fri, 02 Feb 2024 00:26:00 GMT  
		Size: 1.2 MB (1201866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7a566271693a24f462f1117821fdcc4a23cc64f686c845f89a05db132f75aa`  
		Last Modified: Fri, 02 Feb 2024 00:25:59 GMT  
		Size: 4.7 MB (4679249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d909a7e301dd4ccde1c83536b0c3894584dddb57bb4bba6c4aebea359488481`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2ce71c763b5dba0bb0f09e80c70a9430e62efee12ea01c91b900c82cf1de54`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1990aaec86a85bea7c5dab838a1699738f59db5b330181a2539eb7d3d6da4829`  
		Last Modified: Fri, 02 Feb 2024 00:26:26 GMT  
		Size: 157.5 MB (157460405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207b3e1bcaf5adbee8554fece6a2e8e149fbb2bac7a0e144ab02ccf9b7579e3`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f14aa3c10e2086f72ed556eda8d19460fc5d82b83b1907928a09f36a4164d5`  
		Last Modified: Fri, 02 Feb 2024 00:26:41 GMT  
		Size: 40.5 MB (40504147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb38a6164e77c6851bc201aaeccf8c3fb2232a434cc5c76191bdc9d9220925c`  
		Last Modified: Fri, 02 Feb 2024 00:26:35 GMT  
		Size: 313.9 KB (313921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f1f3a607ddd355114411ed00b9b5d84628f9b5d9983316fdd11cf697833b61`  
		Last Modified: Fri, 02 Feb 2024 00:26:35 GMT  
		Size: 1.1 MB (1061142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ea77a409e77dc685cc6f7afce25cc7d0c9d1b13dc4b7b34afaeb7867a15ee646
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251988690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d439934e28b7cd08d1dd54db338ce1cb0cf22971131b27801cf6440d8265a7c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:38:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:38:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:38:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:38:47 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 02:38:47 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:38:47 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 02:38:48 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 02:41:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:41:26 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 02:41:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 02:41:26 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 02:41:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:42:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Feb 2024 02:42:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438b6b7c23286db8dea96cdf7072080a74f406ba4a7410eef9c9f9641523383b`  
		Last Modified: Fri, 02 Feb 2024 03:11:58 GMT  
		Size: 1.2 MB (1201863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a1f0f6848253a24ff4febd2c0b176fbbd1da89e23ec1a09694ebe3cba1cb98`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 5.5 MB (5532029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e614d2391d60a20ea55e27fc4757f6bf1feab494316071f49ab45c581638cb50`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807e86654c3f9af8fbc24df5a78c74fe5269aad2fd964c5428210f0cb4234b38`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cdec50b2982f5dbf33f29c7fb41a1400458bb10cf566abe5c73ba9857b3b50`  
		Last Modified: Fri, 02 Feb 2024 03:12:30 GMT  
		Size: 171.4 MB (171411451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddde60dd4677c9a8031ea604fe475f07800a88ff8dd76656c7424482ff09cc9d`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c611c5a97cbf0cdf9e83341151f6e4e327d36f5f1ec0a3ffffca3ad32b90b6`  
		Last Modified: Fri, 02 Feb 2024 03:12:44 GMT  
		Size: 45.2 MB (45207021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9018935407b2aa0321010be3e88629c37577aca47c2cc6fa04fbcee72458f4`  
		Last Modified: Fri, 02 Feb 2024 03:12:39 GMT  
		Size: 313.9 KB (313926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df260141e23ac900edc232c7425584d8b241f1d4a8e53d7db1c3ddbc57ab044`  
		Last Modified: Fri, 02 Feb 2024 03:12:39 GMT  
		Size: 1.1 MB (1114853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:a97dd3e9d91d9b104fbab59a0dfcfbd0a5ff6c74e2b7fdb4223af6e784e5d477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:d398ebc6d806dff5cef5a0ef88b9efac1fe293ef9ae93a769a073fbe97f69737
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212316453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b8a399d8a77682eb023017d82b64a5ff9b06c4c2542ceeefbcd6c2e9ddb2818`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:47:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:47:22 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 02:47:22 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:47:22 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 02:47:22 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 02:49:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:49:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 02:49:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 02:49:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a0eff542a051aae29e565a80741d3a7b4cd98c32b2ee71ee5e65db2ea8339`  
		Last Modified: Fri, 02 Feb 2024 03:17:20 GMT  
		Size: 1.2 MB (1201927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3571ddcbb373955cce83c06caec6194bba015787cf70532a40f372ad0cfc4909`  
		Last Modified: Fri, 02 Feb 2024 03:17:19 GMT  
		Size: 5.6 MB (5553822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e738e3b521cc9f5634c723d391d85a3a5b9569b3d553421368380ec4b0582e`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5112e8bfde9264cec5c34ecd6175fa4701bc99b5ff0aebeb55286a24376bf0a7`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04476a0b14995e64a377f43280d3fc9f658e1f4005cd08626ea0bd7b8d76a151`  
		Last Modified: Fri, 02 Feb 2024 03:17:45 GMT  
		Size: 177.0 MB (176973755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aabb9a5c8e0fca47efaaf6ca15b59dee3873ec14b91c8ddd10726f63a82f48`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:d93214ce1f60be734e7789d8f5888b3f538eb1bde5e345238794757c1a0362c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187946348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe3e25c4b58573ece7593e276a9d1d90fa5a833a5248e89919e73fe09ab5850`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:13:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:13:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:13:49 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 00:13:50 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 00:13:50 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 00:13:50 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 00:13:50 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 00:16:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:16:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 00:16:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 00:16:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:93eb4c358a70eb4dc4f48209013d08987bf6c1a559df5adba7fc713ba9fc0bf7`  
		Last Modified: Thu, 25 Jan 2024 21:04:32 GMT  
		Size: 24.6 MB (24602341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b7f4d695b13df91b2e25dfb78289b3e42569d62b0797c47d012e7b28a4272f`  
		Last Modified: Fri, 02 Feb 2024 00:26:00 GMT  
		Size: 1.2 MB (1201866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7a566271693a24f462f1117821fdcc4a23cc64f686c845f89a05db132f75aa`  
		Last Modified: Fri, 02 Feb 2024 00:25:59 GMT  
		Size: 4.7 MB (4679249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d909a7e301dd4ccde1c83536b0c3894584dddb57bb4bba6c4aebea359488481`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2ce71c763b5dba0bb0f09e80c70a9430e62efee12ea01c91b900c82cf1de54`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1990aaec86a85bea7c5dab838a1699738f59db5b330181a2539eb7d3d6da4829`  
		Last Modified: Fri, 02 Feb 2024 00:26:26 GMT  
		Size: 157.5 MB (157460405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207b3e1bcaf5adbee8554fece6a2e8e149fbb2bac7a0e144ab02ccf9b7579e3`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fae3e102c68a052eab2f67cb5504e2e6318a26b19ff41a7580fa17005519de8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205352890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6db13b8990630a079eaef8476b61aa5ded705bd0328fd4f07cde441109da25f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:38:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:38:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:38:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:38:47 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 02:38:47 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:38:47 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 02:38:48 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 02:41:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:41:26 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 02:41:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 02:41:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438b6b7c23286db8dea96cdf7072080a74f406ba4a7410eef9c9f9641523383b`  
		Last Modified: Fri, 02 Feb 2024 03:11:58 GMT  
		Size: 1.2 MB (1201863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a1f0f6848253a24ff4febd2c0b176fbbd1da89e23ec1a09694ebe3cba1cb98`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 5.5 MB (5532029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e614d2391d60a20ea55e27fc4757f6bf1feab494316071f49ab45c581638cb50`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807e86654c3f9af8fbc24df5a78c74fe5269aad2fd964c5428210f0cb4234b38`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cdec50b2982f5dbf33f29c7fb41a1400458bb10cf566abe5c73ba9857b3b50`  
		Last Modified: Fri, 02 Feb 2024 03:12:30 GMT  
		Size: 171.4 MB (171411451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddde60dd4677c9a8031ea604fe475f07800a88ff8dd76656c7424482ff09cc9d`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:a97dd3e9d91d9b104fbab59a0dfcfbd0a5ff6c74e2b7fdb4223af6e784e5d477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:d398ebc6d806dff5cef5a0ef88b9efac1fe293ef9ae93a769a073fbe97f69737
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212316453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b8a399d8a77682eb023017d82b64a5ff9b06c4c2542ceeefbcd6c2e9ddb2818`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:47:12 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:20 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:47:21 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:47:22 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 02:47:22 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:47:22 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 02:47:22 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 02:49:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:49:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 02:49:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 02:49:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a0eff542a051aae29e565a80741d3a7b4cd98c32b2ee71ee5e65db2ea8339`  
		Last Modified: Fri, 02 Feb 2024 03:17:20 GMT  
		Size: 1.2 MB (1201927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3571ddcbb373955cce83c06caec6194bba015787cf70532a40f372ad0cfc4909`  
		Last Modified: Fri, 02 Feb 2024 03:17:19 GMT  
		Size: 5.6 MB (5553822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e738e3b521cc9f5634c723d391d85a3a5b9569b3d553421368380ec4b0582e`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5112e8bfde9264cec5c34ecd6175fa4701bc99b5ff0aebeb55286a24376bf0a7`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04476a0b14995e64a377f43280d3fc9f658e1f4005cd08626ea0bd7b8d76a151`  
		Last Modified: Fri, 02 Feb 2024 03:17:45 GMT  
		Size: 177.0 MB (176973755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aabb9a5c8e0fca47efaaf6ca15b59dee3873ec14b91c8ddd10726f63a82f48`  
		Last Modified: Fri, 02 Feb 2024 03:17:17 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:d93214ce1f60be734e7789d8f5888b3f538eb1bde5e345238794757c1a0362c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187946348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe3e25c4b58573ece7593e276a9d1d90fa5a833a5248e89919e73fe09ab5850`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:02:57 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:02:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:02:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:03:00 GMT
ADD file:06dcbc8a8b50c1189965851d9f1a29fe046ec9589e6e850865a8608d0a59ad50 in / 
# Tue, 23 Jan 2024 13:03:00 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:13:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:13:48 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:13:49 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 00:13:50 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 00:13:50 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 00:13:50 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 00:13:50 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 00:16:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:16:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 00:16:05 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 00:16:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:93eb4c358a70eb4dc4f48209013d08987bf6c1a559df5adba7fc713ba9fc0bf7`  
		Last Modified: Thu, 25 Jan 2024 21:04:32 GMT  
		Size: 24.6 MB (24602341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b7f4d695b13df91b2e25dfb78289b3e42569d62b0797c47d012e7b28a4272f`  
		Last Modified: Fri, 02 Feb 2024 00:26:00 GMT  
		Size: 1.2 MB (1201866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7a566271693a24f462f1117821fdcc4a23cc64f686c845f89a05db132f75aa`  
		Last Modified: Fri, 02 Feb 2024 00:25:59 GMT  
		Size: 4.7 MB (4679249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d909a7e301dd4ccde1c83536b0c3894584dddb57bb4bba6c4aebea359488481`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2ce71c763b5dba0bb0f09e80c70a9430e62efee12ea01c91b900c82cf1de54`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1990aaec86a85bea7c5dab838a1699738f59db5b330181a2539eb7d3d6da4829`  
		Last Modified: Fri, 02 Feb 2024 00:26:26 GMT  
		Size: 157.5 MB (157460405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207b3e1bcaf5adbee8554fece6a2e8e149fbb2bac7a0e144ab02ccf9b7579e3`  
		Last Modified: Fri, 02 Feb 2024 00:25:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fae3e102c68a052eab2f67cb5504e2e6318a26b19ff41a7580fa17005519de8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205352890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6db13b8990630a079eaef8476b61aa5ded705bd0328fd4f07cde441109da25f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:38:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:38:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:38:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 02 Feb 2024 02:38:47 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Feb 2024 02:38:47 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 02:38:47 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Feb 2024 02:38:48 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Feb 2024 02:41:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 02:41:26 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Feb 2024 02:41:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Feb 2024 02:41:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438b6b7c23286db8dea96cdf7072080a74f406ba4a7410eef9c9f9641523383b`  
		Last Modified: Fri, 02 Feb 2024 03:11:58 GMT  
		Size: 1.2 MB (1201863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a1f0f6848253a24ff4febd2c0b176fbbd1da89e23ec1a09694ebe3cba1cb98`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 5.5 MB (5532029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e614d2391d60a20ea55e27fc4757f6bf1feab494316071f49ab45c581638cb50`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807e86654c3f9af8fbc24df5a78c74fe5269aad2fd964c5428210f0cb4234b38`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cdec50b2982f5dbf33f29c7fb41a1400458bb10cf566abe5c73ba9857b3b50`  
		Last Modified: Fri, 02 Feb 2024 03:12:30 GMT  
		Size: 171.4 MB (171411451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddde60dd4677c9a8031ea604fe475f07800a88ff8dd76656c7424482ff09cc9d`  
		Last Modified: Fri, 02 Feb 2024 03:11:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling`

```console
$ docker pull ros@sha256:d4d3283755e3105e325d885237a8d5a4afbb210d3df54ae08263f866a13f0a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:257e7f523237bf7e45f175e334ed99d2ed20bd03605c387580d28cb6923fea19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268717186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433bd7fa0dad5ba8b911a649f63936938a40ea6e8d0228b9cb4ebbd251266827`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:45:48 GMT
ENV ROS_DISTRO=rolling
# Fri, 16 Feb 2024 02:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:46:36 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:46:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:46:36 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 02:47:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:47:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 02:47:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 02:47:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e816e1b53b0a2cfbc020786fc9237866c475b7a1577a3434f22757184feae43a`  
		Last Modified: Fri, 16 Feb 2024 02:55:23 GMT  
		Size: 124.0 MB (124022764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a59c2ece161c660ab1f9845fa7a104a86e1c1ce4c693528dbb9a209ebd5064`  
		Last Modified: Fri, 16 Feb 2024 02:55:03 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb70b401ad3cdd5e5312f608fac50c4d08235c46b4bb7d5b96a4fa3d4adffaa`  
		Last Modified: Fri, 16 Feb 2024 02:55:42 GMT  
		Size: 85.2 MB (85172455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e59a5e57117836224d8592f79069f4396990f938472fd8908c99647acc8bed4`  
		Last Modified: Fri, 16 Feb 2024 02:55:31 GMT  
		Size: 288.3 KB (288267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84db4ed4691b1b8a17e3f51101a41d420677093770a40c6ab13bcc7d8962b6bb`  
		Last Modified: Fri, 16 Feb 2024 02:55:31 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90e53c82be9bb64a07e8642c11539216cae554aeb5583f73c05deb0adbeaec2`  
		Last Modified: Fri, 16 Feb 2024 02:55:35 GMT  
		Size: 23.7 MB (23733355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:febae1c46564a23725589f330c7646a6b9b549d5fe03b7f136abc70206ee5be5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261173526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f27e3c80e7ef0cb25280c59e8a5fe35bdc22689279fcc5c287c4490b5db11d7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:36:11 GMT
ENV ROS_DISTRO=rolling
# Fri, 16 Feb 2024 05:36:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:36:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:36:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:36:51 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 05:37:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:37:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 05:37:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 05:37:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f5ba27e09156f2abd707c31ae4b3c30fba1cb7cc093834e02213c76a491920`  
		Last Modified: Fri, 16 Feb 2024 05:44:56 GMT  
		Size: 121.5 MB (121514724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c354b27f981f31060a6bc28d16882869ff3cea5aa8f51e2f01aeb59d51cb2d4b`  
		Last Modified: Fri, 16 Feb 2024 05:44:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073be48ee18b888bdb5c24da37b988d2b052da8cf145531ab73fa0445128685a`  
		Last Modified: Fri, 16 Feb 2024 05:45:14 GMT  
		Size: 82.8 MB (82846557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5ba1697514e19d58532dd5504508d8b7064c817df9cc114872b71f2c7f090d`  
		Last Modified: Fri, 16 Feb 2024 05:45:06 GMT  
		Size: 288.3 KB (288272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7fe0b2c75f5a9d76b0e16f87ee5742545c5d13f47f45fd005ec0e3cf3523b1`  
		Last Modified: Fri, 16 Feb 2024 05:45:06 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3820ab663dcc8467f214e63948aabc8674a0c40002cee43566e0d8a524aa92`  
		Last Modified: Fri, 16 Feb 2024 05:45:09 GMT  
		Size: 23.1 MB (23101747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:7f27d949206140004b0f3499027d13b9b9f61047aecab07bcfeba8fe8131597c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:afcaba5fc6bbc0b70cbbf010d1ad402b3e1c8f47c3c0f95025800325cea2c330
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.1 MB (961072350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9105f3bbb81b1d6bd844917d73239dffc41a2f909ef9ea291925faaa26a163`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:45:48 GMT
ENV ROS_DISTRO=rolling
# Fri, 16 Feb 2024 02:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:46:36 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:46:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:46:36 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 02:47:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:47:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 02:47:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 02:47:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:49:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e816e1b53b0a2cfbc020786fc9237866c475b7a1577a3434f22757184feae43a`  
		Last Modified: Fri, 16 Feb 2024 02:55:23 GMT  
		Size: 124.0 MB (124022764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a59c2ece161c660ab1f9845fa7a104a86e1c1ce4c693528dbb9a209ebd5064`  
		Last Modified: Fri, 16 Feb 2024 02:55:03 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb70b401ad3cdd5e5312f608fac50c4d08235c46b4bb7d5b96a4fa3d4adffaa`  
		Last Modified: Fri, 16 Feb 2024 02:55:42 GMT  
		Size: 85.2 MB (85172455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e59a5e57117836224d8592f79069f4396990f938472fd8908c99647acc8bed4`  
		Last Modified: Fri, 16 Feb 2024 02:55:31 GMT  
		Size: 288.3 KB (288267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84db4ed4691b1b8a17e3f51101a41d420677093770a40c6ab13bcc7d8962b6bb`  
		Last Modified: Fri, 16 Feb 2024 02:55:31 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90e53c82be9bb64a07e8642c11539216cae554aeb5583f73c05deb0adbeaec2`  
		Last Modified: Fri, 16 Feb 2024 02:55:35 GMT  
		Size: 23.7 MB (23733355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3714e19d249980578d5b43bb699436b994ae29b3fcb161b137fcb8912ce5cfd`  
		Last Modified: Fri, 16 Feb 2024 02:57:26 GMT  
		Size: 692.4 MB (692355164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cf9a5e2843e818d94b386fe0925982ad02a7120b9fd6bb44c8f80b2a40de4aff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.4 MB (921371813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8acc19911fa655ae7768fddfc42b3aac88a27487f2c3604a395eac365ee3792`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:36:11 GMT
ENV ROS_DISTRO=rolling
# Fri, 16 Feb 2024 05:36:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:36:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:36:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:36:51 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 05:37:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:37:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 05:37:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 05:37:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:39:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f5ba27e09156f2abd707c31ae4b3c30fba1cb7cc093834e02213c76a491920`  
		Last Modified: Fri, 16 Feb 2024 05:44:56 GMT  
		Size: 121.5 MB (121514724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c354b27f981f31060a6bc28d16882869ff3cea5aa8f51e2f01aeb59d51cb2d4b`  
		Last Modified: Fri, 16 Feb 2024 05:44:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073be48ee18b888bdb5c24da37b988d2b052da8cf145531ab73fa0445128685a`  
		Last Modified: Fri, 16 Feb 2024 05:45:14 GMT  
		Size: 82.8 MB (82846557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5ba1697514e19d58532dd5504508d8b7064c817df9cc114872b71f2c7f090d`  
		Last Modified: Fri, 16 Feb 2024 05:45:06 GMT  
		Size: 288.3 KB (288272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7fe0b2c75f5a9d76b0e16f87ee5742545c5d13f47f45fd005ec0e3cf3523b1`  
		Last Modified: Fri, 16 Feb 2024 05:45:06 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3820ab663dcc8467f214e63948aabc8674a0c40002cee43566e0d8a524aa92`  
		Last Modified: Fri, 16 Feb 2024 05:45:09 GMT  
		Size: 23.1 MB (23101747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ea8db1138bc712cf216edfa2f027f2de7b389cf5495fa5df7606b2ad1f630e`  
		Last Modified: Fri, 16 Feb 2024 05:46:31 GMT  
		Size: 660.2 MB (660198287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception-jammy`

```console
$ docker pull ros@sha256:7f27d949206140004b0f3499027d13b9b9f61047aecab07bcfeba8fe8131597c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:afcaba5fc6bbc0b70cbbf010d1ad402b3e1c8f47c3c0f95025800325cea2c330
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.1 MB (961072350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9105f3bbb81b1d6bd844917d73239dffc41a2f909ef9ea291925faaa26a163`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:45:48 GMT
ENV ROS_DISTRO=rolling
# Fri, 16 Feb 2024 02:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:46:36 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:46:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:46:36 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 02:47:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:47:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 02:47:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 02:47:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:49:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e816e1b53b0a2cfbc020786fc9237866c475b7a1577a3434f22757184feae43a`  
		Last Modified: Fri, 16 Feb 2024 02:55:23 GMT  
		Size: 124.0 MB (124022764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a59c2ece161c660ab1f9845fa7a104a86e1c1ce4c693528dbb9a209ebd5064`  
		Last Modified: Fri, 16 Feb 2024 02:55:03 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb70b401ad3cdd5e5312f608fac50c4d08235c46b4bb7d5b96a4fa3d4adffaa`  
		Last Modified: Fri, 16 Feb 2024 02:55:42 GMT  
		Size: 85.2 MB (85172455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e59a5e57117836224d8592f79069f4396990f938472fd8908c99647acc8bed4`  
		Last Modified: Fri, 16 Feb 2024 02:55:31 GMT  
		Size: 288.3 KB (288267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84db4ed4691b1b8a17e3f51101a41d420677093770a40c6ab13bcc7d8962b6bb`  
		Last Modified: Fri, 16 Feb 2024 02:55:31 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90e53c82be9bb64a07e8642c11539216cae554aeb5583f73c05deb0adbeaec2`  
		Last Modified: Fri, 16 Feb 2024 02:55:35 GMT  
		Size: 23.7 MB (23733355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3714e19d249980578d5b43bb699436b994ae29b3fcb161b137fcb8912ce5cfd`  
		Last Modified: Fri, 16 Feb 2024 02:57:26 GMT  
		Size: 692.4 MB (692355164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cf9a5e2843e818d94b386fe0925982ad02a7120b9fd6bb44c8f80b2a40de4aff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.4 MB (921371813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8acc19911fa655ae7768fddfc42b3aac88a27487f2c3604a395eac365ee3792`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:36:11 GMT
ENV ROS_DISTRO=rolling
# Fri, 16 Feb 2024 05:36:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:36:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:36:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:36:51 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 05:37:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:37:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 05:37:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 05:37:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:39:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f5ba27e09156f2abd707c31ae4b3c30fba1cb7cc093834e02213c76a491920`  
		Last Modified: Fri, 16 Feb 2024 05:44:56 GMT  
		Size: 121.5 MB (121514724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c354b27f981f31060a6bc28d16882869ff3cea5aa8f51e2f01aeb59d51cb2d4b`  
		Last Modified: Fri, 16 Feb 2024 05:44:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073be48ee18b888bdb5c24da37b988d2b052da8cf145531ab73fa0445128685a`  
		Last Modified: Fri, 16 Feb 2024 05:45:14 GMT  
		Size: 82.8 MB (82846557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5ba1697514e19d58532dd5504508d8b7064c817df9cc114872b71f2c7f090d`  
		Last Modified: Fri, 16 Feb 2024 05:45:06 GMT  
		Size: 288.3 KB (288272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7fe0b2c75f5a9d76b0e16f87ee5742545c5d13f47f45fd005ec0e3cf3523b1`  
		Last Modified: Fri, 16 Feb 2024 05:45:06 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3820ab663dcc8467f214e63948aabc8674a0c40002cee43566e0d8a524aa92`  
		Last Modified: Fri, 16 Feb 2024 05:45:09 GMT  
		Size: 23.1 MB (23101747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ea8db1138bc712cf216edfa2f027f2de7b389cf5495fa5df7606b2ad1f630e`  
		Last Modified: Fri, 16 Feb 2024 05:46:31 GMT  
		Size: 660.2 MB (660198287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:d4d3283755e3105e325d885237a8d5a4afbb210d3df54ae08263f866a13f0a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:257e7f523237bf7e45f175e334ed99d2ed20bd03605c387580d28cb6923fea19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268717186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433bd7fa0dad5ba8b911a649f63936938a40ea6e8d0228b9cb4ebbd251266827`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:45:48 GMT
ENV ROS_DISTRO=rolling
# Fri, 16 Feb 2024 02:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:46:36 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:46:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:46:36 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 02:47:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:47:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 02:47:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 02:47:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e816e1b53b0a2cfbc020786fc9237866c475b7a1577a3434f22757184feae43a`  
		Last Modified: Fri, 16 Feb 2024 02:55:23 GMT  
		Size: 124.0 MB (124022764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a59c2ece161c660ab1f9845fa7a104a86e1c1ce4c693528dbb9a209ebd5064`  
		Last Modified: Fri, 16 Feb 2024 02:55:03 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb70b401ad3cdd5e5312f608fac50c4d08235c46b4bb7d5b96a4fa3d4adffaa`  
		Last Modified: Fri, 16 Feb 2024 02:55:42 GMT  
		Size: 85.2 MB (85172455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e59a5e57117836224d8592f79069f4396990f938472fd8908c99647acc8bed4`  
		Last Modified: Fri, 16 Feb 2024 02:55:31 GMT  
		Size: 288.3 KB (288267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84db4ed4691b1b8a17e3f51101a41d420677093770a40c6ab13bcc7d8962b6bb`  
		Last Modified: Fri, 16 Feb 2024 02:55:31 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90e53c82be9bb64a07e8642c11539216cae554aeb5583f73c05deb0adbeaec2`  
		Last Modified: Fri, 16 Feb 2024 02:55:35 GMT  
		Size: 23.7 MB (23733355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:febae1c46564a23725589f330c7646a6b9b549d5fe03b7f136abc70206ee5be5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261173526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f27e3c80e7ef0cb25280c59e8a5fe35bdc22689279fcc5c287c4490b5db11d7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:36:11 GMT
ENV ROS_DISTRO=rolling
# Fri, 16 Feb 2024 05:36:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:36:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:36:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:36:51 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 05:37:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:37:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 05:37:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 05:37:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f5ba27e09156f2abd707c31ae4b3c30fba1cb7cc093834e02213c76a491920`  
		Last Modified: Fri, 16 Feb 2024 05:44:56 GMT  
		Size: 121.5 MB (121514724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c354b27f981f31060a6bc28d16882869ff3cea5aa8f51e2f01aeb59d51cb2d4b`  
		Last Modified: Fri, 16 Feb 2024 05:44:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073be48ee18b888bdb5c24da37b988d2b052da8cf145531ab73fa0445128685a`  
		Last Modified: Fri, 16 Feb 2024 05:45:14 GMT  
		Size: 82.8 MB (82846557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5ba1697514e19d58532dd5504508d8b7064c817df9cc114872b71f2c7f090d`  
		Last Modified: Fri, 16 Feb 2024 05:45:06 GMT  
		Size: 288.3 KB (288272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7fe0b2c75f5a9d76b0e16f87ee5742545c5d13f47f45fd005ec0e3cf3523b1`  
		Last Modified: Fri, 16 Feb 2024 05:45:06 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3820ab663dcc8467f214e63948aabc8674a0c40002cee43566e0d8a524aa92`  
		Last Modified: Fri, 16 Feb 2024 05:45:09 GMT  
		Size: 23.1 MB (23101747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base-jammy`

```console
$ docker pull ros@sha256:d4d3283755e3105e325d885237a8d5a4afbb210d3df54ae08263f866a13f0a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:257e7f523237bf7e45f175e334ed99d2ed20bd03605c387580d28cb6923fea19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268717186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433bd7fa0dad5ba8b911a649f63936938a40ea6e8d0228b9cb4ebbd251266827`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:45:48 GMT
ENV ROS_DISTRO=rolling
# Fri, 16 Feb 2024 02:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:46:36 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:46:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:46:36 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 02:47:03 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:47:08 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 02:47:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 02:47:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e816e1b53b0a2cfbc020786fc9237866c475b7a1577a3434f22757184feae43a`  
		Last Modified: Fri, 16 Feb 2024 02:55:23 GMT  
		Size: 124.0 MB (124022764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a59c2ece161c660ab1f9845fa7a104a86e1c1ce4c693528dbb9a209ebd5064`  
		Last Modified: Fri, 16 Feb 2024 02:55:03 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb70b401ad3cdd5e5312f608fac50c4d08235c46b4bb7d5b96a4fa3d4adffaa`  
		Last Modified: Fri, 16 Feb 2024 02:55:42 GMT  
		Size: 85.2 MB (85172455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e59a5e57117836224d8592f79069f4396990f938472fd8908c99647acc8bed4`  
		Last Modified: Fri, 16 Feb 2024 02:55:31 GMT  
		Size: 288.3 KB (288267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84db4ed4691b1b8a17e3f51101a41d420677093770a40c6ab13bcc7d8962b6bb`  
		Last Modified: Fri, 16 Feb 2024 02:55:31 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90e53c82be9bb64a07e8642c11539216cae554aeb5583f73c05deb0adbeaec2`  
		Last Modified: Fri, 16 Feb 2024 02:55:35 GMT  
		Size: 23.7 MB (23733355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:febae1c46564a23725589f330c7646a6b9b549d5fe03b7f136abc70206ee5be5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261173526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f27e3c80e7ef0cb25280c59e8a5fe35bdc22689279fcc5c287c4490b5db11d7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:36:11 GMT
ENV ROS_DISTRO=rolling
# Fri, 16 Feb 2024 05:36:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:36:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:36:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:36:51 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 05:37:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:37:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 16 Feb 2024 05:37:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 16 Feb 2024 05:37:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f5ba27e09156f2abd707c31ae4b3c30fba1cb7cc093834e02213c76a491920`  
		Last Modified: Fri, 16 Feb 2024 05:44:56 GMT  
		Size: 121.5 MB (121514724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c354b27f981f31060a6bc28d16882869ff3cea5aa8f51e2f01aeb59d51cb2d4b`  
		Last Modified: Fri, 16 Feb 2024 05:44:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073be48ee18b888bdb5c24da37b988d2b052da8cf145531ab73fa0445128685a`  
		Last Modified: Fri, 16 Feb 2024 05:45:14 GMT  
		Size: 82.8 MB (82846557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5ba1697514e19d58532dd5504508d8b7064c817df9cc114872b71f2c7f090d`  
		Last Modified: Fri, 16 Feb 2024 05:45:06 GMT  
		Size: 288.3 KB (288272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7fe0b2c75f5a9d76b0e16f87ee5742545c5d13f47f45fd005ec0e3cf3523b1`  
		Last Modified: Fri, 16 Feb 2024 05:45:06 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3820ab663dcc8467f214e63948aabc8674a0c40002cee43566e0d8a524aa92`  
		Last Modified: Fri, 16 Feb 2024 05:45:09 GMT  
		Size: 23.1 MB (23101747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:e41f6e0629cff49dd82899ef8395bc32d61ec1c46bd13b8a91d288613e0d1ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:d6c4b9d24e2307f9185eccf23d9c9eff18874f4defa48abd6fec033cc84a3799
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 MB (159520615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0de4810cf30802941316dade053ba2f4fed40c96176fcca058d336adc4df27c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:45:48 GMT
ENV ROS_DISTRO=rolling
# Fri, 16 Feb 2024 02:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:46:36 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:46:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:46:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e816e1b53b0a2cfbc020786fc9237866c475b7a1577a3434f22757184feae43a`  
		Last Modified: Fri, 16 Feb 2024 02:55:23 GMT  
		Size: 124.0 MB (124022764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a59c2ece161c660ab1f9845fa7a104a86e1c1ce4c693528dbb9a209ebd5064`  
		Last Modified: Fri, 16 Feb 2024 02:55:03 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e31d2dbe903ff2a67c3116f4d4b13e66369583246f3fe724a34c9a17826c11cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154934459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a5a914b4f37e209816668d0034b75a3c5bce6d5f64b38104e9d6b316166798`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:36:11 GMT
ENV ROS_DISTRO=rolling
# Fri, 16 Feb 2024 05:36:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:36:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:36:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:36:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f5ba27e09156f2abd707c31ae4b3c30fba1cb7cc093834e02213c76a491920`  
		Last Modified: Fri, 16 Feb 2024 05:44:56 GMT  
		Size: 121.5 MB (121514724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c354b27f981f31060a6bc28d16882869ff3cea5aa8f51e2f01aeb59d51cb2d4b`  
		Last Modified: Fri, 16 Feb 2024 05:44:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core-jammy`

```console
$ docker pull ros@sha256:e41f6e0629cff49dd82899ef8395bc32d61ec1c46bd13b8a91d288613e0d1ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:d6c4b9d24e2307f9185eccf23d9c9eff18874f4defa48abd6fec033cc84a3799
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 MB (159520615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0de4810cf30802941316dade053ba2f4fed40c96176fcca058d336adc4df27c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:31:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:31:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 02:31:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 02:31:09 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 02:45:48 GMT
ENV ROS_DISTRO=rolling
# Fri, 16 Feb 2024 02:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:46:36 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 02:46:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 02:46:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f145a21311ee2676d7d50a1dd8ae62c41d1aeeceac5bef19888eb66efa40e74`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 1.2 MB (1216244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab1b3ba0a6544273bb017a8c40004ea367a38835db2e6a05ed5ff35b05f7f2e`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 3.8 MB (3829043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950c0cf8179dff570ff58b4dda0e8f1edbdaac8c8289d0d78fb5927a34de99`  
		Last Modified: Fri, 16 Feb 2024 02:49:54 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef09cb8b54aeee254b1c15dad1b5c4cf4147fad3cb4cf4827d51818dfb7975ec`  
		Last Modified: Fri, 16 Feb 2024 02:49:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e816e1b53b0a2cfbc020786fc9237866c475b7a1577a3434f22757184feae43a`  
		Last Modified: Fri, 16 Feb 2024 02:55:23 GMT  
		Size: 124.0 MB (124022764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a59c2ece161c660ab1f9845fa7a104a86e1c1ce4c693528dbb9a209ebd5064`  
		Last Modified: Fri, 16 Feb 2024 02:55:03 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e31d2dbe903ff2a67c3116f4d4b13e66369583246f3fe724a34c9a17826c11cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154934459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a5a914b4f37e209816668d0034b75a3c5bce6d5f64b38104e9d6b316166798`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:19:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:19:47 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Fri, 16 Feb 2024 05:19:48 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 05:19:48 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2024 05:36:11 GMT
ENV ROS_DISTRO=rolling
# Fri, 16 Feb 2024 05:36:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:36:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 16 Feb 2024 05:36:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2024 05:36:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58d1c96678c838f4d5f7c9f40f8248208e9176227ee91f318afa92eaa15509b`  
		Last Modified: Fri, 16 Feb 2024 05:39:56 GMT  
		Size: 1.2 MB (1216357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5844573deaff285dfd056ae1a7713800357ebc01f1c3d163b7f58ba1469a1c8f`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 3.8 MB (3800568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddacd785c7e69418c66ed7aedb4b58a560cc91670e23cf08e757483f161ebe60`  
		Last Modified: Fri, 16 Feb 2024 05:39:53 GMT  
		Size: 2.0 KB (2022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fcdb1a8e7770851176fd0f70a4eaaa230431223a4b3dd238f309095be8f3b7`  
		Last Modified: Fri, 16 Feb 2024 05:39:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f5ba27e09156f2abd707c31ae4b3c30fba1cb7cc093834e02213c76a491920`  
		Last Modified: Fri, 16 Feb 2024 05:44:56 GMT  
		Size: 121.5 MB (121514724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c354b27f981f31060a6bc28d16882869ff3cea5aa8f51e2f01aeb59d51cb2d4b`  
		Last Modified: Fri, 16 Feb 2024 05:44:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
