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
$ docker pull ros@sha256:21f9b375b1d4a89a6be7df9f9e16226adb6c22a0b00636c4aaebb0f1d94d447f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:75c0cb090ceb7df06886e441dd4bc631926bbcdd7afc0e0d81a0b602c7b8676d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263536467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bffe566456e658f822a7fe6639d7416c2bcd8d721adcb683ee798e30393dda`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:52:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:53:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 03:53:09 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV ROS_DISTRO=humble
# Thu, 02 May 2024 03:54:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:54:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 03:54:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 03:54:45 GMT
CMD ["bash"]
# Thu, 02 May 2024 03:55:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:55:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 03:55:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 03:56:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241eb05ebc5e6ea5f32f2caf6dd3c37d4f0f42a159ad0e1d4c0c246b5c579d`  
		Last Modified: Thu, 02 May 2024 04:23:00 GMT  
		Size: 1.2 MB (1214648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed01123290208c9ef427cac5587ee6a8c9fe8436b7ef5b42cd25485488b6eed7`  
		Last Modified: Thu, 02 May 2024 04:22:58 GMT  
		Size: 3.8 MB (3829571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4421d97df0323dadf48afbce56f12c3ba90a5bf89b3c2fe15d7d020a3b641ff`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f513a41943ab224507627773bca05b495269f5ab3b28699f90dad15339a59b1`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1879d69635a4959bc89d1dde41dcc2301611c85aaa81c97927842f2c91aa21ab`  
		Last Modified: Thu, 02 May 2024 04:23:13 GMT  
		Size: 106.5 MB (106483069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb6f24d072dea4bb47d142b42a63cf859b9f4b3465cdc8d7a969a16a0d41ce0`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bf28d34f5067790b257e942b80bb9163a6e065cbdd25f31f22ec0b2184d60f`  
		Last Modified: Thu, 02 May 2024 04:23:36 GMT  
		Size: 98.1 MB (98144552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ce4e76da8053503a90eab1800bcc134e4fe971d8ce33cd3b1f49cca69a8e62`  
		Last Modified: Thu, 02 May 2024 04:23:23 GMT  
		Size: 318.6 KB (318631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6504ec22124445470d795d45cf380d7f456cb8ab82eb4331070d9541a058567c`  
		Last Modified: Thu, 02 May 2024 04:23:23 GMT  
		Size: 2.5 KB (2480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe5a8233a9ad7f74178a851247c83d9ba97f54c0dbef6d4fcd429b6de002874`  
		Last Modified: Thu, 02 May 2024 04:23:27 GMT  
		Size: 23.1 MB (23101378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c31d82f3ba351376d516d401d19762509aa1d9ccef236b2218bb0a56de160921
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256155507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3835b03b534ad13ede7d3581db60cdee3e5a002fb585c9bb666c093ee785588`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:50:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:50:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 01:50:38 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:50:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 01:50:39 GMT
ENV ROS_DISTRO=humble
# Thu, 02 May 2024 01:51:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:51:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 01:51:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 01:51:54 GMT
CMD ["bash"]
# Thu, 02 May 2024 01:52:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:52:35 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 01:52:39 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 01:53:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b98a01e18caa44fca308118b2642ea1421284f3e1a78c8e3ccf7acc9ef0d6b`  
		Last Modified: Thu, 02 May 2024 02:28:23 GMT  
		Size: 1.2 MB (1215198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c8a40f001666a8880755fe6ca8f93d5720196592b2f27661076aadf3f0f5c`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 3.8 MB (3801595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb1b0e62af26fc19758e95e3537df8d155c07712f502a5b71f5d2ca3d9736f8`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d471f288eff37436fb649dd79b38c81f05f50772590927e9126129bbd5207`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509cd74b317af888c828eaa210af614cdc02cf60c703efb6a96fbfefbc117d98`  
		Last Modified: Thu, 02 May 2024 02:28:41 GMT  
		Size: 104.2 MB (104203704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79337a550a6b91ed51d48ae3efe36d87a32a0f53df59b33e1af0a19c4a616ad1`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26db6393e0d50752ece84aa012c083ec2e765fbc6c29d51b7332a383c0edfa11`  
		Last Modified: Thu, 02 May 2024 02:29:00 GMT  
		Size: 95.7 MB (95689496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7673b38fa65d4dd14d96df37491248cf3d2301a7f0fb2ab2a7adee845f4fb1`  
		Last Modified: Thu, 02 May 2024 02:28:49 GMT  
		Size: 318.6 KB (318615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040d7a25c1861364a9439ae412e6675c329c4870c86961a7190455ebb6e78f99`  
		Last Modified: Thu, 02 May 2024 02:28:49 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d776fd0281a8bf1b7893046cd99c81b1ba582c0b59fc6235cf52e743dbb409`  
		Last Modified: Thu, 02 May 2024 02:28:53 GMT  
		Size: 22.5 MB (22520746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception`

```console
$ docker pull ros@sha256:76cbc14b927751267c5a3068343cb532f71a157d2b1a3a9ed1c116e571149f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:5e89ff59efbb078a85138b0f80de643568d8055ae762ed2fd8d2e98af69ffcf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.0 MB (955044782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c3b909fd12cf21256f93a76b1abf07d0bda67d6d70adf68623a31aa4782c60`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:52:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:53:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 03:53:09 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV ROS_DISTRO=humble
# Thu, 02 May 2024 03:54:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:54:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 03:54:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 03:54:45 GMT
CMD ["bash"]
# Thu, 02 May 2024 03:55:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:55:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 03:55:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 03:56:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241eb05ebc5e6ea5f32f2caf6dd3c37d4f0f42a159ad0e1d4c0c246b5c579d`  
		Last Modified: Thu, 02 May 2024 04:23:00 GMT  
		Size: 1.2 MB (1214648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed01123290208c9ef427cac5587ee6a8c9fe8436b7ef5b42cd25485488b6eed7`  
		Last Modified: Thu, 02 May 2024 04:22:58 GMT  
		Size: 3.8 MB (3829571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4421d97df0323dadf48afbce56f12c3ba90a5bf89b3c2fe15d7d020a3b641ff`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f513a41943ab224507627773bca05b495269f5ab3b28699f90dad15339a59b1`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1879d69635a4959bc89d1dde41dcc2301611c85aaa81c97927842f2c91aa21ab`  
		Last Modified: Thu, 02 May 2024 04:23:13 GMT  
		Size: 106.5 MB (106483069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb6f24d072dea4bb47d142b42a63cf859b9f4b3465cdc8d7a969a16a0d41ce0`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bf28d34f5067790b257e942b80bb9163a6e065cbdd25f31f22ec0b2184d60f`  
		Last Modified: Thu, 02 May 2024 04:23:36 GMT  
		Size: 98.1 MB (98144552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ce4e76da8053503a90eab1800bcc134e4fe971d8ce33cd3b1f49cca69a8e62`  
		Last Modified: Thu, 02 May 2024 04:23:23 GMT  
		Size: 318.6 KB (318631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6504ec22124445470d795d45cf380d7f456cb8ab82eb4331070d9541a058567c`  
		Last Modified: Thu, 02 May 2024 04:23:23 GMT  
		Size: 2.5 KB (2480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe5a8233a9ad7f74178a851247c83d9ba97f54c0dbef6d4fcd429b6de002874`  
		Last Modified: Thu, 02 May 2024 04:23:27 GMT  
		Size: 23.1 MB (23101378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea05761ab4a89d59e7ed163b729bcf7c144a6e7074d8d268c4c6df6ee762f04`  
		Last Modified: Thu, 02 May 2024 04:25:17 GMT  
		Size: 691.5 MB (691508315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8668a14387e321d0f7d90523e31482279d1af4c6dfaea8f8adcd26ed26b7fc08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.6 MB (915617873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3cc9424e571cce205b1f5aafe818c877b19deeeb141f7b8eb324d7e36c540a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:50:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:50:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 01:50:38 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:50:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 01:50:39 GMT
ENV ROS_DISTRO=humble
# Thu, 02 May 2024 01:51:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:51:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 01:51:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 01:51:54 GMT
CMD ["bash"]
# Thu, 02 May 2024 01:52:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:52:35 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 01:52:39 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 01:53:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:07:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b98a01e18caa44fca308118b2642ea1421284f3e1a78c8e3ccf7acc9ef0d6b`  
		Last Modified: Thu, 02 May 2024 02:28:23 GMT  
		Size: 1.2 MB (1215198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c8a40f001666a8880755fe6ca8f93d5720196592b2f27661076aadf3f0f5c`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 3.8 MB (3801595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb1b0e62af26fc19758e95e3537df8d155c07712f502a5b71f5d2ca3d9736f8`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d471f288eff37436fb649dd79b38c81f05f50772590927e9126129bbd5207`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509cd74b317af888c828eaa210af614cdc02cf60c703efb6a96fbfefbc117d98`  
		Last Modified: Thu, 02 May 2024 02:28:41 GMT  
		Size: 104.2 MB (104203704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79337a550a6b91ed51d48ae3efe36d87a32a0f53df59b33e1af0a19c4a616ad1`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26db6393e0d50752ece84aa012c083ec2e765fbc6c29d51b7332a383c0edfa11`  
		Last Modified: Thu, 02 May 2024 02:29:00 GMT  
		Size: 95.7 MB (95689496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7673b38fa65d4dd14d96df37491248cf3d2301a7f0fb2ab2a7adee845f4fb1`  
		Last Modified: Thu, 02 May 2024 02:28:49 GMT  
		Size: 318.6 KB (318615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040d7a25c1861364a9439ae412e6675c329c4870c86961a7190455ebb6e78f99`  
		Last Modified: Thu, 02 May 2024 02:28:49 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d776fd0281a8bf1b7893046cd99c81b1ba582c0b59fc6235cf52e743dbb409`  
		Last Modified: Thu, 02 May 2024 02:28:53 GMT  
		Size: 22.5 MB (22520746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799c0af82dd605deb4c57beff9a1e2ca2b703f60b1633ab5221ff8a76ba6e437`  
		Last Modified: Thu, 02 May 2024 02:30:36 GMT  
		Size: 659.5 MB (659462366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:76cbc14b927751267c5a3068343cb532f71a157d2b1a3a9ed1c116e571149f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:5e89ff59efbb078a85138b0f80de643568d8055ae762ed2fd8d2e98af69ffcf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **955.0 MB (955044782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c3b909fd12cf21256f93a76b1abf07d0bda67d6d70adf68623a31aa4782c60`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:52:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:53:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 03:53:09 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV ROS_DISTRO=humble
# Thu, 02 May 2024 03:54:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:54:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 03:54:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 03:54:45 GMT
CMD ["bash"]
# Thu, 02 May 2024 03:55:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:55:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 03:55:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 03:56:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241eb05ebc5e6ea5f32f2caf6dd3c37d4f0f42a159ad0e1d4c0c246b5c579d`  
		Last Modified: Thu, 02 May 2024 04:23:00 GMT  
		Size: 1.2 MB (1214648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed01123290208c9ef427cac5587ee6a8c9fe8436b7ef5b42cd25485488b6eed7`  
		Last Modified: Thu, 02 May 2024 04:22:58 GMT  
		Size: 3.8 MB (3829571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4421d97df0323dadf48afbce56f12c3ba90a5bf89b3c2fe15d7d020a3b641ff`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f513a41943ab224507627773bca05b495269f5ab3b28699f90dad15339a59b1`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1879d69635a4959bc89d1dde41dcc2301611c85aaa81c97927842f2c91aa21ab`  
		Last Modified: Thu, 02 May 2024 04:23:13 GMT  
		Size: 106.5 MB (106483069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb6f24d072dea4bb47d142b42a63cf859b9f4b3465cdc8d7a969a16a0d41ce0`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bf28d34f5067790b257e942b80bb9163a6e065cbdd25f31f22ec0b2184d60f`  
		Last Modified: Thu, 02 May 2024 04:23:36 GMT  
		Size: 98.1 MB (98144552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ce4e76da8053503a90eab1800bcc134e4fe971d8ce33cd3b1f49cca69a8e62`  
		Last Modified: Thu, 02 May 2024 04:23:23 GMT  
		Size: 318.6 KB (318631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6504ec22124445470d795d45cf380d7f456cb8ab82eb4331070d9541a058567c`  
		Last Modified: Thu, 02 May 2024 04:23:23 GMT  
		Size: 2.5 KB (2480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe5a8233a9ad7f74178a851247c83d9ba97f54c0dbef6d4fcd429b6de002874`  
		Last Modified: Thu, 02 May 2024 04:23:27 GMT  
		Size: 23.1 MB (23101378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea05761ab4a89d59e7ed163b729bcf7c144a6e7074d8d268c4c6df6ee762f04`  
		Last Modified: Thu, 02 May 2024 04:25:17 GMT  
		Size: 691.5 MB (691508315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8668a14387e321d0f7d90523e31482279d1af4c6dfaea8f8adcd26ed26b7fc08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **915.6 MB (915617873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3cc9424e571cce205b1f5aafe818c877b19deeeb141f7b8eb324d7e36c540a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:50:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:50:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 01:50:38 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:50:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 01:50:39 GMT
ENV ROS_DISTRO=humble
# Thu, 02 May 2024 01:51:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:51:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 01:51:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 01:51:54 GMT
CMD ["bash"]
# Thu, 02 May 2024 01:52:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:52:35 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 01:52:39 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 01:53:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:07:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b98a01e18caa44fca308118b2642ea1421284f3e1a78c8e3ccf7acc9ef0d6b`  
		Last Modified: Thu, 02 May 2024 02:28:23 GMT  
		Size: 1.2 MB (1215198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c8a40f001666a8880755fe6ca8f93d5720196592b2f27661076aadf3f0f5c`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 3.8 MB (3801595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb1b0e62af26fc19758e95e3537df8d155c07712f502a5b71f5d2ca3d9736f8`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d471f288eff37436fb649dd79b38c81f05f50772590927e9126129bbd5207`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509cd74b317af888c828eaa210af614cdc02cf60c703efb6a96fbfefbc117d98`  
		Last Modified: Thu, 02 May 2024 02:28:41 GMT  
		Size: 104.2 MB (104203704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79337a550a6b91ed51d48ae3efe36d87a32a0f53df59b33e1af0a19c4a616ad1`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26db6393e0d50752ece84aa012c083ec2e765fbc6c29d51b7332a383c0edfa11`  
		Last Modified: Thu, 02 May 2024 02:29:00 GMT  
		Size: 95.7 MB (95689496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7673b38fa65d4dd14d96df37491248cf3d2301a7f0fb2ab2a7adee845f4fb1`  
		Last Modified: Thu, 02 May 2024 02:28:49 GMT  
		Size: 318.6 KB (318615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040d7a25c1861364a9439ae412e6675c329c4870c86961a7190455ebb6e78f99`  
		Last Modified: Thu, 02 May 2024 02:28:49 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d776fd0281a8bf1b7893046cd99c81b1ba582c0b59fc6235cf52e743dbb409`  
		Last Modified: Thu, 02 May 2024 02:28:53 GMT  
		Size: 22.5 MB (22520746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799c0af82dd605deb4c57beff9a1e2ca2b703f60b1633ab5221ff8a76ba6e437`  
		Last Modified: Thu, 02 May 2024 02:30:36 GMT  
		Size: 659.5 MB (659462366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:21f9b375b1d4a89a6be7df9f9e16226adb6c22a0b00636c4aaebb0f1d94d447f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:75c0cb090ceb7df06886e441dd4bc631926bbcdd7afc0e0d81a0b602c7b8676d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263536467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bffe566456e658f822a7fe6639d7416c2bcd8d721adcb683ee798e30393dda`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:52:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:53:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 03:53:09 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV ROS_DISTRO=humble
# Thu, 02 May 2024 03:54:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:54:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 03:54:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 03:54:45 GMT
CMD ["bash"]
# Thu, 02 May 2024 03:55:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:55:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 03:55:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 03:56:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241eb05ebc5e6ea5f32f2caf6dd3c37d4f0f42a159ad0e1d4c0c246b5c579d`  
		Last Modified: Thu, 02 May 2024 04:23:00 GMT  
		Size: 1.2 MB (1214648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed01123290208c9ef427cac5587ee6a8c9fe8436b7ef5b42cd25485488b6eed7`  
		Last Modified: Thu, 02 May 2024 04:22:58 GMT  
		Size: 3.8 MB (3829571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4421d97df0323dadf48afbce56f12c3ba90a5bf89b3c2fe15d7d020a3b641ff`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f513a41943ab224507627773bca05b495269f5ab3b28699f90dad15339a59b1`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1879d69635a4959bc89d1dde41dcc2301611c85aaa81c97927842f2c91aa21ab`  
		Last Modified: Thu, 02 May 2024 04:23:13 GMT  
		Size: 106.5 MB (106483069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb6f24d072dea4bb47d142b42a63cf859b9f4b3465cdc8d7a969a16a0d41ce0`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bf28d34f5067790b257e942b80bb9163a6e065cbdd25f31f22ec0b2184d60f`  
		Last Modified: Thu, 02 May 2024 04:23:36 GMT  
		Size: 98.1 MB (98144552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ce4e76da8053503a90eab1800bcc134e4fe971d8ce33cd3b1f49cca69a8e62`  
		Last Modified: Thu, 02 May 2024 04:23:23 GMT  
		Size: 318.6 KB (318631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6504ec22124445470d795d45cf380d7f456cb8ab82eb4331070d9541a058567c`  
		Last Modified: Thu, 02 May 2024 04:23:23 GMT  
		Size: 2.5 KB (2480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe5a8233a9ad7f74178a851247c83d9ba97f54c0dbef6d4fcd429b6de002874`  
		Last Modified: Thu, 02 May 2024 04:23:27 GMT  
		Size: 23.1 MB (23101378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c31d82f3ba351376d516d401d19762509aa1d9ccef236b2218bb0a56de160921
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256155507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3835b03b534ad13ede7d3581db60cdee3e5a002fb585c9bb666c093ee785588`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:50:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:50:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 01:50:38 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:50:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 01:50:39 GMT
ENV ROS_DISTRO=humble
# Thu, 02 May 2024 01:51:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:51:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 01:51:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 01:51:54 GMT
CMD ["bash"]
# Thu, 02 May 2024 01:52:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:52:35 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 01:52:39 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 01:53:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b98a01e18caa44fca308118b2642ea1421284f3e1a78c8e3ccf7acc9ef0d6b`  
		Last Modified: Thu, 02 May 2024 02:28:23 GMT  
		Size: 1.2 MB (1215198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c8a40f001666a8880755fe6ca8f93d5720196592b2f27661076aadf3f0f5c`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 3.8 MB (3801595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb1b0e62af26fc19758e95e3537df8d155c07712f502a5b71f5d2ca3d9736f8`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d471f288eff37436fb649dd79b38c81f05f50772590927e9126129bbd5207`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509cd74b317af888c828eaa210af614cdc02cf60c703efb6a96fbfefbc117d98`  
		Last Modified: Thu, 02 May 2024 02:28:41 GMT  
		Size: 104.2 MB (104203704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79337a550a6b91ed51d48ae3efe36d87a32a0f53df59b33e1af0a19c4a616ad1`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26db6393e0d50752ece84aa012c083ec2e765fbc6c29d51b7332a383c0edfa11`  
		Last Modified: Thu, 02 May 2024 02:29:00 GMT  
		Size: 95.7 MB (95689496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7673b38fa65d4dd14d96df37491248cf3d2301a7f0fb2ab2a7adee845f4fb1`  
		Last Modified: Thu, 02 May 2024 02:28:49 GMT  
		Size: 318.6 KB (318615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040d7a25c1861364a9439ae412e6675c329c4870c86961a7190455ebb6e78f99`  
		Last Modified: Thu, 02 May 2024 02:28:49 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d776fd0281a8bf1b7893046cd99c81b1ba582c0b59fc6235cf52e743dbb409`  
		Last Modified: Thu, 02 May 2024 02:28:53 GMT  
		Size: 22.5 MB (22520746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:21f9b375b1d4a89a6be7df9f9e16226adb6c22a0b00636c4aaebb0f1d94d447f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:75c0cb090ceb7df06886e441dd4bc631926bbcdd7afc0e0d81a0b602c7b8676d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263536467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bffe566456e658f822a7fe6639d7416c2bcd8d721adcb683ee798e30393dda`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:52:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:53:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 03:53:09 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV ROS_DISTRO=humble
# Thu, 02 May 2024 03:54:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:54:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 03:54:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 03:54:45 GMT
CMD ["bash"]
# Thu, 02 May 2024 03:55:46 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:55:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 03:55:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 03:56:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241eb05ebc5e6ea5f32f2caf6dd3c37d4f0f42a159ad0e1d4c0c246b5c579d`  
		Last Modified: Thu, 02 May 2024 04:23:00 GMT  
		Size: 1.2 MB (1214648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed01123290208c9ef427cac5587ee6a8c9fe8436b7ef5b42cd25485488b6eed7`  
		Last Modified: Thu, 02 May 2024 04:22:58 GMT  
		Size: 3.8 MB (3829571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4421d97df0323dadf48afbce56f12c3ba90a5bf89b3c2fe15d7d020a3b641ff`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f513a41943ab224507627773bca05b495269f5ab3b28699f90dad15339a59b1`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1879d69635a4959bc89d1dde41dcc2301611c85aaa81c97927842f2c91aa21ab`  
		Last Modified: Thu, 02 May 2024 04:23:13 GMT  
		Size: 106.5 MB (106483069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb6f24d072dea4bb47d142b42a63cf859b9f4b3465cdc8d7a969a16a0d41ce0`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bf28d34f5067790b257e942b80bb9163a6e065cbdd25f31f22ec0b2184d60f`  
		Last Modified: Thu, 02 May 2024 04:23:36 GMT  
		Size: 98.1 MB (98144552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ce4e76da8053503a90eab1800bcc134e4fe971d8ce33cd3b1f49cca69a8e62`  
		Last Modified: Thu, 02 May 2024 04:23:23 GMT  
		Size: 318.6 KB (318631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6504ec22124445470d795d45cf380d7f456cb8ab82eb4331070d9541a058567c`  
		Last Modified: Thu, 02 May 2024 04:23:23 GMT  
		Size: 2.5 KB (2480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe5a8233a9ad7f74178a851247c83d9ba97f54c0dbef6d4fcd429b6de002874`  
		Last Modified: Thu, 02 May 2024 04:23:27 GMT  
		Size: 23.1 MB (23101378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c31d82f3ba351376d516d401d19762509aa1d9ccef236b2218bb0a56de160921
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256155507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3835b03b534ad13ede7d3581db60cdee3e5a002fb585c9bb666c093ee785588`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:50:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:50:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 01:50:38 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:50:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 01:50:39 GMT
ENV ROS_DISTRO=humble
# Thu, 02 May 2024 01:51:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:51:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 01:51:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 01:51:54 GMT
CMD ["bash"]
# Thu, 02 May 2024 01:52:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:52:35 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 01:52:39 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 01:53:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b98a01e18caa44fca308118b2642ea1421284f3e1a78c8e3ccf7acc9ef0d6b`  
		Last Modified: Thu, 02 May 2024 02:28:23 GMT  
		Size: 1.2 MB (1215198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c8a40f001666a8880755fe6ca8f93d5720196592b2f27661076aadf3f0f5c`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 3.8 MB (3801595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb1b0e62af26fc19758e95e3537df8d155c07712f502a5b71f5d2ca3d9736f8`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d471f288eff37436fb649dd79b38c81f05f50772590927e9126129bbd5207`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509cd74b317af888c828eaa210af614cdc02cf60c703efb6a96fbfefbc117d98`  
		Last Modified: Thu, 02 May 2024 02:28:41 GMT  
		Size: 104.2 MB (104203704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79337a550a6b91ed51d48ae3efe36d87a32a0f53df59b33e1af0a19c4a616ad1`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26db6393e0d50752ece84aa012c083ec2e765fbc6c29d51b7332a383c0edfa11`  
		Last Modified: Thu, 02 May 2024 02:29:00 GMT  
		Size: 95.7 MB (95689496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7673b38fa65d4dd14d96df37491248cf3d2301a7f0fb2ab2a7adee845f4fb1`  
		Last Modified: Thu, 02 May 2024 02:28:49 GMT  
		Size: 318.6 KB (318615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040d7a25c1861364a9439ae412e6675c329c4870c86961a7190455ebb6e78f99`  
		Last Modified: Thu, 02 May 2024 02:28:49 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d776fd0281a8bf1b7893046cd99c81b1ba582c0b59fc6235cf52e743dbb409`  
		Last Modified: Thu, 02 May 2024 02:28:53 GMT  
		Size: 22.5 MB (22520746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:eb78c6e7f45c08210500beb5f0b1f54936b26f94e622abcb14d4a87a4cc968f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:9034628a90878e0c506088d85c4789a5a57ab1b0e21c747732e574332367f949
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141969426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2cae1957db5b4de3187baf4f62077716b2bd3607f0e73f5002494804378010`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:52:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:53:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 03:53:09 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV ROS_DISTRO=humble
# Thu, 02 May 2024 03:54:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:54:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 03:54:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 03:54:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241eb05ebc5e6ea5f32f2caf6dd3c37d4f0f42a159ad0e1d4c0c246b5c579d`  
		Last Modified: Thu, 02 May 2024 04:23:00 GMT  
		Size: 1.2 MB (1214648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed01123290208c9ef427cac5587ee6a8c9fe8436b7ef5b42cd25485488b6eed7`  
		Last Modified: Thu, 02 May 2024 04:22:58 GMT  
		Size: 3.8 MB (3829571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4421d97df0323dadf48afbce56f12c3ba90a5bf89b3c2fe15d7d020a3b641ff`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f513a41943ab224507627773bca05b495269f5ab3b28699f90dad15339a59b1`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1879d69635a4959bc89d1dde41dcc2301611c85aaa81c97927842f2c91aa21ab`  
		Last Modified: Thu, 02 May 2024 04:23:13 GMT  
		Size: 106.5 MB (106483069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb6f24d072dea4bb47d142b42a63cf859b9f4b3465cdc8d7a969a16a0d41ce0`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:07123e8516d8c513f7e583b7377dfc00821eeacd74f657e389f2f399a8745e05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137624163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9230aa2a4bd437148b6a8161e29bdc12a1835b5c87e8f2cca4917ea27a7ea8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:50:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:50:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 01:50:38 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:50:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 01:50:39 GMT
ENV ROS_DISTRO=humble
# Thu, 02 May 2024 01:51:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:51:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 01:51:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 01:51:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b98a01e18caa44fca308118b2642ea1421284f3e1a78c8e3ccf7acc9ef0d6b`  
		Last Modified: Thu, 02 May 2024 02:28:23 GMT  
		Size: 1.2 MB (1215198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c8a40f001666a8880755fe6ca8f93d5720196592b2f27661076aadf3f0f5c`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 3.8 MB (3801595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb1b0e62af26fc19758e95e3537df8d155c07712f502a5b71f5d2ca3d9736f8`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d471f288eff37436fb649dd79b38c81f05f50772590927e9126129bbd5207`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509cd74b317af888c828eaa210af614cdc02cf60c703efb6a96fbfefbc117d98`  
		Last Modified: Thu, 02 May 2024 02:28:41 GMT  
		Size: 104.2 MB (104203704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79337a550a6b91ed51d48ae3efe36d87a32a0f53df59b33e1af0a19c4a616ad1`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:eb78c6e7f45c08210500beb5f0b1f54936b26f94e622abcb14d4a87a4cc968f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:9034628a90878e0c506088d85c4789a5a57ab1b0e21c747732e574332367f949
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141969426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2cae1957db5b4de3187baf4f62077716b2bd3607f0e73f5002494804378010`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:52:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:53:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 03:53:09 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV ROS_DISTRO=humble
# Thu, 02 May 2024 03:54:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:54:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 03:54:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 03:54:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241eb05ebc5e6ea5f32f2caf6dd3c37d4f0f42a159ad0e1d4c0c246b5c579d`  
		Last Modified: Thu, 02 May 2024 04:23:00 GMT  
		Size: 1.2 MB (1214648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed01123290208c9ef427cac5587ee6a8c9fe8436b7ef5b42cd25485488b6eed7`  
		Last Modified: Thu, 02 May 2024 04:22:58 GMT  
		Size: 3.8 MB (3829571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4421d97df0323dadf48afbce56f12c3ba90a5bf89b3c2fe15d7d020a3b641ff`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f513a41943ab224507627773bca05b495269f5ab3b28699f90dad15339a59b1`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1879d69635a4959bc89d1dde41dcc2301611c85aaa81c97927842f2c91aa21ab`  
		Last Modified: Thu, 02 May 2024 04:23:13 GMT  
		Size: 106.5 MB (106483069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb6f24d072dea4bb47d142b42a63cf859b9f4b3465cdc8d7a969a16a0d41ce0`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:07123e8516d8c513f7e583b7377dfc00821eeacd74f657e389f2f399a8745e05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137624163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9230aa2a4bd437148b6a8161e29bdc12a1835b5c87e8f2cca4917ea27a7ea8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:50:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:50:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 01:50:38 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:50:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 01:50:39 GMT
ENV ROS_DISTRO=humble
# Thu, 02 May 2024 01:51:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:51:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 01:51:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 01:51:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b98a01e18caa44fca308118b2642ea1421284f3e1a78c8e3ccf7acc9ef0d6b`  
		Last Modified: Thu, 02 May 2024 02:28:23 GMT  
		Size: 1.2 MB (1215198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c8a40f001666a8880755fe6ca8f93d5720196592b2f27661076aadf3f0f5c`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 3.8 MB (3801595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb1b0e62af26fc19758e95e3537df8d155c07712f502a5b71f5d2ca3d9736f8`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d471f288eff37436fb649dd79b38c81f05f50772590927e9126129bbd5207`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509cd74b317af888c828eaa210af614cdc02cf60c703efb6a96fbfefbc117d98`  
		Last Modified: Thu, 02 May 2024 02:28:41 GMT  
		Size: 104.2 MB (104203704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79337a550a6b91ed51d48ae3efe36d87a32a0f53df59b33e1af0a19c4a616ad1`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron`

```console
$ docker pull ros@sha256:4c1352c7ae7c86cd6f8321c7de79ebd68c4f694c23b2ad1de4012771004cddf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron` - linux; amd64

```console
$ docker pull ros@sha256:1384517a1a88001154a0b866cf0c5c9c313e6cd99329b274bc4ab837fb031e6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268930393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd71a4fb909dc656e5ac662b3cf086312ab0cbf3ef3e10c00941bee65a47d21`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:52:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:53:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 03:53:09 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 04:04:48 GMT
ENV ROS_DISTRO=iron
# Thu, 02 May 2024 04:05:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:05:36 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 04:05:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 04:05:36 GMT
CMD ["bash"]
# Thu, 02 May 2024 04:06:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:06:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 04:06:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 04:06:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241eb05ebc5e6ea5f32f2caf6dd3c37d4f0f42a159ad0e1d4c0c246b5c579d`  
		Last Modified: Thu, 02 May 2024 04:23:00 GMT  
		Size: 1.2 MB (1214648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed01123290208c9ef427cac5587ee6a8c9fe8436b7ef5b42cd25485488b6eed7`  
		Last Modified: Thu, 02 May 2024 04:22:58 GMT  
		Size: 3.8 MB (3829571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4421d97df0323dadf48afbce56f12c3ba90a5bf89b3c2fe15d7d020a3b641ff`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f513a41943ab224507627773bca05b495269f5ab3b28699f90dad15339a59b1`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d91e0671b73494532cc2f2cb058e2ed66c603366141af0db09b78520be2657`  
		Last Modified: Thu, 02 May 2024 04:25:47 GMT  
		Size: 124.2 MB (124231063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afa36c1c6f86bfca1f25e223d165bfc1e4c9f85816464694f59e1a52c3918db`  
		Last Modified: Thu, 02 May 2024 04:25:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422fedfa5dfaebcc566c7e92541fc27655abe22d8a1f0169b92ff8f1e26027db`  
		Last Modified: Thu, 02 May 2024 04:26:06 GMT  
		Size: 85.2 MB (85172267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253d6e13893607b9fd2bb089d76803f28222334db07a7e6c039347d211e28e75`  
		Last Modified: Thu, 02 May 2024 04:25:56 GMT  
		Size: 304.2 KB (304160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e341714e0e3da5410ec70095a96eeb8251f8070cf3591b0862e78b4fd412f594`  
		Last Modified: Thu, 02 May 2024 04:25:56 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dae7fb87701eea4937f651281711cb460971549f82ead0db6ae4e1e9f3d9b3`  
		Last Modified: Thu, 02 May 2024 04:26:00 GMT  
		Size: 23.7 MB (23734076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:af11fa5cd8c7f9d99336bea199426d0363d049ec677bb23a40ad52d49468db11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261417977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1e0338adc38cb58f920044ca462b59fa1500e84d947adb6bd02529848d37e9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:50:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:50:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 01:50:38 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:50:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 02:07:37 GMT
ENV ROS_DISTRO=iron
# Thu, 02 May 2024 02:08:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:08:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 02:08:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 02:08:24 GMT
CMD ["bash"]
# Thu, 02 May 2024 02:08:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:08:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 02:08:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 02:09:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b98a01e18caa44fca308118b2642ea1421284f3e1a78c8e3ccf7acc9ef0d6b`  
		Last Modified: Thu, 02 May 2024 02:28:23 GMT  
		Size: 1.2 MB (1215198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c8a40f001666a8880755fe6ca8f93d5720196592b2f27661076aadf3f0f5c`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 3.8 MB (3801595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb1b0e62af26fc19758e95e3537df8d155c07712f502a5b71f5d2ca3d9736f8`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d471f288eff37436fb649dd79b38c81f05f50772590927e9126129bbd5207`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a674d9efb72e31cf3dadb7136dc3ff9bd2661e49d9aebc1766fda9652435fa`  
		Last Modified: Thu, 02 May 2024 02:31:09 GMT  
		Size: 121.7 MB (121721772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f0ee788352297555d68b026eac715cd3ed64835dbac315ed8cbe05a0f20c2e`  
		Last Modified: Thu, 02 May 2024 02:30:45 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e141b1e1a2efbe10e3f3075a2d730ebe345b8504c8f84c2ffdfaebc832d186d5`  
		Last Modified: Thu, 02 May 2024 02:31:26 GMT  
		Size: 82.8 MB (82848104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d081fe18a08dd428be0bea55cb3f204c354537ddf7f84b6ba9b308188be65a5`  
		Last Modified: Thu, 02 May 2024 02:31:17 GMT  
		Size: 304.2 KB (304158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315ce52124298db734bb8b0baef727eb109dbb79d7d7201081235658d7da6d8c`  
		Last Modified: Thu, 02 May 2024 02:31:17 GMT  
		Size: 2.5 KB (2525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f5e0de463364cf7347335adf553225674b10caba09d044b782b6383a48194a`  
		Last Modified: Thu, 02 May 2024 02:31:21 GMT  
		Size: 23.1 MB (23120959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-perception`

```console
$ docker pull ros@sha256:b4aa7d47c5efb8c4e8ffdcd6020b45211dec6381a0bd13ffc3bbdc4a6378296d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception` - linux; amd64

```console
$ docker pull ros@sha256:7f6dfc11086c40bebfabe083bd773cf272d6fe6f0f5f25947fb88c6cec2b5ae2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.1 MB (961130287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f36a9892612a1dcee82a9459d97660383eb1d7fd8a1213e0bd79b7e2991a01c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:52:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:53:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 03:53:09 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 04:04:48 GMT
ENV ROS_DISTRO=iron
# Thu, 02 May 2024 04:05:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:05:36 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 04:05:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 04:05:36 GMT
CMD ["bash"]
# Thu, 02 May 2024 04:06:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:06:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 04:06:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 04:06:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241eb05ebc5e6ea5f32f2caf6dd3c37d4f0f42a159ad0e1d4c0c246b5c579d`  
		Last Modified: Thu, 02 May 2024 04:23:00 GMT  
		Size: 1.2 MB (1214648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed01123290208c9ef427cac5587ee6a8c9fe8436b7ef5b42cd25485488b6eed7`  
		Last Modified: Thu, 02 May 2024 04:22:58 GMT  
		Size: 3.8 MB (3829571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4421d97df0323dadf48afbce56f12c3ba90a5bf89b3c2fe15d7d020a3b641ff`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f513a41943ab224507627773bca05b495269f5ab3b28699f90dad15339a59b1`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d91e0671b73494532cc2f2cb058e2ed66c603366141af0db09b78520be2657`  
		Last Modified: Thu, 02 May 2024 04:25:47 GMT  
		Size: 124.2 MB (124231063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afa36c1c6f86bfca1f25e223d165bfc1e4c9f85816464694f59e1a52c3918db`  
		Last Modified: Thu, 02 May 2024 04:25:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422fedfa5dfaebcc566c7e92541fc27655abe22d8a1f0169b92ff8f1e26027db`  
		Last Modified: Thu, 02 May 2024 04:26:06 GMT  
		Size: 85.2 MB (85172267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253d6e13893607b9fd2bb089d76803f28222334db07a7e6c039347d211e28e75`  
		Last Modified: Thu, 02 May 2024 04:25:56 GMT  
		Size: 304.2 KB (304160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e341714e0e3da5410ec70095a96eeb8251f8070cf3591b0862e78b4fd412f594`  
		Last Modified: Thu, 02 May 2024 04:25:56 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dae7fb87701eea4937f651281711cb460971549f82ead0db6ae4e1e9f3d9b3`  
		Last Modified: Thu, 02 May 2024 04:26:00 GMT  
		Size: 23.7 MB (23734076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb85359bb36b142d7f4bd7d8edd9d15e7b05c147f516fa87054fefd9ea0f5798`  
		Last Modified: Thu, 02 May 2024 04:27:46 GMT  
		Size: 692.2 MB (692199894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4afb846ea1d60da761e40c312388f609133bbdee6c5b3b5988744649e9329ccd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.5 MB (921508016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc015eebaf2949da9137113386c2c7922a66a5bb30b9cd2760d113372b57896`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:50:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:50:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 01:50:38 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:50:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 02:07:37 GMT
ENV ROS_DISTRO=iron
# Thu, 02 May 2024 02:08:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:08:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 02:08:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 02:08:24 GMT
CMD ["bash"]
# Thu, 02 May 2024 02:08:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:08:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 02:08:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 02:09:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:10:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b98a01e18caa44fca308118b2642ea1421284f3e1a78c8e3ccf7acc9ef0d6b`  
		Last Modified: Thu, 02 May 2024 02:28:23 GMT  
		Size: 1.2 MB (1215198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c8a40f001666a8880755fe6ca8f93d5720196592b2f27661076aadf3f0f5c`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 3.8 MB (3801595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb1b0e62af26fc19758e95e3537df8d155c07712f502a5b71f5d2ca3d9736f8`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d471f288eff37436fb649dd79b38c81f05f50772590927e9126129bbd5207`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a674d9efb72e31cf3dadb7136dc3ff9bd2661e49d9aebc1766fda9652435fa`  
		Last Modified: Thu, 02 May 2024 02:31:09 GMT  
		Size: 121.7 MB (121721772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f0ee788352297555d68b026eac715cd3ed64835dbac315ed8cbe05a0f20c2e`  
		Last Modified: Thu, 02 May 2024 02:30:45 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e141b1e1a2efbe10e3f3075a2d730ebe345b8504c8f84c2ffdfaebc832d186d5`  
		Last Modified: Thu, 02 May 2024 02:31:26 GMT  
		Size: 82.8 MB (82848104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d081fe18a08dd428be0bea55cb3f204c354537ddf7f84b6ba9b308188be65a5`  
		Last Modified: Thu, 02 May 2024 02:31:17 GMT  
		Size: 304.2 KB (304158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315ce52124298db734bb8b0baef727eb109dbb79d7d7201081235658d7da6d8c`  
		Last Modified: Thu, 02 May 2024 02:31:17 GMT  
		Size: 2.5 KB (2525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f5e0de463364cf7347335adf553225674b10caba09d044b782b6383a48194a`  
		Last Modified: Thu, 02 May 2024 02:31:21 GMT  
		Size: 23.1 MB (23120959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce8148c703f48a18bb69e9fae192639680768cf3617ad602db9c21d28ede665`  
		Last Modified: Thu, 02 May 2024 02:32:59 GMT  
		Size: 660.1 MB (660090039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:b4aa7d47c5efb8c4e8ffdcd6020b45211dec6381a0bd13ffc3bbdc4a6378296d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:7f6dfc11086c40bebfabe083bd773cf272d6fe6f0f5f25947fb88c6cec2b5ae2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **961.1 MB (961130287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f36a9892612a1dcee82a9459d97660383eb1d7fd8a1213e0bd79b7e2991a01c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:52:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:53:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 03:53:09 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 04:04:48 GMT
ENV ROS_DISTRO=iron
# Thu, 02 May 2024 04:05:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:05:36 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 04:05:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 04:05:36 GMT
CMD ["bash"]
# Thu, 02 May 2024 04:06:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:06:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 04:06:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 04:06:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241eb05ebc5e6ea5f32f2caf6dd3c37d4f0f42a159ad0e1d4c0c246b5c579d`  
		Last Modified: Thu, 02 May 2024 04:23:00 GMT  
		Size: 1.2 MB (1214648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed01123290208c9ef427cac5587ee6a8c9fe8436b7ef5b42cd25485488b6eed7`  
		Last Modified: Thu, 02 May 2024 04:22:58 GMT  
		Size: 3.8 MB (3829571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4421d97df0323dadf48afbce56f12c3ba90a5bf89b3c2fe15d7d020a3b641ff`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f513a41943ab224507627773bca05b495269f5ab3b28699f90dad15339a59b1`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d91e0671b73494532cc2f2cb058e2ed66c603366141af0db09b78520be2657`  
		Last Modified: Thu, 02 May 2024 04:25:47 GMT  
		Size: 124.2 MB (124231063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afa36c1c6f86bfca1f25e223d165bfc1e4c9f85816464694f59e1a52c3918db`  
		Last Modified: Thu, 02 May 2024 04:25:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422fedfa5dfaebcc566c7e92541fc27655abe22d8a1f0169b92ff8f1e26027db`  
		Last Modified: Thu, 02 May 2024 04:26:06 GMT  
		Size: 85.2 MB (85172267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253d6e13893607b9fd2bb089d76803f28222334db07a7e6c039347d211e28e75`  
		Last Modified: Thu, 02 May 2024 04:25:56 GMT  
		Size: 304.2 KB (304160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e341714e0e3da5410ec70095a96eeb8251f8070cf3591b0862e78b4fd412f594`  
		Last Modified: Thu, 02 May 2024 04:25:56 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dae7fb87701eea4937f651281711cb460971549f82ead0db6ae4e1e9f3d9b3`  
		Last Modified: Thu, 02 May 2024 04:26:00 GMT  
		Size: 23.7 MB (23734076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb85359bb36b142d7f4bd7d8edd9d15e7b05c147f516fa87054fefd9ea0f5798`  
		Last Modified: Thu, 02 May 2024 04:27:46 GMT  
		Size: 692.2 MB (692199894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4afb846ea1d60da761e40c312388f609133bbdee6c5b3b5988744649e9329ccd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **921.5 MB (921508016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc015eebaf2949da9137113386c2c7922a66a5bb30b9cd2760d113372b57896`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:50:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:50:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 01:50:38 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:50:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 02:07:37 GMT
ENV ROS_DISTRO=iron
# Thu, 02 May 2024 02:08:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:08:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 02:08:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 02:08:24 GMT
CMD ["bash"]
# Thu, 02 May 2024 02:08:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:08:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 02:08:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 02:09:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:10:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b98a01e18caa44fca308118b2642ea1421284f3e1a78c8e3ccf7acc9ef0d6b`  
		Last Modified: Thu, 02 May 2024 02:28:23 GMT  
		Size: 1.2 MB (1215198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c8a40f001666a8880755fe6ca8f93d5720196592b2f27661076aadf3f0f5c`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 3.8 MB (3801595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb1b0e62af26fc19758e95e3537df8d155c07712f502a5b71f5d2ca3d9736f8`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d471f288eff37436fb649dd79b38c81f05f50772590927e9126129bbd5207`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a674d9efb72e31cf3dadb7136dc3ff9bd2661e49d9aebc1766fda9652435fa`  
		Last Modified: Thu, 02 May 2024 02:31:09 GMT  
		Size: 121.7 MB (121721772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f0ee788352297555d68b026eac715cd3ed64835dbac315ed8cbe05a0f20c2e`  
		Last Modified: Thu, 02 May 2024 02:30:45 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e141b1e1a2efbe10e3f3075a2d730ebe345b8504c8f84c2ffdfaebc832d186d5`  
		Last Modified: Thu, 02 May 2024 02:31:26 GMT  
		Size: 82.8 MB (82848104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d081fe18a08dd428be0bea55cb3f204c354537ddf7f84b6ba9b308188be65a5`  
		Last Modified: Thu, 02 May 2024 02:31:17 GMT  
		Size: 304.2 KB (304158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315ce52124298db734bb8b0baef727eb109dbb79d7d7201081235658d7da6d8c`  
		Last Modified: Thu, 02 May 2024 02:31:17 GMT  
		Size: 2.5 KB (2525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f5e0de463364cf7347335adf553225674b10caba09d044b782b6383a48194a`  
		Last Modified: Thu, 02 May 2024 02:31:21 GMT  
		Size: 23.1 MB (23120959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce8148c703f48a18bb69e9fae192639680768cf3617ad602db9c21d28ede665`  
		Last Modified: Thu, 02 May 2024 02:32:59 GMT  
		Size: 660.1 MB (660090039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-base`

```console
$ docker pull ros@sha256:4c1352c7ae7c86cd6f8321c7de79ebd68c4f694c23b2ad1de4012771004cddf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:1384517a1a88001154a0b866cf0c5c9c313e6cd99329b274bc4ab837fb031e6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268930393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd71a4fb909dc656e5ac662b3cf086312ab0cbf3ef3e10c00941bee65a47d21`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:52:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:53:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 03:53:09 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 04:04:48 GMT
ENV ROS_DISTRO=iron
# Thu, 02 May 2024 04:05:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:05:36 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 04:05:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 04:05:36 GMT
CMD ["bash"]
# Thu, 02 May 2024 04:06:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:06:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 04:06:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 04:06:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241eb05ebc5e6ea5f32f2caf6dd3c37d4f0f42a159ad0e1d4c0c246b5c579d`  
		Last Modified: Thu, 02 May 2024 04:23:00 GMT  
		Size: 1.2 MB (1214648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed01123290208c9ef427cac5587ee6a8c9fe8436b7ef5b42cd25485488b6eed7`  
		Last Modified: Thu, 02 May 2024 04:22:58 GMT  
		Size: 3.8 MB (3829571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4421d97df0323dadf48afbce56f12c3ba90a5bf89b3c2fe15d7d020a3b641ff`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f513a41943ab224507627773bca05b495269f5ab3b28699f90dad15339a59b1`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d91e0671b73494532cc2f2cb058e2ed66c603366141af0db09b78520be2657`  
		Last Modified: Thu, 02 May 2024 04:25:47 GMT  
		Size: 124.2 MB (124231063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afa36c1c6f86bfca1f25e223d165bfc1e4c9f85816464694f59e1a52c3918db`  
		Last Modified: Thu, 02 May 2024 04:25:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422fedfa5dfaebcc566c7e92541fc27655abe22d8a1f0169b92ff8f1e26027db`  
		Last Modified: Thu, 02 May 2024 04:26:06 GMT  
		Size: 85.2 MB (85172267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253d6e13893607b9fd2bb089d76803f28222334db07a7e6c039347d211e28e75`  
		Last Modified: Thu, 02 May 2024 04:25:56 GMT  
		Size: 304.2 KB (304160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e341714e0e3da5410ec70095a96eeb8251f8070cf3591b0862e78b4fd412f594`  
		Last Modified: Thu, 02 May 2024 04:25:56 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dae7fb87701eea4937f651281711cb460971549f82ead0db6ae4e1e9f3d9b3`  
		Last Modified: Thu, 02 May 2024 04:26:00 GMT  
		Size: 23.7 MB (23734076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:af11fa5cd8c7f9d99336bea199426d0363d049ec677bb23a40ad52d49468db11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261417977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1e0338adc38cb58f920044ca462b59fa1500e84d947adb6bd02529848d37e9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:50:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:50:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 01:50:38 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:50:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 02:07:37 GMT
ENV ROS_DISTRO=iron
# Thu, 02 May 2024 02:08:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:08:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 02:08:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 02:08:24 GMT
CMD ["bash"]
# Thu, 02 May 2024 02:08:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:08:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 02:08:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 02:09:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b98a01e18caa44fca308118b2642ea1421284f3e1a78c8e3ccf7acc9ef0d6b`  
		Last Modified: Thu, 02 May 2024 02:28:23 GMT  
		Size: 1.2 MB (1215198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c8a40f001666a8880755fe6ca8f93d5720196592b2f27661076aadf3f0f5c`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 3.8 MB (3801595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb1b0e62af26fc19758e95e3537df8d155c07712f502a5b71f5d2ca3d9736f8`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d471f288eff37436fb649dd79b38c81f05f50772590927e9126129bbd5207`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a674d9efb72e31cf3dadb7136dc3ff9bd2661e49d9aebc1766fda9652435fa`  
		Last Modified: Thu, 02 May 2024 02:31:09 GMT  
		Size: 121.7 MB (121721772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f0ee788352297555d68b026eac715cd3ed64835dbac315ed8cbe05a0f20c2e`  
		Last Modified: Thu, 02 May 2024 02:30:45 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e141b1e1a2efbe10e3f3075a2d730ebe345b8504c8f84c2ffdfaebc832d186d5`  
		Last Modified: Thu, 02 May 2024 02:31:26 GMT  
		Size: 82.8 MB (82848104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d081fe18a08dd428be0bea55cb3f204c354537ddf7f84b6ba9b308188be65a5`  
		Last Modified: Thu, 02 May 2024 02:31:17 GMT  
		Size: 304.2 KB (304158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315ce52124298db734bb8b0baef727eb109dbb79d7d7201081235658d7da6d8c`  
		Last Modified: Thu, 02 May 2024 02:31:17 GMT  
		Size: 2.5 KB (2525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f5e0de463364cf7347335adf553225674b10caba09d044b782b6383a48194a`  
		Last Modified: Thu, 02 May 2024 02:31:21 GMT  
		Size: 23.1 MB (23120959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:4c1352c7ae7c86cd6f8321c7de79ebd68c4f694c23b2ad1de4012771004cddf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:1384517a1a88001154a0b866cf0c5c9c313e6cd99329b274bc4ab837fb031e6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268930393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd71a4fb909dc656e5ac662b3cf086312ab0cbf3ef3e10c00941bee65a47d21`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:52:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:53:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 03:53:09 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 04:04:48 GMT
ENV ROS_DISTRO=iron
# Thu, 02 May 2024 04:05:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:05:36 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 04:05:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 04:05:36 GMT
CMD ["bash"]
# Thu, 02 May 2024 04:06:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:06:07 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 04:06:12 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 04:06:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241eb05ebc5e6ea5f32f2caf6dd3c37d4f0f42a159ad0e1d4c0c246b5c579d`  
		Last Modified: Thu, 02 May 2024 04:23:00 GMT  
		Size: 1.2 MB (1214648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed01123290208c9ef427cac5587ee6a8c9fe8436b7ef5b42cd25485488b6eed7`  
		Last Modified: Thu, 02 May 2024 04:22:58 GMT  
		Size: 3.8 MB (3829571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4421d97df0323dadf48afbce56f12c3ba90a5bf89b3c2fe15d7d020a3b641ff`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f513a41943ab224507627773bca05b495269f5ab3b28699f90dad15339a59b1`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d91e0671b73494532cc2f2cb058e2ed66c603366141af0db09b78520be2657`  
		Last Modified: Thu, 02 May 2024 04:25:47 GMT  
		Size: 124.2 MB (124231063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afa36c1c6f86bfca1f25e223d165bfc1e4c9f85816464694f59e1a52c3918db`  
		Last Modified: Thu, 02 May 2024 04:25:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422fedfa5dfaebcc566c7e92541fc27655abe22d8a1f0169b92ff8f1e26027db`  
		Last Modified: Thu, 02 May 2024 04:26:06 GMT  
		Size: 85.2 MB (85172267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253d6e13893607b9fd2bb089d76803f28222334db07a7e6c039347d211e28e75`  
		Last Modified: Thu, 02 May 2024 04:25:56 GMT  
		Size: 304.2 KB (304160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e341714e0e3da5410ec70095a96eeb8251f8070cf3591b0862e78b4fd412f594`  
		Last Modified: Thu, 02 May 2024 04:25:56 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dae7fb87701eea4937f651281711cb460971549f82ead0db6ae4e1e9f3d9b3`  
		Last Modified: Thu, 02 May 2024 04:26:00 GMT  
		Size: 23.7 MB (23734076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:af11fa5cd8c7f9d99336bea199426d0363d049ec677bb23a40ad52d49468db11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261417977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1e0338adc38cb58f920044ca462b59fa1500e84d947adb6bd02529848d37e9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:50:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:50:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 01:50:38 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:50:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 02:07:37 GMT
ENV ROS_DISTRO=iron
# Thu, 02 May 2024 02:08:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:08:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 02:08:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 02:08:24 GMT
CMD ["bash"]
# Thu, 02 May 2024 02:08:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:08:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 02:08:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 02 May 2024 02:09:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b98a01e18caa44fca308118b2642ea1421284f3e1a78c8e3ccf7acc9ef0d6b`  
		Last Modified: Thu, 02 May 2024 02:28:23 GMT  
		Size: 1.2 MB (1215198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c8a40f001666a8880755fe6ca8f93d5720196592b2f27661076aadf3f0f5c`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 3.8 MB (3801595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb1b0e62af26fc19758e95e3537df8d155c07712f502a5b71f5d2ca3d9736f8`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d471f288eff37436fb649dd79b38c81f05f50772590927e9126129bbd5207`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a674d9efb72e31cf3dadb7136dc3ff9bd2661e49d9aebc1766fda9652435fa`  
		Last Modified: Thu, 02 May 2024 02:31:09 GMT  
		Size: 121.7 MB (121721772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f0ee788352297555d68b026eac715cd3ed64835dbac315ed8cbe05a0f20c2e`  
		Last Modified: Thu, 02 May 2024 02:30:45 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e141b1e1a2efbe10e3f3075a2d730ebe345b8504c8f84c2ffdfaebc832d186d5`  
		Last Modified: Thu, 02 May 2024 02:31:26 GMT  
		Size: 82.8 MB (82848104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d081fe18a08dd428be0bea55cb3f204c354537ddf7f84b6ba9b308188be65a5`  
		Last Modified: Thu, 02 May 2024 02:31:17 GMT  
		Size: 304.2 KB (304158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315ce52124298db734bb8b0baef727eb109dbb79d7d7201081235658d7da6d8c`  
		Last Modified: Thu, 02 May 2024 02:31:17 GMT  
		Size: 2.5 KB (2525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f5e0de463364cf7347335adf553225674b10caba09d044b782b6383a48194a`  
		Last Modified: Thu, 02 May 2024 02:31:21 GMT  
		Size: 23.1 MB (23120959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:46f4f84935e605fd771196decb9dfe1e2657ddcfee6799ed8130ea587bec175d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:09cfd88a39f947bdd8748daa71cabf9350280f68118a62617e6651a5a637246f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159717420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53c5a1919b2412065f601e22bfef6b4a2e972de5e03257e7ac9bc09c7296349`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:52:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:53:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 03:53:09 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 04:04:48 GMT
ENV ROS_DISTRO=iron
# Thu, 02 May 2024 04:05:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:05:36 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 04:05:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 04:05:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241eb05ebc5e6ea5f32f2caf6dd3c37d4f0f42a159ad0e1d4c0c246b5c579d`  
		Last Modified: Thu, 02 May 2024 04:23:00 GMT  
		Size: 1.2 MB (1214648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed01123290208c9ef427cac5587ee6a8c9fe8436b7ef5b42cd25485488b6eed7`  
		Last Modified: Thu, 02 May 2024 04:22:58 GMT  
		Size: 3.8 MB (3829571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4421d97df0323dadf48afbce56f12c3ba90a5bf89b3c2fe15d7d020a3b641ff`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f513a41943ab224507627773bca05b495269f5ab3b28699f90dad15339a59b1`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d91e0671b73494532cc2f2cb058e2ed66c603366141af0db09b78520be2657`  
		Last Modified: Thu, 02 May 2024 04:25:47 GMT  
		Size: 124.2 MB (124231063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afa36c1c6f86bfca1f25e223d165bfc1e4c9f85816464694f59e1a52c3918db`  
		Last Modified: Thu, 02 May 2024 04:25:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ebedf8eb9e357afecda1950f766cbf2a8154f189fa44a9db2a32df3a8f3757da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155142231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9c55419e1a1830f07e05de1ec6330fbcb959692e4c52042a1d91bd56ecd453`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:50:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:50:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 01:50:38 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:50:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 02:07:37 GMT
ENV ROS_DISTRO=iron
# Thu, 02 May 2024 02:08:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:08:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 02:08:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 02:08:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b98a01e18caa44fca308118b2642ea1421284f3e1a78c8e3ccf7acc9ef0d6b`  
		Last Modified: Thu, 02 May 2024 02:28:23 GMT  
		Size: 1.2 MB (1215198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c8a40f001666a8880755fe6ca8f93d5720196592b2f27661076aadf3f0f5c`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 3.8 MB (3801595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb1b0e62af26fc19758e95e3537df8d155c07712f502a5b71f5d2ca3d9736f8`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d471f288eff37436fb649dd79b38c81f05f50772590927e9126129bbd5207`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a674d9efb72e31cf3dadb7136dc3ff9bd2661e49d9aebc1766fda9652435fa`  
		Last Modified: Thu, 02 May 2024 02:31:09 GMT  
		Size: 121.7 MB (121721772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f0ee788352297555d68b026eac715cd3ed64835dbac315ed8cbe05a0f20c2e`  
		Last Modified: Thu, 02 May 2024 02:30:45 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-core-jammy`

```console
$ docker pull ros@sha256:46f4f84935e605fd771196decb9dfe1e2657ddcfee6799ed8130ea587bec175d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:09cfd88a39f947bdd8748daa71cabf9350280f68118a62617e6651a5a637246f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159717420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53c5a1919b2412065f601e22bfef6b4a2e972de5e03257e7ac9bc09c7296349`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:52:49 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:07 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:53:08 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:53:09 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 03:53:09 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:53:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 04:04:48 GMT
ENV ROS_DISTRO=iron
# Thu, 02 May 2024 04:05:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:05:36 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 04:05:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 04:05:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43241eb05ebc5e6ea5f32f2caf6dd3c37d4f0f42a159ad0e1d4c0c246b5c579d`  
		Last Modified: Thu, 02 May 2024 04:23:00 GMT  
		Size: 1.2 MB (1214648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed01123290208c9ef427cac5587ee6a8c9fe8436b7ef5b42cd25485488b6eed7`  
		Last Modified: Thu, 02 May 2024 04:22:58 GMT  
		Size: 3.8 MB (3829571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4421d97df0323dadf48afbce56f12c3ba90a5bf89b3c2fe15d7d020a3b641ff`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 2.0 KB (2020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f513a41943ab224507627773bca05b495269f5ab3b28699f90dad15339a59b1`  
		Last Modified: Thu, 02 May 2024 04:22:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d91e0671b73494532cc2f2cb058e2ed66c603366141af0db09b78520be2657`  
		Last Modified: Thu, 02 May 2024 04:25:47 GMT  
		Size: 124.2 MB (124231063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afa36c1c6f86bfca1f25e223d165bfc1e4c9f85816464694f59e1a52c3918db`  
		Last Modified: Thu, 02 May 2024 04:25:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ebedf8eb9e357afecda1950f766cbf2a8154f189fa44a9db2a32df3a8f3757da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155142231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9c55419e1a1830f07e05de1ec6330fbcb959692e4c52042a1d91bd56ecd453`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:50:31 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:37 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:38 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:50:38 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 01:50:38 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:50:38 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 02:07:37 GMT
ENV ROS_DISTRO=iron
# Thu, 02 May 2024 02:08:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:08:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Thu, 02 May 2024 02:08:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 02:08:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b98a01e18caa44fca308118b2642ea1421284f3e1a78c8e3ccf7acc9ef0d6b`  
		Last Modified: Thu, 02 May 2024 02:28:23 GMT  
		Size: 1.2 MB (1215198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c8a40f001666a8880755fe6ca8f93d5720196592b2f27661076aadf3f0f5c`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 3.8 MB (3801595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb1b0e62af26fc19758e95e3537df8d155c07712f502a5b71f5d2ca3d9736f8`  
		Last Modified: Thu, 02 May 2024 02:28:20 GMT  
		Size: 2.0 KB (2018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d471f288eff37436fb649dd79b38c81f05f50772590927e9126129bbd5207`  
		Last Modified: Thu, 02 May 2024 02:28:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a674d9efb72e31cf3dadb7136dc3ff9bd2661e49d9aebc1766fda9652435fa`  
		Last Modified: Thu, 02 May 2024 02:31:09 GMT  
		Size: 121.7 MB (121721772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f0ee788352297555d68b026eac715cd3ed64835dbac315ed8cbe05a0f20c2e`  
		Last Modified: Thu, 02 May 2024 02:30:45 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy`

```console
$ docker pull ros@sha256:792f28ddc091984c1b2fcd9f780d0cbb4094accdead971724f4762512dc5c5f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy` - linux; amd64

```console
$ docker pull ros@sha256:94903a2e6311026989fbe35c31cacd5e509d5a860bc374467d4ed161d39f70b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302117951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1de2625d3b31b7c6871791708581b2df681f6937ae7006b2cb3feeab1b0de1d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 04:08:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:17:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 04:17:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 04:17:14 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 00:50:47 GMT
ENV ROS_DISTRO=jazzy
# Fri, 24 May 2024 00:52:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 00:52:25 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 00:52:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 00:52:25 GMT
CMD ["bash"]
# Fri, 24 May 2024 00:53:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 00:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 00:53:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 00:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60661c1b414a0df1f47a75ebe6ee30ab62a190e137eadd8830b58f26d265393`  
		Last Modified: Thu, 02 May 2024 04:27:58 GMT  
		Size: 683.6 KB (683555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c08bb4286c80bd46824cabefede6374d8260920dfcae18a52d6db76894e5e4b`  
		Last Modified: Thu, 02 May 2024 04:27:57 GMT  
		Size: 4.6 MB (4617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f6c812b379d4de9914ffcc55c356485f1907555705bd50fdf0629e37742e9`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78533fe08fdd62d113279815db4b7a14ab1686b1f85f09290bc47b27da4004e`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55164a1d20560b2ddf50794087c404c33f1f5aba7b4692b56e05bf7e787727e9`  
		Last Modified: Fri, 24 May 2024 00:59:12 GMT  
		Size: 124.8 MB (124818119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9069c48a70ab1176dafef8ed3f1a3c7bc5e0f555f8a0604ed3c71c343c6f50`  
		Last Modified: Fri, 24 May 2024 00:58:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc72deef87e0bd3e2b9fb1b1332ebb772e7570201e69d13a80a786526c9cc825`  
		Last Modified: Fri, 24 May 2024 00:59:36 GMT  
		Size: 114.3 MB (114312618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c3e4cc06ea4818223f482308fe858138535f4b16b60e6ea752908b0c818b13`  
		Last Modified: Fri, 24 May 2024 00:59:21 GMT  
		Size: 310.6 KB (310567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed492ab0db3f83a748a510c07a2f30f503a9e2a1ef38bf73806def6cc0aca245`  
		Last Modified: Fri, 24 May 2024 00:59:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14706106e0f4a9775057016e557106aa7abafdf3f95290bf62f5d740cd66c60`  
		Last Modified: Fri, 24 May 2024 00:59:25 GMT  
		Size: 27.7 MB (27668097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:291f4c0bebacd781250a880a256d8834646030bb6066ec99ec088af1a845df0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292073626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb57bb1324bca2415c246a1b26b2b2ccb527b81e52135e310a9b102acb8c4c4c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:11:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:11:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:23:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 02:23:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 02:23:04 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 01:05:39 GMT
ENV ROS_DISTRO=jazzy
# Fri, 24 May 2024 01:07:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 01:07:40 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 01:07:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 01:07:41 GMT
CMD ["bash"]
# Fri, 24 May 2024 01:08:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 01:08:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 01:08:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 01:09:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6566430a89b8fd522af510326683dfd547bb47ce3368e0e7c13d03c03a259a73`  
		Last Modified: Thu, 02 May 2024 02:33:11 GMT  
		Size: 683.8 KB (683795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c10c1a69a349bd188a99420ce3e817a3ff04579654dbb1e5fcabc0a226ba0dd`  
		Last Modified: Thu, 02 May 2024 02:33:09 GMT  
		Size: 4.6 MB (4611814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6931defe7f57cf3da1981f2afca9fe611d4b03bf445f980fdc842c4d965bf247`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5315899036e815d56227da46abcb970890f5f1c1388a96cdf9d489dd96e5d058`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0141a49b3e805ba91547642bc9811564e0c44e7380c198e9fe12fd131322ebea`  
		Last Modified: Fri, 24 May 2024 01:15:49 GMT  
		Size: 119.5 MB (119457025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b13531948b1b0049cfd52836e87118bf8b05d8a3852f052b1a18ea633ba4053`  
		Last Modified: Fri, 24 May 2024 01:15:35 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f2b8c0b62382bad46d18ffa279fb2e701a853dbc8f1457806b0140841a622a`  
		Last Modified: Fri, 24 May 2024 01:16:08 GMT  
		Size: 111.2 MB (111153710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33ace28299c354a7a02a6f44bd73e5385aca4a3b0eb87a26f9fe3eb9c2c322d`  
		Last Modified: Fri, 24 May 2024 01:15:57 GMT  
		Size: 310.6 KB (310587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dab07297abace30add756a2eac059cf770c1ed9122df19c8d1e4a9ee2a1300`  
		Last Modified: Fri, 24 May 2024 01:15:57 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac06ef535dced021e53c6859dea1ba0d8d0042a2a6ba8ca087d724f3477f397`  
		Last Modified: Fri, 24 May 2024 01:15:59 GMT  
		Size: 26.8 MB (26813058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy-perception`

```console
$ docker pull ros@sha256:fe5b8be53af2d437922fa6d49b88cc0f0183e048c1e65d7033184cfb15ff39b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-perception` - linux; amd64

```console
$ docker pull ros@sha256:96ce2e48aa94dac3b0ef2986d18ed02d70151232464a2468d82f6118d82f4e9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.0 MB (626039986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ca77c1402e6994748985ffe17212895dd27b3beb30c329b38dc03656492fdb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 04:08:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:17:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 04:17:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 04:17:14 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 00:50:47 GMT
ENV ROS_DISTRO=jazzy
# Fri, 24 May 2024 00:52:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 00:52:25 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 00:52:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 00:52:25 GMT
CMD ["bash"]
# Fri, 24 May 2024 00:53:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 00:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 00:53:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 00:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 00:58:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60661c1b414a0df1f47a75ebe6ee30ab62a190e137eadd8830b58f26d265393`  
		Last Modified: Thu, 02 May 2024 04:27:58 GMT  
		Size: 683.6 KB (683555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c08bb4286c80bd46824cabefede6374d8260920dfcae18a52d6db76894e5e4b`  
		Last Modified: Thu, 02 May 2024 04:27:57 GMT  
		Size: 4.6 MB (4617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f6c812b379d4de9914ffcc55c356485f1907555705bd50fdf0629e37742e9`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78533fe08fdd62d113279815db4b7a14ab1686b1f85f09290bc47b27da4004e`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55164a1d20560b2ddf50794087c404c33f1f5aba7b4692b56e05bf7e787727e9`  
		Last Modified: Fri, 24 May 2024 00:59:12 GMT  
		Size: 124.8 MB (124818119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9069c48a70ab1176dafef8ed3f1a3c7bc5e0f555f8a0604ed3c71c343c6f50`  
		Last Modified: Fri, 24 May 2024 00:58:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc72deef87e0bd3e2b9fb1b1332ebb772e7570201e69d13a80a786526c9cc825`  
		Last Modified: Fri, 24 May 2024 00:59:36 GMT  
		Size: 114.3 MB (114312618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c3e4cc06ea4818223f482308fe858138535f4b16b60e6ea752908b0c818b13`  
		Last Modified: Fri, 24 May 2024 00:59:21 GMT  
		Size: 310.6 KB (310567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed492ab0db3f83a748a510c07a2f30f503a9e2a1ef38bf73806def6cc0aca245`  
		Last Modified: Fri, 24 May 2024 00:59:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14706106e0f4a9775057016e557106aa7abafdf3f95290bf62f5d740cd66c60`  
		Last Modified: Fri, 24 May 2024 00:59:25 GMT  
		Size: 27.7 MB (27668097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fcf4a4822aa31f3c8d1d5b8e870dc4175ac7abc301e8ad0ae03224c4b6c6d1`  
		Last Modified: Fri, 24 May 2024 01:00:34 GMT  
		Size: 323.9 MB (323922035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:11f0aecfdd7d0c1a966de0e524cb77865bb19a031b77f11cf11818bd2dc66848
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.1 MB (569143439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe98ef586cf056ac52e515c1bd5a9e48fb1b2d4301340d0680cf6916a722ba38`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:11:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:11:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:23:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 02:23:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 02:23:04 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 01:05:39 GMT
ENV ROS_DISTRO=jazzy
# Fri, 24 May 2024 01:07:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 01:07:40 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 01:07:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 01:07:41 GMT
CMD ["bash"]
# Fri, 24 May 2024 01:08:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 01:08:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 01:08:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 01:09:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 01:14:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6566430a89b8fd522af510326683dfd547bb47ce3368e0e7c13d03c03a259a73`  
		Last Modified: Thu, 02 May 2024 02:33:11 GMT  
		Size: 683.8 KB (683795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c10c1a69a349bd188a99420ce3e817a3ff04579654dbb1e5fcabc0a226ba0dd`  
		Last Modified: Thu, 02 May 2024 02:33:09 GMT  
		Size: 4.6 MB (4611814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6931defe7f57cf3da1981f2afca9fe611d4b03bf445f980fdc842c4d965bf247`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5315899036e815d56227da46abcb970890f5f1c1388a96cdf9d489dd96e5d058`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0141a49b3e805ba91547642bc9811564e0c44e7380c198e9fe12fd131322ebea`  
		Last Modified: Fri, 24 May 2024 01:15:49 GMT  
		Size: 119.5 MB (119457025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b13531948b1b0049cfd52836e87118bf8b05d8a3852f052b1a18ea633ba4053`  
		Last Modified: Fri, 24 May 2024 01:15:35 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f2b8c0b62382bad46d18ffa279fb2e701a853dbc8f1457806b0140841a622a`  
		Last Modified: Fri, 24 May 2024 01:16:08 GMT  
		Size: 111.2 MB (111153710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33ace28299c354a7a02a6f44bd73e5385aca4a3b0eb87a26f9fe3eb9c2c322d`  
		Last Modified: Fri, 24 May 2024 01:15:57 GMT  
		Size: 310.6 KB (310587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dab07297abace30add756a2eac059cf770c1ed9122df19c8d1e4a9ee2a1300`  
		Last Modified: Fri, 24 May 2024 01:15:57 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac06ef535dced021e53c6859dea1ba0d8d0042a2a6ba8ca087d724f3477f397`  
		Last Modified: Fri, 24 May 2024 01:15:59 GMT  
		Size: 26.8 MB (26813058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffe81f2d4130178710ab334133d66f4247acabb9902a09b441ee5df8e00c814`  
		Last Modified: Fri, 24 May 2024 01:16:48 GMT  
		Size: 277.1 MB (277069813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy-perception-noble`

```console
$ docker pull ros@sha256:fe5b8be53af2d437922fa6d49b88cc0f0183e048c1e65d7033184cfb15ff39b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:96ce2e48aa94dac3b0ef2986d18ed02d70151232464a2468d82f6118d82f4e9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.0 MB (626039986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ca77c1402e6994748985ffe17212895dd27b3beb30c329b38dc03656492fdb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 04:08:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:17:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 04:17:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 04:17:14 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 00:50:47 GMT
ENV ROS_DISTRO=jazzy
# Fri, 24 May 2024 00:52:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 00:52:25 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 00:52:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 00:52:25 GMT
CMD ["bash"]
# Fri, 24 May 2024 00:53:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 00:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 00:53:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 00:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 00:58:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60661c1b414a0df1f47a75ebe6ee30ab62a190e137eadd8830b58f26d265393`  
		Last Modified: Thu, 02 May 2024 04:27:58 GMT  
		Size: 683.6 KB (683555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c08bb4286c80bd46824cabefede6374d8260920dfcae18a52d6db76894e5e4b`  
		Last Modified: Thu, 02 May 2024 04:27:57 GMT  
		Size: 4.6 MB (4617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f6c812b379d4de9914ffcc55c356485f1907555705bd50fdf0629e37742e9`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78533fe08fdd62d113279815db4b7a14ab1686b1f85f09290bc47b27da4004e`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55164a1d20560b2ddf50794087c404c33f1f5aba7b4692b56e05bf7e787727e9`  
		Last Modified: Fri, 24 May 2024 00:59:12 GMT  
		Size: 124.8 MB (124818119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9069c48a70ab1176dafef8ed3f1a3c7bc5e0f555f8a0604ed3c71c343c6f50`  
		Last Modified: Fri, 24 May 2024 00:58:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc72deef87e0bd3e2b9fb1b1332ebb772e7570201e69d13a80a786526c9cc825`  
		Last Modified: Fri, 24 May 2024 00:59:36 GMT  
		Size: 114.3 MB (114312618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c3e4cc06ea4818223f482308fe858138535f4b16b60e6ea752908b0c818b13`  
		Last Modified: Fri, 24 May 2024 00:59:21 GMT  
		Size: 310.6 KB (310567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed492ab0db3f83a748a510c07a2f30f503a9e2a1ef38bf73806def6cc0aca245`  
		Last Modified: Fri, 24 May 2024 00:59:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14706106e0f4a9775057016e557106aa7abafdf3f95290bf62f5d740cd66c60`  
		Last Modified: Fri, 24 May 2024 00:59:25 GMT  
		Size: 27.7 MB (27668097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fcf4a4822aa31f3c8d1d5b8e870dc4175ac7abc301e8ad0ae03224c4b6c6d1`  
		Last Modified: Fri, 24 May 2024 01:00:34 GMT  
		Size: 323.9 MB (323922035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:11f0aecfdd7d0c1a966de0e524cb77865bb19a031b77f11cf11818bd2dc66848
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.1 MB (569143439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe98ef586cf056ac52e515c1bd5a9e48fb1b2d4301340d0680cf6916a722ba38`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:11:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:11:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:23:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 02:23:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 02:23:04 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 01:05:39 GMT
ENV ROS_DISTRO=jazzy
# Fri, 24 May 2024 01:07:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 01:07:40 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 01:07:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 01:07:41 GMT
CMD ["bash"]
# Fri, 24 May 2024 01:08:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 01:08:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 01:08:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 01:09:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 01:14:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6566430a89b8fd522af510326683dfd547bb47ce3368e0e7c13d03c03a259a73`  
		Last Modified: Thu, 02 May 2024 02:33:11 GMT  
		Size: 683.8 KB (683795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c10c1a69a349bd188a99420ce3e817a3ff04579654dbb1e5fcabc0a226ba0dd`  
		Last Modified: Thu, 02 May 2024 02:33:09 GMT  
		Size: 4.6 MB (4611814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6931defe7f57cf3da1981f2afca9fe611d4b03bf445f980fdc842c4d965bf247`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5315899036e815d56227da46abcb970890f5f1c1388a96cdf9d489dd96e5d058`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0141a49b3e805ba91547642bc9811564e0c44e7380c198e9fe12fd131322ebea`  
		Last Modified: Fri, 24 May 2024 01:15:49 GMT  
		Size: 119.5 MB (119457025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b13531948b1b0049cfd52836e87118bf8b05d8a3852f052b1a18ea633ba4053`  
		Last Modified: Fri, 24 May 2024 01:15:35 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f2b8c0b62382bad46d18ffa279fb2e701a853dbc8f1457806b0140841a622a`  
		Last Modified: Fri, 24 May 2024 01:16:08 GMT  
		Size: 111.2 MB (111153710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33ace28299c354a7a02a6f44bd73e5385aca4a3b0eb87a26f9fe3eb9c2c322d`  
		Last Modified: Fri, 24 May 2024 01:15:57 GMT  
		Size: 310.6 KB (310587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dab07297abace30add756a2eac059cf770c1ed9122df19c8d1e4a9ee2a1300`  
		Last Modified: Fri, 24 May 2024 01:15:57 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac06ef535dced021e53c6859dea1ba0d8d0042a2a6ba8ca087d724f3477f397`  
		Last Modified: Fri, 24 May 2024 01:15:59 GMT  
		Size: 26.8 MB (26813058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffe81f2d4130178710ab334133d66f4247acabb9902a09b441ee5df8e00c814`  
		Last Modified: Fri, 24 May 2024 01:16:48 GMT  
		Size: 277.1 MB (277069813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy-ros-base`

```console
$ docker pull ros@sha256:792f28ddc091984c1b2fcd9f780d0cbb4094accdead971724f4762512dc5c5f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:94903a2e6311026989fbe35c31cacd5e509d5a860bc374467d4ed161d39f70b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302117951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1de2625d3b31b7c6871791708581b2df681f6937ae7006b2cb3feeab1b0de1d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 04:08:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:17:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 04:17:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 04:17:14 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 00:50:47 GMT
ENV ROS_DISTRO=jazzy
# Fri, 24 May 2024 00:52:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 00:52:25 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 00:52:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 00:52:25 GMT
CMD ["bash"]
# Fri, 24 May 2024 00:53:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 00:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 00:53:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 00:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60661c1b414a0df1f47a75ebe6ee30ab62a190e137eadd8830b58f26d265393`  
		Last Modified: Thu, 02 May 2024 04:27:58 GMT  
		Size: 683.6 KB (683555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c08bb4286c80bd46824cabefede6374d8260920dfcae18a52d6db76894e5e4b`  
		Last Modified: Thu, 02 May 2024 04:27:57 GMT  
		Size: 4.6 MB (4617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f6c812b379d4de9914ffcc55c356485f1907555705bd50fdf0629e37742e9`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78533fe08fdd62d113279815db4b7a14ab1686b1f85f09290bc47b27da4004e`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55164a1d20560b2ddf50794087c404c33f1f5aba7b4692b56e05bf7e787727e9`  
		Last Modified: Fri, 24 May 2024 00:59:12 GMT  
		Size: 124.8 MB (124818119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9069c48a70ab1176dafef8ed3f1a3c7bc5e0f555f8a0604ed3c71c343c6f50`  
		Last Modified: Fri, 24 May 2024 00:58:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc72deef87e0bd3e2b9fb1b1332ebb772e7570201e69d13a80a786526c9cc825`  
		Last Modified: Fri, 24 May 2024 00:59:36 GMT  
		Size: 114.3 MB (114312618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c3e4cc06ea4818223f482308fe858138535f4b16b60e6ea752908b0c818b13`  
		Last Modified: Fri, 24 May 2024 00:59:21 GMT  
		Size: 310.6 KB (310567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed492ab0db3f83a748a510c07a2f30f503a9e2a1ef38bf73806def6cc0aca245`  
		Last Modified: Fri, 24 May 2024 00:59:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14706106e0f4a9775057016e557106aa7abafdf3f95290bf62f5d740cd66c60`  
		Last Modified: Fri, 24 May 2024 00:59:25 GMT  
		Size: 27.7 MB (27668097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:291f4c0bebacd781250a880a256d8834646030bb6066ec99ec088af1a845df0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292073626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb57bb1324bca2415c246a1b26b2b2ccb527b81e52135e310a9b102acb8c4c4c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:11:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:11:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:23:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 02:23:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 02:23:04 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 01:05:39 GMT
ENV ROS_DISTRO=jazzy
# Fri, 24 May 2024 01:07:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 01:07:40 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 01:07:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 01:07:41 GMT
CMD ["bash"]
# Fri, 24 May 2024 01:08:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 01:08:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 01:08:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 01:09:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6566430a89b8fd522af510326683dfd547bb47ce3368e0e7c13d03c03a259a73`  
		Last Modified: Thu, 02 May 2024 02:33:11 GMT  
		Size: 683.8 KB (683795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c10c1a69a349bd188a99420ce3e817a3ff04579654dbb1e5fcabc0a226ba0dd`  
		Last Modified: Thu, 02 May 2024 02:33:09 GMT  
		Size: 4.6 MB (4611814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6931defe7f57cf3da1981f2afca9fe611d4b03bf445f980fdc842c4d965bf247`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5315899036e815d56227da46abcb970890f5f1c1388a96cdf9d489dd96e5d058`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0141a49b3e805ba91547642bc9811564e0c44e7380c198e9fe12fd131322ebea`  
		Last Modified: Fri, 24 May 2024 01:15:49 GMT  
		Size: 119.5 MB (119457025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b13531948b1b0049cfd52836e87118bf8b05d8a3852f052b1a18ea633ba4053`  
		Last Modified: Fri, 24 May 2024 01:15:35 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f2b8c0b62382bad46d18ffa279fb2e701a853dbc8f1457806b0140841a622a`  
		Last Modified: Fri, 24 May 2024 01:16:08 GMT  
		Size: 111.2 MB (111153710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33ace28299c354a7a02a6f44bd73e5385aca4a3b0eb87a26f9fe3eb9c2c322d`  
		Last Modified: Fri, 24 May 2024 01:15:57 GMT  
		Size: 310.6 KB (310587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dab07297abace30add756a2eac059cf770c1ed9122df19c8d1e4a9ee2a1300`  
		Last Modified: Fri, 24 May 2024 01:15:57 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac06ef535dced021e53c6859dea1ba0d8d0042a2a6ba8ca087d724f3477f397`  
		Last Modified: Fri, 24 May 2024 01:15:59 GMT  
		Size: 26.8 MB (26813058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy-ros-base-noble`

```console
$ docker pull ros@sha256:792f28ddc091984c1b2fcd9f780d0cbb4094accdead971724f4762512dc5c5f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:94903a2e6311026989fbe35c31cacd5e509d5a860bc374467d4ed161d39f70b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302117951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1de2625d3b31b7c6871791708581b2df681f6937ae7006b2cb3feeab1b0de1d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 04:08:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:17:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 04:17:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 04:17:14 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 00:50:47 GMT
ENV ROS_DISTRO=jazzy
# Fri, 24 May 2024 00:52:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 00:52:25 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 00:52:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 00:52:25 GMT
CMD ["bash"]
# Fri, 24 May 2024 00:53:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 00:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 00:53:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 00:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60661c1b414a0df1f47a75ebe6ee30ab62a190e137eadd8830b58f26d265393`  
		Last Modified: Thu, 02 May 2024 04:27:58 GMT  
		Size: 683.6 KB (683555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c08bb4286c80bd46824cabefede6374d8260920dfcae18a52d6db76894e5e4b`  
		Last Modified: Thu, 02 May 2024 04:27:57 GMT  
		Size: 4.6 MB (4617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f6c812b379d4de9914ffcc55c356485f1907555705bd50fdf0629e37742e9`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78533fe08fdd62d113279815db4b7a14ab1686b1f85f09290bc47b27da4004e`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55164a1d20560b2ddf50794087c404c33f1f5aba7b4692b56e05bf7e787727e9`  
		Last Modified: Fri, 24 May 2024 00:59:12 GMT  
		Size: 124.8 MB (124818119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9069c48a70ab1176dafef8ed3f1a3c7bc5e0f555f8a0604ed3c71c343c6f50`  
		Last Modified: Fri, 24 May 2024 00:58:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc72deef87e0bd3e2b9fb1b1332ebb772e7570201e69d13a80a786526c9cc825`  
		Last Modified: Fri, 24 May 2024 00:59:36 GMT  
		Size: 114.3 MB (114312618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c3e4cc06ea4818223f482308fe858138535f4b16b60e6ea752908b0c818b13`  
		Last Modified: Fri, 24 May 2024 00:59:21 GMT  
		Size: 310.6 KB (310567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed492ab0db3f83a748a510c07a2f30f503a9e2a1ef38bf73806def6cc0aca245`  
		Last Modified: Fri, 24 May 2024 00:59:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14706106e0f4a9775057016e557106aa7abafdf3f95290bf62f5d740cd66c60`  
		Last Modified: Fri, 24 May 2024 00:59:25 GMT  
		Size: 27.7 MB (27668097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:291f4c0bebacd781250a880a256d8834646030bb6066ec99ec088af1a845df0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292073626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb57bb1324bca2415c246a1b26b2b2ccb527b81e52135e310a9b102acb8c4c4c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:11:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:11:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:23:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 02:23:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 02:23:04 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 01:05:39 GMT
ENV ROS_DISTRO=jazzy
# Fri, 24 May 2024 01:07:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 01:07:40 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 01:07:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 01:07:41 GMT
CMD ["bash"]
# Fri, 24 May 2024 01:08:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 01:08:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 01:08:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 01:09:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6566430a89b8fd522af510326683dfd547bb47ce3368e0e7c13d03c03a259a73`  
		Last Modified: Thu, 02 May 2024 02:33:11 GMT  
		Size: 683.8 KB (683795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c10c1a69a349bd188a99420ce3e817a3ff04579654dbb1e5fcabc0a226ba0dd`  
		Last Modified: Thu, 02 May 2024 02:33:09 GMT  
		Size: 4.6 MB (4611814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6931defe7f57cf3da1981f2afca9fe611d4b03bf445f980fdc842c4d965bf247`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5315899036e815d56227da46abcb970890f5f1c1388a96cdf9d489dd96e5d058`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0141a49b3e805ba91547642bc9811564e0c44e7380c198e9fe12fd131322ebea`  
		Last Modified: Fri, 24 May 2024 01:15:49 GMT  
		Size: 119.5 MB (119457025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b13531948b1b0049cfd52836e87118bf8b05d8a3852f052b1a18ea633ba4053`  
		Last Modified: Fri, 24 May 2024 01:15:35 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f2b8c0b62382bad46d18ffa279fb2e701a853dbc8f1457806b0140841a622a`  
		Last Modified: Fri, 24 May 2024 01:16:08 GMT  
		Size: 111.2 MB (111153710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33ace28299c354a7a02a6f44bd73e5385aca4a3b0eb87a26f9fe3eb9c2c322d`  
		Last Modified: Fri, 24 May 2024 01:15:57 GMT  
		Size: 310.6 KB (310587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dab07297abace30add756a2eac059cf770c1ed9122df19c8d1e4a9ee2a1300`  
		Last Modified: Fri, 24 May 2024 01:15:57 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac06ef535dced021e53c6859dea1ba0d8d0042a2a6ba8ca087d724f3477f397`  
		Last Modified: Fri, 24 May 2024 01:15:59 GMT  
		Size: 26.8 MB (26813058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy-ros-core`

```console
$ docker pull ros@sha256:dbd591134451cd9c368cc08bcd1a9b76a4d95a7c63afd53dc3ae88863cbec35c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:d94d2a74cc5497c159365a466622d525a0ce46edbd6ae7c2466c7b2562e8fef1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159824177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa02b7fcb92d5f10282c2e7f66d6fe4c018bc62b80c5b5afef5c304e4acdc921`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 04:08:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:17:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 04:17:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 04:17:14 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 00:50:47 GMT
ENV ROS_DISTRO=jazzy
# Fri, 24 May 2024 00:52:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 00:52:25 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 00:52:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 00:52:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60661c1b414a0df1f47a75ebe6ee30ab62a190e137eadd8830b58f26d265393`  
		Last Modified: Thu, 02 May 2024 04:27:58 GMT  
		Size: 683.6 KB (683555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c08bb4286c80bd46824cabefede6374d8260920dfcae18a52d6db76894e5e4b`  
		Last Modified: Thu, 02 May 2024 04:27:57 GMT  
		Size: 4.6 MB (4617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f6c812b379d4de9914ffcc55c356485f1907555705bd50fdf0629e37742e9`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78533fe08fdd62d113279815db4b7a14ab1686b1f85f09290bc47b27da4004e`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55164a1d20560b2ddf50794087c404c33f1f5aba7b4692b56e05bf7e787727e9`  
		Last Modified: Fri, 24 May 2024 00:59:12 GMT  
		Size: 124.8 MB (124818119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9069c48a70ab1176dafef8ed3f1a3c7bc5e0f555f8a0604ed3c71c343c6f50`  
		Last Modified: Fri, 24 May 2024 00:58:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fe4140542afd1130e2ce0636ef8659110722b54eae1c4a01860e570533db3abf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153793792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cd740e828406e4057cfb26574e4fbecdef26bd237a2317922d5e2083f2325c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:11:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:11:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:23:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 02:23:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 02:23:04 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 01:05:39 GMT
ENV ROS_DISTRO=jazzy
# Fri, 24 May 2024 01:07:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 01:07:40 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 01:07:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 01:07:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6566430a89b8fd522af510326683dfd547bb47ce3368e0e7c13d03c03a259a73`  
		Last Modified: Thu, 02 May 2024 02:33:11 GMT  
		Size: 683.8 KB (683795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c10c1a69a349bd188a99420ce3e817a3ff04579654dbb1e5fcabc0a226ba0dd`  
		Last Modified: Thu, 02 May 2024 02:33:09 GMT  
		Size: 4.6 MB (4611814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6931defe7f57cf3da1981f2afca9fe611d4b03bf445f980fdc842c4d965bf247`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5315899036e815d56227da46abcb970890f5f1c1388a96cdf9d489dd96e5d058`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0141a49b3e805ba91547642bc9811564e0c44e7380c198e9fe12fd131322ebea`  
		Last Modified: Fri, 24 May 2024 01:15:49 GMT  
		Size: 119.5 MB (119457025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b13531948b1b0049cfd52836e87118bf8b05d8a3852f052b1a18ea633ba4053`  
		Last Modified: Fri, 24 May 2024 01:15:35 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:jazzy-ros-core-noble`

```console
$ docker pull ros@sha256:dbd591134451cd9c368cc08bcd1a9b76a4d95a7c63afd53dc3ae88863cbec35c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:jazzy-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:d94d2a74cc5497c159365a466622d525a0ce46edbd6ae7c2466c7b2562e8fef1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159824177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa02b7fcb92d5f10282c2e7f66d6fe4c018bc62b80c5b5afef5c304e4acdc921`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 04:08:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:17:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 04:17:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 04:17:14 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 00:50:47 GMT
ENV ROS_DISTRO=jazzy
# Fri, 24 May 2024 00:52:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 00:52:25 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 00:52:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 00:52:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60661c1b414a0df1f47a75ebe6ee30ab62a190e137eadd8830b58f26d265393`  
		Last Modified: Thu, 02 May 2024 04:27:58 GMT  
		Size: 683.6 KB (683555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c08bb4286c80bd46824cabefede6374d8260920dfcae18a52d6db76894e5e4b`  
		Last Modified: Thu, 02 May 2024 04:27:57 GMT  
		Size: 4.6 MB (4617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f6c812b379d4de9914ffcc55c356485f1907555705bd50fdf0629e37742e9`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78533fe08fdd62d113279815db4b7a14ab1686b1f85f09290bc47b27da4004e`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55164a1d20560b2ddf50794087c404c33f1f5aba7b4692b56e05bf7e787727e9`  
		Last Modified: Fri, 24 May 2024 00:59:12 GMT  
		Size: 124.8 MB (124818119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9069c48a70ab1176dafef8ed3f1a3c7bc5e0f555f8a0604ed3c71c343c6f50`  
		Last Modified: Fri, 24 May 2024 00:58:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:jazzy-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fe4140542afd1130e2ce0636ef8659110722b54eae1c4a01860e570533db3abf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153793792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cd740e828406e4057cfb26574e4fbecdef26bd237a2317922d5e2083f2325c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:11:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:11:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:23:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 02:23:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 02:23:04 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 01:05:39 GMT
ENV ROS_DISTRO=jazzy
# Fri, 24 May 2024 01:07:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 01:07:40 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 01:07:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 01:07:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6566430a89b8fd522af510326683dfd547bb47ce3368e0e7c13d03c03a259a73`  
		Last Modified: Thu, 02 May 2024 02:33:11 GMT  
		Size: 683.8 KB (683795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c10c1a69a349bd188a99420ce3e817a3ff04579654dbb1e5fcabc0a226ba0dd`  
		Last Modified: Thu, 02 May 2024 02:33:09 GMT  
		Size: 4.6 MB (4611814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6931defe7f57cf3da1981f2afca9fe611d4b03bf445f980fdc842c4d965bf247`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5315899036e815d56227da46abcb970890f5f1c1388a96cdf9d489dd96e5d058`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0141a49b3e805ba91547642bc9811564e0c44e7380c198e9fe12fd131322ebea`  
		Last Modified: Fri, 24 May 2024 01:15:49 GMT  
		Size: 119.5 MB (119457025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b13531948b1b0049cfd52836e87118bf8b05d8a3852f052b1a18ea633ba4053`  
		Last Modified: Fri, 24 May 2024 01:15:35 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:latest`

```console
$ docker pull ros@sha256:792f28ddc091984c1b2fcd9f780d0cbb4094accdead971724f4762512dc5c5f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:94903a2e6311026989fbe35c31cacd5e509d5a860bc374467d4ed161d39f70b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302117951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1de2625d3b31b7c6871791708581b2df681f6937ae7006b2cb3feeab1b0de1d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 04:08:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:17:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 04:17:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 04:17:14 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 00:50:47 GMT
ENV ROS_DISTRO=jazzy
# Fri, 24 May 2024 00:52:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 00:52:25 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 00:52:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 00:52:25 GMT
CMD ["bash"]
# Fri, 24 May 2024 00:53:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 00:53:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 00:53:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 00:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60661c1b414a0df1f47a75ebe6ee30ab62a190e137eadd8830b58f26d265393`  
		Last Modified: Thu, 02 May 2024 04:27:58 GMT  
		Size: 683.6 KB (683555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c08bb4286c80bd46824cabefede6374d8260920dfcae18a52d6db76894e5e4b`  
		Last Modified: Thu, 02 May 2024 04:27:57 GMT  
		Size: 4.6 MB (4617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f6c812b379d4de9914ffcc55c356485f1907555705bd50fdf0629e37742e9`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78533fe08fdd62d113279815db4b7a14ab1686b1f85f09290bc47b27da4004e`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55164a1d20560b2ddf50794087c404c33f1f5aba7b4692b56e05bf7e787727e9`  
		Last Modified: Fri, 24 May 2024 00:59:12 GMT  
		Size: 124.8 MB (124818119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9069c48a70ab1176dafef8ed3f1a3c7bc5e0f555f8a0604ed3c71c343c6f50`  
		Last Modified: Fri, 24 May 2024 00:58:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc72deef87e0bd3e2b9fb1b1332ebb772e7570201e69d13a80a786526c9cc825`  
		Last Modified: Fri, 24 May 2024 00:59:36 GMT  
		Size: 114.3 MB (114312618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c3e4cc06ea4818223f482308fe858138535f4b16b60e6ea752908b0c818b13`  
		Last Modified: Fri, 24 May 2024 00:59:21 GMT  
		Size: 310.6 KB (310567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed492ab0db3f83a748a510c07a2f30f503a9e2a1ef38bf73806def6cc0aca245`  
		Last Modified: Fri, 24 May 2024 00:59:21 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14706106e0f4a9775057016e557106aa7abafdf3f95290bf62f5d740cd66c60`  
		Last Modified: Fri, 24 May 2024 00:59:25 GMT  
		Size: 27.7 MB (27668097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:291f4c0bebacd781250a880a256d8834646030bb6066ec99ec088af1a845df0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292073626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb57bb1324bca2415c246a1b26b2b2ccb527b81e52135e310a9b102acb8c4c4c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:11:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:11:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:23:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 02:23:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 02:23:04 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 May 2024 01:05:39 GMT
ENV ROS_DISTRO=jazzy
# Fri, 24 May 2024 01:07:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 01:07:40 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 01:07:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 01:07:41 GMT
CMD ["bash"]
# Fri, 24 May 2024 01:08:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 01:08:31 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 01:08:35 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 01:09:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-jazzy-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6566430a89b8fd522af510326683dfd547bb47ce3368e0e7c13d03c03a259a73`  
		Last Modified: Thu, 02 May 2024 02:33:11 GMT  
		Size: 683.8 KB (683795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c10c1a69a349bd188a99420ce3e817a3ff04579654dbb1e5fcabc0a226ba0dd`  
		Last Modified: Thu, 02 May 2024 02:33:09 GMT  
		Size: 4.6 MB (4611814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6931defe7f57cf3da1981f2afca9fe611d4b03bf445f980fdc842c4d965bf247`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5315899036e815d56227da46abcb970890f5f1c1388a96cdf9d489dd96e5d058`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0141a49b3e805ba91547642bc9811564e0c44e7380c198e9fe12fd131322ebea`  
		Last Modified: Fri, 24 May 2024 01:15:49 GMT  
		Size: 119.5 MB (119457025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b13531948b1b0049cfd52836e87118bf8b05d8a3852f052b1a18ea633ba4053`  
		Last Modified: Fri, 24 May 2024 01:15:35 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f2b8c0b62382bad46d18ffa279fb2e701a853dbc8f1457806b0140841a622a`  
		Last Modified: Fri, 24 May 2024 01:16:08 GMT  
		Size: 111.2 MB (111153710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33ace28299c354a7a02a6f44bd73e5385aca4a3b0eb87a26f9fe3eb9c2c322d`  
		Last Modified: Fri, 24 May 2024 01:15:57 GMT  
		Size: 310.6 KB (310587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dab07297abace30add756a2eac059cf770c1ed9122df19c8d1e4a9ee2a1300`  
		Last Modified: Fri, 24 May 2024 01:15:57 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac06ef535dced021e53c6859dea1ba0d8d0042a2a6ba8ca087d724f3477f397`  
		Last Modified: Fri, 24 May 2024 01:15:59 GMT  
		Size: 26.8 MB (26813058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic`

```console
$ docker pull ros@sha256:781549532b63191b08acb2912cd989c80434edf03b8feed7973c181232363d59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:2fa31dda2e7666e0081f86dfc8b964ddd28078134a1c98f6ce77c41184ac62ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264729301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38effce76149ab2539a54ef9e175cd0e999e12862e55adc4b4459a06c0ef83b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:15:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:15:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:43:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:43:03 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 03:43:03 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:43:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 03:43:03 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 03:45:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:45:04 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 03:45:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 03:45:04 GMT
CMD ["bash"]
# Thu, 02 May 2024 03:45:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:45:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 03:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9f83335e3f34356129a65a46777f2c11b35558325643aeceb57ad34fcf26ae`  
		Last Modified: Thu, 02 May 2024 02:23:52 GMT  
		Size: 1.2 MB (1198590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9931bbbdc456888cafcfb45518f1f74377f7ded26c5caeba3779574b953c2f0`  
		Last Modified: Thu, 02 May 2024 02:23:51 GMT  
		Size: 5.6 MB (5553874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e642e2cde42d5ceebe85aeb8cafeb95dc3f33549056c16605dc5472621eeda6`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dca1471511de82e7b7117acd23c83c7a4b2921a02eb47a1a3af345c02fb841f`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dd00e528c2ec50f993c02fd6160d509b48e5a5acb8dfdf02312d1b1e167bbf`  
		Last Modified: Thu, 02 May 2024 04:20:49 GMT  
		Size: 177.0 MB (176995985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e02cf37cc416afb9263eebbfb2704d7335a88671a8dcd1510f44432d2c0623`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c3ee459bf535e354c3ae5772e5dc01acfc7c39896912f2cb3d0e028f483594`  
		Last Modified: Thu, 02 May 2024 04:21:05 GMT  
		Size: 50.9 MB (50942130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78880207582f574785e219e4fe9c0ed76d6a71bdb7737257f3e1e5eebbb9512`  
		Last Modified: Thu, 02 May 2024 04:20:58 GMT  
		Size: 321.3 KB (321273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e2631648f5934240033e56e0e8675f135439fcb185b941b63b2ad7b837cf7e`  
		Last Modified: Thu, 02 May 2024 04:20:58 GMT  
		Size: 1.1 MB (1130667 bytes)  
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
$ docker pull ros@sha256:426b24a25e905e7a99c5d27a0e884d6c27c1639540df0e81ed004218e83650e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251968388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4acf20dd6f86b259ef4aa91f7c85222bacb77ff86efa97f8ba4393441a1522e1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:34:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:35:16 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 01:35:16 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:35:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 01:35:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 01:38:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:38:45 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 01:38:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 01:38:46 GMT
CMD ["bash"]
# Thu, 02 May 2024 01:39:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:39:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 01:39:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:83049506c6eb6b11ef1a8774b3486a01a1804f7d13bd230b44788bc63248282d`  
		Last Modified: Mon, 29 Apr 2024 19:12:05 GMT  
		Size: 27.2 MB (27206145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf8574ed521f52190151260cb46f81577cb9462f025e4d0bd31fd5ef9164221`  
		Last Modified: Thu, 02 May 2024 02:25:54 GMT  
		Size: 1.2 MB (1199077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ba8bc7b1d97ec2940a42ab430797d38e66d94e8e1c3e1c239667352ac4a2be`  
		Last Modified: Thu, 02 May 2024 02:25:52 GMT  
		Size: 5.5 MB (5532618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170d525ddc0031398baf96e838661fd2ce78157cfebca7aa2ffef78821eaa76d`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3221e023c87709c99c3aa21599a3fb2755e867f8624231d7e701936a3942a9`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285463fcd2b1351b20e5bff4e1d55006a3f5afb2fc3f0798587caf9a3cfb0165`  
		Last Modified: Thu, 02 May 2024 02:26:25 GMT  
		Size: 171.4 MB (171383372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be132e8d75da72ae76fe687e3168eee676ea41b61b67592613c4d27948d4a842`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04978fbd01f4ac1f8deb48a3af3b6ae2156a3391bae378b5b70c6034c28bc86b`  
		Last Modified: Thu, 02 May 2024 02:26:39 GMT  
		Size: 45.2 MB (45207993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806a3b7368effc67cf6c5233658704ca94e11ba21d4cb3f96dc5dbd5c4c22152`  
		Last Modified: Thu, 02 May 2024 02:26:34 GMT  
		Size: 321.3 KB (321274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f453d39198ddd342125de1b67017e7b7cd521133b18a37e4d153b8c10f01f7c0`  
		Last Modified: Thu, 02 May 2024 02:26:34 GMT  
		Size: 1.1 MB (1115420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:8adc35d49bd4365cd92c6b94f730bc5b7770d802c71d412518e2782d23b2d3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:8d012e1794d7019802be9cb462448788898509e1f98ee46ad7a23bbb2f8513f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.4 MB (835402970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be917fe752a096a8264db442912bd583c805319b0f7bd93941978ff4cf6bb88`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:15:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:15:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:43:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:43:03 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 03:43:03 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:43:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 03:43:03 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 03:45:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:45:04 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 03:45:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 03:45:04 GMT
CMD ["bash"]
# Thu, 02 May 2024 03:45:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:45:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 03:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:52:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9f83335e3f34356129a65a46777f2c11b35558325643aeceb57ad34fcf26ae`  
		Last Modified: Thu, 02 May 2024 02:23:52 GMT  
		Size: 1.2 MB (1198590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9931bbbdc456888cafcfb45518f1f74377f7ded26c5caeba3779574b953c2f0`  
		Last Modified: Thu, 02 May 2024 02:23:51 GMT  
		Size: 5.6 MB (5553874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e642e2cde42d5ceebe85aeb8cafeb95dc3f33549056c16605dc5472621eeda6`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dca1471511de82e7b7117acd23c83c7a4b2921a02eb47a1a3af345c02fb841f`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dd00e528c2ec50f993c02fd6160d509b48e5a5acb8dfdf02312d1b1e167bbf`  
		Last Modified: Thu, 02 May 2024 04:20:49 GMT  
		Size: 177.0 MB (176995985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e02cf37cc416afb9263eebbfb2704d7335a88671a8dcd1510f44432d2c0623`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c3ee459bf535e354c3ae5772e5dc01acfc7c39896912f2cb3d0e028f483594`  
		Last Modified: Thu, 02 May 2024 04:21:05 GMT  
		Size: 50.9 MB (50942130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78880207582f574785e219e4fe9c0ed76d6a71bdb7737257f3e1e5eebbb9512`  
		Last Modified: Thu, 02 May 2024 04:20:58 GMT  
		Size: 321.3 KB (321273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e2631648f5934240033e56e0e8675f135439fcb185b941b63b2ad7b837cf7e`  
		Last Modified: Thu, 02 May 2024 04:20:58 GMT  
		Size: 1.1 MB (1130667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6c72841ac154ae796f224a0247b3ca6fb15ac539e54561cc2b9b23443bacf8`  
		Last Modified: Thu, 02 May 2024 04:22:46 GMT  
		Size: 570.7 MB (570673669 bytes)  
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
$ docker pull ros@sha256:4fbbe768e3d8f62c74b207d8066be5d19e60603f02c3f412bdc8705040443c06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.6 MB (785607788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14eac203a831c8bc83122c4c2c5719138c5a2ad7da6e1756e3d543cea245781c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:34:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:35:16 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 01:35:16 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:35:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 01:35:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 01:38:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:38:45 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 01:38:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 01:38:46 GMT
CMD ["bash"]
# Thu, 02 May 2024 01:39:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:39:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 01:39:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:83049506c6eb6b11ef1a8774b3486a01a1804f7d13bd230b44788bc63248282d`  
		Last Modified: Mon, 29 Apr 2024 19:12:05 GMT  
		Size: 27.2 MB (27206145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf8574ed521f52190151260cb46f81577cb9462f025e4d0bd31fd5ef9164221`  
		Last Modified: Thu, 02 May 2024 02:25:54 GMT  
		Size: 1.2 MB (1199077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ba8bc7b1d97ec2940a42ab430797d38e66d94e8e1c3e1c239667352ac4a2be`  
		Last Modified: Thu, 02 May 2024 02:25:52 GMT  
		Size: 5.5 MB (5532618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170d525ddc0031398baf96e838661fd2ce78157cfebca7aa2ffef78821eaa76d`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3221e023c87709c99c3aa21599a3fb2755e867f8624231d7e701936a3942a9`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285463fcd2b1351b20e5bff4e1d55006a3f5afb2fc3f0798587caf9a3cfb0165`  
		Last Modified: Thu, 02 May 2024 02:26:25 GMT  
		Size: 171.4 MB (171383372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be132e8d75da72ae76fe687e3168eee676ea41b61b67592613c4d27948d4a842`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04978fbd01f4ac1f8deb48a3af3b6ae2156a3391bae378b5b70c6034c28bc86b`  
		Last Modified: Thu, 02 May 2024 02:26:39 GMT  
		Size: 45.2 MB (45207993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806a3b7368effc67cf6c5233658704ca94e11ba21d4cb3f96dc5dbd5c4c22152`  
		Last Modified: Thu, 02 May 2024 02:26:34 GMT  
		Size: 321.3 KB (321274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f453d39198ddd342125de1b67017e7b7cd521133b18a37e4d153b8c10f01f7c0`  
		Last Modified: Thu, 02 May 2024 02:26:34 GMT  
		Size: 1.1 MB (1115420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901273720d18672c8e8b0a89f41fa95c3c247baa7502a07c5a44170b616d9ddc`  
		Last Modified: Thu, 02 May 2024 02:28:11 GMT  
		Size: 533.6 MB (533639400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:8adc35d49bd4365cd92c6b94f730bc5b7770d802c71d412518e2782d23b2d3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:8d012e1794d7019802be9cb462448788898509e1f98ee46ad7a23bbb2f8513f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.4 MB (835402970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be917fe752a096a8264db442912bd583c805319b0f7bd93941978ff4cf6bb88`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:15:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:15:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:43:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:43:03 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 03:43:03 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:43:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 03:43:03 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 03:45:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:45:04 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 03:45:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 03:45:04 GMT
CMD ["bash"]
# Thu, 02 May 2024 03:45:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:45:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 03:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:52:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9f83335e3f34356129a65a46777f2c11b35558325643aeceb57ad34fcf26ae`  
		Last Modified: Thu, 02 May 2024 02:23:52 GMT  
		Size: 1.2 MB (1198590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9931bbbdc456888cafcfb45518f1f74377f7ded26c5caeba3779574b953c2f0`  
		Last Modified: Thu, 02 May 2024 02:23:51 GMT  
		Size: 5.6 MB (5553874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e642e2cde42d5ceebe85aeb8cafeb95dc3f33549056c16605dc5472621eeda6`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dca1471511de82e7b7117acd23c83c7a4b2921a02eb47a1a3af345c02fb841f`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dd00e528c2ec50f993c02fd6160d509b48e5a5acb8dfdf02312d1b1e167bbf`  
		Last Modified: Thu, 02 May 2024 04:20:49 GMT  
		Size: 177.0 MB (176995985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e02cf37cc416afb9263eebbfb2704d7335a88671a8dcd1510f44432d2c0623`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c3ee459bf535e354c3ae5772e5dc01acfc7c39896912f2cb3d0e028f483594`  
		Last Modified: Thu, 02 May 2024 04:21:05 GMT  
		Size: 50.9 MB (50942130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78880207582f574785e219e4fe9c0ed76d6a71bdb7737257f3e1e5eebbb9512`  
		Last Modified: Thu, 02 May 2024 04:20:58 GMT  
		Size: 321.3 KB (321273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e2631648f5934240033e56e0e8675f135439fcb185b941b63b2ad7b837cf7e`  
		Last Modified: Thu, 02 May 2024 04:20:58 GMT  
		Size: 1.1 MB (1130667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6c72841ac154ae796f224a0247b3ca6fb15ac539e54561cc2b9b23443bacf8`  
		Last Modified: Thu, 02 May 2024 04:22:46 GMT  
		Size: 570.7 MB (570673669 bytes)  
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
$ docker pull ros@sha256:4fbbe768e3d8f62c74b207d8066be5d19e60603f02c3f412bdc8705040443c06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.6 MB (785607788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14eac203a831c8bc83122c4c2c5719138c5a2ad7da6e1756e3d543cea245781c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:34:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:35:16 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 01:35:16 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:35:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 01:35:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 01:38:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:38:45 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 01:38:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 01:38:46 GMT
CMD ["bash"]
# Thu, 02 May 2024 01:39:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:39:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 01:39:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:50:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:83049506c6eb6b11ef1a8774b3486a01a1804f7d13bd230b44788bc63248282d`  
		Last Modified: Mon, 29 Apr 2024 19:12:05 GMT  
		Size: 27.2 MB (27206145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf8574ed521f52190151260cb46f81577cb9462f025e4d0bd31fd5ef9164221`  
		Last Modified: Thu, 02 May 2024 02:25:54 GMT  
		Size: 1.2 MB (1199077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ba8bc7b1d97ec2940a42ab430797d38e66d94e8e1c3e1c239667352ac4a2be`  
		Last Modified: Thu, 02 May 2024 02:25:52 GMT  
		Size: 5.5 MB (5532618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170d525ddc0031398baf96e838661fd2ce78157cfebca7aa2ffef78821eaa76d`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3221e023c87709c99c3aa21599a3fb2755e867f8624231d7e701936a3942a9`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285463fcd2b1351b20e5bff4e1d55006a3f5afb2fc3f0798587caf9a3cfb0165`  
		Last Modified: Thu, 02 May 2024 02:26:25 GMT  
		Size: 171.4 MB (171383372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be132e8d75da72ae76fe687e3168eee676ea41b61b67592613c4d27948d4a842`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04978fbd01f4ac1f8deb48a3af3b6ae2156a3391bae378b5b70c6034c28bc86b`  
		Last Modified: Thu, 02 May 2024 02:26:39 GMT  
		Size: 45.2 MB (45207993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806a3b7368effc67cf6c5233658704ca94e11ba21d4cb3f96dc5dbd5c4c22152`  
		Last Modified: Thu, 02 May 2024 02:26:34 GMT  
		Size: 321.3 KB (321274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f453d39198ddd342125de1b67017e7b7cd521133b18a37e4d153b8c10f01f7c0`  
		Last Modified: Thu, 02 May 2024 02:26:34 GMT  
		Size: 1.1 MB (1115420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901273720d18672c8e8b0a89f41fa95c3c247baa7502a07c5a44170b616d9ddc`  
		Last Modified: Thu, 02 May 2024 02:28:11 GMT  
		Size: 533.6 MB (533639400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:32f09dabf219dc56dd8353f1c9d08d0f4d9d5158d2f47050e8de9dc96334f529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:3a6f7d904d7206bdd94bfd40c22b2f1026dd2a3a1be8df17d4b8cb018b5b417f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.7 MB (281658097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22055ee262111566fa4b4d36987ba4a4a675c5466f12198185335dae6769b1c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:15:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:15:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:43:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:43:03 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 03:43:03 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:43:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 03:43:03 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 03:45:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:45:04 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 03:45:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 03:45:04 GMT
CMD ["bash"]
# Thu, 02 May 2024 03:45:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:45:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 03:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:46:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9f83335e3f34356129a65a46777f2c11b35558325643aeceb57ad34fcf26ae`  
		Last Modified: Thu, 02 May 2024 02:23:52 GMT  
		Size: 1.2 MB (1198590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9931bbbdc456888cafcfb45518f1f74377f7ded26c5caeba3779574b953c2f0`  
		Last Modified: Thu, 02 May 2024 02:23:51 GMT  
		Size: 5.6 MB (5553874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e642e2cde42d5ceebe85aeb8cafeb95dc3f33549056c16605dc5472621eeda6`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dca1471511de82e7b7117acd23c83c7a4b2921a02eb47a1a3af345c02fb841f`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dd00e528c2ec50f993c02fd6160d509b48e5a5acb8dfdf02312d1b1e167bbf`  
		Last Modified: Thu, 02 May 2024 04:20:49 GMT  
		Size: 177.0 MB (176995985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e02cf37cc416afb9263eebbfb2704d7335a88671a8dcd1510f44432d2c0623`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c3ee459bf535e354c3ae5772e5dc01acfc7c39896912f2cb3d0e028f483594`  
		Last Modified: Thu, 02 May 2024 04:21:05 GMT  
		Size: 50.9 MB (50942130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78880207582f574785e219e4fe9c0ed76d6a71bdb7737257f3e1e5eebbb9512`  
		Last Modified: Thu, 02 May 2024 04:20:58 GMT  
		Size: 321.3 KB (321273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e2631648f5934240033e56e0e8675f135439fcb185b941b63b2ad7b837cf7e`  
		Last Modified: Thu, 02 May 2024 04:20:58 GMT  
		Size: 1.1 MB (1130667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148e744f802628ef1fda93f6cb2ec95d7f4aadb4525b14f70393b4a6961b27a3`  
		Last Modified: Thu, 02 May 2024 04:21:18 GMT  
		Size: 16.9 MB (16928796 bytes)  
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
$ docker pull ros@sha256:2bbcfd1f11e78cd501eb506b9114a869f65c71a7f06adbf1380c0f31e3f7604f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268498987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8bb70ca791bae66bf01a804f85d049232180028269cb2330fd0a95b0732514`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:34:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:35:16 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 01:35:16 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:35:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 01:35:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 01:38:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:38:45 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 01:38:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 01:38:46 GMT
CMD ["bash"]
# Thu, 02 May 2024 01:39:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:39:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 01:39:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:40:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:83049506c6eb6b11ef1a8774b3486a01a1804f7d13bd230b44788bc63248282d`  
		Last Modified: Mon, 29 Apr 2024 19:12:05 GMT  
		Size: 27.2 MB (27206145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf8574ed521f52190151260cb46f81577cb9462f025e4d0bd31fd5ef9164221`  
		Last Modified: Thu, 02 May 2024 02:25:54 GMT  
		Size: 1.2 MB (1199077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ba8bc7b1d97ec2940a42ab430797d38e66d94e8e1c3e1c239667352ac4a2be`  
		Last Modified: Thu, 02 May 2024 02:25:52 GMT  
		Size: 5.5 MB (5532618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170d525ddc0031398baf96e838661fd2ce78157cfebca7aa2ffef78821eaa76d`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3221e023c87709c99c3aa21599a3fb2755e867f8624231d7e701936a3942a9`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285463fcd2b1351b20e5bff4e1d55006a3f5afb2fc3f0798587caf9a3cfb0165`  
		Last Modified: Thu, 02 May 2024 02:26:25 GMT  
		Size: 171.4 MB (171383372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be132e8d75da72ae76fe687e3168eee676ea41b61b67592613c4d27948d4a842`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04978fbd01f4ac1f8deb48a3af3b6ae2156a3391bae378b5b70c6034c28bc86b`  
		Last Modified: Thu, 02 May 2024 02:26:39 GMT  
		Size: 45.2 MB (45207993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806a3b7368effc67cf6c5233658704ca94e11ba21d4cb3f96dc5dbd5c4c22152`  
		Last Modified: Thu, 02 May 2024 02:26:34 GMT  
		Size: 321.3 KB (321274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f453d39198ddd342125de1b67017e7b7cd521133b18a37e4d153b8c10f01f7c0`  
		Last Modified: Thu, 02 May 2024 02:26:34 GMT  
		Size: 1.1 MB (1115420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c6f686cb916978707587c24919108b59142326731a176c99d6adf9a4740e89`  
		Last Modified: Thu, 02 May 2024 02:26:55 GMT  
		Size: 16.5 MB (16530599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:32f09dabf219dc56dd8353f1c9d08d0f4d9d5158d2f47050e8de9dc96334f529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:3a6f7d904d7206bdd94bfd40c22b2f1026dd2a3a1be8df17d4b8cb018b5b417f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.7 MB (281658097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22055ee262111566fa4b4d36987ba4a4a675c5466f12198185335dae6769b1c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:15:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:15:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:43:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:43:03 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 03:43:03 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:43:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 03:43:03 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 03:45:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:45:04 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 03:45:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 03:45:04 GMT
CMD ["bash"]
# Thu, 02 May 2024 03:45:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:45:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 03:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:46:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9f83335e3f34356129a65a46777f2c11b35558325643aeceb57ad34fcf26ae`  
		Last Modified: Thu, 02 May 2024 02:23:52 GMT  
		Size: 1.2 MB (1198590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9931bbbdc456888cafcfb45518f1f74377f7ded26c5caeba3779574b953c2f0`  
		Last Modified: Thu, 02 May 2024 02:23:51 GMT  
		Size: 5.6 MB (5553874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e642e2cde42d5ceebe85aeb8cafeb95dc3f33549056c16605dc5472621eeda6`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dca1471511de82e7b7117acd23c83c7a4b2921a02eb47a1a3af345c02fb841f`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dd00e528c2ec50f993c02fd6160d509b48e5a5acb8dfdf02312d1b1e167bbf`  
		Last Modified: Thu, 02 May 2024 04:20:49 GMT  
		Size: 177.0 MB (176995985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e02cf37cc416afb9263eebbfb2704d7335a88671a8dcd1510f44432d2c0623`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c3ee459bf535e354c3ae5772e5dc01acfc7c39896912f2cb3d0e028f483594`  
		Last Modified: Thu, 02 May 2024 04:21:05 GMT  
		Size: 50.9 MB (50942130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78880207582f574785e219e4fe9c0ed76d6a71bdb7737257f3e1e5eebbb9512`  
		Last Modified: Thu, 02 May 2024 04:20:58 GMT  
		Size: 321.3 KB (321273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e2631648f5934240033e56e0e8675f135439fcb185b941b63b2ad7b837cf7e`  
		Last Modified: Thu, 02 May 2024 04:20:58 GMT  
		Size: 1.1 MB (1130667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148e744f802628ef1fda93f6cb2ec95d7f4aadb4525b14f70393b4a6961b27a3`  
		Last Modified: Thu, 02 May 2024 04:21:18 GMT  
		Size: 16.9 MB (16928796 bytes)  
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
$ docker pull ros@sha256:2bbcfd1f11e78cd501eb506b9114a869f65c71a7f06adbf1380c0f31e3f7604f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268498987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8bb70ca791bae66bf01a804f85d049232180028269cb2330fd0a95b0732514`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:34:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:35:16 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 01:35:16 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:35:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 01:35:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 01:38:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:38:45 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 01:38:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 01:38:46 GMT
CMD ["bash"]
# Thu, 02 May 2024 01:39:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:39:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 01:39:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:40:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:83049506c6eb6b11ef1a8774b3486a01a1804f7d13bd230b44788bc63248282d`  
		Last Modified: Mon, 29 Apr 2024 19:12:05 GMT  
		Size: 27.2 MB (27206145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf8574ed521f52190151260cb46f81577cb9462f025e4d0bd31fd5ef9164221`  
		Last Modified: Thu, 02 May 2024 02:25:54 GMT  
		Size: 1.2 MB (1199077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ba8bc7b1d97ec2940a42ab430797d38e66d94e8e1c3e1c239667352ac4a2be`  
		Last Modified: Thu, 02 May 2024 02:25:52 GMT  
		Size: 5.5 MB (5532618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170d525ddc0031398baf96e838661fd2ce78157cfebca7aa2ffef78821eaa76d`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3221e023c87709c99c3aa21599a3fb2755e867f8624231d7e701936a3942a9`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285463fcd2b1351b20e5bff4e1d55006a3f5afb2fc3f0798587caf9a3cfb0165`  
		Last Modified: Thu, 02 May 2024 02:26:25 GMT  
		Size: 171.4 MB (171383372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be132e8d75da72ae76fe687e3168eee676ea41b61b67592613c4d27948d4a842`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04978fbd01f4ac1f8deb48a3af3b6ae2156a3391bae378b5b70c6034c28bc86b`  
		Last Modified: Thu, 02 May 2024 02:26:39 GMT  
		Size: 45.2 MB (45207993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806a3b7368effc67cf6c5233658704ca94e11ba21d4cb3f96dc5dbd5c4c22152`  
		Last Modified: Thu, 02 May 2024 02:26:34 GMT  
		Size: 321.3 KB (321274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f453d39198ddd342125de1b67017e7b7cd521133b18a37e4d153b8c10f01f7c0`  
		Last Modified: Thu, 02 May 2024 02:26:34 GMT  
		Size: 1.1 MB (1115420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c6f686cb916978707587c24919108b59142326731a176c99d6adf9a4740e89`  
		Last Modified: Thu, 02 May 2024 02:26:55 GMT  
		Size: 16.5 MB (16530599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:781549532b63191b08acb2912cd989c80434edf03b8feed7973c181232363d59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:2fa31dda2e7666e0081f86dfc8b964ddd28078134a1c98f6ce77c41184ac62ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264729301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38effce76149ab2539a54ef9e175cd0e999e12862e55adc4b4459a06c0ef83b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:15:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:15:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:43:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:43:03 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 03:43:03 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:43:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 03:43:03 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 03:45:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:45:04 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 03:45:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 03:45:04 GMT
CMD ["bash"]
# Thu, 02 May 2024 03:45:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:45:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 03:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9f83335e3f34356129a65a46777f2c11b35558325643aeceb57ad34fcf26ae`  
		Last Modified: Thu, 02 May 2024 02:23:52 GMT  
		Size: 1.2 MB (1198590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9931bbbdc456888cafcfb45518f1f74377f7ded26c5caeba3779574b953c2f0`  
		Last Modified: Thu, 02 May 2024 02:23:51 GMT  
		Size: 5.6 MB (5553874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e642e2cde42d5ceebe85aeb8cafeb95dc3f33549056c16605dc5472621eeda6`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dca1471511de82e7b7117acd23c83c7a4b2921a02eb47a1a3af345c02fb841f`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dd00e528c2ec50f993c02fd6160d509b48e5a5acb8dfdf02312d1b1e167bbf`  
		Last Modified: Thu, 02 May 2024 04:20:49 GMT  
		Size: 177.0 MB (176995985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e02cf37cc416afb9263eebbfb2704d7335a88671a8dcd1510f44432d2c0623`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c3ee459bf535e354c3ae5772e5dc01acfc7c39896912f2cb3d0e028f483594`  
		Last Modified: Thu, 02 May 2024 04:21:05 GMT  
		Size: 50.9 MB (50942130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78880207582f574785e219e4fe9c0ed76d6a71bdb7737257f3e1e5eebbb9512`  
		Last Modified: Thu, 02 May 2024 04:20:58 GMT  
		Size: 321.3 KB (321273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e2631648f5934240033e56e0e8675f135439fcb185b941b63b2ad7b837cf7e`  
		Last Modified: Thu, 02 May 2024 04:20:58 GMT  
		Size: 1.1 MB (1130667 bytes)  
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
$ docker pull ros@sha256:426b24a25e905e7a99c5d27a0e884d6c27c1639540df0e81ed004218e83650e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251968388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4acf20dd6f86b259ef4aa91f7c85222bacb77ff86efa97f8ba4393441a1522e1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:34:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:35:16 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 01:35:16 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:35:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 01:35:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 01:38:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:38:45 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 01:38:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 01:38:46 GMT
CMD ["bash"]
# Thu, 02 May 2024 01:39:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:39:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 01:39:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:83049506c6eb6b11ef1a8774b3486a01a1804f7d13bd230b44788bc63248282d`  
		Last Modified: Mon, 29 Apr 2024 19:12:05 GMT  
		Size: 27.2 MB (27206145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf8574ed521f52190151260cb46f81577cb9462f025e4d0bd31fd5ef9164221`  
		Last Modified: Thu, 02 May 2024 02:25:54 GMT  
		Size: 1.2 MB (1199077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ba8bc7b1d97ec2940a42ab430797d38e66d94e8e1c3e1c239667352ac4a2be`  
		Last Modified: Thu, 02 May 2024 02:25:52 GMT  
		Size: 5.5 MB (5532618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170d525ddc0031398baf96e838661fd2ce78157cfebca7aa2ffef78821eaa76d`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3221e023c87709c99c3aa21599a3fb2755e867f8624231d7e701936a3942a9`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285463fcd2b1351b20e5bff4e1d55006a3f5afb2fc3f0798587caf9a3cfb0165`  
		Last Modified: Thu, 02 May 2024 02:26:25 GMT  
		Size: 171.4 MB (171383372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be132e8d75da72ae76fe687e3168eee676ea41b61b67592613c4d27948d4a842`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04978fbd01f4ac1f8deb48a3af3b6ae2156a3391bae378b5b70c6034c28bc86b`  
		Last Modified: Thu, 02 May 2024 02:26:39 GMT  
		Size: 45.2 MB (45207993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806a3b7368effc67cf6c5233658704ca94e11ba21d4cb3f96dc5dbd5c4c22152`  
		Last Modified: Thu, 02 May 2024 02:26:34 GMT  
		Size: 321.3 KB (321274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f453d39198ddd342125de1b67017e7b7cd521133b18a37e4d153b8c10f01f7c0`  
		Last Modified: Thu, 02 May 2024 02:26:34 GMT  
		Size: 1.1 MB (1115420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:781549532b63191b08acb2912cd989c80434edf03b8feed7973c181232363d59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:2fa31dda2e7666e0081f86dfc8b964ddd28078134a1c98f6ce77c41184ac62ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.7 MB (264729301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38effce76149ab2539a54ef9e175cd0e999e12862e55adc4b4459a06c0ef83b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:15:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:15:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:43:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:43:03 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 03:43:03 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:43:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 03:43:03 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 03:45:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:45:04 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 03:45:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 03:45:04 GMT
CMD ["bash"]
# Thu, 02 May 2024 03:45:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:45:36 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 03:45:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9f83335e3f34356129a65a46777f2c11b35558325643aeceb57ad34fcf26ae`  
		Last Modified: Thu, 02 May 2024 02:23:52 GMT  
		Size: 1.2 MB (1198590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9931bbbdc456888cafcfb45518f1f74377f7ded26c5caeba3779574b953c2f0`  
		Last Modified: Thu, 02 May 2024 02:23:51 GMT  
		Size: 5.6 MB (5553874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e642e2cde42d5ceebe85aeb8cafeb95dc3f33549056c16605dc5472621eeda6`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dca1471511de82e7b7117acd23c83c7a4b2921a02eb47a1a3af345c02fb841f`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dd00e528c2ec50f993c02fd6160d509b48e5a5acb8dfdf02312d1b1e167bbf`  
		Last Modified: Thu, 02 May 2024 04:20:49 GMT  
		Size: 177.0 MB (176995985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e02cf37cc416afb9263eebbfb2704d7335a88671a8dcd1510f44432d2c0623`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c3ee459bf535e354c3ae5772e5dc01acfc7c39896912f2cb3d0e028f483594`  
		Last Modified: Thu, 02 May 2024 04:21:05 GMT  
		Size: 50.9 MB (50942130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78880207582f574785e219e4fe9c0ed76d6a71bdb7737257f3e1e5eebbb9512`  
		Last Modified: Thu, 02 May 2024 04:20:58 GMT  
		Size: 321.3 KB (321273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e2631648f5934240033e56e0e8675f135439fcb185b941b63b2ad7b837cf7e`  
		Last Modified: Thu, 02 May 2024 04:20:58 GMT  
		Size: 1.1 MB (1130667 bytes)  
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
$ docker pull ros@sha256:426b24a25e905e7a99c5d27a0e884d6c27c1639540df0e81ed004218e83650e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251968388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4acf20dd6f86b259ef4aa91f7c85222bacb77ff86efa97f8ba4393441a1522e1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:34:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:35:16 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 01:35:16 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:35:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 01:35:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 01:38:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:38:45 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 01:38:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 01:38:46 GMT
CMD ["bash"]
# Thu, 02 May 2024 01:39:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:39:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 02 May 2024 01:39:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:83049506c6eb6b11ef1a8774b3486a01a1804f7d13bd230b44788bc63248282d`  
		Last Modified: Mon, 29 Apr 2024 19:12:05 GMT  
		Size: 27.2 MB (27206145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf8574ed521f52190151260cb46f81577cb9462f025e4d0bd31fd5ef9164221`  
		Last Modified: Thu, 02 May 2024 02:25:54 GMT  
		Size: 1.2 MB (1199077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ba8bc7b1d97ec2940a42ab430797d38e66d94e8e1c3e1c239667352ac4a2be`  
		Last Modified: Thu, 02 May 2024 02:25:52 GMT  
		Size: 5.5 MB (5532618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170d525ddc0031398baf96e838661fd2ce78157cfebca7aa2ffef78821eaa76d`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3221e023c87709c99c3aa21599a3fb2755e867f8624231d7e701936a3942a9`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285463fcd2b1351b20e5bff4e1d55006a3f5afb2fc3f0798587caf9a3cfb0165`  
		Last Modified: Thu, 02 May 2024 02:26:25 GMT  
		Size: 171.4 MB (171383372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be132e8d75da72ae76fe687e3168eee676ea41b61b67592613c4d27948d4a842`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04978fbd01f4ac1f8deb48a3af3b6ae2156a3391bae378b5b70c6034c28bc86b`  
		Last Modified: Thu, 02 May 2024 02:26:39 GMT  
		Size: 45.2 MB (45207993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806a3b7368effc67cf6c5233658704ca94e11ba21d4cb3f96dc5dbd5c4c22152`  
		Last Modified: Thu, 02 May 2024 02:26:34 GMT  
		Size: 321.3 KB (321274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f453d39198ddd342125de1b67017e7b7cd521133b18a37e4d153b8c10f01f7c0`  
		Last Modified: Thu, 02 May 2024 02:26:34 GMT  
		Size: 1.1 MB (1115420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:aead2395cd620305cb44153ce061a4035b97d2639b37a8649fd2f41b3062b04f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:1549c01a19e137ca2adffb8adcc064dfc68b69c93dcac6c8db94f56423b60153
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212335231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e33aa049acce3cd38efcd9d823ab68d2bc759d1f5b16293a790e4a6e08825f3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:15:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:15:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:43:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:43:03 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 03:43:03 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:43:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 03:43:03 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 03:45:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:45:04 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 03:45:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 03:45:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9f83335e3f34356129a65a46777f2c11b35558325643aeceb57ad34fcf26ae`  
		Last Modified: Thu, 02 May 2024 02:23:52 GMT  
		Size: 1.2 MB (1198590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9931bbbdc456888cafcfb45518f1f74377f7ded26c5caeba3779574b953c2f0`  
		Last Modified: Thu, 02 May 2024 02:23:51 GMT  
		Size: 5.6 MB (5553874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e642e2cde42d5ceebe85aeb8cafeb95dc3f33549056c16605dc5472621eeda6`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dca1471511de82e7b7117acd23c83c7a4b2921a02eb47a1a3af345c02fb841f`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dd00e528c2ec50f993c02fd6160d509b48e5a5acb8dfdf02312d1b1e167bbf`  
		Last Modified: Thu, 02 May 2024 04:20:49 GMT  
		Size: 177.0 MB (176995985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e02cf37cc416afb9263eebbfb2704d7335a88671a8dcd1510f44432d2c0623`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 196.0 B  
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
$ docker pull ros@sha256:f83872bc4b9d0c7cac26a6496321cf50e6892632baf94337b77b76b13df6d87a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205323701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e165c10d9970e0beb7affaa1f8fcaac53cc411d2b78d3c25300459ef805a50a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:34:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:35:16 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 01:35:16 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:35:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 01:35:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 01:38:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:38:45 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 01:38:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 01:38:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:83049506c6eb6b11ef1a8774b3486a01a1804f7d13bd230b44788bc63248282d`  
		Last Modified: Mon, 29 Apr 2024 19:12:05 GMT  
		Size: 27.2 MB (27206145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf8574ed521f52190151260cb46f81577cb9462f025e4d0bd31fd5ef9164221`  
		Last Modified: Thu, 02 May 2024 02:25:54 GMT  
		Size: 1.2 MB (1199077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ba8bc7b1d97ec2940a42ab430797d38e66d94e8e1c3e1c239667352ac4a2be`  
		Last Modified: Thu, 02 May 2024 02:25:52 GMT  
		Size: 5.5 MB (5532618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170d525ddc0031398baf96e838661fd2ce78157cfebca7aa2ffef78821eaa76d`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3221e023c87709c99c3aa21599a3fb2755e867f8624231d7e701936a3942a9`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285463fcd2b1351b20e5bff4e1d55006a3f5afb2fc3f0798587caf9a3cfb0165`  
		Last Modified: Thu, 02 May 2024 02:26:25 GMT  
		Size: 171.4 MB (171383372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be132e8d75da72ae76fe687e3168eee676ea41b61b67592613c4d27948d4a842`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:aead2395cd620305cb44153ce061a4035b97d2639b37a8649fd2f41b3062b04f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:1549c01a19e137ca2adffb8adcc064dfc68b69c93dcac6c8db94f56423b60153
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212335231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e33aa049acce3cd38efcd9d823ab68d2bc759d1f5b16293a790e4a6e08825f3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:15:46 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:15:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:43:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 03:43:03 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 03:43:03 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 03:43:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 03:43:03 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 03:45:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:45:04 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 03:45:04 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 03:45:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9f83335e3f34356129a65a46777f2c11b35558325643aeceb57ad34fcf26ae`  
		Last Modified: Thu, 02 May 2024 02:23:52 GMT  
		Size: 1.2 MB (1198590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9931bbbdc456888cafcfb45518f1f74377f7ded26c5caeba3779574b953c2f0`  
		Last Modified: Thu, 02 May 2024 02:23:51 GMT  
		Size: 5.6 MB (5553874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e642e2cde42d5ceebe85aeb8cafeb95dc3f33549056c16605dc5472621eeda6`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 2.0 KB (2017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dca1471511de82e7b7117acd23c83c7a4b2921a02eb47a1a3af345c02fb841f`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dd00e528c2ec50f993c02fd6160d509b48e5a5acb8dfdf02312d1b1e167bbf`  
		Last Modified: Thu, 02 May 2024 04:20:49 GMT  
		Size: 177.0 MB (176995985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e02cf37cc416afb9263eebbfb2704d7335a88671a8dcd1510f44432d2c0623`  
		Last Modified: Thu, 02 May 2024 04:20:22 GMT  
		Size: 196.0 B  
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
$ docker pull ros@sha256:f83872bc4b9d0c7cac26a6496321cf50e6892632baf94337b77b76b13df6d87a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205323701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e165c10d9970e0beb7affaa1f8fcaac53cc411d2b78d3c25300459ef805a50a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:34:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:35:15 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 01:35:16 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 02 May 2024 01:35:16 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 01:35:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 01:35:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 02 May 2024 01:38:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:38:45 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 02 May 2024 01:38:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 02 May 2024 01:38:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:83049506c6eb6b11ef1a8774b3486a01a1804f7d13bd230b44788bc63248282d`  
		Last Modified: Mon, 29 Apr 2024 19:12:05 GMT  
		Size: 27.2 MB (27206145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf8574ed521f52190151260cb46f81577cb9462f025e4d0bd31fd5ef9164221`  
		Last Modified: Thu, 02 May 2024 02:25:54 GMT  
		Size: 1.2 MB (1199077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ba8bc7b1d97ec2940a42ab430797d38e66d94e8e1c3e1c239667352ac4a2be`  
		Last Modified: Thu, 02 May 2024 02:25:52 GMT  
		Size: 5.5 MB (5532618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170d525ddc0031398baf96e838661fd2ce78157cfebca7aa2ffef78821eaa76d`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3221e023c87709c99c3aa21599a3fb2755e867f8624231d7e701936a3942a9`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285463fcd2b1351b20e5bff4e1d55006a3f5afb2fc3f0798587caf9a3cfb0165`  
		Last Modified: Thu, 02 May 2024 02:26:25 GMT  
		Size: 171.4 MB (171383372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be132e8d75da72ae76fe687e3168eee676ea41b61b67592613c4d27948d4a842`  
		Last Modified: Thu, 02 May 2024 02:25:51 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling`

```console
$ docker pull ros@sha256:b9eab8ac3d73d8d83cee11b014845a6387f3681db5a4629a5f90d03327d8a67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:e9abb5783131b9944bb30f3bf77814bc7215506d0b69c22ab23580107a59426d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302115842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1186d494b6a39e4ca32a14a08a99e937943a2d5cba14b76e35bfbfdce2b1dc67`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 04:08:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:17:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 04:17:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 04:17:14 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 21:34:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 21:34:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 21:34:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 21:34:24 GMT
CMD ["bash"]
# Fri, 24 May 2024 21:35:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 21:35:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 21:35:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 21:35:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60661c1b414a0df1f47a75ebe6ee30ab62a190e137eadd8830b58f26d265393`  
		Last Modified: Thu, 02 May 2024 04:27:58 GMT  
		Size: 683.6 KB (683555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c08bb4286c80bd46824cabefede6374d8260920dfcae18a52d6db76894e5e4b`  
		Last Modified: Thu, 02 May 2024 04:27:57 GMT  
		Size: 4.6 MB (4617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f6c812b379d4de9914ffcc55c356485f1907555705bd50fdf0629e37742e9`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78533fe08fdd62d113279815db4b7a14ab1686b1f85f09290bc47b27da4004e`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85106c03d3ddc3385408b7c37cd8222141a83aba79b86de526e777de6451996f`  
		Last Modified: Fri, 24 May 2024 21:39:02 GMT  
		Size: 124.8 MB (124817026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23c173b29a00075fea4ff0384195c1b2f433920a2791c5de0a5734608221f99`  
		Last Modified: Fri, 24 May 2024 21:38:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ccd436aff1797542d785fe2d21548bbdbd33bfa9de21a9a4e07709515de564`  
		Last Modified: Fri, 24 May 2024 21:39:25 GMT  
		Size: 114.3 MB (114313028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9311ed60be103591ef6803f1c0d07f49e5654402d542e34de9bb76b78b840e43`  
		Last Modified: Fri, 24 May 2024 21:39:10 GMT  
		Size: 311.1 KB (311084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da4b7a314399a6d8f2aa03ba296793df4ac9a320dcb6b14ea8a94854338d715`  
		Last Modified: Fri, 24 May 2024 21:39:10 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7079b7225bc737db75abdd31d0ebb0eda29aeea1151692ce63045bdda8101503`  
		Last Modified: Fri, 24 May 2024 21:39:14 GMT  
		Size: 27.7 MB (27666160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d75a60d43eb1dd6c47ce55b6a2b7a115749a7abcd0cb698cd0f48f21148602d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292070170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c048e95ca6ada87453d5b29bd5d6a1c83aae48f7f34d1b61aff99de50d780e1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:11:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:11:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:23:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 02:23:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 02:23:04 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 22:29:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 22:29:49 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 22:29:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 22:29:49 GMT
CMD ["bash"]
# Fri, 24 May 2024 22:30:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 22:30:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 22:30:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 22:31:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6566430a89b8fd522af510326683dfd547bb47ce3368e0e7c13d03c03a259a73`  
		Last Modified: Thu, 02 May 2024 02:33:11 GMT  
		Size: 683.8 KB (683795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c10c1a69a349bd188a99420ce3e817a3ff04579654dbb1e5fcabc0a226ba0dd`  
		Last Modified: Thu, 02 May 2024 02:33:09 GMT  
		Size: 4.6 MB (4611814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6931defe7f57cf3da1981f2afca9fe611d4b03bf445f980fdc842c4d965bf247`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5315899036e815d56227da46abcb970890f5f1c1388a96cdf9d489dd96e5d058`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f29c42f8d570f69bfb90310c0b1ced461b209f637cc57060163682ff0e82fc`  
		Last Modified: Fri, 24 May 2024 22:34:25 GMT  
		Size: 119.5 MB (119455126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9722aa09e2806b22bc37868ef46302c1e92883f25b36415de9d7015347f6c2`  
		Last Modified: Fri, 24 May 2024 22:34:11 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6dbe923948c5e24d28f7c91f0ceaedb29a6f80fce780350a85fdef3bef12fd`  
		Last Modified: Fri, 24 May 2024 22:34:44 GMT  
		Size: 111.2 MB (111153371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee72e281a670cd589a7a7d5b632b3ec3fcbedc4ffaffa13069cb5114a1a43ba`  
		Last Modified: Fri, 24 May 2024 22:34:33 GMT  
		Size: 311.1 KB (311079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928e44bba5163104f72339d66644ca5888d777918553e690f0fbedde1698a67b`  
		Last Modified: Fri, 24 May 2024 22:34:33 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2586d979f632496536ad00cdec2f7816d536c46cef1a1ae169be4dcc1d08a7b`  
		Last Modified: Fri, 24 May 2024 22:34:36 GMT  
		Size: 26.8 MB (26811360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:91314ee1dc4b7ec1aa57829aad118a8fe31a2346d9e57cbdd741ab72c15caaf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:3619813fbf6a9ece0be81f1d792029f43f0f4ebb65ba1cb9cb137fb165a5703e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.2 MB (626154819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761f6479de3d09f62cee5db9cba33af8a4afb4aad6444661983ed0780f3bc4ac`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 04:08:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:17:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 04:17:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 04:17:14 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 21:34:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 21:34:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 21:34:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 21:34:24 GMT
CMD ["bash"]
# Fri, 24 May 2024 21:35:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 21:35:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 21:35:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 21:35:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 21:37:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60661c1b414a0df1f47a75ebe6ee30ab62a190e137eadd8830b58f26d265393`  
		Last Modified: Thu, 02 May 2024 04:27:58 GMT  
		Size: 683.6 KB (683555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c08bb4286c80bd46824cabefede6374d8260920dfcae18a52d6db76894e5e4b`  
		Last Modified: Thu, 02 May 2024 04:27:57 GMT  
		Size: 4.6 MB (4617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f6c812b379d4de9914ffcc55c356485f1907555705bd50fdf0629e37742e9`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78533fe08fdd62d113279815db4b7a14ab1686b1f85f09290bc47b27da4004e`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85106c03d3ddc3385408b7c37cd8222141a83aba79b86de526e777de6451996f`  
		Last Modified: Fri, 24 May 2024 21:39:02 GMT  
		Size: 124.8 MB (124817026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23c173b29a00075fea4ff0384195c1b2f433920a2791c5de0a5734608221f99`  
		Last Modified: Fri, 24 May 2024 21:38:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ccd436aff1797542d785fe2d21548bbdbd33bfa9de21a9a4e07709515de564`  
		Last Modified: Fri, 24 May 2024 21:39:25 GMT  
		Size: 114.3 MB (114313028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9311ed60be103591ef6803f1c0d07f49e5654402d542e34de9bb76b78b840e43`  
		Last Modified: Fri, 24 May 2024 21:39:10 GMT  
		Size: 311.1 KB (311084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da4b7a314399a6d8f2aa03ba296793df4ac9a320dcb6b14ea8a94854338d715`  
		Last Modified: Fri, 24 May 2024 21:39:10 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7079b7225bc737db75abdd31d0ebb0eda29aeea1151692ce63045bdda8101503`  
		Last Modified: Fri, 24 May 2024 21:39:14 GMT  
		Size: 27.7 MB (27666160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9451ac84327c4e39e3d330b9ba0250b07cd5758ed340c8c97e2ff1551fa46f`  
		Last Modified: Fri, 24 May 2024 21:40:18 GMT  
		Size: 324.0 MB (324038977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:62cbe08efede949e4f1d1a4e8f44d4f8f18a4df4653a6f6c64de6e53e9754660
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.2 MB (569244524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb4725a4bab77a85d50a66ae43acbec29cd39d1bcb7d59d90e7490ff470e767`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:11:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:11:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:23:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 02:23:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 02:23:04 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 22:29:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 22:29:49 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 22:29:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 22:29:49 GMT
CMD ["bash"]
# Fri, 24 May 2024 22:30:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 22:30:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 22:30:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 22:31:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 22:33:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6566430a89b8fd522af510326683dfd547bb47ce3368e0e7c13d03c03a259a73`  
		Last Modified: Thu, 02 May 2024 02:33:11 GMT  
		Size: 683.8 KB (683795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c10c1a69a349bd188a99420ce3e817a3ff04579654dbb1e5fcabc0a226ba0dd`  
		Last Modified: Thu, 02 May 2024 02:33:09 GMT  
		Size: 4.6 MB (4611814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6931defe7f57cf3da1981f2afca9fe611d4b03bf445f980fdc842c4d965bf247`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5315899036e815d56227da46abcb970890f5f1c1388a96cdf9d489dd96e5d058`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f29c42f8d570f69bfb90310c0b1ced461b209f637cc57060163682ff0e82fc`  
		Last Modified: Fri, 24 May 2024 22:34:25 GMT  
		Size: 119.5 MB (119455126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9722aa09e2806b22bc37868ef46302c1e92883f25b36415de9d7015347f6c2`  
		Last Modified: Fri, 24 May 2024 22:34:11 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6dbe923948c5e24d28f7c91f0ceaedb29a6f80fce780350a85fdef3bef12fd`  
		Last Modified: Fri, 24 May 2024 22:34:44 GMT  
		Size: 111.2 MB (111153371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee72e281a670cd589a7a7d5b632b3ec3fcbedc4ffaffa13069cb5114a1a43ba`  
		Last Modified: Fri, 24 May 2024 22:34:33 GMT  
		Size: 311.1 KB (311079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928e44bba5163104f72339d66644ca5888d777918553e690f0fbedde1698a67b`  
		Last Modified: Fri, 24 May 2024 22:34:33 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2586d979f632496536ad00cdec2f7816d536c46cef1a1ae169be4dcc1d08a7b`  
		Last Modified: Fri, 24 May 2024 22:34:36 GMT  
		Size: 26.8 MB (26811360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03869d9ac5e66ba6afd267ed4e9e4548d797cabcfebb34de3f88e55750aceb50`  
		Last Modified: Fri, 24 May 2024 22:35:23 GMT  
		Size: 277.2 MB (277174354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception-noble`

```console
$ docker pull ros@sha256:91314ee1dc4b7ec1aa57829aad118a8fe31a2346d9e57cbdd741ab72c15caaf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception-noble` - linux; amd64

```console
$ docker pull ros@sha256:3619813fbf6a9ece0be81f1d792029f43f0f4ebb65ba1cb9cb137fb165a5703e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.2 MB (626154819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761f6479de3d09f62cee5db9cba33af8a4afb4aad6444661983ed0780f3bc4ac`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 04:08:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:17:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 04:17:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 04:17:14 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 21:34:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 21:34:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 21:34:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 21:34:24 GMT
CMD ["bash"]
# Fri, 24 May 2024 21:35:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 21:35:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 21:35:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 21:35:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 21:37:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60661c1b414a0df1f47a75ebe6ee30ab62a190e137eadd8830b58f26d265393`  
		Last Modified: Thu, 02 May 2024 04:27:58 GMT  
		Size: 683.6 KB (683555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c08bb4286c80bd46824cabefede6374d8260920dfcae18a52d6db76894e5e4b`  
		Last Modified: Thu, 02 May 2024 04:27:57 GMT  
		Size: 4.6 MB (4617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f6c812b379d4de9914ffcc55c356485f1907555705bd50fdf0629e37742e9`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78533fe08fdd62d113279815db4b7a14ab1686b1f85f09290bc47b27da4004e`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85106c03d3ddc3385408b7c37cd8222141a83aba79b86de526e777de6451996f`  
		Last Modified: Fri, 24 May 2024 21:39:02 GMT  
		Size: 124.8 MB (124817026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23c173b29a00075fea4ff0384195c1b2f433920a2791c5de0a5734608221f99`  
		Last Modified: Fri, 24 May 2024 21:38:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ccd436aff1797542d785fe2d21548bbdbd33bfa9de21a9a4e07709515de564`  
		Last Modified: Fri, 24 May 2024 21:39:25 GMT  
		Size: 114.3 MB (114313028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9311ed60be103591ef6803f1c0d07f49e5654402d542e34de9bb76b78b840e43`  
		Last Modified: Fri, 24 May 2024 21:39:10 GMT  
		Size: 311.1 KB (311084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da4b7a314399a6d8f2aa03ba296793df4ac9a320dcb6b14ea8a94854338d715`  
		Last Modified: Fri, 24 May 2024 21:39:10 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7079b7225bc737db75abdd31d0ebb0eda29aeea1151692ce63045bdda8101503`  
		Last Modified: Fri, 24 May 2024 21:39:14 GMT  
		Size: 27.7 MB (27666160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9451ac84327c4e39e3d330b9ba0250b07cd5758ed340c8c97e2ff1551fa46f`  
		Last Modified: Fri, 24 May 2024 21:40:18 GMT  
		Size: 324.0 MB (324038977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:62cbe08efede949e4f1d1a4e8f44d4f8f18a4df4653a6f6c64de6e53e9754660
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.2 MB (569244524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb4725a4bab77a85d50a66ae43acbec29cd39d1bcb7d59d90e7490ff470e767`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:11:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:11:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:23:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 02:23:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 02:23:04 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 22:29:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 22:29:49 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 22:29:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 22:29:49 GMT
CMD ["bash"]
# Fri, 24 May 2024 22:30:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 22:30:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 22:30:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 22:31:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 22:33:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6566430a89b8fd522af510326683dfd547bb47ce3368e0e7c13d03c03a259a73`  
		Last Modified: Thu, 02 May 2024 02:33:11 GMT  
		Size: 683.8 KB (683795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c10c1a69a349bd188a99420ce3e817a3ff04579654dbb1e5fcabc0a226ba0dd`  
		Last Modified: Thu, 02 May 2024 02:33:09 GMT  
		Size: 4.6 MB (4611814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6931defe7f57cf3da1981f2afca9fe611d4b03bf445f980fdc842c4d965bf247`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5315899036e815d56227da46abcb970890f5f1c1388a96cdf9d489dd96e5d058`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f29c42f8d570f69bfb90310c0b1ced461b209f637cc57060163682ff0e82fc`  
		Last Modified: Fri, 24 May 2024 22:34:25 GMT  
		Size: 119.5 MB (119455126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9722aa09e2806b22bc37868ef46302c1e92883f25b36415de9d7015347f6c2`  
		Last Modified: Fri, 24 May 2024 22:34:11 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6dbe923948c5e24d28f7c91f0ceaedb29a6f80fce780350a85fdef3bef12fd`  
		Last Modified: Fri, 24 May 2024 22:34:44 GMT  
		Size: 111.2 MB (111153371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee72e281a670cd589a7a7d5b632b3ec3fcbedc4ffaffa13069cb5114a1a43ba`  
		Last Modified: Fri, 24 May 2024 22:34:33 GMT  
		Size: 311.1 KB (311079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928e44bba5163104f72339d66644ca5888d777918553e690f0fbedde1698a67b`  
		Last Modified: Fri, 24 May 2024 22:34:33 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2586d979f632496536ad00cdec2f7816d536c46cef1a1ae169be4dcc1d08a7b`  
		Last Modified: Fri, 24 May 2024 22:34:36 GMT  
		Size: 26.8 MB (26811360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03869d9ac5e66ba6afd267ed4e9e4548d797cabcfebb34de3f88e55750aceb50`  
		Last Modified: Fri, 24 May 2024 22:35:23 GMT  
		Size: 277.2 MB (277174354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:b9eab8ac3d73d8d83cee11b014845a6387f3681db5a4629a5f90d03327d8a67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:e9abb5783131b9944bb30f3bf77814bc7215506d0b69c22ab23580107a59426d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302115842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1186d494b6a39e4ca32a14a08a99e937943a2d5cba14b76e35bfbfdce2b1dc67`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 04:08:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:17:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 04:17:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 04:17:14 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 21:34:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 21:34:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 21:34:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 21:34:24 GMT
CMD ["bash"]
# Fri, 24 May 2024 21:35:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 21:35:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 21:35:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 21:35:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60661c1b414a0df1f47a75ebe6ee30ab62a190e137eadd8830b58f26d265393`  
		Last Modified: Thu, 02 May 2024 04:27:58 GMT  
		Size: 683.6 KB (683555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c08bb4286c80bd46824cabefede6374d8260920dfcae18a52d6db76894e5e4b`  
		Last Modified: Thu, 02 May 2024 04:27:57 GMT  
		Size: 4.6 MB (4617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f6c812b379d4de9914ffcc55c356485f1907555705bd50fdf0629e37742e9`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78533fe08fdd62d113279815db4b7a14ab1686b1f85f09290bc47b27da4004e`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85106c03d3ddc3385408b7c37cd8222141a83aba79b86de526e777de6451996f`  
		Last Modified: Fri, 24 May 2024 21:39:02 GMT  
		Size: 124.8 MB (124817026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23c173b29a00075fea4ff0384195c1b2f433920a2791c5de0a5734608221f99`  
		Last Modified: Fri, 24 May 2024 21:38:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ccd436aff1797542d785fe2d21548bbdbd33bfa9de21a9a4e07709515de564`  
		Last Modified: Fri, 24 May 2024 21:39:25 GMT  
		Size: 114.3 MB (114313028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9311ed60be103591ef6803f1c0d07f49e5654402d542e34de9bb76b78b840e43`  
		Last Modified: Fri, 24 May 2024 21:39:10 GMT  
		Size: 311.1 KB (311084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da4b7a314399a6d8f2aa03ba296793df4ac9a320dcb6b14ea8a94854338d715`  
		Last Modified: Fri, 24 May 2024 21:39:10 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7079b7225bc737db75abdd31d0ebb0eda29aeea1151692ce63045bdda8101503`  
		Last Modified: Fri, 24 May 2024 21:39:14 GMT  
		Size: 27.7 MB (27666160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d75a60d43eb1dd6c47ce55b6a2b7a115749a7abcd0cb698cd0f48f21148602d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292070170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c048e95ca6ada87453d5b29bd5d6a1c83aae48f7f34d1b61aff99de50d780e1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:11:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:11:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:23:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 02:23:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 02:23:04 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 22:29:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 22:29:49 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 22:29:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 22:29:49 GMT
CMD ["bash"]
# Fri, 24 May 2024 22:30:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 22:30:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 22:30:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 22:31:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6566430a89b8fd522af510326683dfd547bb47ce3368e0e7c13d03c03a259a73`  
		Last Modified: Thu, 02 May 2024 02:33:11 GMT  
		Size: 683.8 KB (683795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c10c1a69a349bd188a99420ce3e817a3ff04579654dbb1e5fcabc0a226ba0dd`  
		Last Modified: Thu, 02 May 2024 02:33:09 GMT  
		Size: 4.6 MB (4611814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6931defe7f57cf3da1981f2afca9fe611d4b03bf445f980fdc842c4d965bf247`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5315899036e815d56227da46abcb970890f5f1c1388a96cdf9d489dd96e5d058`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f29c42f8d570f69bfb90310c0b1ced461b209f637cc57060163682ff0e82fc`  
		Last Modified: Fri, 24 May 2024 22:34:25 GMT  
		Size: 119.5 MB (119455126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9722aa09e2806b22bc37868ef46302c1e92883f25b36415de9d7015347f6c2`  
		Last Modified: Fri, 24 May 2024 22:34:11 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6dbe923948c5e24d28f7c91f0ceaedb29a6f80fce780350a85fdef3bef12fd`  
		Last Modified: Fri, 24 May 2024 22:34:44 GMT  
		Size: 111.2 MB (111153371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee72e281a670cd589a7a7d5b632b3ec3fcbedc4ffaffa13069cb5114a1a43ba`  
		Last Modified: Fri, 24 May 2024 22:34:33 GMT  
		Size: 311.1 KB (311079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928e44bba5163104f72339d66644ca5888d777918553e690f0fbedde1698a67b`  
		Last Modified: Fri, 24 May 2024 22:34:33 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2586d979f632496536ad00cdec2f7816d536c46cef1a1ae169be4dcc1d08a7b`  
		Last Modified: Fri, 24 May 2024 22:34:36 GMT  
		Size: 26.8 MB (26811360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base-noble`

```console
$ docker pull ros@sha256:b9eab8ac3d73d8d83cee11b014845a6387f3681db5a4629a5f90d03327d8a67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-noble` - linux; amd64

```console
$ docker pull ros@sha256:e9abb5783131b9944bb30f3bf77814bc7215506d0b69c22ab23580107a59426d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302115842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1186d494b6a39e4ca32a14a08a99e937943a2d5cba14b76e35bfbfdce2b1dc67`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 04:08:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:17:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 04:17:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 04:17:14 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 21:34:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 21:34:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 21:34:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 21:34:24 GMT
CMD ["bash"]
# Fri, 24 May 2024 21:35:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 21:35:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 21:35:17 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 21:35:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60661c1b414a0df1f47a75ebe6ee30ab62a190e137eadd8830b58f26d265393`  
		Last Modified: Thu, 02 May 2024 04:27:58 GMT  
		Size: 683.6 KB (683555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c08bb4286c80bd46824cabefede6374d8260920dfcae18a52d6db76894e5e4b`  
		Last Modified: Thu, 02 May 2024 04:27:57 GMT  
		Size: 4.6 MB (4617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f6c812b379d4de9914ffcc55c356485f1907555705bd50fdf0629e37742e9`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78533fe08fdd62d113279815db4b7a14ab1686b1f85f09290bc47b27da4004e`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85106c03d3ddc3385408b7c37cd8222141a83aba79b86de526e777de6451996f`  
		Last Modified: Fri, 24 May 2024 21:39:02 GMT  
		Size: 124.8 MB (124817026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23c173b29a00075fea4ff0384195c1b2f433920a2791c5de0a5734608221f99`  
		Last Modified: Fri, 24 May 2024 21:38:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ccd436aff1797542d785fe2d21548bbdbd33bfa9de21a9a4e07709515de564`  
		Last Modified: Fri, 24 May 2024 21:39:25 GMT  
		Size: 114.3 MB (114313028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9311ed60be103591ef6803f1c0d07f49e5654402d542e34de9bb76b78b840e43`  
		Last Modified: Fri, 24 May 2024 21:39:10 GMT  
		Size: 311.1 KB (311084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da4b7a314399a6d8f2aa03ba296793df4ac9a320dcb6b14ea8a94854338d715`  
		Last Modified: Fri, 24 May 2024 21:39:10 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7079b7225bc737db75abdd31d0ebb0eda29aeea1151692ce63045bdda8101503`  
		Last Modified: Fri, 24 May 2024 21:39:14 GMT  
		Size: 27.7 MB (27666160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d75a60d43eb1dd6c47ce55b6a2b7a115749a7abcd0cb698cd0f48f21148602d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292070170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c048e95ca6ada87453d5b29bd5d6a1c83aae48f7f34d1b61aff99de50d780e1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:11:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:11:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:23:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 02:23:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 02:23:04 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 22:29:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 22:29:49 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 22:29:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 22:29:49 GMT
CMD ["bash"]
# Fri, 24 May 2024 22:30:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 22:30:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 May 2024 22:30:36 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 May 2024 22:31:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6566430a89b8fd522af510326683dfd547bb47ce3368e0e7c13d03c03a259a73`  
		Last Modified: Thu, 02 May 2024 02:33:11 GMT  
		Size: 683.8 KB (683795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c10c1a69a349bd188a99420ce3e817a3ff04579654dbb1e5fcabc0a226ba0dd`  
		Last Modified: Thu, 02 May 2024 02:33:09 GMT  
		Size: 4.6 MB (4611814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6931defe7f57cf3da1981f2afca9fe611d4b03bf445f980fdc842c4d965bf247`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5315899036e815d56227da46abcb970890f5f1c1388a96cdf9d489dd96e5d058`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f29c42f8d570f69bfb90310c0b1ced461b209f637cc57060163682ff0e82fc`  
		Last Modified: Fri, 24 May 2024 22:34:25 GMT  
		Size: 119.5 MB (119455126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9722aa09e2806b22bc37868ef46302c1e92883f25b36415de9d7015347f6c2`  
		Last Modified: Fri, 24 May 2024 22:34:11 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6dbe923948c5e24d28f7c91f0ceaedb29a6f80fce780350a85fdef3bef12fd`  
		Last Modified: Fri, 24 May 2024 22:34:44 GMT  
		Size: 111.2 MB (111153371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee72e281a670cd589a7a7d5b632b3ec3fcbedc4ffaffa13069cb5114a1a43ba`  
		Last Modified: Fri, 24 May 2024 22:34:33 GMT  
		Size: 311.1 KB (311079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928e44bba5163104f72339d66644ca5888d777918553e690f0fbedde1698a67b`  
		Last Modified: Fri, 24 May 2024 22:34:33 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2586d979f632496536ad00cdec2f7816d536c46cef1a1ae169be4dcc1d08a7b`  
		Last Modified: Fri, 24 May 2024 22:34:36 GMT  
		Size: 26.8 MB (26811360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:bf6bec93ec45d9336fa90ab96ba7c0615755d149ec816ebf7372797b38bfefc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:b15467c2f996f925952cc2a6d65b228faa6bdc38278f06cbc8a0199ce7ae07de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159823084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbafa2931e716ef5e0b0d9a55e2155ad15e48014c0dd905c4e1c3e667291f64`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 04:08:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:17:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 04:17:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 04:17:14 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 21:34:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 21:34:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 21:34:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 21:34:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60661c1b414a0df1f47a75ebe6ee30ab62a190e137eadd8830b58f26d265393`  
		Last Modified: Thu, 02 May 2024 04:27:58 GMT  
		Size: 683.6 KB (683555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c08bb4286c80bd46824cabefede6374d8260920dfcae18a52d6db76894e5e4b`  
		Last Modified: Thu, 02 May 2024 04:27:57 GMT  
		Size: 4.6 MB (4617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f6c812b379d4de9914ffcc55c356485f1907555705bd50fdf0629e37742e9`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78533fe08fdd62d113279815db4b7a14ab1686b1f85f09290bc47b27da4004e`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85106c03d3ddc3385408b7c37cd8222141a83aba79b86de526e777de6451996f`  
		Last Modified: Fri, 24 May 2024 21:39:02 GMT  
		Size: 124.8 MB (124817026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23c173b29a00075fea4ff0384195c1b2f433920a2791c5de0a5734608221f99`  
		Last Modified: Fri, 24 May 2024 21:38:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:532a0acd6efbaf926e967d5e393cf73a775b2f5774720c576bb9544d6c9fe866
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153791893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6358efb54e7e2f80fb995424aa99633be4bc0b4c9f1414f963b6b8a72b2737ed`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:11:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:11:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:23:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 02:23:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 02:23:04 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 22:29:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 22:29:49 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 22:29:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 22:29:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6566430a89b8fd522af510326683dfd547bb47ce3368e0e7c13d03c03a259a73`  
		Last Modified: Thu, 02 May 2024 02:33:11 GMT  
		Size: 683.8 KB (683795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c10c1a69a349bd188a99420ce3e817a3ff04579654dbb1e5fcabc0a226ba0dd`  
		Last Modified: Thu, 02 May 2024 02:33:09 GMT  
		Size: 4.6 MB (4611814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6931defe7f57cf3da1981f2afca9fe611d4b03bf445f980fdc842c4d965bf247`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5315899036e815d56227da46abcb970890f5f1c1388a96cdf9d489dd96e5d058`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f29c42f8d570f69bfb90310c0b1ced461b209f637cc57060163682ff0e82fc`  
		Last Modified: Fri, 24 May 2024 22:34:25 GMT  
		Size: 119.5 MB (119455126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9722aa09e2806b22bc37868ef46302c1e92883f25b36415de9d7015347f6c2`  
		Last Modified: Fri, 24 May 2024 22:34:11 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core-noble`

```console
$ docker pull ros@sha256:bf6bec93ec45d9336fa90ab96ba7c0615755d149ec816ebf7372797b38bfefc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-noble` - linux; amd64

```console
$ docker pull ros@sha256:b15467c2f996f925952cc2a6d65b228faa6bdc38278f06cbc8a0199ce7ae07de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159823084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbafa2931e716ef5e0b0d9a55e2155ad15e48014c0dd905c4e1c3e667291f64`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 04:08:40 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:08:57 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:17:13 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 04:17:14 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 04:17:14 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 04:17:14 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 21:34:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 21:34:24 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 21:34:24 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 21:34:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60661c1b414a0df1f47a75ebe6ee30ab62a190e137eadd8830b58f26d265393`  
		Last Modified: Thu, 02 May 2024 04:27:58 GMT  
		Size: 683.6 KB (683555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c08bb4286c80bd46824cabefede6374d8260920dfcae18a52d6db76894e5e4b`  
		Last Modified: Thu, 02 May 2024 04:27:57 GMT  
		Size: 4.6 MB (4617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f6c812b379d4de9914ffcc55c356485f1907555705bd50fdf0629e37742e9`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78533fe08fdd62d113279815db4b7a14ab1686b1f85f09290bc47b27da4004e`  
		Last Modified: Thu, 02 May 2024 04:29:42 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85106c03d3ddc3385408b7c37cd8222141a83aba79b86de526e777de6451996f`  
		Last Modified: Fri, 24 May 2024 21:39:02 GMT  
		Size: 124.8 MB (124817026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23c173b29a00075fea4ff0384195c1b2f433920a2791c5de0a5734608221f99`  
		Last Modified: Fri, 24 May 2024 21:38:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core-noble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:532a0acd6efbaf926e967d5e393cf73a775b2f5774720c576bb9544d6c9fe866
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153791893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6358efb54e7e2f80fb995424aa99633be4bc0b4c9f1414f963b6b8a72b2737ed`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:11:22 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:11:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:23:03 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros2-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME"
# Thu, 02 May 2024 02:23:04 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros2-latest-archive-keyring.gpg ] http://packages.ros.org/ros2/ubuntu noble main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 02 May 2024 02:23:04 GMT
ENV LANG=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV LC_ALL=C.UTF-8
# Thu, 02 May 2024 02:23:04 GMT
ENV ROS_DISTRO=rolling
# Fri, 24 May 2024 22:29:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.11.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 May 2024 22:29:49 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 24 May 2024 22:29:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 May 2024 22:29:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6566430a89b8fd522af510326683dfd547bb47ce3368e0e7c13d03c03a259a73`  
		Last Modified: Thu, 02 May 2024 02:33:11 GMT  
		Size: 683.8 KB (683795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c10c1a69a349bd188a99420ce3e817a3ff04579654dbb1e5fcabc0a226ba0dd`  
		Last Modified: Thu, 02 May 2024 02:33:09 GMT  
		Size: 4.6 MB (4611814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6931defe7f57cf3da1981f2afca9fe611d4b03bf445f980fdc842c4d965bf247`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5315899036e815d56227da46abcb970890f5f1c1388a96cdf9d489dd96e5d058`  
		Last Modified: Thu, 02 May 2024 02:34:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f29c42f8d570f69bfb90310c0b1ced461b209f637cc57060163682ff0e82fc`  
		Last Modified: Fri, 24 May 2024 22:34:25 GMT  
		Size: 119.5 MB (119455126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9722aa09e2806b22bc37868ef46302c1e92883f25b36415de9d7015347f6c2`  
		Last Modified: Fri, 24 May 2024 22:34:11 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
