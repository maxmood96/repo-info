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
$ docker pull ros@sha256:c2f05668bc47f0c29de8a062e858b4d292328c9a8ab5d3a4578989dfe5a47991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:15dbc5efef92470bd7998b50de6cb878b2b42122c45141beedff16ed68371072
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263475791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f430a3a98e1d1077d42502cbd151c0570d0ff47b4378a56585ca1c8749929fbc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV ROS_DISTRO=humble
# Sat, 02 Dec 2023 05:29:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:29:10 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:29:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:29:10 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:30:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:30:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:30:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 05:31:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d22f69dca6b33151e4b9388a9f7ffc2f1ccb05009cafb47af44d1565638d82e`  
		Last Modified: Sat, 02 Dec 2023 06:02:16 GMT  
		Size: 106.4 MB (106428506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed0ac7540d8cbc42b0b790363b67898ca9290d22d22fefcc247e489e7fe717c`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57968e329ced147f78a11c69c9cd74f92b334c69380d6ebf3adc06e69dcb8174`  
		Last Modified: Sat, 02 Dec 2023 06:02:38 GMT  
		Size: 98.1 MB (98135742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57236380704a693bf951c36f099cc471cb04f9b903274748f681edd88f30abb`  
		Last Modified: Sat, 02 Dec 2023 06:02:25 GMT  
		Size: 323.2 KB (323214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23037007ece943d7f15c0f6426263385c4047ae880b538f481f4595aec37af78`  
		Last Modified: Sat, 02 Dec 2023 06:02:24 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60ac8a3380ba7335b0de60247b803ba619fa658e6b91face35adcdd2f387e25`  
		Last Modified: Sat, 02 Dec 2023 06:02:28 GMT  
		Size: 23.1 MB (23094946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2ca8f5ca27eec486ec33659c99e37b1f7460b644fb090e33041205d9a32d1261
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256103479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1212a2909e03ae80c1f2ab71d19622de52cfd7740b02a750aece6ca616bb0555`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV ROS_DISTRO=humble
# Sat, 02 Dec 2023 06:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:37:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:37:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:37:43 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:38:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:38:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:38:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 06:39:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6560159c3ed92884911dccc962df12029fdb9e5ed9843502ab99d0110387a673`  
		Last Modified: Sat, 02 Dec 2023 06:58:52 GMT  
		Size: 104.2 MB (104155922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5ee50527375d201d52693c03b3b332487481893259003896909f62b2349034`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109606fc1cf4f571739382eda69dd7629b266ddb7b108f59718296836d31e1cf`  
		Last Modified: Sat, 02 Dec 2023 06:59:12 GMT  
		Size: 95.7 MB (95685282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c752ed94011d4054bd9ab9659ba8bd3fed9ece70cb476d960a6fc2db7fae55`  
		Last Modified: Sat, 02 Dec 2023 06:59:01 GMT  
		Size: 323.2 KB (323214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5dfebc2c0d59cdd3bb9da21d144fe2edbb6ad79841baa31521626c14e74aa0`  
		Last Modified: Sat, 02 Dec 2023 06:59:01 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78c320048bffeec8ead9a46877e6bbe02f4abf89a70dffcc2c23dd65eff458b`  
		Last Modified: Sat, 02 Dec 2023 06:59:04 GMT  
		Size: 22.5 MB (22517964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception`

```console
$ docker pull ros@sha256:c06dac51a8c01c28d80bcb7c50622a2db5c27472d135a1009a74c271d06234f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:550a364e2372dc962c9ad7a49b0f13f987e0c0f74ec671a89679712921a8a404
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **953.7 MB (953705616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadef2c99d297e4f635fa0796dd2be53f5710c78e2b3677843cf42d2cdfaa96e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV ROS_DISTRO=humble
# Sat, 02 Dec 2023 05:29:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:29:10 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:29:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:29:10 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:30:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:30:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:30:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 05:31:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:50:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d22f69dca6b33151e4b9388a9f7ffc2f1ccb05009cafb47af44d1565638d82e`  
		Last Modified: Sat, 02 Dec 2023 06:02:16 GMT  
		Size: 106.4 MB (106428506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed0ac7540d8cbc42b0b790363b67898ca9290d22d22fefcc247e489e7fe717c`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57968e329ced147f78a11c69c9cd74f92b334c69380d6ebf3adc06e69dcb8174`  
		Last Modified: Sat, 02 Dec 2023 06:02:38 GMT  
		Size: 98.1 MB (98135742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57236380704a693bf951c36f099cc471cb04f9b903274748f681edd88f30abb`  
		Last Modified: Sat, 02 Dec 2023 06:02:25 GMT  
		Size: 323.2 KB (323214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23037007ece943d7f15c0f6426263385c4047ae880b538f481f4595aec37af78`  
		Last Modified: Sat, 02 Dec 2023 06:02:24 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60ac8a3380ba7335b0de60247b803ba619fa658e6b91face35adcdd2f387e25`  
		Last Modified: Sat, 02 Dec 2023 06:02:28 GMT  
		Size: 23.1 MB (23094946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a045ee76092b010efb1a4a9a879ae4c5ccb65256e0d6718c060bfb11de796ab4`  
		Last Modified: Sat, 02 Dec 2023 06:04:16 GMT  
		Size: 690.2 MB (690229825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5429573be4e152a3677541182775ce7d42855b0fde61c86d5ab34b86eb20e456
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.2 MB (914204304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db8ebb582f0fa8e6231dd3c58db2339c6d8805d6736be3aa1dd03c35878ba60`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV ROS_DISTRO=humble
# Sat, 02 Dec 2023 06:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:37:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:37:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:37:43 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:38:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:38:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:38:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 06:39:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:48:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6560159c3ed92884911dccc962df12029fdb9e5ed9843502ab99d0110387a673`  
		Last Modified: Sat, 02 Dec 2023 06:58:52 GMT  
		Size: 104.2 MB (104155922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5ee50527375d201d52693c03b3b332487481893259003896909f62b2349034`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109606fc1cf4f571739382eda69dd7629b266ddb7b108f59718296836d31e1cf`  
		Last Modified: Sat, 02 Dec 2023 06:59:12 GMT  
		Size: 95.7 MB (95685282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c752ed94011d4054bd9ab9659ba8bd3fed9ece70cb476d960a6fc2db7fae55`  
		Last Modified: Sat, 02 Dec 2023 06:59:01 GMT  
		Size: 323.2 KB (323214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5dfebc2c0d59cdd3bb9da21d144fe2edbb6ad79841baa31521626c14e74aa0`  
		Last Modified: Sat, 02 Dec 2023 06:59:01 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78c320048bffeec8ead9a46877e6bbe02f4abf89a70dffcc2c23dd65eff458b`  
		Last Modified: Sat, 02 Dec 2023 06:59:04 GMT  
		Size: 22.5 MB (22517964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3ea6e76441d2ce4f898080ed96756f1b85b2a4592b1c03dfa0313716acc579`  
		Last Modified: Sat, 02 Dec 2023 07:00:48 GMT  
		Size: 658.1 MB (658100825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:c06dac51a8c01c28d80bcb7c50622a2db5c27472d135a1009a74c271d06234f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:550a364e2372dc962c9ad7a49b0f13f987e0c0f74ec671a89679712921a8a404
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **953.7 MB (953705616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadef2c99d297e4f635fa0796dd2be53f5710c78e2b3677843cf42d2cdfaa96e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV ROS_DISTRO=humble
# Sat, 02 Dec 2023 05:29:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:29:10 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:29:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:29:10 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:30:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:30:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:30:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 05:31:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:50:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d22f69dca6b33151e4b9388a9f7ffc2f1ccb05009cafb47af44d1565638d82e`  
		Last Modified: Sat, 02 Dec 2023 06:02:16 GMT  
		Size: 106.4 MB (106428506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed0ac7540d8cbc42b0b790363b67898ca9290d22d22fefcc247e489e7fe717c`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57968e329ced147f78a11c69c9cd74f92b334c69380d6ebf3adc06e69dcb8174`  
		Last Modified: Sat, 02 Dec 2023 06:02:38 GMT  
		Size: 98.1 MB (98135742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57236380704a693bf951c36f099cc471cb04f9b903274748f681edd88f30abb`  
		Last Modified: Sat, 02 Dec 2023 06:02:25 GMT  
		Size: 323.2 KB (323214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23037007ece943d7f15c0f6426263385c4047ae880b538f481f4595aec37af78`  
		Last Modified: Sat, 02 Dec 2023 06:02:24 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60ac8a3380ba7335b0de60247b803ba619fa658e6b91face35adcdd2f387e25`  
		Last Modified: Sat, 02 Dec 2023 06:02:28 GMT  
		Size: 23.1 MB (23094946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a045ee76092b010efb1a4a9a879ae4c5ccb65256e0d6718c060bfb11de796ab4`  
		Last Modified: Sat, 02 Dec 2023 06:04:16 GMT  
		Size: 690.2 MB (690229825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5429573be4e152a3677541182775ce7d42855b0fde61c86d5ab34b86eb20e456
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.2 MB (914204304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db8ebb582f0fa8e6231dd3c58db2339c6d8805d6736be3aa1dd03c35878ba60`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV ROS_DISTRO=humble
# Sat, 02 Dec 2023 06:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:37:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:37:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:37:43 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:38:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:38:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:38:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 06:39:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:48:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6560159c3ed92884911dccc962df12029fdb9e5ed9843502ab99d0110387a673`  
		Last Modified: Sat, 02 Dec 2023 06:58:52 GMT  
		Size: 104.2 MB (104155922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5ee50527375d201d52693c03b3b332487481893259003896909f62b2349034`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109606fc1cf4f571739382eda69dd7629b266ddb7b108f59718296836d31e1cf`  
		Last Modified: Sat, 02 Dec 2023 06:59:12 GMT  
		Size: 95.7 MB (95685282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c752ed94011d4054bd9ab9659ba8bd3fed9ece70cb476d960a6fc2db7fae55`  
		Last Modified: Sat, 02 Dec 2023 06:59:01 GMT  
		Size: 323.2 KB (323214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5dfebc2c0d59cdd3bb9da21d144fe2edbb6ad79841baa31521626c14e74aa0`  
		Last Modified: Sat, 02 Dec 2023 06:59:01 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78c320048bffeec8ead9a46877e6bbe02f4abf89a70dffcc2c23dd65eff458b`  
		Last Modified: Sat, 02 Dec 2023 06:59:04 GMT  
		Size: 22.5 MB (22517964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3ea6e76441d2ce4f898080ed96756f1b85b2a4592b1c03dfa0313716acc579`  
		Last Modified: Sat, 02 Dec 2023 07:00:48 GMT  
		Size: 658.1 MB (658100825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:c2f05668bc47f0c29de8a062e858b4d292328c9a8ab5d3a4578989dfe5a47991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:15dbc5efef92470bd7998b50de6cb878b2b42122c45141beedff16ed68371072
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263475791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f430a3a98e1d1077d42502cbd151c0570d0ff47b4378a56585ca1c8749929fbc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV ROS_DISTRO=humble
# Sat, 02 Dec 2023 05:29:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:29:10 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:29:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:29:10 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:30:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:30:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:30:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 05:31:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d22f69dca6b33151e4b9388a9f7ffc2f1ccb05009cafb47af44d1565638d82e`  
		Last Modified: Sat, 02 Dec 2023 06:02:16 GMT  
		Size: 106.4 MB (106428506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed0ac7540d8cbc42b0b790363b67898ca9290d22d22fefcc247e489e7fe717c`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57968e329ced147f78a11c69c9cd74f92b334c69380d6ebf3adc06e69dcb8174`  
		Last Modified: Sat, 02 Dec 2023 06:02:38 GMT  
		Size: 98.1 MB (98135742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57236380704a693bf951c36f099cc471cb04f9b903274748f681edd88f30abb`  
		Last Modified: Sat, 02 Dec 2023 06:02:25 GMT  
		Size: 323.2 KB (323214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23037007ece943d7f15c0f6426263385c4047ae880b538f481f4595aec37af78`  
		Last Modified: Sat, 02 Dec 2023 06:02:24 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60ac8a3380ba7335b0de60247b803ba619fa658e6b91face35adcdd2f387e25`  
		Last Modified: Sat, 02 Dec 2023 06:02:28 GMT  
		Size: 23.1 MB (23094946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2ca8f5ca27eec486ec33659c99e37b1f7460b644fb090e33041205d9a32d1261
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256103479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1212a2909e03ae80c1f2ab71d19622de52cfd7740b02a750aece6ca616bb0555`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV ROS_DISTRO=humble
# Sat, 02 Dec 2023 06:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:37:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:37:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:37:43 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:38:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:38:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:38:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 06:39:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6560159c3ed92884911dccc962df12029fdb9e5ed9843502ab99d0110387a673`  
		Last Modified: Sat, 02 Dec 2023 06:58:52 GMT  
		Size: 104.2 MB (104155922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5ee50527375d201d52693c03b3b332487481893259003896909f62b2349034`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109606fc1cf4f571739382eda69dd7629b266ddb7b108f59718296836d31e1cf`  
		Last Modified: Sat, 02 Dec 2023 06:59:12 GMT  
		Size: 95.7 MB (95685282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c752ed94011d4054bd9ab9659ba8bd3fed9ece70cb476d960a6fc2db7fae55`  
		Last Modified: Sat, 02 Dec 2023 06:59:01 GMT  
		Size: 323.2 KB (323214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5dfebc2c0d59cdd3bb9da21d144fe2edbb6ad79841baa31521626c14e74aa0`  
		Last Modified: Sat, 02 Dec 2023 06:59:01 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78c320048bffeec8ead9a46877e6bbe02f4abf89a70dffcc2c23dd65eff458b`  
		Last Modified: Sat, 02 Dec 2023 06:59:04 GMT  
		Size: 22.5 MB (22517964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:c2f05668bc47f0c29de8a062e858b4d292328c9a8ab5d3a4578989dfe5a47991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:15dbc5efef92470bd7998b50de6cb878b2b42122c45141beedff16ed68371072
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263475791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f430a3a98e1d1077d42502cbd151c0570d0ff47b4378a56585ca1c8749929fbc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV ROS_DISTRO=humble
# Sat, 02 Dec 2023 05:29:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:29:10 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:29:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:29:10 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:30:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:30:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:30:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 05:31:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d22f69dca6b33151e4b9388a9f7ffc2f1ccb05009cafb47af44d1565638d82e`  
		Last Modified: Sat, 02 Dec 2023 06:02:16 GMT  
		Size: 106.4 MB (106428506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed0ac7540d8cbc42b0b790363b67898ca9290d22d22fefcc247e489e7fe717c`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57968e329ced147f78a11c69c9cd74f92b334c69380d6ebf3adc06e69dcb8174`  
		Last Modified: Sat, 02 Dec 2023 06:02:38 GMT  
		Size: 98.1 MB (98135742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57236380704a693bf951c36f099cc471cb04f9b903274748f681edd88f30abb`  
		Last Modified: Sat, 02 Dec 2023 06:02:25 GMT  
		Size: 323.2 KB (323214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23037007ece943d7f15c0f6426263385c4047ae880b538f481f4595aec37af78`  
		Last Modified: Sat, 02 Dec 2023 06:02:24 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60ac8a3380ba7335b0de60247b803ba619fa658e6b91face35adcdd2f387e25`  
		Last Modified: Sat, 02 Dec 2023 06:02:28 GMT  
		Size: 23.1 MB (23094946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2ca8f5ca27eec486ec33659c99e37b1f7460b644fb090e33041205d9a32d1261
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256103479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1212a2909e03ae80c1f2ab71d19622de52cfd7740b02a750aece6ca616bb0555`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV ROS_DISTRO=humble
# Sat, 02 Dec 2023 06:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:37:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:37:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:37:43 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:38:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:38:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:38:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 06:39:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6560159c3ed92884911dccc962df12029fdb9e5ed9843502ab99d0110387a673`  
		Last Modified: Sat, 02 Dec 2023 06:58:52 GMT  
		Size: 104.2 MB (104155922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5ee50527375d201d52693c03b3b332487481893259003896909f62b2349034`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109606fc1cf4f571739382eda69dd7629b266ddb7b108f59718296836d31e1cf`  
		Last Modified: Sat, 02 Dec 2023 06:59:12 GMT  
		Size: 95.7 MB (95685282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c752ed94011d4054bd9ab9659ba8bd3fed9ece70cb476d960a6fc2db7fae55`  
		Last Modified: Sat, 02 Dec 2023 06:59:01 GMT  
		Size: 323.2 KB (323214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5dfebc2c0d59cdd3bb9da21d144fe2edbb6ad79841baa31521626c14e74aa0`  
		Last Modified: Sat, 02 Dec 2023 06:59:01 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78c320048bffeec8ead9a46877e6bbe02f4abf89a70dffcc2c23dd65eff458b`  
		Last Modified: Sat, 02 Dec 2023 06:59:04 GMT  
		Size: 22.5 MB (22517964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:320933c8b5502974f491900623af5b8968c36aebf639b05c358e78e8d1f003f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:cb3002a2cc0251b2eba8eaa242b6af9f1fe828b6faad75aa9c51021088ba17ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141919425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349dc90f9f8fad7039d4bbf26c2519cd59d2cd043c44190346ce3b660aba67fc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV ROS_DISTRO=humble
# Sat, 02 Dec 2023 05:29:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:29:10 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:29:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:29:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d22f69dca6b33151e4b9388a9f7ffc2f1ccb05009cafb47af44d1565638d82e`  
		Last Modified: Sat, 02 Dec 2023 06:02:16 GMT  
		Size: 106.4 MB (106428506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed0ac7540d8cbc42b0b790363b67898ca9290d22d22fefcc247e489e7fe717c`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f2ab9e6f1a21df7993e00acd303ef45865c8947e0c0d65dd74dbdba997edf879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137574542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad61cd2154f91217cb5b3488c38fbfffdbfa6b8ab21e6cee53962988437827b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV ROS_DISTRO=humble
# Sat, 02 Dec 2023 06:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:37:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:37:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:37:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6560159c3ed92884911dccc962df12029fdb9e5ed9843502ab99d0110387a673`  
		Last Modified: Sat, 02 Dec 2023 06:58:52 GMT  
		Size: 104.2 MB (104155922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5ee50527375d201d52693c03b3b332487481893259003896909f62b2349034`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:320933c8b5502974f491900623af5b8968c36aebf639b05c358e78e8d1f003f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:cb3002a2cc0251b2eba8eaa242b6af9f1fe828b6faad75aa9c51021088ba17ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141919425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349dc90f9f8fad7039d4bbf26c2519cd59d2cd043c44190346ce3b660aba67fc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV ROS_DISTRO=humble
# Sat, 02 Dec 2023 05:29:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:29:10 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:29:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:29:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d22f69dca6b33151e4b9388a9f7ffc2f1ccb05009cafb47af44d1565638d82e`  
		Last Modified: Sat, 02 Dec 2023 06:02:16 GMT  
		Size: 106.4 MB (106428506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed0ac7540d8cbc42b0b790363b67898ca9290d22d22fefcc247e489e7fe717c`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f2ab9e6f1a21df7993e00acd303ef45865c8947e0c0d65dd74dbdba997edf879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137574542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad61cd2154f91217cb5b3488c38fbfffdbfa6b8ab21e6cee53962988437827b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV ROS_DISTRO=humble
# Sat, 02 Dec 2023 06:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:37:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:37:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:37:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6560159c3ed92884911dccc962df12029fdb9e5ed9843502ab99d0110387a673`  
		Last Modified: Sat, 02 Dec 2023 06:58:52 GMT  
		Size: 104.2 MB (104155922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5ee50527375d201d52693c03b3b332487481893259003896909f62b2349034`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron`

```console
$ docker pull ros@sha256:a3c3a64387415b81f24df2cd911e3850ffd2f70eda174704d00ba30f2d9a73ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron` - linux; amd64

```console
$ docker pull ros@sha256:95c8d7e760bdace352b40801d74d82c74c8d8a3d517ab91626dded6b7838e04c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268919994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a01f270fe50dde28a60ac9e407b2c2170d6b4b06d3c541ef576064037cd47cc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:51:06 GMT
ENV ROS_DISTRO=iron
# Sat, 02 Dec 2023 05:52:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:52:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:52:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:52:51 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:53:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:53:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:53:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 05:53:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55970dcb7fa90692b2898147d21e6b7e0f5e68377f2c76abc9cc9835b3e1c54e`  
		Last Modified: Sat, 02 Dec 2023 06:04:48 GMT  
		Size: 124.2 MB (124216210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8396d9129ad2c371dc2833e37d47be0334635d73ad57281ba8a3ea3c7165c891`  
		Last Modified: Sat, 02 Dec 2023 06:04:29 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eac5058ff99e0df90c1b680752035609ff5033e07aa0a5f924c7e1ac26d5a1b`  
		Last Modified: Sat, 02 Dec 2023 06:05:07 GMT  
		Size: 85.2 MB (85169226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab40920f7ffd72d0a2db3dcd77869f4c5a5600fb81e29fc3186fd083b935ec9f`  
		Last Modified: Sat, 02 Dec 2023 06:04:57 GMT  
		Size: 308.6 KB (308556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a2108c2c74486e73d941900a61a2f2a535d73a636419fc1627781e539737be`  
		Last Modified: Sat, 02 Dec 2023 06:04:57 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c284bd6fd5658111dd8e8df3c8543c1340de31d5bd21b3b438ad3a5daaea0d`  
		Last Modified: Sat, 02 Dec 2023 06:05:00 GMT  
		Size: 23.7 MB (23732633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b23155291265f94ee17b584be3440583e953306c71a1067227a77ebacdceaa1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261368382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0873a406c54079c1be0f2e77a219bbf94c35101a78fe9565cf09e19a497f42d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:48:57 GMT
ENV ROS_DISTRO=iron
# Sat, 02 Dec 2023 06:49:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:49:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:49:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:49:43 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:50:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:50:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:50:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 06:50:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c07f727a0cfab8f804fb7d07d7775fec316e6bed370e382264495262155e7d`  
		Last Modified: Sat, 02 Dec 2023 07:01:21 GMT  
		Size: 121.7 MB (121673366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431aa29c67a95ca2aa991d33932727e74558d1c93adc588818163d8f34c75daf`  
		Last Modified: Sat, 02 Dec 2023 07:00:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2889362a5c51bef9df737c5c551cb027da6dc6d40a76eb42c0ef20e43c503ee9`  
		Last Modified: Sat, 02 Dec 2023 07:01:40 GMT  
		Size: 82.8 MB (82845418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efdecdc5548e93ba799103042e04c09a1d67b083a3afa7a62e202a9e33c209f`  
		Last Modified: Sat, 02 Dec 2023 07:01:31 GMT  
		Size: 308.6 KB (308560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b73f54309b9404ff54005ee91f4524e46e522491de3eac3ae30c1b47524002`  
		Last Modified: Sat, 02 Dec 2023 07:01:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fdce5f40277a21f604fdbb7966d2529d8b25ac2026cd156bc813cc4d8e0f8c`  
		Last Modified: Sat, 02 Dec 2023 07:01:35 GMT  
		Size: 23.1 MB (23119969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-perception`

```console
$ docker pull ros@sha256:33afc82836b5050181ae7420a6c6c751614759ae40cb633c16f3437eab92312a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception` - linux; amd64

```console
$ docker pull ros@sha256:9ca4bad0063f8dbac24320f16436938128449cb076adc73406ea0b21b35ebdb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **959.9 MB (959858691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037b6d758152039293f5d18633f43e3ad58848dafcfc03774a60763735b209d0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:51:06 GMT
ENV ROS_DISTRO=iron
# Sat, 02 Dec 2023 05:52:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:52:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:52:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:52:51 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:53:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:53:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:53:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 05:53:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:55:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55970dcb7fa90692b2898147d21e6b7e0f5e68377f2c76abc9cc9835b3e1c54e`  
		Last Modified: Sat, 02 Dec 2023 06:04:48 GMT  
		Size: 124.2 MB (124216210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8396d9129ad2c371dc2833e37d47be0334635d73ad57281ba8a3ea3c7165c891`  
		Last Modified: Sat, 02 Dec 2023 06:04:29 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eac5058ff99e0df90c1b680752035609ff5033e07aa0a5f924c7e1ac26d5a1b`  
		Last Modified: Sat, 02 Dec 2023 06:05:07 GMT  
		Size: 85.2 MB (85169226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab40920f7ffd72d0a2db3dcd77869f4c5a5600fb81e29fc3186fd083b935ec9f`  
		Last Modified: Sat, 02 Dec 2023 06:04:57 GMT  
		Size: 308.6 KB (308556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a2108c2c74486e73d941900a61a2f2a535d73a636419fc1627781e539737be`  
		Last Modified: Sat, 02 Dec 2023 06:04:57 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c284bd6fd5658111dd8e8df3c8543c1340de31d5bd21b3b438ad3a5daaea0d`  
		Last Modified: Sat, 02 Dec 2023 06:05:00 GMT  
		Size: 23.7 MB (23732633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a5540a77a2c09fdf6b065cc1885362190c49869552c2d13002040bab67ecfe`  
		Last Modified: Sat, 02 Dec 2023 06:06:44 GMT  
		Size: 690.9 MB (690938697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ff345d10633a61159eef1b1be20cbd0b9c5b7ac819d98d7cfb3960d97a8b00cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.1 MB (920095073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779b07d6256c53136c33d1c908049129c76481a33a35b24da939471164827bd0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:48:57 GMT
ENV ROS_DISTRO=iron
# Sat, 02 Dec 2023 06:49:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:49:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:49:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:49:43 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:50:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:50:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:50:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 06:50:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:52:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c07f727a0cfab8f804fb7d07d7775fec316e6bed370e382264495262155e7d`  
		Last Modified: Sat, 02 Dec 2023 07:01:21 GMT  
		Size: 121.7 MB (121673366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431aa29c67a95ca2aa991d33932727e74558d1c93adc588818163d8f34c75daf`  
		Last Modified: Sat, 02 Dec 2023 07:00:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2889362a5c51bef9df737c5c551cb027da6dc6d40a76eb42c0ef20e43c503ee9`  
		Last Modified: Sat, 02 Dec 2023 07:01:40 GMT  
		Size: 82.8 MB (82845418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efdecdc5548e93ba799103042e04c09a1d67b083a3afa7a62e202a9e33c209f`  
		Last Modified: Sat, 02 Dec 2023 07:01:31 GMT  
		Size: 308.6 KB (308560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b73f54309b9404ff54005ee91f4524e46e522491de3eac3ae30c1b47524002`  
		Last Modified: Sat, 02 Dec 2023 07:01:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fdce5f40277a21f604fdbb7966d2529d8b25ac2026cd156bc813cc4d8e0f8c`  
		Last Modified: Sat, 02 Dec 2023 07:01:35 GMT  
		Size: 23.1 MB (23119969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd90590ea10a49bf63b58b6d8579843453d951170562df0160d76a2c254b473`  
		Last Modified: Sat, 02 Dec 2023 07:03:15 GMT  
		Size: 658.7 MB (658726691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:33afc82836b5050181ae7420a6c6c751614759ae40cb633c16f3437eab92312a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:9ca4bad0063f8dbac24320f16436938128449cb076adc73406ea0b21b35ebdb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **959.9 MB (959858691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037b6d758152039293f5d18633f43e3ad58848dafcfc03774a60763735b209d0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:51:06 GMT
ENV ROS_DISTRO=iron
# Sat, 02 Dec 2023 05:52:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:52:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:52:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:52:51 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:53:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:53:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:53:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 05:53:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:55:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55970dcb7fa90692b2898147d21e6b7e0f5e68377f2c76abc9cc9835b3e1c54e`  
		Last Modified: Sat, 02 Dec 2023 06:04:48 GMT  
		Size: 124.2 MB (124216210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8396d9129ad2c371dc2833e37d47be0334635d73ad57281ba8a3ea3c7165c891`  
		Last Modified: Sat, 02 Dec 2023 06:04:29 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eac5058ff99e0df90c1b680752035609ff5033e07aa0a5f924c7e1ac26d5a1b`  
		Last Modified: Sat, 02 Dec 2023 06:05:07 GMT  
		Size: 85.2 MB (85169226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab40920f7ffd72d0a2db3dcd77869f4c5a5600fb81e29fc3186fd083b935ec9f`  
		Last Modified: Sat, 02 Dec 2023 06:04:57 GMT  
		Size: 308.6 KB (308556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a2108c2c74486e73d941900a61a2f2a535d73a636419fc1627781e539737be`  
		Last Modified: Sat, 02 Dec 2023 06:04:57 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c284bd6fd5658111dd8e8df3c8543c1340de31d5bd21b3b438ad3a5daaea0d`  
		Last Modified: Sat, 02 Dec 2023 06:05:00 GMT  
		Size: 23.7 MB (23732633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a5540a77a2c09fdf6b065cc1885362190c49869552c2d13002040bab67ecfe`  
		Last Modified: Sat, 02 Dec 2023 06:06:44 GMT  
		Size: 690.9 MB (690938697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ff345d10633a61159eef1b1be20cbd0b9c5b7ac819d98d7cfb3960d97a8b00cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.1 MB (920095073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779b07d6256c53136c33d1c908049129c76481a33a35b24da939471164827bd0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:48:57 GMT
ENV ROS_DISTRO=iron
# Sat, 02 Dec 2023 06:49:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:49:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:49:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:49:43 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:50:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:50:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:50:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 06:50:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:52:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c07f727a0cfab8f804fb7d07d7775fec316e6bed370e382264495262155e7d`  
		Last Modified: Sat, 02 Dec 2023 07:01:21 GMT  
		Size: 121.7 MB (121673366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431aa29c67a95ca2aa991d33932727e74558d1c93adc588818163d8f34c75daf`  
		Last Modified: Sat, 02 Dec 2023 07:00:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2889362a5c51bef9df737c5c551cb027da6dc6d40a76eb42c0ef20e43c503ee9`  
		Last Modified: Sat, 02 Dec 2023 07:01:40 GMT  
		Size: 82.8 MB (82845418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efdecdc5548e93ba799103042e04c09a1d67b083a3afa7a62e202a9e33c209f`  
		Last Modified: Sat, 02 Dec 2023 07:01:31 GMT  
		Size: 308.6 KB (308560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b73f54309b9404ff54005ee91f4524e46e522491de3eac3ae30c1b47524002`  
		Last Modified: Sat, 02 Dec 2023 07:01:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fdce5f40277a21f604fdbb7966d2529d8b25ac2026cd156bc813cc4d8e0f8c`  
		Last Modified: Sat, 02 Dec 2023 07:01:35 GMT  
		Size: 23.1 MB (23119969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd90590ea10a49bf63b58b6d8579843453d951170562df0160d76a2c254b473`  
		Last Modified: Sat, 02 Dec 2023 07:03:15 GMT  
		Size: 658.7 MB (658726691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-base`

```console
$ docker pull ros@sha256:a3c3a64387415b81f24df2cd911e3850ffd2f70eda174704d00ba30f2d9a73ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:95c8d7e760bdace352b40801d74d82c74c8d8a3d517ab91626dded6b7838e04c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268919994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a01f270fe50dde28a60ac9e407b2c2170d6b4b06d3c541ef576064037cd47cc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:51:06 GMT
ENV ROS_DISTRO=iron
# Sat, 02 Dec 2023 05:52:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:52:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:52:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:52:51 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:53:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:53:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:53:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 05:53:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55970dcb7fa90692b2898147d21e6b7e0f5e68377f2c76abc9cc9835b3e1c54e`  
		Last Modified: Sat, 02 Dec 2023 06:04:48 GMT  
		Size: 124.2 MB (124216210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8396d9129ad2c371dc2833e37d47be0334635d73ad57281ba8a3ea3c7165c891`  
		Last Modified: Sat, 02 Dec 2023 06:04:29 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eac5058ff99e0df90c1b680752035609ff5033e07aa0a5f924c7e1ac26d5a1b`  
		Last Modified: Sat, 02 Dec 2023 06:05:07 GMT  
		Size: 85.2 MB (85169226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab40920f7ffd72d0a2db3dcd77869f4c5a5600fb81e29fc3186fd083b935ec9f`  
		Last Modified: Sat, 02 Dec 2023 06:04:57 GMT  
		Size: 308.6 KB (308556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a2108c2c74486e73d941900a61a2f2a535d73a636419fc1627781e539737be`  
		Last Modified: Sat, 02 Dec 2023 06:04:57 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c284bd6fd5658111dd8e8df3c8543c1340de31d5bd21b3b438ad3a5daaea0d`  
		Last Modified: Sat, 02 Dec 2023 06:05:00 GMT  
		Size: 23.7 MB (23732633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b23155291265f94ee17b584be3440583e953306c71a1067227a77ebacdceaa1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261368382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0873a406c54079c1be0f2e77a219bbf94c35101a78fe9565cf09e19a497f42d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:48:57 GMT
ENV ROS_DISTRO=iron
# Sat, 02 Dec 2023 06:49:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:49:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:49:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:49:43 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:50:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:50:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:50:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 06:50:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c07f727a0cfab8f804fb7d07d7775fec316e6bed370e382264495262155e7d`  
		Last Modified: Sat, 02 Dec 2023 07:01:21 GMT  
		Size: 121.7 MB (121673366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431aa29c67a95ca2aa991d33932727e74558d1c93adc588818163d8f34c75daf`  
		Last Modified: Sat, 02 Dec 2023 07:00:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2889362a5c51bef9df737c5c551cb027da6dc6d40a76eb42c0ef20e43c503ee9`  
		Last Modified: Sat, 02 Dec 2023 07:01:40 GMT  
		Size: 82.8 MB (82845418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efdecdc5548e93ba799103042e04c09a1d67b083a3afa7a62e202a9e33c209f`  
		Last Modified: Sat, 02 Dec 2023 07:01:31 GMT  
		Size: 308.6 KB (308560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b73f54309b9404ff54005ee91f4524e46e522491de3eac3ae30c1b47524002`  
		Last Modified: Sat, 02 Dec 2023 07:01:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fdce5f40277a21f604fdbb7966d2529d8b25ac2026cd156bc813cc4d8e0f8c`  
		Last Modified: Sat, 02 Dec 2023 07:01:35 GMT  
		Size: 23.1 MB (23119969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:a3c3a64387415b81f24df2cd911e3850ffd2f70eda174704d00ba30f2d9a73ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:95c8d7e760bdace352b40801d74d82c74c8d8a3d517ab91626dded6b7838e04c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268919994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a01f270fe50dde28a60ac9e407b2c2170d6b4b06d3c541ef576064037cd47cc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:51:06 GMT
ENV ROS_DISTRO=iron
# Sat, 02 Dec 2023 05:52:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:52:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:52:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:52:51 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:53:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:53:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:53:26 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 05:53:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55970dcb7fa90692b2898147d21e6b7e0f5e68377f2c76abc9cc9835b3e1c54e`  
		Last Modified: Sat, 02 Dec 2023 06:04:48 GMT  
		Size: 124.2 MB (124216210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8396d9129ad2c371dc2833e37d47be0334635d73ad57281ba8a3ea3c7165c891`  
		Last Modified: Sat, 02 Dec 2023 06:04:29 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eac5058ff99e0df90c1b680752035609ff5033e07aa0a5f924c7e1ac26d5a1b`  
		Last Modified: Sat, 02 Dec 2023 06:05:07 GMT  
		Size: 85.2 MB (85169226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab40920f7ffd72d0a2db3dcd77869f4c5a5600fb81e29fc3186fd083b935ec9f`  
		Last Modified: Sat, 02 Dec 2023 06:04:57 GMT  
		Size: 308.6 KB (308556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a2108c2c74486e73d941900a61a2f2a535d73a636419fc1627781e539737be`  
		Last Modified: Sat, 02 Dec 2023 06:04:57 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c284bd6fd5658111dd8e8df3c8543c1340de31d5bd21b3b438ad3a5daaea0d`  
		Last Modified: Sat, 02 Dec 2023 06:05:00 GMT  
		Size: 23.7 MB (23732633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b23155291265f94ee17b584be3440583e953306c71a1067227a77ebacdceaa1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261368382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0873a406c54079c1be0f2e77a219bbf94c35101a78fe9565cf09e19a497f42d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:48:57 GMT
ENV ROS_DISTRO=iron
# Sat, 02 Dec 2023 06:49:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:49:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:49:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:49:43 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:50:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:50:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:50:18 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 06:50:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c07f727a0cfab8f804fb7d07d7775fec316e6bed370e382264495262155e7d`  
		Last Modified: Sat, 02 Dec 2023 07:01:21 GMT  
		Size: 121.7 MB (121673366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431aa29c67a95ca2aa991d33932727e74558d1c93adc588818163d8f34c75daf`  
		Last Modified: Sat, 02 Dec 2023 07:00:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2889362a5c51bef9df737c5c551cb027da6dc6d40a76eb42c0ef20e43c503ee9`  
		Last Modified: Sat, 02 Dec 2023 07:01:40 GMT  
		Size: 82.8 MB (82845418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efdecdc5548e93ba799103042e04c09a1d67b083a3afa7a62e202a9e33c209f`  
		Last Modified: Sat, 02 Dec 2023 07:01:31 GMT  
		Size: 308.6 KB (308560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b73f54309b9404ff54005ee91f4524e46e522491de3eac3ae30c1b47524002`  
		Last Modified: Sat, 02 Dec 2023 07:01:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fdce5f40277a21f604fdbb7966d2529d8b25ac2026cd156bc813cc4d8e0f8c`  
		Last Modified: Sat, 02 Dec 2023 07:01:35 GMT  
		Size: 23.1 MB (23119969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:71308ba269810dba67e5027fb4e7fd1ed51679254ea472049015b16e0afa08c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:e72be73bac2f1194de395c9365c3c6b231810288998e9dd7d7a4b1b6332bd3ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159707128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7309103b9f163d0005fc12ab9b18b31266751f3d711b3b2a0054627947e6d7e7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:51:06 GMT
ENV ROS_DISTRO=iron
# Sat, 02 Dec 2023 05:52:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:52:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:52:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:52:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55970dcb7fa90692b2898147d21e6b7e0f5e68377f2c76abc9cc9835b3e1c54e`  
		Last Modified: Sat, 02 Dec 2023 06:04:48 GMT  
		Size: 124.2 MB (124216210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8396d9129ad2c371dc2833e37d47be0334635d73ad57281ba8a3ea3c7165c891`  
		Last Modified: Sat, 02 Dec 2023 06:04:29 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8357eb3e12238ba980c629a9c02a96182d4b2660a54571fa48b4d978bbbc9d95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155091986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e26d066f7795392f62312099badaf1803f410063c38a54d95d223894003cf96`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:48:57 GMT
ENV ROS_DISTRO=iron
# Sat, 02 Dec 2023 06:49:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:49:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:49:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:49:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c07f727a0cfab8f804fb7d07d7775fec316e6bed370e382264495262155e7d`  
		Last Modified: Sat, 02 Dec 2023 07:01:21 GMT  
		Size: 121.7 MB (121673366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431aa29c67a95ca2aa991d33932727e74558d1c93adc588818163d8f34c75daf`  
		Last Modified: Sat, 02 Dec 2023 07:00:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-core-jammy`

```console
$ docker pull ros@sha256:71308ba269810dba67e5027fb4e7fd1ed51679254ea472049015b16e0afa08c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:e72be73bac2f1194de395c9365c3c6b231810288998e9dd7d7a4b1b6332bd3ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159707128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7309103b9f163d0005fc12ab9b18b31266751f3d711b3b2a0054627947e6d7e7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:51:06 GMT
ENV ROS_DISTRO=iron
# Sat, 02 Dec 2023 05:52:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:52:51 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:52:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:52:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55970dcb7fa90692b2898147d21e6b7e0f5e68377f2c76abc9cc9835b3e1c54e`  
		Last Modified: Sat, 02 Dec 2023 06:04:48 GMT  
		Size: 124.2 MB (124216210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8396d9129ad2c371dc2833e37d47be0334635d73ad57281ba8a3ea3c7165c891`  
		Last Modified: Sat, 02 Dec 2023 06:04:29 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8357eb3e12238ba980c629a9c02a96182d4b2660a54571fa48b4d978bbbc9d95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155091986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e26d066f7795392f62312099badaf1803f410063c38a54d95d223894003cf96`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:48:57 GMT
ENV ROS_DISTRO=iron
# Sat, 02 Dec 2023 06:49:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:49:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:49:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:49:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c07f727a0cfab8f804fb7d07d7775fec316e6bed370e382264495262155e7d`  
		Last Modified: Sat, 02 Dec 2023 07:01:21 GMT  
		Size: 121.7 MB (121673366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431aa29c67a95ca2aa991d33932727e74558d1c93adc588818163d8f34c75daf`  
		Last Modified: Sat, 02 Dec 2023 07:00:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:latest`

```console
$ docker pull ros@sha256:c2f05668bc47f0c29de8a062e858b4d292328c9a8ab5d3a4578989dfe5a47991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:15dbc5efef92470bd7998b50de6cb878b2b42122c45141beedff16ed68371072
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263475791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f430a3a98e1d1077d42502cbd151c0570d0ff47b4378a56585ca1c8749929fbc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV ROS_DISTRO=humble
# Sat, 02 Dec 2023 05:29:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:29:10 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:29:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:29:10 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:30:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:30:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:30:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 05:31:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d22f69dca6b33151e4b9388a9f7ffc2f1ccb05009cafb47af44d1565638d82e`  
		Last Modified: Sat, 02 Dec 2023 06:02:16 GMT  
		Size: 106.4 MB (106428506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed0ac7540d8cbc42b0b790363b67898ca9290d22d22fefcc247e489e7fe717c`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57968e329ced147f78a11c69c9cd74f92b334c69380d6ebf3adc06e69dcb8174`  
		Last Modified: Sat, 02 Dec 2023 06:02:38 GMT  
		Size: 98.1 MB (98135742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57236380704a693bf951c36f099cc471cb04f9b903274748f681edd88f30abb`  
		Last Modified: Sat, 02 Dec 2023 06:02:25 GMT  
		Size: 323.2 KB (323214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23037007ece943d7f15c0f6426263385c4047ae880b538f481f4595aec37af78`  
		Last Modified: Sat, 02 Dec 2023 06:02:24 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60ac8a3380ba7335b0de60247b803ba619fa658e6b91face35adcdd2f387e25`  
		Last Modified: Sat, 02 Dec 2023 06:02:28 GMT  
		Size: 23.1 MB (23094946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2ca8f5ca27eec486ec33659c99e37b1f7460b644fb090e33041205d9a32d1261
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256103479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1212a2909e03ae80c1f2ab71d19622de52cfd7740b02a750aece6ca616bb0555`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV ROS_DISTRO=humble
# Sat, 02 Dec 2023 06:37:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:37:43 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:37:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:37:43 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:38:27 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:38:33 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:38:38 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 06:39:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6560159c3ed92884911dccc962df12029fdb9e5ed9843502ab99d0110387a673`  
		Last Modified: Sat, 02 Dec 2023 06:58:52 GMT  
		Size: 104.2 MB (104155922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5ee50527375d201d52693c03b3b332487481893259003896909f62b2349034`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109606fc1cf4f571739382eda69dd7629b266ddb7b108f59718296836d31e1cf`  
		Last Modified: Sat, 02 Dec 2023 06:59:12 GMT  
		Size: 95.7 MB (95685282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c752ed94011d4054bd9ab9659ba8bd3fed9ece70cb476d960a6fc2db7fae55`  
		Last Modified: Sat, 02 Dec 2023 06:59:01 GMT  
		Size: 323.2 KB (323214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5dfebc2c0d59cdd3bb9da21d144fe2edbb6ad79841baa31521626c14e74aa0`  
		Last Modified: Sat, 02 Dec 2023 06:59:01 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78c320048bffeec8ead9a46877e6bbe02f4abf89a70dffcc2c23dd65eff458b`  
		Last Modified: Sat, 02 Dec 2023 06:59:04 GMT  
		Size: 22.5 MB (22517964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic`

```console
$ docker pull ros@sha256:fc8b890012d2a92eb570f95e8df44917b940c8a6db361842e156ce94413204c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:aa2cf66a0f6d613a56907d64c1325f9219b8b151d9d675bcfd85b6944e999572
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343162706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a5187b601f631f06e901329e1c6c9ee32ed4e1e4e235f6cd34d5af345f2cdc`
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
# Sat, 02 Dec 2023 05:04:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 05:04:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:04:43 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:04:44 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:04:44 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 05:08:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:08:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 05:08:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:08:11 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:09:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:09:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:12:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:9a419a7e57fda2f71bea1f99c76305ff5c0f72c3daed9b7440ca105cc25f1de9`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a539454a4493a46768eee29a1cca9b7bfe5f4ab383e3669dde75e208d63790`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83efb03e5f38cd29b39c48abc1bff37c30a6eec8221b87f6142d287789f8b90e`  
		Last Modified: Sat, 02 Dec 2023 06:00:00 GMT  
		Size: 177.0 MB (176955899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e272aac7dcd28168b51bf129cec650d8e7e10fcecca57eb3b33f1111504ca93e`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80787bbb4e152705c432d0f6be72de515673d0bd1e13c308b0b2b79dab42b28c`  
		Last Modified: Sat, 02 Dec 2023 06:00:19 GMT  
		Size: 50.9 MB (50940359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f0aa48fdc5b62a25880ad49af8531594ffd5a9eec93f28c14935098f88138`  
		Last Modified: Sat, 02 Dec 2023 06:00:12 GMT  
		Size: 310.9 KB (310898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0836b9b651f92dfca6a4c94574298a84d6bacf8a6bca656aed2e8303d90f6687`  
		Last Modified: Sat, 02 Dec 2023 06:00:23 GMT  
		Size: 79.6 MB (79616330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:0fd9dea9c5d965b8f1aac9de754061a9af491ee68a5f83f8ce06b3739794de24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289245500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5c45a515d47a675244ea3d82b56837ee4fbb452d87b30d3d6614dd9161af57`
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
# Sat, 02 Dec 2023 07:01:17 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 07:01:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 07:01:18 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 07:01:18 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 07:01:18 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 07:03:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:03:29 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 07:03:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 07:03:29 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 07:03:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:04:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 07:05:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:700d02c0ea931efe14e2787d9a108ce7be4927838ae272c0f7d0a3123e074214`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0309a3bc2624e575400f5b6b328b4051009dddc1cae5172d69b1cb7c48737613`  
		Last Modified: Sat, 02 Dec 2023 07:13:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7837275d18d2f920e3095d8ee319704f32b263367279d99c0beb73e98d19d5cb`  
		Last Modified: Sat, 02 Dec 2023 07:14:25 GMT  
		Size: 157.5 MB (157451014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f07c7b1c4fe9a13100d0a76927283689304aed91f55b5623835bba50ba680d`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57b79dd0ed94f80d2de78257d78c33d475395e1d9e55732cd72ada3887a0717`  
		Last Modified: Sat, 02 Dec 2023 07:14:39 GMT  
		Size: 40.5 MB (40503315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5a3f5071b46f597aab2326583c0f774fd82fecc054a20570259f785de32873`  
		Last Modified: Sat, 02 Dec 2023 07:14:34 GMT  
		Size: 310.9 KB (310893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de56d1947f08554ee75c5bda5801bfebf9ec01d3683acd6a10c163711051742e`  
		Last Modified: Sat, 02 Dec 2023 07:14:43 GMT  
		Size: 60.5 MB (60499537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:86754d86372cc5705c9dcdcb2078f2206e84f1533c8db73c737a8557e22d5cfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 MB (322842615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90418c9f216065116e56913f7c337bb94efc9ea7a6ec2cf94548ea3efe4a99be`
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
# Sat, 02 Dec 2023 06:21:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 06:21:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:21:39 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:21:39 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:21:39 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 06:24:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:24:12 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 06:24:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:24:12 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:24:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:24:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:27:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:d7a226081f8a70c4f599d30b20ce997f62d1e905cf9c67c492294bac8071b607`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe6ea0943f0c7094d8154300d91fd338570e64eb43e6eae14dba82bb6151929`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173666c6bdc8678ac5e3778749bb781f2ff0c4b2641586efecd2419419ebc8bb`  
		Last Modified: Sat, 02 Dec 2023 06:56:44 GMT  
		Size: 171.4 MB (171416337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31355226fb339c9831c6b1ad12084bdd113795b7cd6022fcc589aacdbdf9f42`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2270ce1b1ab74f6a22bb249c1e772e63b0d3ede8da05dce0dd2b7c9965f3c20`  
		Last Modified: Sat, 02 Dec 2023 06:56:58 GMT  
		Size: 45.2 MB (45205899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739604b9ea2a1ceaa377c06051f683917437130648ea4f1d94825fd4c213a9c1`  
		Last Modified: Sat, 02 Dec 2023 06:56:52 GMT  
		Size: 310.9 KB (310898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4198184c381704c040a49d0b342520596e024d46e12a627f21e6849afbf2b8b`  
		Last Modified: Sat, 02 Dec 2023 06:57:01 GMT  
		Size: 72.0 MB (71972220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:f96abec03b1506208628be1defbe482c5b809722b6caa353304aa5e285eab2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:add07200059a54540c46cb990e55dddc6018789c43104487410533d4f89d82f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.2 MB (835224729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a867085d1635dac8fde7ab1596056f1d0e21a3a6a15ee435893f8ae816b081`
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
# Sat, 02 Dec 2023 05:04:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 05:04:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:04:43 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:04:44 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:04:44 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 05:08:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:08:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 05:08:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:08:11 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:09:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:09:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:12:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:26:36 GMT
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
	-	`sha256:9a419a7e57fda2f71bea1f99c76305ff5c0f72c3daed9b7440ca105cc25f1de9`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a539454a4493a46768eee29a1cca9b7bfe5f4ab383e3669dde75e208d63790`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83efb03e5f38cd29b39c48abc1bff37c30a6eec8221b87f6142d287789f8b90e`  
		Last Modified: Sat, 02 Dec 2023 06:00:00 GMT  
		Size: 177.0 MB (176955899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e272aac7dcd28168b51bf129cec650d8e7e10fcecca57eb3b33f1111504ca93e`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80787bbb4e152705c432d0f6be72de515673d0bd1e13c308b0b2b79dab42b28c`  
		Last Modified: Sat, 02 Dec 2023 06:00:19 GMT  
		Size: 50.9 MB (50940359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f0aa48fdc5b62a25880ad49af8531594ffd5a9eec93f28c14935098f88138`  
		Last Modified: Sat, 02 Dec 2023 06:00:12 GMT  
		Size: 310.9 KB (310898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0836b9b651f92dfca6a4c94574298a84d6bacf8a6bca656aed2e8303d90f6687`  
		Last Modified: Sat, 02 Dec 2023 06:00:23 GMT  
		Size: 79.6 MB (79616330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e08a52cd18ecff85a2af954179b7f58ad2681e4da109deb8121259776ea6b9`  
		Last Modified: Sat, 02 Dec 2023 06:01:51 GMT  
		Size: 492.1 MB (492062023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:f55730d0da7c9e398f8862a66912ce52ad6b3c21692c6913a6ca8e37428b1818
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.3 MB (726255150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585611a88ecb8583e54176ecc37e05b0325d905eb2fcef35785a0dd7ed7e1dd8`
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
# Sat, 02 Dec 2023 07:01:17 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 07:01:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 07:01:18 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 07:01:18 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 07:01:18 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 07:03:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:03:29 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 07:03:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 07:03:29 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 07:03:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:04:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 07:05:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:13:28 GMT
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
	-	`sha256:700d02c0ea931efe14e2787d9a108ce7be4927838ae272c0f7d0a3123e074214`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0309a3bc2624e575400f5b6b328b4051009dddc1cae5172d69b1cb7c48737613`  
		Last Modified: Sat, 02 Dec 2023 07:13:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7837275d18d2f920e3095d8ee319704f32b263367279d99c0beb73e98d19d5cb`  
		Last Modified: Sat, 02 Dec 2023 07:14:25 GMT  
		Size: 157.5 MB (157451014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f07c7b1c4fe9a13100d0a76927283689304aed91f55b5623835bba50ba680d`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57b79dd0ed94f80d2de78257d78c33d475395e1d9e55732cd72ada3887a0717`  
		Last Modified: Sat, 02 Dec 2023 07:14:39 GMT  
		Size: 40.5 MB (40503315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5a3f5071b46f597aab2326583c0f774fd82fecc054a20570259f785de32873`  
		Last Modified: Sat, 02 Dec 2023 07:14:34 GMT  
		Size: 310.9 KB (310893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de56d1947f08554ee75c5bda5801bfebf9ec01d3683acd6a10c163711051742e`  
		Last Modified: Sat, 02 Dec 2023 07:14:43 GMT  
		Size: 60.5 MB (60499537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541d1d2ef223203476c472b78caaeadd73bd038a31c12b2bff77974f8d73ec0a`  
		Last Modified: Sat, 02 Dec 2023 07:16:05 GMT  
		Size: 437.0 MB (437009650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:deea8f39742cc227f8983c614daf143f27185eca8e944ec3dcaa39d978ab5994
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.5 MB (785524608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39dbf8e9f48e0875c9544ce9a023e76040a66516b96102952f0809c4163e7a8`
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
# Sat, 02 Dec 2023 06:21:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 06:21:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:21:39 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:21:39 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:21:39 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 06:24:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:24:12 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 06:24:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:24:12 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:24:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:24:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:27:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:35:57 GMT
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
	-	`sha256:d7a226081f8a70c4f599d30b20ce997f62d1e905cf9c67c492294bac8071b607`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe6ea0943f0c7094d8154300d91fd338570e64eb43e6eae14dba82bb6151929`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173666c6bdc8678ac5e3778749bb781f2ff0c4b2641586efecd2419419ebc8bb`  
		Last Modified: Sat, 02 Dec 2023 06:56:44 GMT  
		Size: 171.4 MB (171416337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31355226fb339c9831c6b1ad12084bdd113795b7cd6022fcc589aacdbdf9f42`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2270ce1b1ab74f6a22bb249c1e772e63b0d3ede8da05dce0dd2b7c9965f3c20`  
		Last Modified: Sat, 02 Dec 2023 06:56:58 GMT  
		Size: 45.2 MB (45205899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739604b9ea2a1ceaa377c06051f683917437130648ea4f1d94825fd4c213a9c1`  
		Last Modified: Sat, 02 Dec 2023 06:56:52 GMT  
		Size: 310.9 KB (310898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4198184c381704c040a49d0b342520596e024d46e12a627f21e6849afbf2b8b`  
		Last Modified: Sat, 02 Dec 2023 06:57:01 GMT  
		Size: 72.0 MB (71972220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f758c022229fc495f183047506001fdf4fa836cab1a3a7169633e8b963f5c3`  
		Last Modified: Sat, 02 Dec 2023 06:58:24 GMT  
		Size: 462.7 MB (462681993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:f96abec03b1506208628be1defbe482c5b809722b6caa353304aa5e285eab2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:add07200059a54540c46cb990e55dddc6018789c43104487410533d4f89d82f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.2 MB (835224729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a867085d1635dac8fde7ab1596056f1d0e21a3a6a15ee435893f8ae816b081`
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
# Sat, 02 Dec 2023 05:04:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 05:04:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:04:43 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:04:44 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:04:44 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 05:08:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:08:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 05:08:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:08:11 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:09:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:09:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:12:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:26:36 GMT
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
	-	`sha256:9a419a7e57fda2f71bea1f99c76305ff5c0f72c3daed9b7440ca105cc25f1de9`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a539454a4493a46768eee29a1cca9b7bfe5f4ab383e3669dde75e208d63790`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83efb03e5f38cd29b39c48abc1bff37c30a6eec8221b87f6142d287789f8b90e`  
		Last Modified: Sat, 02 Dec 2023 06:00:00 GMT  
		Size: 177.0 MB (176955899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e272aac7dcd28168b51bf129cec650d8e7e10fcecca57eb3b33f1111504ca93e`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80787bbb4e152705c432d0f6be72de515673d0bd1e13c308b0b2b79dab42b28c`  
		Last Modified: Sat, 02 Dec 2023 06:00:19 GMT  
		Size: 50.9 MB (50940359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f0aa48fdc5b62a25880ad49af8531594ffd5a9eec93f28c14935098f88138`  
		Last Modified: Sat, 02 Dec 2023 06:00:12 GMT  
		Size: 310.9 KB (310898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0836b9b651f92dfca6a4c94574298a84d6bacf8a6bca656aed2e8303d90f6687`  
		Last Modified: Sat, 02 Dec 2023 06:00:23 GMT  
		Size: 79.6 MB (79616330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e08a52cd18ecff85a2af954179b7f58ad2681e4da109deb8121259776ea6b9`  
		Last Modified: Sat, 02 Dec 2023 06:01:51 GMT  
		Size: 492.1 MB (492062023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:f55730d0da7c9e398f8862a66912ce52ad6b3c21692c6913a6ca8e37428b1818
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.3 MB (726255150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585611a88ecb8583e54176ecc37e05b0325d905eb2fcef35785a0dd7ed7e1dd8`
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
# Sat, 02 Dec 2023 07:01:17 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 07:01:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 07:01:18 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 07:01:18 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 07:01:18 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 07:03:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:03:29 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 07:03:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 07:03:29 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 07:03:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:04:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 07:05:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:13:28 GMT
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
	-	`sha256:700d02c0ea931efe14e2787d9a108ce7be4927838ae272c0f7d0a3123e074214`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0309a3bc2624e575400f5b6b328b4051009dddc1cae5172d69b1cb7c48737613`  
		Last Modified: Sat, 02 Dec 2023 07:13:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7837275d18d2f920e3095d8ee319704f32b263367279d99c0beb73e98d19d5cb`  
		Last Modified: Sat, 02 Dec 2023 07:14:25 GMT  
		Size: 157.5 MB (157451014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f07c7b1c4fe9a13100d0a76927283689304aed91f55b5623835bba50ba680d`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57b79dd0ed94f80d2de78257d78c33d475395e1d9e55732cd72ada3887a0717`  
		Last Modified: Sat, 02 Dec 2023 07:14:39 GMT  
		Size: 40.5 MB (40503315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5a3f5071b46f597aab2326583c0f774fd82fecc054a20570259f785de32873`  
		Last Modified: Sat, 02 Dec 2023 07:14:34 GMT  
		Size: 310.9 KB (310893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de56d1947f08554ee75c5bda5801bfebf9ec01d3683acd6a10c163711051742e`  
		Last Modified: Sat, 02 Dec 2023 07:14:43 GMT  
		Size: 60.5 MB (60499537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541d1d2ef223203476c472b78caaeadd73bd038a31c12b2bff77974f8d73ec0a`  
		Last Modified: Sat, 02 Dec 2023 07:16:05 GMT  
		Size: 437.0 MB (437009650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:deea8f39742cc227f8983c614daf143f27185eca8e944ec3dcaa39d978ab5994
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.5 MB (785524608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39dbf8e9f48e0875c9544ce9a023e76040a66516b96102952f0809c4163e7a8`
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
# Sat, 02 Dec 2023 06:21:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 06:21:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:21:39 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:21:39 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:21:39 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 06:24:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:24:12 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 06:24:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:24:12 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:24:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:24:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:27:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:35:57 GMT
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
	-	`sha256:d7a226081f8a70c4f599d30b20ce997f62d1e905cf9c67c492294bac8071b607`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe6ea0943f0c7094d8154300d91fd338570e64eb43e6eae14dba82bb6151929`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173666c6bdc8678ac5e3778749bb781f2ff0c4b2641586efecd2419419ebc8bb`  
		Last Modified: Sat, 02 Dec 2023 06:56:44 GMT  
		Size: 171.4 MB (171416337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31355226fb339c9831c6b1ad12084bdd113795b7cd6022fcc589aacdbdf9f42`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2270ce1b1ab74f6a22bb249c1e772e63b0d3ede8da05dce0dd2b7c9965f3c20`  
		Last Modified: Sat, 02 Dec 2023 06:56:58 GMT  
		Size: 45.2 MB (45205899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739604b9ea2a1ceaa377c06051f683917437130648ea4f1d94825fd4c213a9c1`  
		Last Modified: Sat, 02 Dec 2023 06:56:52 GMT  
		Size: 310.9 KB (310898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4198184c381704c040a49d0b342520596e024d46e12a627f21e6849afbf2b8b`  
		Last Modified: Sat, 02 Dec 2023 06:57:01 GMT  
		Size: 72.0 MB (71972220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f758c022229fc495f183047506001fdf4fa836cab1a3a7169633e8b963f5c3`  
		Last Modified: Sat, 02 Dec 2023 06:58:24 GMT  
		Size: 462.7 MB (462681993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:ea779db8b8c7beb65bc482d78a4678dc0c8afbd7e572596835caedd8a5e6e614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:46b143e6e166f6835b44a9df9531e29d733cf1b2139573a024a313003e25c94b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359027835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221af724a940e4c9238dd20a30f49f069b7656e2f5fbbb62b35c646df34075c8`
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
# Sat, 02 Dec 2023 05:04:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 05:04:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:04:43 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:04:44 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:04:44 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 05:08:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:08:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 05:08:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:08:11 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:09:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:09:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:12:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:14:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:9a419a7e57fda2f71bea1f99c76305ff5c0f72c3daed9b7440ca105cc25f1de9`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a539454a4493a46768eee29a1cca9b7bfe5f4ab383e3669dde75e208d63790`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83efb03e5f38cd29b39c48abc1bff37c30a6eec8221b87f6142d287789f8b90e`  
		Last Modified: Sat, 02 Dec 2023 06:00:00 GMT  
		Size: 177.0 MB (176955899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e272aac7dcd28168b51bf129cec650d8e7e10fcecca57eb3b33f1111504ca93e`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80787bbb4e152705c432d0f6be72de515673d0bd1e13c308b0b2b79dab42b28c`  
		Last Modified: Sat, 02 Dec 2023 06:00:19 GMT  
		Size: 50.9 MB (50940359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f0aa48fdc5b62a25880ad49af8531594ffd5a9eec93f28c14935098f88138`  
		Last Modified: Sat, 02 Dec 2023 06:00:12 GMT  
		Size: 310.9 KB (310898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0836b9b651f92dfca6a4c94574298a84d6bacf8a6bca656aed2e8303d90f6687`  
		Last Modified: Sat, 02 Dec 2023 06:00:23 GMT  
		Size: 79.6 MB (79616330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04515b65aa2a72273e6c2be3982c2c9058a2a457af1c0c3fca60032201f6fd24`  
		Last Modified: Sat, 02 Dec 2023 06:00:36 GMT  
		Size: 15.9 MB (15865129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:e748455f6e095efe7ab741c196cb552491aa93fa01ac8254f416decedbc5f4bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303314243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b144f85b364ab7c4b4e4e378acf76803989825691d7ddf73956e870d9af411ed`
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
# Sat, 02 Dec 2023 07:01:17 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 07:01:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 07:01:18 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 07:01:18 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 07:01:18 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 07:03:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:03:29 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 07:03:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 07:03:29 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 07:03:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:04:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 07:05:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:06:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:700d02c0ea931efe14e2787d9a108ce7be4927838ae272c0f7d0a3123e074214`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0309a3bc2624e575400f5b6b328b4051009dddc1cae5172d69b1cb7c48737613`  
		Last Modified: Sat, 02 Dec 2023 07:13:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7837275d18d2f920e3095d8ee319704f32b263367279d99c0beb73e98d19d5cb`  
		Last Modified: Sat, 02 Dec 2023 07:14:25 GMT  
		Size: 157.5 MB (157451014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f07c7b1c4fe9a13100d0a76927283689304aed91f55b5623835bba50ba680d`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57b79dd0ed94f80d2de78257d78c33d475395e1d9e55732cd72ada3887a0717`  
		Last Modified: Sat, 02 Dec 2023 07:14:39 GMT  
		Size: 40.5 MB (40503315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5a3f5071b46f597aab2326583c0f774fd82fecc054a20570259f785de32873`  
		Last Modified: Sat, 02 Dec 2023 07:14:34 GMT  
		Size: 310.9 KB (310893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de56d1947f08554ee75c5bda5801bfebf9ec01d3683acd6a10c163711051742e`  
		Last Modified: Sat, 02 Dec 2023 07:14:43 GMT  
		Size: 60.5 MB (60499537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c630b2ad4936e8897fb1f7617f4c4a7214d47d0e8de47480bd200a0c4f369cb`  
		Last Modified: Sat, 02 Dec 2023 07:14:56 GMT  
		Size: 14.1 MB (14068743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1a7477eaddb353d421bb95bb1a9fabede537f24e296b56147d665edd6fc0ca13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338301808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4966b07294a490cd05918e2f143d4b0eb6e37ff3d6e3793bd046a01198bdaab1`
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
# Sat, 02 Dec 2023 06:21:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 06:21:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:21:39 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:21:39 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:21:39 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 06:24:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:24:12 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 06:24:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:24:12 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:24:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:24:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:27:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:28:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:d7a226081f8a70c4f599d30b20ce997f62d1e905cf9c67c492294bac8071b607`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe6ea0943f0c7094d8154300d91fd338570e64eb43e6eae14dba82bb6151929`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173666c6bdc8678ac5e3778749bb781f2ff0c4b2641586efecd2419419ebc8bb`  
		Last Modified: Sat, 02 Dec 2023 06:56:44 GMT  
		Size: 171.4 MB (171416337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31355226fb339c9831c6b1ad12084bdd113795b7cd6022fcc589aacdbdf9f42`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2270ce1b1ab74f6a22bb249c1e772e63b0d3ede8da05dce0dd2b7c9965f3c20`  
		Last Modified: Sat, 02 Dec 2023 06:56:58 GMT  
		Size: 45.2 MB (45205899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739604b9ea2a1ceaa377c06051f683917437130648ea4f1d94825fd4c213a9c1`  
		Last Modified: Sat, 02 Dec 2023 06:56:52 GMT  
		Size: 310.9 KB (310898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4198184c381704c040a49d0b342520596e024d46e12a627f21e6849afbf2b8b`  
		Last Modified: Sat, 02 Dec 2023 06:57:01 GMT  
		Size: 72.0 MB (71972220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31aa9346699ce3e70a28482d2d33dbb7417e7980ba4c51cc34451a0d3721c4d3`  
		Last Modified: Sat, 02 Dec 2023 06:57:14 GMT  
		Size: 15.5 MB (15459193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:ea779db8b8c7beb65bc482d78a4678dc0c8afbd7e572596835caedd8a5e6e614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:46b143e6e166f6835b44a9df9531e29d733cf1b2139573a024a313003e25c94b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359027835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221af724a940e4c9238dd20a30f49f069b7656e2f5fbbb62b35c646df34075c8`
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
# Sat, 02 Dec 2023 05:04:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 05:04:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:04:43 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:04:44 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:04:44 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 05:08:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:08:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 05:08:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:08:11 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:09:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:09:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:12:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:14:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:9a419a7e57fda2f71bea1f99c76305ff5c0f72c3daed9b7440ca105cc25f1de9`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a539454a4493a46768eee29a1cca9b7bfe5f4ab383e3669dde75e208d63790`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83efb03e5f38cd29b39c48abc1bff37c30a6eec8221b87f6142d287789f8b90e`  
		Last Modified: Sat, 02 Dec 2023 06:00:00 GMT  
		Size: 177.0 MB (176955899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e272aac7dcd28168b51bf129cec650d8e7e10fcecca57eb3b33f1111504ca93e`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80787bbb4e152705c432d0f6be72de515673d0bd1e13c308b0b2b79dab42b28c`  
		Last Modified: Sat, 02 Dec 2023 06:00:19 GMT  
		Size: 50.9 MB (50940359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f0aa48fdc5b62a25880ad49af8531594ffd5a9eec93f28c14935098f88138`  
		Last Modified: Sat, 02 Dec 2023 06:00:12 GMT  
		Size: 310.9 KB (310898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0836b9b651f92dfca6a4c94574298a84d6bacf8a6bca656aed2e8303d90f6687`  
		Last Modified: Sat, 02 Dec 2023 06:00:23 GMT  
		Size: 79.6 MB (79616330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04515b65aa2a72273e6c2be3982c2c9058a2a457af1c0c3fca60032201f6fd24`  
		Last Modified: Sat, 02 Dec 2023 06:00:36 GMT  
		Size: 15.9 MB (15865129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:e748455f6e095efe7ab741c196cb552491aa93fa01ac8254f416decedbc5f4bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303314243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b144f85b364ab7c4b4e4e378acf76803989825691d7ddf73956e870d9af411ed`
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
# Sat, 02 Dec 2023 07:01:17 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 07:01:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 07:01:18 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 07:01:18 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 07:01:18 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 07:03:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:03:29 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 07:03:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 07:03:29 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 07:03:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:04:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 07:05:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:06:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:700d02c0ea931efe14e2787d9a108ce7be4927838ae272c0f7d0a3123e074214`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0309a3bc2624e575400f5b6b328b4051009dddc1cae5172d69b1cb7c48737613`  
		Last Modified: Sat, 02 Dec 2023 07:13:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7837275d18d2f920e3095d8ee319704f32b263367279d99c0beb73e98d19d5cb`  
		Last Modified: Sat, 02 Dec 2023 07:14:25 GMT  
		Size: 157.5 MB (157451014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f07c7b1c4fe9a13100d0a76927283689304aed91f55b5623835bba50ba680d`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57b79dd0ed94f80d2de78257d78c33d475395e1d9e55732cd72ada3887a0717`  
		Last Modified: Sat, 02 Dec 2023 07:14:39 GMT  
		Size: 40.5 MB (40503315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5a3f5071b46f597aab2326583c0f774fd82fecc054a20570259f785de32873`  
		Last Modified: Sat, 02 Dec 2023 07:14:34 GMT  
		Size: 310.9 KB (310893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de56d1947f08554ee75c5bda5801bfebf9ec01d3683acd6a10c163711051742e`  
		Last Modified: Sat, 02 Dec 2023 07:14:43 GMT  
		Size: 60.5 MB (60499537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c630b2ad4936e8897fb1f7617f4c4a7214d47d0e8de47480bd200a0c4f369cb`  
		Last Modified: Sat, 02 Dec 2023 07:14:56 GMT  
		Size: 14.1 MB (14068743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1a7477eaddb353d421bb95bb1a9fabede537f24e296b56147d665edd6fc0ca13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338301808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4966b07294a490cd05918e2f143d4b0eb6e37ff3d6e3793bd046a01198bdaab1`
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
# Sat, 02 Dec 2023 06:21:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 06:21:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:21:39 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:21:39 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:21:39 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 06:24:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:24:12 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 06:24:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:24:12 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:24:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:24:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:27:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:28:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:d7a226081f8a70c4f599d30b20ce997f62d1e905cf9c67c492294bac8071b607`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe6ea0943f0c7094d8154300d91fd338570e64eb43e6eae14dba82bb6151929`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173666c6bdc8678ac5e3778749bb781f2ff0c4b2641586efecd2419419ebc8bb`  
		Last Modified: Sat, 02 Dec 2023 06:56:44 GMT  
		Size: 171.4 MB (171416337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31355226fb339c9831c6b1ad12084bdd113795b7cd6022fcc589aacdbdf9f42`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2270ce1b1ab74f6a22bb249c1e772e63b0d3ede8da05dce0dd2b7c9965f3c20`  
		Last Modified: Sat, 02 Dec 2023 06:56:58 GMT  
		Size: 45.2 MB (45205899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739604b9ea2a1ceaa377c06051f683917437130648ea4f1d94825fd4c213a9c1`  
		Last Modified: Sat, 02 Dec 2023 06:56:52 GMT  
		Size: 310.9 KB (310898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4198184c381704c040a49d0b342520596e024d46e12a627f21e6849afbf2b8b`  
		Last Modified: Sat, 02 Dec 2023 06:57:01 GMT  
		Size: 72.0 MB (71972220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31aa9346699ce3e70a28482d2d33dbb7417e7980ba4c51cc34451a0d3721c4d3`  
		Last Modified: Sat, 02 Dec 2023 06:57:14 GMT  
		Size: 15.5 MB (15459193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:fc8b890012d2a92eb570f95e8df44917b940c8a6db361842e156ce94413204c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:aa2cf66a0f6d613a56907d64c1325f9219b8b151d9d675bcfd85b6944e999572
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343162706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a5187b601f631f06e901329e1c6c9ee32ed4e1e4e235f6cd34d5af345f2cdc`
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
# Sat, 02 Dec 2023 05:04:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 05:04:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:04:43 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:04:44 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:04:44 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 05:08:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:08:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 05:08:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:08:11 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:09:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:09:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:12:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:9a419a7e57fda2f71bea1f99c76305ff5c0f72c3daed9b7440ca105cc25f1de9`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a539454a4493a46768eee29a1cca9b7bfe5f4ab383e3669dde75e208d63790`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83efb03e5f38cd29b39c48abc1bff37c30a6eec8221b87f6142d287789f8b90e`  
		Last Modified: Sat, 02 Dec 2023 06:00:00 GMT  
		Size: 177.0 MB (176955899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e272aac7dcd28168b51bf129cec650d8e7e10fcecca57eb3b33f1111504ca93e`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80787bbb4e152705c432d0f6be72de515673d0bd1e13c308b0b2b79dab42b28c`  
		Last Modified: Sat, 02 Dec 2023 06:00:19 GMT  
		Size: 50.9 MB (50940359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f0aa48fdc5b62a25880ad49af8531594ffd5a9eec93f28c14935098f88138`  
		Last Modified: Sat, 02 Dec 2023 06:00:12 GMT  
		Size: 310.9 KB (310898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0836b9b651f92dfca6a4c94574298a84d6bacf8a6bca656aed2e8303d90f6687`  
		Last Modified: Sat, 02 Dec 2023 06:00:23 GMT  
		Size: 79.6 MB (79616330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:0fd9dea9c5d965b8f1aac9de754061a9af491ee68a5f83f8ce06b3739794de24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289245500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5c45a515d47a675244ea3d82b56837ee4fbb452d87b30d3d6614dd9161af57`
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
# Sat, 02 Dec 2023 07:01:17 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 07:01:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 07:01:18 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 07:01:18 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 07:01:18 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 07:03:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:03:29 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 07:03:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 07:03:29 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 07:03:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:04:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 07:05:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:700d02c0ea931efe14e2787d9a108ce7be4927838ae272c0f7d0a3123e074214`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0309a3bc2624e575400f5b6b328b4051009dddc1cae5172d69b1cb7c48737613`  
		Last Modified: Sat, 02 Dec 2023 07:13:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7837275d18d2f920e3095d8ee319704f32b263367279d99c0beb73e98d19d5cb`  
		Last Modified: Sat, 02 Dec 2023 07:14:25 GMT  
		Size: 157.5 MB (157451014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f07c7b1c4fe9a13100d0a76927283689304aed91f55b5623835bba50ba680d`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57b79dd0ed94f80d2de78257d78c33d475395e1d9e55732cd72ada3887a0717`  
		Last Modified: Sat, 02 Dec 2023 07:14:39 GMT  
		Size: 40.5 MB (40503315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5a3f5071b46f597aab2326583c0f774fd82fecc054a20570259f785de32873`  
		Last Modified: Sat, 02 Dec 2023 07:14:34 GMT  
		Size: 310.9 KB (310893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de56d1947f08554ee75c5bda5801bfebf9ec01d3683acd6a10c163711051742e`  
		Last Modified: Sat, 02 Dec 2023 07:14:43 GMT  
		Size: 60.5 MB (60499537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:86754d86372cc5705c9dcdcb2078f2206e84f1533c8db73c737a8557e22d5cfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 MB (322842615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90418c9f216065116e56913f7c337bb94efc9ea7a6ec2cf94548ea3efe4a99be`
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
# Sat, 02 Dec 2023 06:21:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 06:21:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:21:39 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:21:39 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:21:39 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 06:24:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:24:12 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 06:24:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:24:12 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:24:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:24:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:27:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:d7a226081f8a70c4f599d30b20ce997f62d1e905cf9c67c492294bac8071b607`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe6ea0943f0c7094d8154300d91fd338570e64eb43e6eae14dba82bb6151929`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173666c6bdc8678ac5e3778749bb781f2ff0c4b2641586efecd2419419ebc8bb`  
		Last Modified: Sat, 02 Dec 2023 06:56:44 GMT  
		Size: 171.4 MB (171416337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31355226fb339c9831c6b1ad12084bdd113795b7cd6022fcc589aacdbdf9f42`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2270ce1b1ab74f6a22bb249c1e772e63b0d3ede8da05dce0dd2b7c9965f3c20`  
		Last Modified: Sat, 02 Dec 2023 06:56:58 GMT  
		Size: 45.2 MB (45205899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739604b9ea2a1ceaa377c06051f683917437130648ea4f1d94825fd4c213a9c1`  
		Last Modified: Sat, 02 Dec 2023 06:56:52 GMT  
		Size: 310.9 KB (310898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4198184c381704c040a49d0b342520596e024d46e12a627f21e6849afbf2b8b`  
		Last Modified: Sat, 02 Dec 2023 06:57:01 GMT  
		Size: 72.0 MB (71972220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:fc8b890012d2a92eb570f95e8df44917b940c8a6db361842e156ce94413204c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:aa2cf66a0f6d613a56907d64c1325f9219b8b151d9d675bcfd85b6944e999572
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343162706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a5187b601f631f06e901329e1c6c9ee32ed4e1e4e235f6cd34d5af345f2cdc`
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
# Sat, 02 Dec 2023 05:04:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 05:04:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:04:43 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:04:44 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:04:44 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 05:08:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:08:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 05:08:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:08:11 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:09:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:09:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:12:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:9a419a7e57fda2f71bea1f99c76305ff5c0f72c3daed9b7440ca105cc25f1de9`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a539454a4493a46768eee29a1cca9b7bfe5f4ab383e3669dde75e208d63790`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83efb03e5f38cd29b39c48abc1bff37c30a6eec8221b87f6142d287789f8b90e`  
		Last Modified: Sat, 02 Dec 2023 06:00:00 GMT  
		Size: 177.0 MB (176955899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e272aac7dcd28168b51bf129cec650d8e7e10fcecca57eb3b33f1111504ca93e`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80787bbb4e152705c432d0f6be72de515673d0bd1e13c308b0b2b79dab42b28c`  
		Last Modified: Sat, 02 Dec 2023 06:00:19 GMT  
		Size: 50.9 MB (50940359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f0aa48fdc5b62a25880ad49af8531594ffd5a9eec93f28c14935098f88138`  
		Last Modified: Sat, 02 Dec 2023 06:00:12 GMT  
		Size: 310.9 KB (310898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0836b9b651f92dfca6a4c94574298a84d6bacf8a6bca656aed2e8303d90f6687`  
		Last Modified: Sat, 02 Dec 2023 06:00:23 GMT  
		Size: 79.6 MB (79616330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:0fd9dea9c5d965b8f1aac9de754061a9af491ee68a5f83f8ce06b3739794de24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289245500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5c45a515d47a675244ea3d82b56837ee4fbb452d87b30d3d6614dd9161af57`
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
# Sat, 02 Dec 2023 07:01:17 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 07:01:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 07:01:18 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 07:01:18 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 07:01:18 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 07:03:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:03:29 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 07:03:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 07:03:29 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 07:03:54 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:04:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 07:05:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:700d02c0ea931efe14e2787d9a108ce7be4927838ae272c0f7d0a3123e074214`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0309a3bc2624e575400f5b6b328b4051009dddc1cae5172d69b1cb7c48737613`  
		Last Modified: Sat, 02 Dec 2023 07:13:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7837275d18d2f920e3095d8ee319704f32b263367279d99c0beb73e98d19d5cb`  
		Last Modified: Sat, 02 Dec 2023 07:14:25 GMT  
		Size: 157.5 MB (157451014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f07c7b1c4fe9a13100d0a76927283689304aed91f55b5623835bba50ba680d`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57b79dd0ed94f80d2de78257d78c33d475395e1d9e55732cd72ada3887a0717`  
		Last Modified: Sat, 02 Dec 2023 07:14:39 GMT  
		Size: 40.5 MB (40503315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5a3f5071b46f597aab2326583c0f774fd82fecc054a20570259f785de32873`  
		Last Modified: Sat, 02 Dec 2023 07:14:34 GMT  
		Size: 310.9 KB (310893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de56d1947f08554ee75c5bda5801bfebf9ec01d3683acd6a10c163711051742e`  
		Last Modified: Sat, 02 Dec 2023 07:14:43 GMT  
		Size: 60.5 MB (60499537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:86754d86372cc5705c9dcdcb2078f2206e84f1533c8db73c737a8557e22d5cfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 MB (322842615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90418c9f216065116e56913f7c337bb94efc9ea7a6ec2cf94548ea3efe4a99be`
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
# Sat, 02 Dec 2023 06:21:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 06:21:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:21:39 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:21:39 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:21:39 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 06:24:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:24:12 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 06:24:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:24:12 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:24:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:24:53 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:27:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:d7a226081f8a70c4f599d30b20ce997f62d1e905cf9c67c492294bac8071b607`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe6ea0943f0c7094d8154300d91fd338570e64eb43e6eae14dba82bb6151929`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173666c6bdc8678ac5e3778749bb781f2ff0c4b2641586efecd2419419ebc8bb`  
		Last Modified: Sat, 02 Dec 2023 06:56:44 GMT  
		Size: 171.4 MB (171416337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31355226fb339c9831c6b1ad12084bdd113795b7cd6022fcc589aacdbdf9f42`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2270ce1b1ab74f6a22bb249c1e772e63b0d3ede8da05dce0dd2b7c9965f3c20`  
		Last Modified: Sat, 02 Dec 2023 06:56:58 GMT  
		Size: 45.2 MB (45205899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739604b9ea2a1ceaa377c06051f683917437130648ea4f1d94825fd4c213a9c1`  
		Last Modified: Sat, 02 Dec 2023 06:56:52 GMT  
		Size: 310.9 KB (310898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4198184c381704c040a49d0b342520596e024d46e12a627f21e6849afbf2b8b`  
		Last Modified: Sat, 02 Dec 2023 06:57:01 GMT  
		Size: 72.0 MB (71972220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:6deea48e89bb9417a7d5a2b1a649620b9f088a185d4c7ce9afb7d7e6b8d6de61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:70499a0de7e1d7fdf1a0222f4e293ffbfec29887876e3fe909ee59356fa5027f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212295119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99510bebad11edb8da57e16b7670c8840d01f5750214610e0c56aac29f6ff2ce`
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
# Sat, 02 Dec 2023 05:04:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 05:04:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:04:43 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:04:44 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:04:44 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 05:08:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:08:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 05:08:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:08:11 GMT
CMD ["bash"]
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
	-	`sha256:9a419a7e57fda2f71bea1f99c76305ff5c0f72c3daed9b7440ca105cc25f1de9`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a539454a4493a46768eee29a1cca9b7bfe5f4ab383e3669dde75e208d63790`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83efb03e5f38cd29b39c48abc1bff37c30a6eec8221b87f6142d287789f8b90e`  
		Last Modified: Sat, 02 Dec 2023 06:00:00 GMT  
		Size: 177.0 MB (176955899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e272aac7dcd28168b51bf129cec650d8e7e10fcecca57eb3b33f1111504ca93e`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:3a959d9abd2fc21701051bfbf7b8d23648f3773c39708fe8b61cd6fbe983d7a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187931755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b587218d6d73a6ea201f2f7ded20a51cfe5d13611ac897bb68f83ba9fc5627c5`
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
# Sat, 02 Dec 2023 07:01:17 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 07:01:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 07:01:18 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 07:01:18 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 07:01:18 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 07:03:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:03:29 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 07:03:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 07:03:29 GMT
CMD ["bash"]
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
	-	`sha256:700d02c0ea931efe14e2787d9a108ce7be4927838ae272c0f7d0a3123e074214`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0309a3bc2624e575400f5b6b328b4051009dddc1cae5172d69b1cb7c48737613`  
		Last Modified: Sat, 02 Dec 2023 07:13:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7837275d18d2f920e3095d8ee319704f32b263367279d99c0beb73e98d19d5cb`  
		Last Modified: Sat, 02 Dec 2023 07:14:25 GMT  
		Size: 157.5 MB (157451014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f07c7b1c4fe9a13100d0a76927283689304aed91f55b5623835bba50ba680d`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6da542443d0ea7ce78eec9b231a2b3e8265cee685438f2226f175ae3f512aa9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205353598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c036f063f427d225340a1503b1248c1d1483cf24691d8833fe22216cbeddb5`
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
# Sat, 02 Dec 2023 06:21:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 06:21:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:21:39 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:21:39 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:21:39 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 06:24:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:24:12 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 06:24:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:24:12 GMT
CMD ["bash"]
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
	-	`sha256:d7a226081f8a70c4f599d30b20ce997f62d1e905cf9c67c492294bac8071b607`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe6ea0943f0c7094d8154300d91fd338570e64eb43e6eae14dba82bb6151929`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173666c6bdc8678ac5e3778749bb781f2ff0c4b2641586efecd2419419ebc8bb`  
		Last Modified: Sat, 02 Dec 2023 06:56:44 GMT  
		Size: 171.4 MB (171416337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31355226fb339c9831c6b1ad12084bdd113795b7cd6022fcc589aacdbdf9f42`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:6deea48e89bb9417a7d5a2b1a649620b9f088a185d4c7ce9afb7d7e6b8d6de61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:70499a0de7e1d7fdf1a0222f4e293ffbfec29887876e3fe909ee59356fa5027f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212295119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99510bebad11edb8da57e16b7670c8840d01f5750214610e0c56aac29f6ff2ce`
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
# Sat, 02 Dec 2023 05:04:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 05:04:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:04:43 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:04:44 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:04:44 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 05:08:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:08:11 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 05:08:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:08:11 GMT
CMD ["bash"]
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
	-	`sha256:9a419a7e57fda2f71bea1f99c76305ff5c0f72c3daed9b7440ca105cc25f1de9`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a539454a4493a46768eee29a1cca9b7bfe5f4ab383e3669dde75e208d63790`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83efb03e5f38cd29b39c48abc1bff37c30a6eec8221b87f6142d287789f8b90e`  
		Last Modified: Sat, 02 Dec 2023 06:00:00 GMT  
		Size: 177.0 MB (176955899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e272aac7dcd28168b51bf129cec650d8e7e10fcecca57eb3b33f1111504ca93e`  
		Last Modified: Sat, 02 Dec 2023 05:59:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:3a959d9abd2fc21701051bfbf7b8d23648f3773c39708fe8b61cd6fbe983d7a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187931755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b587218d6d73a6ea201f2f7ded20a51cfe5d13611ac897bb68f83ba9fc5627c5`
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
# Sat, 02 Dec 2023 07:01:17 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 07:01:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 07:01:18 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 07:01:18 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 07:01:18 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 07:03:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:03:29 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 07:03:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 07:03:29 GMT
CMD ["bash"]
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
	-	`sha256:700d02c0ea931efe14e2787d9a108ce7be4927838ae272c0f7d0a3123e074214`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0309a3bc2624e575400f5b6b328b4051009dddc1cae5172d69b1cb7c48737613`  
		Last Modified: Sat, 02 Dec 2023 07:13:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7837275d18d2f920e3095d8ee319704f32b263367279d99c0beb73e98d19d5cb`  
		Last Modified: Sat, 02 Dec 2023 07:14:25 GMT  
		Size: 157.5 MB (157451014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f07c7b1c4fe9a13100d0a76927283689304aed91f55b5623835bba50ba680d`  
		Last Modified: Sat, 02 Dec 2023 07:13:56 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6da542443d0ea7ce78eec9b231a2b3e8265cee685438f2226f175ae3f512aa9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205353598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c036f063f427d225340a1503b1248c1d1483cf24691d8833fe22216cbeddb5`
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
# Sat, 02 Dec 2023 06:21:38 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 02 Dec 2023 06:21:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:21:39 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:21:39 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:21:39 GMT
ENV ROS_DISTRO=noetic
# Sat, 02 Dec 2023 06:24:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:24:12 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Sat, 02 Dec 2023 06:24:12 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:24:12 GMT
CMD ["bash"]
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
	-	`sha256:d7a226081f8a70c4f599d30b20ce997f62d1e905cf9c67c492294bac8071b607`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe6ea0943f0c7094d8154300d91fd338570e64eb43e6eae14dba82bb6151929`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173666c6bdc8678ac5e3778749bb781f2ff0c4b2641586efecd2419419ebc8bb`  
		Last Modified: Sat, 02 Dec 2023 06:56:44 GMT  
		Size: 171.4 MB (171416337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31355226fb339c9831c6b1ad12084bdd113795b7cd6022fcc589aacdbdf9f42`  
		Last Modified: Sat, 02 Dec 2023 06:56:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling`

```console
$ docker pull ros@sha256:eb05cb3d0c3b819a402c7f28b3ae0313f9d41a692d92a2d642ba6dbe109a3a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:57ed363844b88e69c892ab60c196c459a4370ba2b3d55c8664091d817684d033
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269017852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15700c2d31c62a8c49f085258b7aac62c20d1d93b1f8db4d5764f6b1d2ccaff9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:55:52 GMT
ENV ROS_DISTRO=rolling
# Sat, 02 Dec 2023 05:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:56:37 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:56:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:56:37 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:56:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:57:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:57:04 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 05:57:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70cdec7f7f494d3cb2ea302a0b42630c0353133474a693a309d1b5950b3d1b1`  
		Last Modified: Sat, 02 Dec 2023 06:07:11 GMT  
		Size: 124.3 MB (124271649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb056cc69d86752a925eb68c836ad08186757af76db68041db5eb1da10a0e15`  
		Last Modified: Sat, 02 Dec 2023 06:06:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655e7b257add838be46a798525b40ef3b18fea490caf612f09c1151ebbe6f7a6`  
		Last Modified: Sat, 02 Dec 2023 06:07:31 GMT  
		Size: 85.2 MB (85172080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf0a91322021b1c4e36dd3a6fb62d30b3c54e6098d0755a4f5bdfc328aa0040`  
		Last Modified: Sat, 02 Dec 2023 06:07:21 GMT  
		Size: 302.3 KB (302307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f42b45f4e05e21e47e74869b5b88a9964383d8448055d257f47a34694c6eae0`  
		Last Modified: Sat, 02 Dec 2023 06:07:21 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7f58f28f44789d5600868e9ca68910d022964a421870c5b3bbbb5ae9cb08c`  
		Last Modified: Sat, 02 Dec 2023 06:07:24 GMT  
		Size: 23.8 MB (23778449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9f7d538dae51b42502aa3924a51443726ae3bfc56717848ebeb5ea8ca8e84228
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261474671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2391866dff714c0dd40f9c6312fd8e4f812ac2e4021af81b3dccc50667db06f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:52:29 GMT
ENV ROS_DISTRO=rolling
# Sat, 02 Dec 2023 06:53:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:53:11 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:53:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:53:11 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:53:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:53:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:53:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 06:53:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c57f456ff177333c5356ffa95267bf81ffda007282ce077aefc6dad7287b95`  
		Last Modified: Sat, 02 Dec 2023 07:03:49 GMT  
		Size: 121.7 MB (121738352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ea17e58cc534987e4066afb39789529299e5bc0f0963a20f3a8e3abb5798f5`  
		Last Modified: Sat, 02 Dec 2023 07:03:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d83f0b90f7994538015346ea0103817e07f6da588cecd5abbe0dd1627ebc4ac`  
		Last Modified: Sat, 02 Dec 2023 07:04:06 GMT  
		Size: 82.8 MB (82848039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c43d34c57d89c613359ac8be6efbbcf83426b61e4b6af0fb3066fec67df503`  
		Last Modified: Sat, 02 Dec 2023 07:03:57 GMT  
		Size: 302.3 KB (302296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a216765a08949157ffe626c1703f66b7e09f03610e3d0424d53cefaa986f0877`  
		Last Modified: Sat, 02 Dec 2023 07:03:56 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca613d7f9aa91e5aa03a762cb8204133388b9cf71737c8afb097c084023b36`  
		Last Modified: Sat, 02 Dec 2023 07:04:01 GMT  
		Size: 23.2 MB (23164918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:926b1d08083e1bc09891617da3fab01c1b816879d76a79379eb306710881327c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:cc7066833e4bc91cf30a6ff2071e0507e1850e433ab947bb7db9765baf817514
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **959.9 MB (959931532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9398061bf4afb5deaf168bc397874a59dcb0509c5226b74875a75883c030ad99`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:55:52 GMT
ENV ROS_DISTRO=rolling
# Sat, 02 Dec 2023 05:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:56:37 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:56:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:56:37 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:56:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:57:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:57:04 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 05:57:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:58:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70cdec7f7f494d3cb2ea302a0b42630c0353133474a693a309d1b5950b3d1b1`  
		Last Modified: Sat, 02 Dec 2023 06:07:11 GMT  
		Size: 124.3 MB (124271649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb056cc69d86752a925eb68c836ad08186757af76db68041db5eb1da10a0e15`  
		Last Modified: Sat, 02 Dec 2023 06:06:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655e7b257add838be46a798525b40ef3b18fea490caf612f09c1151ebbe6f7a6`  
		Last Modified: Sat, 02 Dec 2023 06:07:31 GMT  
		Size: 85.2 MB (85172080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf0a91322021b1c4e36dd3a6fb62d30b3c54e6098d0755a4f5bdfc328aa0040`  
		Last Modified: Sat, 02 Dec 2023 06:07:21 GMT  
		Size: 302.3 KB (302307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f42b45f4e05e21e47e74869b5b88a9964383d8448055d257f47a34694c6eae0`  
		Last Modified: Sat, 02 Dec 2023 06:07:21 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7f58f28f44789d5600868e9ca68910d022964a421870c5b3bbbb5ae9cb08c`  
		Last Modified: Sat, 02 Dec 2023 06:07:24 GMT  
		Size: 23.8 MB (23778449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f623afbab66cfa921bc142fdbc3182c107255770f7586d5fbe97df35f8d24890`  
		Last Modified: Sat, 02 Dec 2023 06:09:08 GMT  
		Size: 690.9 MB (690913680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8493f256e99822754a625976fbff3141dc8252f937f64b9c1417d3f79e0e1159
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.2 MB (920230507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8736dbef879b4aeea4ad4246294caa41444baa768529c4d49fc9572bdabc36cd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:52:29 GMT
ENV ROS_DISTRO=rolling
# Sat, 02 Dec 2023 06:53:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:53:11 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:53:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:53:11 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:53:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:53:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:53:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 06:53:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:55:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c57f456ff177333c5356ffa95267bf81ffda007282ce077aefc6dad7287b95`  
		Last Modified: Sat, 02 Dec 2023 07:03:49 GMT  
		Size: 121.7 MB (121738352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ea17e58cc534987e4066afb39789529299e5bc0f0963a20f3a8e3abb5798f5`  
		Last Modified: Sat, 02 Dec 2023 07:03:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d83f0b90f7994538015346ea0103817e07f6da588cecd5abbe0dd1627ebc4ac`  
		Last Modified: Sat, 02 Dec 2023 07:04:06 GMT  
		Size: 82.8 MB (82848039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c43d34c57d89c613359ac8be6efbbcf83426b61e4b6af0fb3066fec67df503`  
		Last Modified: Sat, 02 Dec 2023 07:03:57 GMT  
		Size: 302.3 KB (302296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a216765a08949157ffe626c1703f66b7e09f03610e3d0424d53cefaa986f0877`  
		Last Modified: Sat, 02 Dec 2023 07:03:56 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca613d7f9aa91e5aa03a762cb8204133388b9cf71737c8afb097c084023b36`  
		Last Modified: Sat, 02 Dec 2023 07:04:01 GMT  
		Size: 23.2 MB (23164918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210a93a5bf952bcc123fcfc114a7b4639054f592c0d48f290cc2bd7c0bced571`  
		Last Modified: Sat, 02 Dec 2023 07:05:39 GMT  
		Size: 658.8 MB (658755836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception-jammy`

```console
$ docker pull ros@sha256:926b1d08083e1bc09891617da3fab01c1b816879d76a79379eb306710881327c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:cc7066833e4bc91cf30a6ff2071e0507e1850e433ab947bb7db9765baf817514
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **959.9 MB (959931532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9398061bf4afb5deaf168bc397874a59dcb0509c5226b74875a75883c030ad99`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:55:52 GMT
ENV ROS_DISTRO=rolling
# Sat, 02 Dec 2023 05:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:56:37 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:56:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:56:37 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:56:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:57:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:57:04 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 05:57:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:58:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70cdec7f7f494d3cb2ea302a0b42630c0353133474a693a309d1b5950b3d1b1`  
		Last Modified: Sat, 02 Dec 2023 06:07:11 GMT  
		Size: 124.3 MB (124271649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb056cc69d86752a925eb68c836ad08186757af76db68041db5eb1da10a0e15`  
		Last Modified: Sat, 02 Dec 2023 06:06:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655e7b257add838be46a798525b40ef3b18fea490caf612f09c1151ebbe6f7a6`  
		Last Modified: Sat, 02 Dec 2023 06:07:31 GMT  
		Size: 85.2 MB (85172080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf0a91322021b1c4e36dd3a6fb62d30b3c54e6098d0755a4f5bdfc328aa0040`  
		Last Modified: Sat, 02 Dec 2023 06:07:21 GMT  
		Size: 302.3 KB (302307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f42b45f4e05e21e47e74869b5b88a9964383d8448055d257f47a34694c6eae0`  
		Last Modified: Sat, 02 Dec 2023 06:07:21 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7f58f28f44789d5600868e9ca68910d022964a421870c5b3bbbb5ae9cb08c`  
		Last Modified: Sat, 02 Dec 2023 06:07:24 GMT  
		Size: 23.8 MB (23778449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f623afbab66cfa921bc142fdbc3182c107255770f7586d5fbe97df35f8d24890`  
		Last Modified: Sat, 02 Dec 2023 06:09:08 GMT  
		Size: 690.9 MB (690913680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8493f256e99822754a625976fbff3141dc8252f937f64b9c1417d3f79e0e1159
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.2 MB (920230507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8736dbef879b4aeea4ad4246294caa41444baa768529c4d49fc9572bdabc36cd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:52:29 GMT
ENV ROS_DISTRO=rolling
# Sat, 02 Dec 2023 06:53:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:53:11 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:53:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:53:11 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:53:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:53:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:53:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 06:53:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:55:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c57f456ff177333c5356ffa95267bf81ffda007282ce077aefc6dad7287b95`  
		Last Modified: Sat, 02 Dec 2023 07:03:49 GMT  
		Size: 121.7 MB (121738352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ea17e58cc534987e4066afb39789529299e5bc0f0963a20f3a8e3abb5798f5`  
		Last Modified: Sat, 02 Dec 2023 07:03:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d83f0b90f7994538015346ea0103817e07f6da588cecd5abbe0dd1627ebc4ac`  
		Last Modified: Sat, 02 Dec 2023 07:04:06 GMT  
		Size: 82.8 MB (82848039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c43d34c57d89c613359ac8be6efbbcf83426b61e4b6af0fb3066fec67df503`  
		Last Modified: Sat, 02 Dec 2023 07:03:57 GMT  
		Size: 302.3 KB (302296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a216765a08949157ffe626c1703f66b7e09f03610e3d0424d53cefaa986f0877`  
		Last Modified: Sat, 02 Dec 2023 07:03:56 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca613d7f9aa91e5aa03a762cb8204133388b9cf71737c8afb097c084023b36`  
		Last Modified: Sat, 02 Dec 2023 07:04:01 GMT  
		Size: 23.2 MB (23164918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210a93a5bf952bcc123fcfc114a7b4639054f592c0d48f290cc2bd7c0bced571`  
		Last Modified: Sat, 02 Dec 2023 07:05:39 GMT  
		Size: 658.8 MB (658755836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:eb05cb3d0c3b819a402c7f28b3ae0313f9d41a692d92a2d642ba6dbe109a3a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:57ed363844b88e69c892ab60c196c459a4370ba2b3d55c8664091d817684d033
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269017852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15700c2d31c62a8c49f085258b7aac62c20d1d93b1f8db4d5764f6b1d2ccaff9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:55:52 GMT
ENV ROS_DISTRO=rolling
# Sat, 02 Dec 2023 05:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:56:37 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:56:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:56:37 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:56:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:57:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:57:04 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 05:57:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70cdec7f7f494d3cb2ea302a0b42630c0353133474a693a309d1b5950b3d1b1`  
		Last Modified: Sat, 02 Dec 2023 06:07:11 GMT  
		Size: 124.3 MB (124271649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb056cc69d86752a925eb68c836ad08186757af76db68041db5eb1da10a0e15`  
		Last Modified: Sat, 02 Dec 2023 06:06:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655e7b257add838be46a798525b40ef3b18fea490caf612f09c1151ebbe6f7a6`  
		Last Modified: Sat, 02 Dec 2023 06:07:31 GMT  
		Size: 85.2 MB (85172080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf0a91322021b1c4e36dd3a6fb62d30b3c54e6098d0755a4f5bdfc328aa0040`  
		Last Modified: Sat, 02 Dec 2023 06:07:21 GMT  
		Size: 302.3 KB (302307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f42b45f4e05e21e47e74869b5b88a9964383d8448055d257f47a34694c6eae0`  
		Last Modified: Sat, 02 Dec 2023 06:07:21 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7f58f28f44789d5600868e9ca68910d022964a421870c5b3bbbb5ae9cb08c`  
		Last Modified: Sat, 02 Dec 2023 06:07:24 GMT  
		Size: 23.8 MB (23778449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9f7d538dae51b42502aa3924a51443726ae3bfc56717848ebeb5ea8ca8e84228
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261474671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2391866dff714c0dd40f9c6312fd8e4f812ac2e4021af81b3dccc50667db06f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:52:29 GMT
ENV ROS_DISTRO=rolling
# Sat, 02 Dec 2023 06:53:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:53:11 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:53:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:53:11 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:53:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:53:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:53:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 06:53:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c57f456ff177333c5356ffa95267bf81ffda007282ce077aefc6dad7287b95`  
		Last Modified: Sat, 02 Dec 2023 07:03:49 GMT  
		Size: 121.7 MB (121738352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ea17e58cc534987e4066afb39789529299e5bc0f0963a20f3a8e3abb5798f5`  
		Last Modified: Sat, 02 Dec 2023 07:03:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d83f0b90f7994538015346ea0103817e07f6da588cecd5abbe0dd1627ebc4ac`  
		Last Modified: Sat, 02 Dec 2023 07:04:06 GMT  
		Size: 82.8 MB (82848039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c43d34c57d89c613359ac8be6efbbcf83426b61e4b6af0fb3066fec67df503`  
		Last Modified: Sat, 02 Dec 2023 07:03:57 GMT  
		Size: 302.3 KB (302296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a216765a08949157ffe626c1703f66b7e09f03610e3d0424d53cefaa986f0877`  
		Last Modified: Sat, 02 Dec 2023 07:03:56 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca613d7f9aa91e5aa03a762cb8204133388b9cf71737c8afb097c084023b36`  
		Last Modified: Sat, 02 Dec 2023 07:04:01 GMT  
		Size: 23.2 MB (23164918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base-jammy`

```console
$ docker pull ros@sha256:eb05cb3d0c3b819a402c7f28b3ae0313f9d41a692d92a2d642ba6dbe109a3a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:57ed363844b88e69c892ab60c196c459a4370ba2b3d55c8664091d817684d033
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269017852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15700c2d31c62a8c49f085258b7aac62c20d1d93b1f8db4d5764f6b1d2ccaff9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:55:52 GMT
ENV ROS_DISTRO=rolling
# Sat, 02 Dec 2023 05:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:56:37 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:56:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:56:37 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 05:56:56 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:57:01 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 05:57:04 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 05:57:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70cdec7f7f494d3cb2ea302a0b42630c0353133474a693a309d1b5950b3d1b1`  
		Last Modified: Sat, 02 Dec 2023 06:07:11 GMT  
		Size: 124.3 MB (124271649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb056cc69d86752a925eb68c836ad08186757af76db68041db5eb1da10a0e15`  
		Last Modified: Sat, 02 Dec 2023 06:06:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655e7b257add838be46a798525b40ef3b18fea490caf612f09c1151ebbe6f7a6`  
		Last Modified: Sat, 02 Dec 2023 06:07:31 GMT  
		Size: 85.2 MB (85172080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf0a91322021b1c4e36dd3a6fb62d30b3c54e6098d0755a4f5bdfc328aa0040`  
		Last Modified: Sat, 02 Dec 2023 06:07:21 GMT  
		Size: 302.3 KB (302307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f42b45f4e05e21e47e74869b5b88a9964383d8448055d257f47a34694c6eae0`  
		Last Modified: Sat, 02 Dec 2023 06:07:21 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d7f58f28f44789d5600868e9ca68910d022964a421870c5b3bbbb5ae9cb08c`  
		Last Modified: Sat, 02 Dec 2023 06:07:24 GMT  
		Size: 23.8 MB (23778449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9f7d538dae51b42502aa3924a51443726ae3bfc56717848ebeb5ea8ca8e84228
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261474671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2391866dff714c0dd40f9c6312fd8e4f812ac2e4021af81b3dccc50667db06f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:52:29 GMT
ENV ROS_DISTRO=rolling
# Sat, 02 Dec 2023 06:53:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:53:11 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:53:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:53:11 GMT
CMD ["bash"]
# Sat, 02 Dec 2023 06:53:30 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:53:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 02 Dec 2023 06:53:37 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 02 Dec 2023 06:53:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c57f456ff177333c5356ffa95267bf81ffda007282ce077aefc6dad7287b95`  
		Last Modified: Sat, 02 Dec 2023 07:03:49 GMT  
		Size: 121.7 MB (121738352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ea17e58cc534987e4066afb39789529299e5bc0f0963a20f3a8e3abb5798f5`  
		Last Modified: Sat, 02 Dec 2023 07:03:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d83f0b90f7994538015346ea0103817e07f6da588cecd5abbe0dd1627ebc4ac`  
		Last Modified: Sat, 02 Dec 2023 07:04:06 GMT  
		Size: 82.8 MB (82848039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c43d34c57d89c613359ac8be6efbbcf83426b61e4b6af0fb3066fec67df503`  
		Last Modified: Sat, 02 Dec 2023 07:03:57 GMT  
		Size: 302.3 KB (302296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a216765a08949157ffe626c1703f66b7e09f03610e3d0424d53cefaa986f0877`  
		Last Modified: Sat, 02 Dec 2023 07:03:56 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca613d7f9aa91e5aa03a762cb8204133388b9cf71737c8afb097c084023b36`  
		Last Modified: Sat, 02 Dec 2023 07:04:01 GMT  
		Size: 23.2 MB (23164918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:0c5ce27abd73340efca0ae78536b104cc0d2ee269362947031b10517ff6a4d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:2dbe6d85e28cb0882945c203dddc773aa5fe26d4bcab19a5aaa4900ff98ea113
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159762568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e567315f0c281a0d9d436237b15e221cd0d236fd63b7140605e670e9c48eb94`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:55:52 GMT
ENV ROS_DISTRO=rolling
# Sat, 02 Dec 2023 05:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:56:37 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:56:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:56:37 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70cdec7f7f494d3cb2ea302a0b42630c0353133474a693a309d1b5950b3d1b1`  
		Last Modified: Sat, 02 Dec 2023 06:07:11 GMT  
		Size: 124.3 MB (124271649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb056cc69d86752a925eb68c836ad08186757af76db68041db5eb1da10a0e15`  
		Last Modified: Sat, 02 Dec 2023 06:06:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c06f2e640db0fa06e63dcbf4784718e8cf5c441e0c3eb09ce7d51a8ca3b3501f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155156970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87daa1fa38379ec479bcbaed6312b6d2fa2a11a650d6f796adb74d13b42c3c2a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:52:29 GMT
ENV ROS_DISTRO=rolling
# Sat, 02 Dec 2023 06:53:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:53:11 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:53:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:53:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c57f456ff177333c5356ffa95267bf81ffda007282ce077aefc6dad7287b95`  
		Last Modified: Sat, 02 Dec 2023 07:03:49 GMT  
		Size: 121.7 MB (121738352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ea17e58cc534987e4066afb39789529299e5bc0f0963a20f3a8e3abb5798f5`  
		Last Modified: Sat, 02 Dec 2023 07:03:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core-jammy`

```console
$ docker pull ros@sha256:0c5ce27abd73340efca0ae78536b104cc0d2ee269362947031b10517ff6a4d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:2dbe6d85e28cb0882945c203dddc773aa5fe26d4bcab19a5aaa4900ff98ea113
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159762568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e567315f0c281a0d9d436237b15e221cd0d236fd63b7140605e670e9c48eb94`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:27:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:47 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:48 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 05:27:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 05:27:49 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 05:55:52 GMT
ENV ROS_DISTRO=rolling
# Sat, 02 Dec 2023 05:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:56:37 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 05:56:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 05:56:37 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bf7725f2e681d0c15f152b2f888f77c84c4d12171d80cd7fa4f49f3d492f10`  
		Last Modified: Sat, 02 Dec 2023 06:02:02 GMT  
		Size: 1.2 MB (1213167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779e38ab231d64c0df2d7580b11ddac752bacf4e52cd32b110d15cdbe06c8fbc`  
		Last Modified: Sat, 02 Dec 2023 06:02:01 GMT  
		Size: 3.8 MB (3829013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeba364b2019d92e87cbcab89bd90f200d06ac74f5d4a1a9d74bf074212553f`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749b34d74c1a492cae4e3f4683f2d86855ac6e95e57c6b6cfbf50462c1600cee`  
		Last Modified: Sat, 02 Dec 2023 06:02:00 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70cdec7f7f494d3cb2ea302a0b42630c0353133474a693a309d1b5950b3d1b1`  
		Last Modified: Sat, 02 Dec 2023 06:07:11 GMT  
		Size: 124.3 MB (124271649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb056cc69d86752a925eb68c836ad08186757af76db68041db5eb1da10a0e15`  
		Last Modified: Sat, 02 Dec 2023 06:06:53 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c06f2e640db0fa06e63dcbf4784718e8cf5c441e0c3eb09ce7d51a8ca3b3501f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155156970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87daa1fa38379ec479bcbaed6312b6d2fa2a11a650d6f796adb74d13b42c3c2a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:36:21 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:26 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:36:27 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Sat, 02 Dec 2023 06:36:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LANG=C.UTF-8
# Sat, 02 Dec 2023 06:36:28 GMT
ENV LC_ALL=C.UTF-8
# Sat, 02 Dec 2023 06:52:29 GMT
ENV ROS_DISTRO=rolling
# Sat, 02 Dec 2023 06:53:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 06:53:11 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 02 Dec 2023 06:53:11 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 02 Dec 2023 06:53:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce86a03a18f78cf25cdf581531142e7367f0fe08a1fdd01402d6c7f4ce8d2b`  
		Last Modified: Sat, 02 Dec 2023 06:58:34 GMT  
		Size: 1.2 MB (1214421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8480855a5f2a943f3f15f49e414e94fa9a8a0ad577b7c9d09b27005d302b32b`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 3.8 MB (3801844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacde95041d65db11f59b618d0187c7722c802e812531af2c76787a51c0686c5`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78181ef16d6caeb69a5c457d1a62ae92b8145fa0fef38cd44bd1b0a41f7100a`  
		Last Modified: Sat, 02 Dec 2023 06:58:32 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c57f456ff177333c5356ffa95267bf81ffda007282ce077aefc6dad7287b95`  
		Last Modified: Sat, 02 Dec 2023 07:03:49 GMT  
		Size: 121.7 MB (121738352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ea17e58cc534987e4066afb39789529299e5bc0f0963a20f3a8e3abb5798f5`  
		Last Modified: Sat, 02 Dec 2023 07:03:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
