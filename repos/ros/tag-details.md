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
-	[`ros:latest`](#roslatest)
-	[`ros:melodic`](#rosmelodic)
-	[`ros:melodic-perception`](#rosmelodic-perception)
-	[`ros:melodic-perception-bionic`](#rosmelodic-perception-bionic)
-	[`ros:melodic-robot`](#rosmelodic-robot)
-	[`ros:melodic-robot-bionic`](#rosmelodic-robot-bionic)
-	[`ros:melodic-ros-base`](#rosmelodic-ros-base)
-	[`ros:melodic-ros-base-bionic`](#rosmelodic-ros-base-bionic)
-	[`ros:melodic-ros-core`](#rosmelodic-ros-core)
-	[`ros:melodic-ros-core-bionic`](#rosmelodic-ros-core-bionic)
-	[`ros:noetic`](#rosnoetic)
-	[`ros:noetic-perception`](#rosnoetic-perception)
-	[`ros:noetic-perception-buster`](#rosnoetic-perception-buster)
-	[`ros:noetic-perception-focal`](#rosnoetic-perception-focal)
-	[`ros:noetic-robot`](#rosnoetic-robot)
-	[`ros:noetic-robot-buster`](#rosnoetic-robot-buster)
-	[`ros:noetic-robot-focal`](#rosnoetic-robot-focal)
-	[`ros:noetic-ros-base`](#rosnoetic-ros-base)
-	[`ros:noetic-ros-base-buster`](#rosnoetic-ros-base-buster)
-	[`ros:noetic-ros-base-focal`](#rosnoetic-ros-base-focal)
-	[`ros:noetic-ros-core`](#rosnoetic-ros-core)
-	[`ros:noetic-ros-core-buster`](#rosnoetic-ros-core-buster)
-	[`ros:noetic-ros-core-focal`](#rosnoetic-ros-core-focal)
-	[`ros:rolling`](#rosrolling)
-	[`ros:rolling-perception`](#rosrolling-perception)
-	[`ros:rolling-perception-jammy`](#rosrolling-perception-jammy)
-	[`ros:rolling-ros-base`](#rosrolling-ros-base)
-	[`ros:rolling-ros-base-jammy`](#rosrolling-ros-base-jammy)
-	[`ros:rolling-ros-core`](#rosrolling-ros-core)
-	[`ros:rolling-ros-core-jammy`](#rosrolling-ros-core-jammy)

## `ros:foxy`

```console
$ docker pull ros@sha256:02ba160fa839b96ba6acb22a554190c4743285cdc17745e28c0f13585b10c345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy` - linux; amd64

```console
$ docker pull ros@sha256:2a2cb6ec4fa94c8405549a3ba868f1be8e7cc9ba3530bf9909f1d7517fc33acd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250910730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79dc804c68414a56e2bc462fd1705c10a1815d04042c72e88ced0971e695f5b8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 07:26:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:26:27 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:26:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:26:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:27:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:27:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:27:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:28:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122af75c69e965a1d4b50e964ea95ec60ddd9997347536d0e79ecf1dc96f8e4d`  
		Last Modified: Tue, 25 Oct 2022 07:59:22 GMT  
		Size: 120.4 MB (120353945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fb29cc59034ebd9df4a3ddc0a423888144631e3a1e4b4cffff2ce4396d52ed`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5fb36af82e519ef989f9d9107e767f04c18c153572130e0f6c3a343ebb0ce0`  
		Last Modified: Tue, 25 Oct 2022 07:59:43 GMT  
		Size: 73.3 MB (73325743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837655cef3c4cc06788fbad7c6df8a77081a39d3392b8bafed1ea74c35a302e3`  
		Last Modified: Tue, 25 Oct 2022 07:59:32 GMT  
		Size: 269.4 KB (269364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb41d05e0bd11afe16ecfcf7ef668e3908835201cc94fa813d0bf7783c3ba24f`  
		Last Modified: Tue, 25 Oct 2022 07:59:31 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0f073c138f041e9b85ff0ddae19609c388a359370280ec72e5d549f73206c8`  
		Last Modified: Tue, 25 Oct 2022 07:59:35 GMT  
		Size: 21.7 MB (21663794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1814ed410f2086291253ecfb6ae7f91372772eeae0dce2bdfe0a5be0164af52b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226763797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5022b17e9054bde6a86e41848695fea694d49265ee919d449400104fe721b737`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:33:04 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:33:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 21:34:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:35:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:35:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:35:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:35:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:36:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:36:08 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:36:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf249399bc0440c14b3771796a8a9749b00b8b1f768beabb4bf65173978661`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a95e1d715258f8932e6718ed06a1eb17a823b5bb14f27e1ca7cead6b3cdb64a`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1125e614642ae08f414585e39268e20619496243391fc14223c48efb76567fe`  
		Last Modified: Tue, 25 Oct 2022 22:06:20 GMT  
		Size: 104.5 MB (104549412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3257e5f004cfece29d48f51619b6b61a55c530aa1ecbc38e1be4208caa2ae368`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414db4c36b110ea6ec637828a4983215f3c8120f5113c6b8a1b1e7b63d490652`  
		Last Modified: Tue, 25 Oct 2022 22:06:39 GMT  
		Size: 67.7 MB (67673997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29c8a2e8faff52e903b8c6eb0d283754c1de2db5a4f0fa1c50542d8ed3bf757`  
		Last Modified: Tue, 25 Oct 2022 22:06:31 GMT  
		Size: 269.4 KB (269368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650fa392d56bb2a49e8e5ceaea16096752cb2cddfae87d9cf1a6193b59b1da7a`  
		Last Modified: Tue, 25 Oct 2022 22:06:30 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cee9901e31fd356db4bc05acd8610220bec8ba0ced72c5658083ba9b7e4d51`  
		Last Modified: Tue, 25 Oct 2022 22:06:34 GMT  
		Size: 20.4 MB (20372962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-base`

```console
$ docker pull ros@sha256:02ba160fa839b96ba6acb22a554190c4743285cdc17745e28c0f13585b10c345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:2a2cb6ec4fa94c8405549a3ba868f1be8e7cc9ba3530bf9909f1d7517fc33acd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250910730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79dc804c68414a56e2bc462fd1705c10a1815d04042c72e88ced0971e695f5b8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 07:26:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:26:27 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:26:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:26:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:27:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:27:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:27:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:28:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122af75c69e965a1d4b50e964ea95ec60ddd9997347536d0e79ecf1dc96f8e4d`  
		Last Modified: Tue, 25 Oct 2022 07:59:22 GMT  
		Size: 120.4 MB (120353945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fb29cc59034ebd9df4a3ddc0a423888144631e3a1e4b4cffff2ce4396d52ed`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5fb36af82e519ef989f9d9107e767f04c18c153572130e0f6c3a343ebb0ce0`  
		Last Modified: Tue, 25 Oct 2022 07:59:43 GMT  
		Size: 73.3 MB (73325743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837655cef3c4cc06788fbad7c6df8a77081a39d3392b8bafed1ea74c35a302e3`  
		Last Modified: Tue, 25 Oct 2022 07:59:32 GMT  
		Size: 269.4 KB (269364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb41d05e0bd11afe16ecfcf7ef668e3908835201cc94fa813d0bf7783c3ba24f`  
		Last Modified: Tue, 25 Oct 2022 07:59:31 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0f073c138f041e9b85ff0ddae19609c388a359370280ec72e5d549f73206c8`  
		Last Modified: Tue, 25 Oct 2022 07:59:35 GMT  
		Size: 21.7 MB (21663794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1814ed410f2086291253ecfb6ae7f91372772eeae0dce2bdfe0a5be0164af52b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226763797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5022b17e9054bde6a86e41848695fea694d49265ee919d449400104fe721b737`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:33:04 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:33:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 21:34:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:35:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:35:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:35:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:35:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:36:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:36:08 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:36:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf249399bc0440c14b3771796a8a9749b00b8b1f768beabb4bf65173978661`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a95e1d715258f8932e6718ed06a1eb17a823b5bb14f27e1ca7cead6b3cdb64a`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1125e614642ae08f414585e39268e20619496243391fc14223c48efb76567fe`  
		Last Modified: Tue, 25 Oct 2022 22:06:20 GMT  
		Size: 104.5 MB (104549412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3257e5f004cfece29d48f51619b6b61a55c530aa1ecbc38e1be4208caa2ae368`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414db4c36b110ea6ec637828a4983215f3c8120f5113c6b8a1b1e7b63d490652`  
		Last Modified: Tue, 25 Oct 2022 22:06:39 GMT  
		Size: 67.7 MB (67673997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29c8a2e8faff52e903b8c6eb0d283754c1de2db5a4f0fa1c50542d8ed3bf757`  
		Last Modified: Tue, 25 Oct 2022 22:06:31 GMT  
		Size: 269.4 KB (269368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650fa392d56bb2a49e8e5ceaea16096752cb2cddfae87d9cf1a6193b59b1da7a`  
		Last Modified: Tue, 25 Oct 2022 22:06:30 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cee9901e31fd356db4bc05acd8610220bec8ba0ced72c5658083ba9b7e4d51`  
		Last Modified: Tue, 25 Oct 2022 22:06:34 GMT  
		Size: 20.4 MB (20372962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-base-focal`

```console
$ docker pull ros@sha256:02ba160fa839b96ba6acb22a554190c4743285cdc17745e28c0f13585b10c345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:2a2cb6ec4fa94c8405549a3ba868f1be8e7cc9ba3530bf9909f1d7517fc33acd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250910730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79dc804c68414a56e2bc462fd1705c10a1815d04042c72e88ced0971e695f5b8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 07:26:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:26:27 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:26:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:26:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:27:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:27:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:27:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:28:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122af75c69e965a1d4b50e964ea95ec60ddd9997347536d0e79ecf1dc96f8e4d`  
		Last Modified: Tue, 25 Oct 2022 07:59:22 GMT  
		Size: 120.4 MB (120353945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fb29cc59034ebd9df4a3ddc0a423888144631e3a1e4b4cffff2ce4396d52ed`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5fb36af82e519ef989f9d9107e767f04c18c153572130e0f6c3a343ebb0ce0`  
		Last Modified: Tue, 25 Oct 2022 07:59:43 GMT  
		Size: 73.3 MB (73325743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837655cef3c4cc06788fbad7c6df8a77081a39d3392b8bafed1ea74c35a302e3`  
		Last Modified: Tue, 25 Oct 2022 07:59:32 GMT  
		Size: 269.4 KB (269364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb41d05e0bd11afe16ecfcf7ef668e3908835201cc94fa813d0bf7783c3ba24f`  
		Last Modified: Tue, 25 Oct 2022 07:59:31 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0f073c138f041e9b85ff0ddae19609c388a359370280ec72e5d549f73206c8`  
		Last Modified: Tue, 25 Oct 2022 07:59:35 GMT  
		Size: 21.7 MB (21663794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1814ed410f2086291253ecfb6ae7f91372772eeae0dce2bdfe0a5be0164af52b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226763797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5022b17e9054bde6a86e41848695fea694d49265ee919d449400104fe721b737`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:33:04 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:33:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 21:34:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:35:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:35:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:35:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:35:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:36:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:36:08 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:36:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf249399bc0440c14b3771796a8a9749b00b8b1f768beabb4bf65173978661`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a95e1d715258f8932e6718ed06a1eb17a823b5bb14f27e1ca7cead6b3cdb64a`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1125e614642ae08f414585e39268e20619496243391fc14223c48efb76567fe`  
		Last Modified: Tue, 25 Oct 2022 22:06:20 GMT  
		Size: 104.5 MB (104549412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3257e5f004cfece29d48f51619b6b61a55c530aa1ecbc38e1be4208caa2ae368`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414db4c36b110ea6ec637828a4983215f3c8120f5113c6b8a1b1e7b63d490652`  
		Last Modified: Tue, 25 Oct 2022 22:06:39 GMT  
		Size: 67.7 MB (67673997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29c8a2e8faff52e903b8c6eb0d283754c1de2db5a4f0fa1c50542d8ed3bf757`  
		Last Modified: Tue, 25 Oct 2022 22:06:31 GMT  
		Size: 269.4 KB (269368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650fa392d56bb2a49e8e5ceaea16096752cb2cddfae87d9cf1a6193b59b1da7a`  
		Last Modified: Tue, 25 Oct 2022 22:06:30 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cee9901e31fd356db4bc05acd8610220bec8ba0ced72c5658083ba9b7e4d51`  
		Last Modified: Tue, 25 Oct 2022 22:06:34 GMT  
		Size: 20.4 MB (20372962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-core`

```console
$ docker pull ros@sha256:03528d3871764da0c6cee24e7baaeee8562c4ba3e90debfae5746ecd42ac82ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:87d8f4e045ca908ea1e9fc36cd58992b068c2243cd417af51df28015cae361c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155649379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f133e19ba781eb57466f334011e632c7258cb020aa4bd3f02210dc2724fc2f68`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 07:26:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:26:27 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:26:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:26:27 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122af75c69e965a1d4b50e964ea95ec60ddd9997347536d0e79ecf1dc96f8e4d`  
		Last Modified: Tue, 25 Oct 2022 07:59:22 GMT  
		Size: 120.4 MB (120353945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fb29cc59034ebd9df4a3ddc0a423888144631e3a1e4b4cffff2ce4396d52ed`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:14b37ec2f8cb57f1f948ddcb5dde6683ad4fed9db0365ff2ba990b3008ede6e7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138445026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aaad4dee75eed93cc82b94029a2a7353ef3d2e022f002a56599f1750b75818a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:33:04 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:33:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 21:34:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:35:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:35:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:35:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf249399bc0440c14b3771796a8a9749b00b8b1f768beabb4bf65173978661`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a95e1d715258f8932e6718ed06a1eb17a823b5bb14f27e1ca7cead6b3cdb64a`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1125e614642ae08f414585e39268e20619496243391fc14223c48efb76567fe`  
		Last Modified: Tue, 25 Oct 2022 22:06:20 GMT  
		Size: 104.5 MB (104549412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3257e5f004cfece29d48f51619b6b61a55c530aa1ecbc38e1be4208caa2ae368`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-core-focal`

```console
$ docker pull ros@sha256:03528d3871764da0c6cee24e7baaeee8562c4ba3e90debfae5746ecd42ac82ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:87d8f4e045ca908ea1e9fc36cd58992b068c2243cd417af51df28015cae361c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155649379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f133e19ba781eb57466f334011e632c7258cb020aa4bd3f02210dc2724fc2f68`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 07:26:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:26:27 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:26:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:26:27 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122af75c69e965a1d4b50e964ea95ec60ddd9997347536d0e79ecf1dc96f8e4d`  
		Last Modified: Tue, 25 Oct 2022 07:59:22 GMT  
		Size: 120.4 MB (120353945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fb29cc59034ebd9df4a3ddc0a423888144631e3a1e4b4cffff2ce4396d52ed`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:14b37ec2f8cb57f1f948ddcb5dde6683ad4fed9db0365ff2ba990b3008ede6e7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138445026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aaad4dee75eed93cc82b94029a2a7353ef3d2e022f002a56599f1750b75818a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:33:04 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:33:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 21:34:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:35:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:35:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:35:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf249399bc0440c14b3771796a8a9749b00b8b1f768beabb4bf65173978661`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a95e1d715258f8932e6718ed06a1eb17a823b5bb14f27e1ca7cead6b3cdb64a`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1125e614642ae08f414585e39268e20619496243391fc14223c48efb76567fe`  
		Last Modified: Tue, 25 Oct 2022 22:06:20 GMT  
		Size: 104.5 MB (104549412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3257e5f004cfece29d48f51619b6b61a55c530aa1ecbc38e1be4208caa2ae368`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros1-bridge`

```console
$ docker pull ros@sha256:db3ff614975f6835e7f6f97ac76fc02690a312f250a753a7ef92b0c8754a03a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:a5a14cf96a615b81a6a77674968ec07922a7104e7df9f40fa9f9cc33a9e0a915
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349017846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a30f6376fb966081fc8055995c025832ef196fa1baac2115c933459278beae`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 07:26:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:26:27 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:26:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:26:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:27:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:27:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:27:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:28:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:28:11 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:28:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:28:12 GMT
ENV ROS1_DISTRO=noetic
# Tue, 25 Oct 2022 07:28:13 GMT
ENV ROS2_DISTRO=foxy
# Tue, 25 Oct 2022 07:29:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:29:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:29:38 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122af75c69e965a1d4b50e964ea95ec60ddd9997347536d0e79ecf1dc96f8e4d`  
		Last Modified: Tue, 25 Oct 2022 07:59:22 GMT  
		Size: 120.4 MB (120353945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fb29cc59034ebd9df4a3ddc0a423888144631e3a1e4b4cffff2ce4396d52ed`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5fb36af82e519ef989f9d9107e767f04c18c153572130e0f6c3a343ebb0ce0`  
		Last Modified: Tue, 25 Oct 2022 07:59:43 GMT  
		Size: 73.3 MB (73325743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837655cef3c4cc06788fbad7c6df8a77081a39d3392b8bafed1ea74c35a302e3`  
		Last Modified: Tue, 25 Oct 2022 07:59:32 GMT  
		Size: 269.4 KB (269364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb41d05e0bd11afe16ecfcf7ef668e3908835201cc94fa813d0bf7783c3ba24f`  
		Last Modified: Tue, 25 Oct 2022 07:59:31 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0f073c138f041e9b85ff0ddae19609c388a359370280ec72e5d549f73206c8`  
		Last Modified: Tue, 25 Oct 2022 07:59:35 GMT  
		Size: 21.7 MB (21663794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b18f13baebbb1e3f7ffc35466142e70d5913b88c27a49f5e5dbb9eab829e68e`  
		Last Modified: Tue, 25 Oct 2022 07:59:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff282c273773346a09f274c19f2310cf509f62c59ff80bf3c1831cb16577d048`  
		Last Modified: Tue, 25 Oct 2022 07:59:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084feb2aa93fcf8c7e68b0013adaf1d13ea903cabbc95d109fdc87c981859bb3`  
		Last Modified: Tue, 25 Oct 2022 08:00:15 GMT  
		Size: 76.4 MB (76434548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cadfac8cbf4b04e9e6ae0d30ae6985b445e23b413674c326c68a9a8688d00ee`  
		Last Modified: Tue, 25 Oct 2022 08:00:02 GMT  
		Size: 21.7 MB (21671942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4d8f780e2f7a944a9cbf79dd4545e29a7068cc6da18d290768c7a2c7a5dc59`  
		Last Modified: Tue, 25 Oct 2022 07:59:55 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7cf0d5c6ba9866cdc208048aa6a8637c2ab70997d91b7728eafafb40610fd2fb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.6 MB (317586189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430a6894eca1853128c921cba5b2b2d2190ac62a856f619df8f706668cb643d4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:33:04 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:33:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 21:34:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:35:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:35:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:35:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:35:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:36:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:36:08 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:36:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:37:05 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 21:37:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:37:06 GMT
ENV ROS1_DISTRO=noetic
# Tue, 25 Oct 2022 21:37:06 GMT
ENV ROS2_DISTRO=foxy
# Tue, 25 Oct 2022 21:38:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:38:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:38:38 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf249399bc0440c14b3771796a8a9749b00b8b1f768beabb4bf65173978661`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a95e1d715258f8932e6718ed06a1eb17a823b5bb14f27e1ca7cead6b3cdb64a`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1125e614642ae08f414585e39268e20619496243391fc14223c48efb76567fe`  
		Last Modified: Tue, 25 Oct 2022 22:06:20 GMT  
		Size: 104.5 MB (104549412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3257e5f004cfece29d48f51619b6b61a55c530aa1ecbc38e1be4208caa2ae368`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414db4c36b110ea6ec637828a4983215f3c8120f5113c6b8a1b1e7b63d490652`  
		Last Modified: Tue, 25 Oct 2022 22:06:39 GMT  
		Size: 67.7 MB (67673997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29c8a2e8faff52e903b8c6eb0d283754c1de2db5a4f0fa1c50542d8ed3bf757`  
		Last Modified: Tue, 25 Oct 2022 22:06:31 GMT  
		Size: 269.4 KB (269368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650fa392d56bb2a49e8e5ceaea16096752cb2cddfae87d9cf1a6193b59b1da7a`  
		Last Modified: Tue, 25 Oct 2022 22:06:30 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cee9901e31fd356db4bc05acd8610220bec8ba0ced72c5658083ba9b7e4d51`  
		Last Modified: Tue, 25 Oct 2022 22:06:34 GMT  
		Size: 20.4 MB (20372962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf5433e7c9e061f27cf48f334ed9ad7cc4a5ae501c1b108833008725972b866`  
		Last Modified: Tue, 25 Oct 2022 22:06:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb74af6d3b5c37adef97f1fd6e95e116863e798184de223195cd2bed8dcbeba2`  
		Last Modified: Tue, 25 Oct 2022 22:06:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f420526906050934cc358b07ad0fc7eb75f00fb532e634a89120c99fa12c4b`  
		Last Modified: Tue, 25 Oct 2022 22:07:09 GMT  
		Size: 76.5 MB (76498135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e83da535cea3510c390e46cacfb76f7c2e44b10a2a3f2a9cdeb3588df562d1`  
		Last Modified: Tue, 25 Oct 2022 22:06:56 GMT  
		Size: 14.3 MB (14323630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82106a27fefc9b7d0614542f8d3d1ca6771cf9006d3fb2a6d280abc49a689f17`  
		Last Modified: Tue, 25 Oct 2022 22:06:52 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:db3ff614975f6835e7f6f97ac76fc02690a312f250a753a7ef92b0c8754a03a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:a5a14cf96a615b81a6a77674968ec07922a7104e7df9f40fa9f9cc33a9e0a915
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349017846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a30f6376fb966081fc8055995c025832ef196fa1baac2115c933459278beae`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 07:26:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:26:27 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:26:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:26:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:27:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:27:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:27:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:28:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:28:11 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:28:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:28:12 GMT
ENV ROS1_DISTRO=noetic
# Tue, 25 Oct 2022 07:28:13 GMT
ENV ROS2_DISTRO=foxy
# Tue, 25 Oct 2022 07:29:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:29:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:29:38 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122af75c69e965a1d4b50e964ea95ec60ddd9997347536d0e79ecf1dc96f8e4d`  
		Last Modified: Tue, 25 Oct 2022 07:59:22 GMT  
		Size: 120.4 MB (120353945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fb29cc59034ebd9df4a3ddc0a423888144631e3a1e4b4cffff2ce4396d52ed`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5fb36af82e519ef989f9d9107e767f04c18c153572130e0f6c3a343ebb0ce0`  
		Last Modified: Tue, 25 Oct 2022 07:59:43 GMT  
		Size: 73.3 MB (73325743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837655cef3c4cc06788fbad7c6df8a77081a39d3392b8bafed1ea74c35a302e3`  
		Last Modified: Tue, 25 Oct 2022 07:59:32 GMT  
		Size: 269.4 KB (269364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb41d05e0bd11afe16ecfcf7ef668e3908835201cc94fa813d0bf7783c3ba24f`  
		Last Modified: Tue, 25 Oct 2022 07:59:31 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0f073c138f041e9b85ff0ddae19609c388a359370280ec72e5d549f73206c8`  
		Last Modified: Tue, 25 Oct 2022 07:59:35 GMT  
		Size: 21.7 MB (21663794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b18f13baebbb1e3f7ffc35466142e70d5913b88c27a49f5e5dbb9eab829e68e`  
		Last Modified: Tue, 25 Oct 2022 07:59:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff282c273773346a09f274c19f2310cf509f62c59ff80bf3c1831cb16577d048`  
		Last Modified: Tue, 25 Oct 2022 07:59:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084feb2aa93fcf8c7e68b0013adaf1d13ea903cabbc95d109fdc87c981859bb3`  
		Last Modified: Tue, 25 Oct 2022 08:00:15 GMT  
		Size: 76.4 MB (76434548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cadfac8cbf4b04e9e6ae0d30ae6985b445e23b413674c326c68a9a8688d00ee`  
		Last Modified: Tue, 25 Oct 2022 08:00:02 GMT  
		Size: 21.7 MB (21671942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4d8f780e2f7a944a9cbf79dd4545e29a7068cc6da18d290768c7a2c7a5dc59`  
		Last Modified: Tue, 25 Oct 2022 07:59:55 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7cf0d5c6ba9866cdc208048aa6a8637c2ab70997d91b7728eafafb40610fd2fb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.6 MB (317586189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430a6894eca1853128c921cba5b2b2d2190ac62a856f619df8f706668cb643d4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:33:04 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:33:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 21:34:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:35:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:35:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:35:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:35:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:36:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:36:08 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:36:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:37:05 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 21:37:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:37:06 GMT
ENV ROS1_DISTRO=noetic
# Tue, 25 Oct 2022 21:37:06 GMT
ENV ROS2_DISTRO=foxy
# Tue, 25 Oct 2022 21:38:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:38:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:38:38 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf249399bc0440c14b3771796a8a9749b00b8b1f768beabb4bf65173978661`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a95e1d715258f8932e6718ed06a1eb17a823b5bb14f27e1ca7cead6b3cdb64a`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1125e614642ae08f414585e39268e20619496243391fc14223c48efb76567fe`  
		Last Modified: Tue, 25 Oct 2022 22:06:20 GMT  
		Size: 104.5 MB (104549412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3257e5f004cfece29d48f51619b6b61a55c530aa1ecbc38e1be4208caa2ae368`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414db4c36b110ea6ec637828a4983215f3c8120f5113c6b8a1b1e7b63d490652`  
		Last Modified: Tue, 25 Oct 2022 22:06:39 GMT  
		Size: 67.7 MB (67673997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29c8a2e8faff52e903b8c6eb0d283754c1de2db5a4f0fa1c50542d8ed3bf757`  
		Last Modified: Tue, 25 Oct 2022 22:06:31 GMT  
		Size: 269.4 KB (269368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650fa392d56bb2a49e8e5ceaea16096752cb2cddfae87d9cf1a6193b59b1da7a`  
		Last Modified: Tue, 25 Oct 2022 22:06:30 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cee9901e31fd356db4bc05acd8610220bec8ba0ced72c5658083ba9b7e4d51`  
		Last Modified: Tue, 25 Oct 2022 22:06:34 GMT  
		Size: 20.4 MB (20372962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf5433e7c9e061f27cf48f334ed9ad7cc4a5ae501c1b108833008725972b866`  
		Last Modified: Tue, 25 Oct 2022 22:06:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb74af6d3b5c37adef97f1fd6e95e116863e798184de223195cd2bed8dcbeba2`  
		Last Modified: Tue, 25 Oct 2022 22:06:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f420526906050934cc358b07ad0fc7eb75f00fb532e634a89120c99fa12c4b`  
		Last Modified: Tue, 25 Oct 2022 22:07:09 GMT  
		Size: 76.5 MB (76498135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e83da535cea3510c390e46cacfb76f7c2e44b10a2a3f2a9cdeb3588df562d1`  
		Last Modified: Tue, 25 Oct 2022 22:06:56 GMT  
		Size: 14.3 MB (14323630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82106a27fefc9b7d0614542f8d3d1ca6771cf9006d3fb2a6d280abc49a689f17`  
		Last Modified: Tue, 25 Oct 2022 22:06:52 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic`

```console
$ docker pull ros@sha256:a97603c10c099c7ea5df2f160c27bc91152964daae0e620157c6afc5a283830c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic` - linux; amd64

```console
$ docker pull ros@sha256:569696e5621fad056b14672265a27fb12507999bba8a6d8dcf332d16e6a2dad1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234891739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da8c152231c267d0724f107b91d186a7da80f21ae25d40984d9b4ce79d3985f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:29:48 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 07:30:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:30:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:30:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:30:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:31:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:31:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:31:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:31:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c34379670d69cf7211d3babcb41e5d7851c837e47be70bf7e93d4c243031e3`  
		Last Modified: Tue, 25 Oct 2022 08:00:51 GMT  
		Size: 103.9 MB (103894975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4200c5a3f7cd026b35c4c14ddd08ce81b9a8286688a9d195b89dd005dac72263`  
		Last Modified: Tue, 25 Oct 2022 08:00:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e7f5b5c701916838562eb61ea9d238d42ecdcf4603217d5f36de002d875373`  
		Last Modified: Tue, 25 Oct 2022 08:01:15 GMT  
		Size: 73.3 MB (73280543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066dfb5edf358837c3acdfe4765a62b10a0588d5ee88a202f18c6decb245a6c4`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 279.6 KB (279618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81213e1334be0f25c6545b79677786f9e06c1aaea8a510b21195f4dc08b6ecac`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c4d1072c5bb0b70378dd5a649ff6468e2763e77a087f95fa4e934dfa18632e`  
		Last Modified: Tue, 25 Oct 2022 08:01:06 GMT  
		Size: 22.1 MB (22138749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:25bf046ff522cf774f874b6261fc95bc68c878db7d76f30646ecf896643d5739
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.6 MB (223597053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a74627c6271f818124d2fb9c79689c1b0fee39c740f2a0a6559bddf5791274e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:33:04 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:33:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:38:42 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 21:39:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:39:18 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:39:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:39:18 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:39:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:39:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:39:42 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:39:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf249399bc0440c14b3771796a8a9749b00b8b1f768beabb4bf65173978661`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a95e1d715258f8932e6718ed06a1eb17a823b5bb14f27e1ca7cead6b3cdb64a`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17eb1844923f36e5d0264c722bf583eee704a021a2a142476d6eca76b79c5df`  
		Last Modified: Tue, 25 Oct 2022 22:07:38 GMT  
		Size: 100.3 MB (100323992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943ba2f0772bc1a1a3faed0480a753c5b8806b0e6bd948fd32b6a7b378dea751`  
		Last Modified: Tue, 25 Oct 2022 22:07:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb15d0de8d57e94728781ae793ebb9c47da6af6d21a8a38c4506decc8066b63`  
		Last Modified: Tue, 25 Oct 2022 22:07:56 GMT  
		Size: 67.6 MB (67619873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e7674f0c0caa8655a1368b99f006f9efd6c9309ac5fb7eb7aa609b2b0e9ceb`  
		Last Modified: Tue, 25 Oct 2022 22:07:47 GMT  
		Size: 279.6 KB (279608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f136bdb9a4de4a69c2fd48d4558581abb495390dbb234332d4e4feecccbc78`  
		Last Modified: Tue, 25 Oct 2022 22:07:47 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5041645cebe7017ddeab3344686c7feca135348dedf51a23c6c4595ba1d2e826`  
		Last Modified: Tue, 25 Oct 2022 22:07:51 GMT  
		Size: 21.5 MB (21475535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-base`

```console
$ docker pull ros@sha256:a97603c10c099c7ea5df2f160c27bc91152964daae0e620157c6afc5a283830c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:569696e5621fad056b14672265a27fb12507999bba8a6d8dcf332d16e6a2dad1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234891739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da8c152231c267d0724f107b91d186a7da80f21ae25d40984d9b4ce79d3985f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:29:48 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 07:30:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:30:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:30:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:30:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:31:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:31:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:31:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:31:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c34379670d69cf7211d3babcb41e5d7851c837e47be70bf7e93d4c243031e3`  
		Last Modified: Tue, 25 Oct 2022 08:00:51 GMT  
		Size: 103.9 MB (103894975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4200c5a3f7cd026b35c4c14ddd08ce81b9a8286688a9d195b89dd005dac72263`  
		Last Modified: Tue, 25 Oct 2022 08:00:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e7f5b5c701916838562eb61ea9d238d42ecdcf4603217d5f36de002d875373`  
		Last Modified: Tue, 25 Oct 2022 08:01:15 GMT  
		Size: 73.3 MB (73280543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066dfb5edf358837c3acdfe4765a62b10a0588d5ee88a202f18c6decb245a6c4`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 279.6 KB (279618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81213e1334be0f25c6545b79677786f9e06c1aaea8a510b21195f4dc08b6ecac`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c4d1072c5bb0b70378dd5a649ff6468e2763e77a087f95fa4e934dfa18632e`  
		Last Modified: Tue, 25 Oct 2022 08:01:06 GMT  
		Size: 22.1 MB (22138749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:25bf046ff522cf774f874b6261fc95bc68c878db7d76f30646ecf896643d5739
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.6 MB (223597053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a74627c6271f818124d2fb9c79689c1b0fee39c740f2a0a6559bddf5791274e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:33:04 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:33:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:38:42 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 21:39:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:39:18 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:39:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:39:18 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:39:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:39:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:39:42 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:39:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf249399bc0440c14b3771796a8a9749b00b8b1f768beabb4bf65173978661`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a95e1d715258f8932e6718ed06a1eb17a823b5bb14f27e1ca7cead6b3cdb64a`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17eb1844923f36e5d0264c722bf583eee704a021a2a142476d6eca76b79c5df`  
		Last Modified: Tue, 25 Oct 2022 22:07:38 GMT  
		Size: 100.3 MB (100323992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943ba2f0772bc1a1a3faed0480a753c5b8806b0e6bd948fd32b6a7b378dea751`  
		Last Modified: Tue, 25 Oct 2022 22:07:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb15d0de8d57e94728781ae793ebb9c47da6af6d21a8a38c4506decc8066b63`  
		Last Modified: Tue, 25 Oct 2022 22:07:56 GMT  
		Size: 67.6 MB (67619873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e7674f0c0caa8655a1368b99f006f9efd6c9309ac5fb7eb7aa609b2b0e9ceb`  
		Last Modified: Tue, 25 Oct 2022 22:07:47 GMT  
		Size: 279.6 KB (279608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f136bdb9a4de4a69c2fd48d4558581abb495390dbb234332d4e4feecccbc78`  
		Last Modified: Tue, 25 Oct 2022 22:07:47 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5041645cebe7017ddeab3344686c7feca135348dedf51a23c6c4595ba1d2e826`  
		Last Modified: Tue, 25 Oct 2022 22:07:51 GMT  
		Size: 21.5 MB (21475535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-base-focal`

```console
$ docker pull ros@sha256:a97603c10c099c7ea5df2f160c27bc91152964daae0e620157c6afc5a283830c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:569696e5621fad056b14672265a27fb12507999bba8a6d8dcf332d16e6a2dad1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234891739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da8c152231c267d0724f107b91d186a7da80f21ae25d40984d9b4ce79d3985f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:29:48 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 07:30:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:30:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:30:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:30:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:31:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:31:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:31:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:31:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c34379670d69cf7211d3babcb41e5d7851c837e47be70bf7e93d4c243031e3`  
		Last Modified: Tue, 25 Oct 2022 08:00:51 GMT  
		Size: 103.9 MB (103894975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4200c5a3f7cd026b35c4c14ddd08ce81b9a8286688a9d195b89dd005dac72263`  
		Last Modified: Tue, 25 Oct 2022 08:00:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e7f5b5c701916838562eb61ea9d238d42ecdcf4603217d5f36de002d875373`  
		Last Modified: Tue, 25 Oct 2022 08:01:15 GMT  
		Size: 73.3 MB (73280543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066dfb5edf358837c3acdfe4765a62b10a0588d5ee88a202f18c6decb245a6c4`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 279.6 KB (279618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81213e1334be0f25c6545b79677786f9e06c1aaea8a510b21195f4dc08b6ecac`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c4d1072c5bb0b70378dd5a649ff6468e2763e77a087f95fa4e934dfa18632e`  
		Last Modified: Tue, 25 Oct 2022 08:01:06 GMT  
		Size: 22.1 MB (22138749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:25bf046ff522cf774f874b6261fc95bc68c878db7d76f30646ecf896643d5739
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.6 MB (223597053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a74627c6271f818124d2fb9c79689c1b0fee39c740f2a0a6559bddf5791274e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:33:04 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:33:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:38:42 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 21:39:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:39:18 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:39:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:39:18 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:39:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:39:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:39:42 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:39:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf249399bc0440c14b3771796a8a9749b00b8b1f768beabb4bf65173978661`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a95e1d715258f8932e6718ed06a1eb17a823b5bb14f27e1ca7cead6b3cdb64a`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17eb1844923f36e5d0264c722bf583eee704a021a2a142476d6eca76b79c5df`  
		Last Modified: Tue, 25 Oct 2022 22:07:38 GMT  
		Size: 100.3 MB (100323992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943ba2f0772bc1a1a3faed0480a753c5b8806b0e6bd948fd32b6a7b378dea751`  
		Last Modified: Tue, 25 Oct 2022 22:07:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb15d0de8d57e94728781ae793ebb9c47da6af6d21a8a38c4506decc8066b63`  
		Last Modified: Tue, 25 Oct 2022 22:07:56 GMT  
		Size: 67.6 MB (67619873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e7674f0c0caa8655a1368b99f006f9efd6c9309ac5fb7eb7aa609b2b0e9ceb`  
		Last Modified: Tue, 25 Oct 2022 22:07:47 GMT  
		Size: 279.6 KB (279608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f136bdb9a4de4a69c2fd48d4558581abb495390dbb234332d4e4feecccbc78`  
		Last Modified: Tue, 25 Oct 2022 22:07:47 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5041645cebe7017ddeab3344686c7feca135348dedf51a23c6c4595ba1d2e826`  
		Last Modified: Tue, 25 Oct 2022 22:07:51 GMT  
		Size: 21.5 MB (21475535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-core`

```console
$ docker pull ros@sha256:5fb1cbfdc5deeaea48407ba875002bf1cd93c858d911c9f7572e9808eb064eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:92e1833b32530d7a5e8f72ebb1d0bffa7c492fc1d1ba6137b107f8df2c94f264
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139190409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9c7553e926bb17363c98f4a1766d20d7e6c10c4b439a1b3746eb1010493a86`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:29:48 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 07:30:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:30:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:30:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:30:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c34379670d69cf7211d3babcb41e5d7851c837e47be70bf7e93d4c243031e3`  
		Last Modified: Tue, 25 Oct 2022 08:00:51 GMT  
		Size: 103.9 MB (103894975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4200c5a3f7cd026b35c4c14ddd08ce81b9a8286688a9d195b89dd005dac72263`  
		Last Modified: Tue, 25 Oct 2022 08:00:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4d315d3003b7dfae479bc9208a5291cc9dae3cb455776c6fa52b0292dcaca2e4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134219606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f40c6313db5ac3b043e637e86bfae908df34d52dcd7c520ebf9c975de69eaf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:33:04 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:33:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:38:42 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 21:39:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:39:18 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:39:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:39:18 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf249399bc0440c14b3771796a8a9749b00b8b1f768beabb4bf65173978661`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a95e1d715258f8932e6718ed06a1eb17a823b5bb14f27e1ca7cead6b3cdb64a`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17eb1844923f36e5d0264c722bf583eee704a021a2a142476d6eca76b79c5df`  
		Last Modified: Tue, 25 Oct 2022 22:07:38 GMT  
		Size: 100.3 MB (100323992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943ba2f0772bc1a1a3faed0480a753c5b8806b0e6bd948fd32b6a7b378dea751`  
		Last Modified: Tue, 25 Oct 2022 22:07:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-core-focal`

```console
$ docker pull ros@sha256:5fb1cbfdc5deeaea48407ba875002bf1cd93c858d911c9f7572e9808eb064eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:92e1833b32530d7a5e8f72ebb1d0bffa7c492fc1d1ba6137b107f8df2c94f264
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139190409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9c7553e926bb17363c98f4a1766d20d7e6c10c4b439a1b3746eb1010493a86`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:29:48 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 07:30:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:30:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:30:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:30:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c34379670d69cf7211d3babcb41e5d7851c837e47be70bf7e93d4c243031e3`  
		Last Modified: Tue, 25 Oct 2022 08:00:51 GMT  
		Size: 103.9 MB (103894975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4200c5a3f7cd026b35c4c14ddd08ce81b9a8286688a9d195b89dd005dac72263`  
		Last Modified: Tue, 25 Oct 2022 08:00:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4d315d3003b7dfae479bc9208a5291cc9dae3cb455776c6fa52b0292dcaca2e4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134219606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f40c6313db5ac3b043e637e86bfae908df34d52dcd7c520ebf9c975de69eaf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:33:04 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:33:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:38:42 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 21:39:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:39:18 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:39:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:39:18 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf249399bc0440c14b3771796a8a9749b00b8b1f768beabb4bf65173978661`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a95e1d715258f8932e6718ed06a1eb17a823b5bb14f27e1ca7cead6b3cdb64a`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17eb1844923f36e5d0264c722bf583eee704a021a2a142476d6eca76b79c5df`  
		Last Modified: Tue, 25 Oct 2022 22:07:38 GMT  
		Size: 100.3 MB (100323992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943ba2f0772bc1a1a3faed0480a753c5b8806b0e6bd948fd32b6a7b378dea751`  
		Last Modified: Tue, 25 Oct 2022 22:07:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros1-bridge`

```console
$ docker pull ros@sha256:fc8d535d5a3f537e62d0ac96c3dc7bbc098544a8e4ee13c3d8a3dc1bb8448cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:fb1588e66a4a6f00f08cfc6630778c7832183cb9e9fd45b0acb7abe3a3f4bf34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.1 MB (330065345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1103face6f7a2af3d3e3c726f3bd94530f4969844ce30db1218e7c14fcfbbb9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:29:48 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 07:30:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:30:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:30:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:30:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:31:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:31:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:31:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:31:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:31:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:31:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:31:37 GMT
ENV ROS1_DISTRO=noetic
# Tue, 25 Oct 2022 07:31:37 GMT
ENV ROS2_DISTRO=galactic
# Tue, 25 Oct 2022 07:32:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:16 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c34379670d69cf7211d3babcb41e5d7851c837e47be70bf7e93d4c243031e3`  
		Last Modified: Tue, 25 Oct 2022 08:00:51 GMT  
		Size: 103.9 MB (103894975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4200c5a3f7cd026b35c4c14ddd08ce81b9a8286688a9d195b89dd005dac72263`  
		Last Modified: Tue, 25 Oct 2022 08:00:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e7f5b5c701916838562eb61ea9d238d42ecdcf4603217d5f36de002d875373`  
		Last Modified: Tue, 25 Oct 2022 08:01:15 GMT  
		Size: 73.3 MB (73280543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066dfb5edf358837c3acdfe4765a62b10a0588d5ee88a202f18c6decb245a6c4`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 279.6 KB (279618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81213e1334be0f25c6545b79677786f9e06c1aaea8a510b21195f4dc08b6ecac`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c4d1072c5bb0b70378dd5a649ff6468e2763e77a087f95fa4e934dfa18632e`  
		Last Modified: Tue, 25 Oct 2022 08:01:06 GMT  
		Size: 22.1 MB (22138749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f8c44f31c8de7186a01b87fd4516c3397f99b9cd341f36f8cd884940d852be`  
		Last Modified: Tue, 25 Oct 2022 08:01:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08eb43ea9a6ec61bf6c97f1d126b6a349c84449712c18182f9bc67d4229193fe`  
		Last Modified: Tue, 25 Oct 2022 08:01:28 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958d3e0b946c5d65a557f59ae5c08267cf58ab8bc2c3cd5532b048ae84be8c57`  
		Last Modified: Tue, 25 Oct 2022 08:01:52 GMT  
		Size: 78.7 MB (78708239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65688e59ce9e0915a5cf388ddd2bd68f8a2ff7aaddfa7a370e04170897984fb`  
		Last Modified: Tue, 25 Oct 2022 08:01:34 GMT  
		Size: 16.5 MB (16464739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86260963e5bdc8000fea22d746d7a7c68579e6bed5f3c76edb7a319a68e5aae`  
		Last Modified: Tue, 25 Oct 2022 08:01:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:136867129b348b9ec08c706aa4705f734dd30b83f456847c0b548c6d6676bf26
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318258712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0422b9f009f34723daed7887d2deed414853709402a9d3a2f3cd23ccc15f4852`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:33:04 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:33:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:38:42 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 21:39:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:39:18 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:39:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:39:18 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:39:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:39:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:39:42 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:39:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:39:56 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 21:39:57 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:39:58 GMT
ENV ROS1_DISTRO=noetic
# Tue, 25 Oct 2022 21:39:58 GMT
ENV ROS2_DISTRO=galactic
# Tue, 25 Oct 2022 21:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:40:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:40:27 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf249399bc0440c14b3771796a8a9749b00b8b1f768beabb4bf65173978661`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a95e1d715258f8932e6718ed06a1eb17a823b5bb14f27e1ca7cead6b3cdb64a`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17eb1844923f36e5d0264c722bf583eee704a021a2a142476d6eca76b79c5df`  
		Last Modified: Tue, 25 Oct 2022 22:07:38 GMT  
		Size: 100.3 MB (100323992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943ba2f0772bc1a1a3faed0480a753c5b8806b0e6bd948fd32b6a7b378dea751`  
		Last Modified: Tue, 25 Oct 2022 22:07:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb15d0de8d57e94728781ae793ebb9c47da6af6d21a8a38c4506decc8066b63`  
		Last Modified: Tue, 25 Oct 2022 22:07:56 GMT  
		Size: 67.6 MB (67619873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e7674f0c0caa8655a1368b99f006f9efd6c9309ac5fb7eb7aa609b2b0e9ceb`  
		Last Modified: Tue, 25 Oct 2022 22:07:47 GMT  
		Size: 279.6 KB (279608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f136bdb9a4de4a69c2fd48d4558581abb495390dbb234332d4e4feecccbc78`  
		Last Modified: Tue, 25 Oct 2022 22:07:47 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5041645cebe7017ddeab3344686c7feca135348dedf51a23c6c4595ba1d2e826`  
		Last Modified: Tue, 25 Oct 2022 22:07:51 GMT  
		Size: 21.5 MB (21475535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e7a424e7ef0057fa34db63d0489365de499500ef3615cbd982ee78c0b4e674`  
		Last Modified: Tue, 25 Oct 2022 22:08:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f618329feb5073887e7596cff8d8ad3752efb4da04ddb54e58b0b42f535cda`  
		Last Modified: Tue, 25 Oct 2022 22:08:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d91e78ebff825fe8eb15f5361c4d83e75f0d88cb7e0975e4abbee79e5207c62`  
		Last Modified: Tue, 25 Oct 2022 22:08:26 GMT  
		Size: 78.7 MB (78674318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426775b2e38908cbea672ba093ff3be1b9856e7eba27eb415ca1132e0839238`  
		Last Modified: Tue, 25 Oct 2022 22:08:12 GMT  
		Size: 16.0 MB (15986715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfa625e83a588d3f3b2bc6c4cbdf8f9e30a8af255a45ba262d8e8c83c8f3878`  
		Last Modified: Tue, 25 Oct 2022 22:08:09 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros1-bridge-focal`

```console
$ docker pull ros@sha256:fc8d535d5a3f537e62d0ac96c3dc7bbc098544a8e4ee13c3d8a3dc1bb8448cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:fb1588e66a4a6f00f08cfc6630778c7832183cb9e9fd45b0acb7abe3a3f4bf34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.1 MB (330065345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1103face6f7a2af3d3e3c726f3bd94530f4969844ce30db1218e7c14fcfbbb9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:29:48 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 07:30:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:30:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:30:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:30:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:31:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:31:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:31:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:31:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:31:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:31:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:31:37 GMT
ENV ROS1_DISTRO=noetic
# Tue, 25 Oct 2022 07:31:37 GMT
ENV ROS2_DISTRO=galactic
# Tue, 25 Oct 2022 07:32:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:16 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c34379670d69cf7211d3babcb41e5d7851c837e47be70bf7e93d4c243031e3`  
		Last Modified: Tue, 25 Oct 2022 08:00:51 GMT  
		Size: 103.9 MB (103894975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4200c5a3f7cd026b35c4c14ddd08ce81b9a8286688a9d195b89dd005dac72263`  
		Last Modified: Tue, 25 Oct 2022 08:00:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e7f5b5c701916838562eb61ea9d238d42ecdcf4603217d5f36de002d875373`  
		Last Modified: Tue, 25 Oct 2022 08:01:15 GMT  
		Size: 73.3 MB (73280543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066dfb5edf358837c3acdfe4765a62b10a0588d5ee88a202f18c6decb245a6c4`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 279.6 KB (279618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81213e1334be0f25c6545b79677786f9e06c1aaea8a510b21195f4dc08b6ecac`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c4d1072c5bb0b70378dd5a649ff6468e2763e77a087f95fa4e934dfa18632e`  
		Last Modified: Tue, 25 Oct 2022 08:01:06 GMT  
		Size: 22.1 MB (22138749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f8c44f31c8de7186a01b87fd4516c3397f99b9cd341f36f8cd884940d852be`  
		Last Modified: Tue, 25 Oct 2022 08:01:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08eb43ea9a6ec61bf6c97f1d126b6a349c84449712c18182f9bc67d4229193fe`  
		Last Modified: Tue, 25 Oct 2022 08:01:28 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958d3e0b946c5d65a557f59ae5c08267cf58ab8bc2c3cd5532b048ae84be8c57`  
		Last Modified: Tue, 25 Oct 2022 08:01:52 GMT  
		Size: 78.7 MB (78708239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65688e59ce9e0915a5cf388ddd2bd68f8a2ff7aaddfa7a370e04170897984fb`  
		Last Modified: Tue, 25 Oct 2022 08:01:34 GMT  
		Size: 16.5 MB (16464739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86260963e5bdc8000fea22d746d7a7c68579e6bed5f3c76edb7a319a68e5aae`  
		Last Modified: Tue, 25 Oct 2022 08:01:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:136867129b348b9ec08c706aa4705f734dd30b83f456847c0b548c6d6676bf26
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318258712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0422b9f009f34723daed7887d2deed414853709402a9d3a2f3cd23ccc15f4852`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:33:04 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:33:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:33:06 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:38:42 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 21:39:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:39:18 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:39:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:39:18 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:39:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:39:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:39:42 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:39:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:39:56 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 21:39:57 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:39:58 GMT
ENV ROS1_DISTRO=noetic
# Tue, 25 Oct 2022 21:39:58 GMT
ENV ROS2_DISTRO=galactic
# Tue, 25 Oct 2022 21:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:40:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:40:27 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bf249399bc0440c14b3771796a8a9749b00b8b1f768beabb4bf65173978661`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a95e1d715258f8932e6718ed06a1eb17a823b5bb14f27e1ca7cead6b3cdb64a`  
		Last Modified: Tue, 25 Oct 2022 22:06:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17eb1844923f36e5d0264c722bf583eee704a021a2a142476d6eca76b79c5df`  
		Last Modified: Tue, 25 Oct 2022 22:07:38 GMT  
		Size: 100.3 MB (100323992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943ba2f0772bc1a1a3faed0480a753c5b8806b0e6bd948fd32b6a7b378dea751`  
		Last Modified: Tue, 25 Oct 2022 22:07:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb15d0de8d57e94728781ae793ebb9c47da6af6d21a8a38c4506decc8066b63`  
		Last Modified: Tue, 25 Oct 2022 22:07:56 GMT  
		Size: 67.6 MB (67619873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e7674f0c0caa8655a1368b99f006f9efd6c9309ac5fb7eb7aa609b2b0e9ceb`  
		Last Modified: Tue, 25 Oct 2022 22:07:47 GMT  
		Size: 279.6 KB (279608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f136bdb9a4de4a69c2fd48d4558581abb495390dbb234332d4e4feecccbc78`  
		Last Modified: Tue, 25 Oct 2022 22:07:47 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5041645cebe7017ddeab3344686c7feca135348dedf51a23c6c4595ba1d2e826`  
		Last Modified: Tue, 25 Oct 2022 22:07:51 GMT  
		Size: 21.5 MB (21475535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e7a424e7ef0057fa34db63d0489365de499500ef3615cbd982ee78c0b4e674`  
		Last Modified: Tue, 25 Oct 2022 22:08:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f618329feb5073887e7596cff8d8ad3752efb4da04ddb54e58b0b42f535cda`  
		Last Modified: Tue, 25 Oct 2022 22:08:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d91e78ebff825fe8eb15f5361c4d83e75f0d88cb7e0975e4abbee79e5207c62`  
		Last Modified: Tue, 25 Oct 2022 22:08:26 GMT  
		Size: 78.7 MB (78674318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7426775b2e38908cbea672ba093ff3be1b9856e7eba27eb415ca1132e0839238`  
		Last Modified: Tue, 25 Oct 2022 22:08:12 GMT  
		Size: 16.0 MB (15986715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfa625e83a588d3f3b2bc6c4cbdf8f9e30a8af255a45ba262d8e8c83c8f3878`  
		Last Modified: Tue, 25 Oct 2022 22:08:09 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble`

```console
$ docker pull ros@sha256:50bcdf7a659f810c5a353ed3da0b1ce32b6d9d8f07422de32034518aefea9863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:0a802223f0f42ce6c021e103c88cebb39d34b33e6f27b6c5eeb664a4384581ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262845111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f340563a38bb44aee9bda8c1ce81c0eb80dde4b3d82200d63cafbf34e511942`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 07:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:34:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:34:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:34:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:35:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:35:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:35:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be1f7ccd647190e134f58b7bdaddc42b6477dff97e50567b748bc31b6303f00`  
		Last Modified: Tue, 25 Oct 2022 08:02:27 GMT  
		Size: 106.2 MB (106227052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd97e132a97f3e5517dacc0f9b6598427f1966b8505acab43d41575f53d2ee8`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd54d8e71568daecc9e521d17654239410a7a8d6895fb3167bb3e4b8735f5e5`  
		Last Modified: Tue, 25 Oct 2022 08:02:52 GMT  
		Size: 97.9 MB (97878471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d389ad8893cc3f537cfc3608c72ea4279d8ef1edc81ecdf82f4dbbdf4b8b604`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 295.6 KB (295633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d846403b95a3d13902aed833ac91f24ab2628f08871623f59fc2ef029c73ab2c`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710da595552b7d9324d2e432bcf0437dc8b7f054bf7ae402a6f33c2d5cbc281c`  
		Last Modified: Tue, 25 Oct 2022 08:02:42 GMT  
		Size: 23.0 MB (23008535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e6d1e6c4518e267f9642f3097c08f57026bb5b23a07518200df6e3aecab64c00
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255538972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63521c990d674cda3c67249e6cfdcec14a99b82c74773fb5d1db4f07f726ab5c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:02 GMT
ADD file:515177312f20fb1814b89bfccfe695fa2354bbb6d43fdb6e018bf5b1acc17e9f in / 
# Tue, 25 Oct 2022 05:55:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:40:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:41:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 21:43:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:43:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:43:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:43:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:44:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:44:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:44:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:45:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56a2caa6b2c66e01954c1a013b37ea359b6e6af8989dbfb958124b6318771af4`  
		Last Modified: Tue, 25 Oct 2022 05:56:14 GMT  
		Size: 28.4 MB (28382489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191d2d5931f4547389f96db79cb360ca3fdcf9f2d51c390b6958348a8a67c347`  
		Last Modified: Tue, 25 Oct 2022 22:08:40 GMT  
		Size: 1.2 MB (1176430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c085abd75940b2d68ae65386a432f481580f2ba06963b1e8c435bf4a06943d1`  
		Last Modified: Tue, 25 Oct 2022 22:08:38 GMT  
		Size: 3.8 MB (3799950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efa6f1ee27186437a210a19aa7cac0243bca4bf8e278464256de1a6c727019e`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ca2e27b815a4a40cfebb2d3e9e35f746c5458629933fdb650f2fe0af8725c7`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f958027197f946bc5c344b5c6d11ee5563140eba9b62b50ebd81ff37e58c0cc2`  
		Last Modified: Tue, 25 Oct 2022 22:08:54 GMT  
		Size: 104.0 MB (103976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a1b379b05f9273bfb87896fa46bf209006cfc9e82c69f9a47067ca2d74aa5`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3b15e7b12a9239bb2946201d3c6989b08423aa83930600af3b36a69b572e5e`  
		Last Modified: Tue, 25 Oct 2022 22:09:16 GMT  
		Size: 95.5 MB (95469663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b453065d137014d9afd7b61bab790935a460401456f9bdcebf6dd134f5d37fc`  
		Last Modified: Tue, 25 Oct 2022 22:09:05 GMT  
		Size: 295.6 KB (295639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2316db5066b2f905bf3ef20d6f817416f350af05c67a3c8d3273d52234b41e4`  
		Last Modified: Tue, 25 Oct 2022 22:09:04 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c024b89761df7b88cd9ede63829964f10f26f025bc3e49c423b1ab95263630`  
		Last Modified: Tue, 25 Oct 2022 22:09:08 GMT  
		Size: 22.4 MB (22433878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception`

```console
$ docker pull ros@sha256:9d11f78a0119cc370a9a1724a2d7de4cc839f4c89ad4fbf3288586e7453d9bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:76645b46dcf6ffbf3fdac6944597995377c4640b15b343bdb7f223d323b81e1f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1087032972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ae91661e2cf574b08b75a61ebef5b0786b5a33c59bdab811b81be7e84e98dd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 07:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:34:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:34:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:34:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:35:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:35:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:35:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:44:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be1f7ccd647190e134f58b7bdaddc42b6477dff97e50567b748bc31b6303f00`  
		Last Modified: Tue, 25 Oct 2022 08:02:27 GMT  
		Size: 106.2 MB (106227052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd97e132a97f3e5517dacc0f9b6598427f1966b8505acab43d41575f53d2ee8`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd54d8e71568daecc9e521d17654239410a7a8d6895fb3167bb3e4b8735f5e5`  
		Last Modified: Tue, 25 Oct 2022 08:02:52 GMT  
		Size: 97.9 MB (97878471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d389ad8893cc3f537cfc3608c72ea4279d8ef1edc81ecdf82f4dbbdf4b8b604`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 295.6 KB (295633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d846403b95a3d13902aed833ac91f24ab2628f08871623f59fc2ef029c73ab2c`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710da595552b7d9324d2e432bcf0437dc8b7f054bf7ae402a6f33c2d5cbc281c`  
		Last Modified: Tue, 25 Oct 2022 08:02:42 GMT  
		Size: 23.0 MB (23008535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811c764114f804d6bc0acc7e66e888ceacf4c5537574a5de8c4d40fb90c9999e`  
		Last Modified: Tue, 25 Oct 2022 08:05:05 GMT  
		Size: 824.2 MB (824187861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:33336c67f4960ddc723f9d7c5453bbba8c9535d10b8d3f2987521aac0101975b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1037303866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a26ac2a442618ec3387a5b4c1c9092b36cb6bad4eb71a1103f9e102d0fb5e45`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:02 GMT
ADD file:515177312f20fb1814b89bfccfe695fa2354bbb6d43fdb6e018bf5b1acc17e9f in / 
# Tue, 25 Oct 2022 05:55:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:40:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:41:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 21:43:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:43:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:43:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:43:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:44:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:44:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:44:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:45:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:54:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56a2caa6b2c66e01954c1a013b37ea359b6e6af8989dbfb958124b6318771af4`  
		Last Modified: Tue, 25 Oct 2022 05:56:14 GMT  
		Size: 28.4 MB (28382489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191d2d5931f4547389f96db79cb360ca3fdcf9f2d51c390b6958348a8a67c347`  
		Last Modified: Tue, 25 Oct 2022 22:08:40 GMT  
		Size: 1.2 MB (1176430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c085abd75940b2d68ae65386a432f481580f2ba06963b1e8c435bf4a06943d1`  
		Last Modified: Tue, 25 Oct 2022 22:08:38 GMT  
		Size: 3.8 MB (3799950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efa6f1ee27186437a210a19aa7cac0243bca4bf8e278464256de1a6c727019e`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ca2e27b815a4a40cfebb2d3e9e35f746c5458629933fdb650f2fe0af8725c7`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f958027197f946bc5c344b5c6d11ee5563140eba9b62b50ebd81ff37e58c0cc2`  
		Last Modified: Tue, 25 Oct 2022 22:08:54 GMT  
		Size: 104.0 MB (103976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a1b379b05f9273bfb87896fa46bf209006cfc9e82c69f9a47067ca2d74aa5`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3b15e7b12a9239bb2946201d3c6989b08423aa83930600af3b36a69b572e5e`  
		Last Modified: Tue, 25 Oct 2022 22:09:16 GMT  
		Size: 95.5 MB (95469663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b453065d137014d9afd7b61bab790935a460401456f9bdcebf6dd134f5d37fc`  
		Last Modified: Tue, 25 Oct 2022 22:09:05 GMT  
		Size: 295.6 KB (295639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2316db5066b2f905bf3ef20d6f817416f350af05c67a3c8d3273d52234b41e4`  
		Last Modified: Tue, 25 Oct 2022 22:09:04 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c024b89761df7b88cd9ede63829964f10f26f025bc3e49c423b1ab95263630`  
		Last Modified: Tue, 25 Oct 2022 22:09:08 GMT  
		Size: 22.4 MB (22433878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11dc0a7c12dae10992fe0253de16a84802e3bed92af6c8edf1a9f82af29ad774`  
		Last Modified: Tue, 25 Oct 2022 22:10:54 GMT  
		Size: 781.8 MB (781764894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:9d11f78a0119cc370a9a1724a2d7de4cc839f4c89ad4fbf3288586e7453d9bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:76645b46dcf6ffbf3fdac6944597995377c4640b15b343bdb7f223d323b81e1f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1087032972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ae91661e2cf574b08b75a61ebef5b0786b5a33c59bdab811b81be7e84e98dd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 07:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:34:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:34:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:34:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:35:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:35:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:35:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:44:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be1f7ccd647190e134f58b7bdaddc42b6477dff97e50567b748bc31b6303f00`  
		Last Modified: Tue, 25 Oct 2022 08:02:27 GMT  
		Size: 106.2 MB (106227052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd97e132a97f3e5517dacc0f9b6598427f1966b8505acab43d41575f53d2ee8`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd54d8e71568daecc9e521d17654239410a7a8d6895fb3167bb3e4b8735f5e5`  
		Last Modified: Tue, 25 Oct 2022 08:02:52 GMT  
		Size: 97.9 MB (97878471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d389ad8893cc3f537cfc3608c72ea4279d8ef1edc81ecdf82f4dbbdf4b8b604`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 295.6 KB (295633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d846403b95a3d13902aed833ac91f24ab2628f08871623f59fc2ef029c73ab2c`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710da595552b7d9324d2e432bcf0437dc8b7f054bf7ae402a6f33c2d5cbc281c`  
		Last Modified: Tue, 25 Oct 2022 08:02:42 GMT  
		Size: 23.0 MB (23008535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811c764114f804d6bc0acc7e66e888ceacf4c5537574a5de8c4d40fb90c9999e`  
		Last Modified: Tue, 25 Oct 2022 08:05:05 GMT  
		Size: 824.2 MB (824187861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:33336c67f4960ddc723f9d7c5453bbba8c9535d10b8d3f2987521aac0101975b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1037303866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a26ac2a442618ec3387a5b4c1c9092b36cb6bad4eb71a1103f9e102d0fb5e45`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:02 GMT
ADD file:515177312f20fb1814b89bfccfe695fa2354bbb6d43fdb6e018bf5b1acc17e9f in / 
# Tue, 25 Oct 2022 05:55:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:40:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:41:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 21:43:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:43:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:43:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:43:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:44:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:44:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:44:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:45:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:54:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56a2caa6b2c66e01954c1a013b37ea359b6e6af8989dbfb958124b6318771af4`  
		Last Modified: Tue, 25 Oct 2022 05:56:14 GMT  
		Size: 28.4 MB (28382489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191d2d5931f4547389f96db79cb360ca3fdcf9f2d51c390b6958348a8a67c347`  
		Last Modified: Tue, 25 Oct 2022 22:08:40 GMT  
		Size: 1.2 MB (1176430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c085abd75940b2d68ae65386a432f481580f2ba06963b1e8c435bf4a06943d1`  
		Last Modified: Tue, 25 Oct 2022 22:08:38 GMT  
		Size: 3.8 MB (3799950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efa6f1ee27186437a210a19aa7cac0243bca4bf8e278464256de1a6c727019e`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ca2e27b815a4a40cfebb2d3e9e35f746c5458629933fdb650f2fe0af8725c7`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f958027197f946bc5c344b5c6d11ee5563140eba9b62b50ebd81ff37e58c0cc2`  
		Last Modified: Tue, 25 Oct 2022 22:08:54 GMT  
		Size: 104.0 MB (103976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a1b379b05f9273bfb87896fa46bf209006cfc9e82c69f9a47067ca2d74aa5`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3b15e7b12a9239bb2946201d3c6989b08423aa83930600af3b36a69b572e5e`  
		Last Modified: Tue, 25 Oct 2022 22:09:16 GMT  
		Size: 95.5 MB (95469663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b453065d137014d9afd7b61bab790935a460401456f9bdcebf6dd134f5d37fc`  
		Last Modified: Tue, 25 Oct 2022 22:09:05 GMT  
		Size: 295.6 KB (295639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2316db5066b2f905bf3ef20d6f817416f350af05c67a3c8d3273d52234b41e4`  
		Last Modified: Tue, 25 Oct 2022 22:09:04 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c024b89761df7b88cd9ede63829964f10f26f025bc3e49c423b1ab95263630`  
		Last Modified: Tue, 25 Oct 2022 22:09:08 GMT  
		Size: 22.4 MB (22433878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11dc0a7c12dae10992fe0253de16a84802e3bed92af6c8edf1a9f82af29ad774`  
		Last Modified: Tue, 25 Oct 2022 22:10:54 GMT  
		Size: 781.8 MB (781764894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:50bcdf7a659f810c5a353ed3da0b1ce32b6d9d8f07422de32034518aefea9863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:0a802223f0f42ce6c021e103c88cebb39d34b33e6f27b6c5eeb664a4384581ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262845111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f340563a38bb44aee9bda8c1ce81c0eb80dde4b3d82200d63cafbf34e511942`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 07:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:34:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:34:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:34:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:35:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:35:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:35:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be1f7ccd647190e134f58b7bdaddc42b6477dff97e50567b748bc31b6303f00`  
		Last Modified: Tue, 25 Oct 2022 08:02:27 GMT  
		Size: 106.2 MB (106227052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd97e132a97f3e5517dacc0f9b6598427f1966b8505acab43d41575f53d2ee8`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd54d8e71568daecc9e521d17654239410a7a8d6895fb3167bb3e4b8735f5e5`  
		Last Modified: Tue, 25 Oct 2022 08:02:52 GMT  
		Size: 97.9 MB (97878471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d389ad8893cc3f537cfc3608c72ea4279d8ef1edc81ecdf82f4dbbdf4b8b604`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 295.6 KB (295633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d846403b95a3d13902aed833ac91f24ab2628f08871623f59fc2ef029c73ab2c`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710da595552b7d9324d2e432bcf0437dc8b7f054bf7ae402a6f33c2d5cbc281c`  
		Last Modified: Tue, 25 Oct 2022 08:02:42 GMT  
		Size: 23.0 MB (23008535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e6d1e6c4518e267f9642f3097c08f57026bb5b23a07518200df6e3aecab64c00
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255538972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63521c990d674cda3c67249e6cfdcec14a99b82c74773fb5d1db4f07f726ab5c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:02 GMT
ADD file:515177312f20fb1814b89bfccfe695fa2354bbb6d43fdb6e018bf5b1acc17e9f in / 
# Tue, 25 Oct 2022 05:55:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:40:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:41:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 21:43:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:43:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:43:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:43:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:44:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:44:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:44:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:45:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56a2caa6b2c66e01954c1a013b37ea359b6e6af8989dbfb958124b6318771af4`  
		Last Modified: Tue, 25 Oct 2022 05:56:14 GMT  
		Size: 28.4 MB (28382489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191d2d5931f4547389f96db79cb360ca3fdcf9f2d51c390b6958348a8a67c347`  
		Last Modified: Tue, 25 Oct 2022 22:08:40 GMT  
		Size: 1.2 MB (1176430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c085abd75940b2d68ae65386a432f481580f2ba06963b1e8c435bf4a06943d1`  
		Last Modified: Tue, 25 Oct 2022 22:08:38 GMT  
		Size: 3.8 MB (3799950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efa6f1ee27186437a210a19aa7cac0243bca4bf8e278464256de1a6c727019e`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ca2e27b815a4a40cfebb2d3e9e35f746c5458629933fdb650f2fe0af8725c7`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f958027197f946bc5c344b5c6d11ee5563140eba9b62b50ebd81ff37e58c0cc2`  
		Last Modified: Tue, 25 Oct 2022 22:08:54 GMT  
		Size: 104.0 MB (103976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a1b379b05f9273bfb87896fa46bf209006cfc9e82c69f9a47067ca2d74aa5`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3b15e7b12a9239bb2946201d3c6989b08423aa83930600af3b36a69b572e5e`  
		Last Modified: Tue, 25 Oct 2022 22:09:16 GMT  
		Size: 95.5 MB (95469663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b453065d137014d9afd7b61bab790935a460401456f9bdcebf6dd134f5d37fc`  
		Last Modified: Tue, 25 Oct 2022 22:09:05 GMT  
		Size: 295.6 KB (295639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2316db5066b2f905bf3ef20d6f817416f350af05c67a3c8d3273d52234b41e4`  
		Last Modified: Tue, 25 Oct 2022 22:09:04 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c024b89761df7b88cd9ede63829964f10f26f025bc3e49c423b1ab95263630`  
		Last Modified: Tue, 25 Oct 2022 22:09:08 GMT  
		Size: 22.4 MB (22433878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:50bcdf7a659f810c5a353ed3da0b1ce32b6d9d8f07422de32034518aefea9863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:0a802223f0f42ce6c021e103c88cebb39d34b33e6f27b6c5eeb664a4384581ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262845111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f340563a38bb44aee9bda8c1ce81c0eb80dde4b3d82200d63cafbf34e511942`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 07:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:34:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:34:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:34:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:35:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:35:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:35:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be1f7ccd647190e134f58b7bdaddc42b6477dff97e50567b748bc31b6303f00`  
		Last Modified: Tue, 25 Oct 2022 08:02:27 GMT  
		Size: 106.2 MB (106227052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd97e132a97f3e5517dacc0f9b6598427f1966b8505acab43d41575f53d2ee8`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd54d8e71568daecc9e521d17654239410a7a8d6895fb3167bb3e4b8735f5e5`  
		Last Modified: Tue, 25 Oct 2022 08:02:52 GMT  
		Size: 97.9 MB (97878471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d389ad8893cc3f537cfc3608c72ea4279d8ef1edc81ecdf82f4dbbdf4b8b604`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 295.6 KB (295633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d846403b95a3d13902aed833ac91f24ab2628f08871623f59fc2ef029c73ab2c`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710da595552b7d9324d2e432bcf0437dc8b7f054bf7ae402a6f33c2d5cbc281c`  
		Last Modified: Tue, 25 Oct 2022 08:02:42 GMT  
		Size: 23.0 MB (23008535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e6d1e6c4518e267f9642f3097c08f57026bb5b23a07518200df6e3aecab64c00
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255538972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63521c990d674cda3c67249e6cfdcec14a99b82c74773fb5d1db4f07f726ab5c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:02 GMT
ADD file:515177312f20fb1814b89bfccfe695fa2354bbb6d43fdb6e018bf5b1acc17e9f in / 
# Tue, 25 Oct 2022 05:55:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:40:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:41:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 21:43:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:43:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:43:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:43:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:44:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:44:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:44:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:45:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56a2caa6b2c66e01954c1a013b37ea359b6e6af8989dbfb958124b6318771af4`  
		Last Modified: Tue, 25 Oct 2022 05:56:14 GMT  
		Size: 28.4 MB (28382489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191d2d5931f4547389f96db79cb360ca3fdcf9f2d51c390b6958348a8a67c347`  
		Last Modified: Tue, 25 Oct 2022 22:08:40 GMT  
		Size: 1.2 MB (1176430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c085abd75940b2d68ae65386a432f481580f2ba06963b1e8c435bf4a06943d1`  
		Last Modified: Tue, 25 Oct 2022 22:08:38 GMT  
		Size: 3.8 MB (3799950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efa6f1ee27186437a210a19aa7cac0243bca4bf8e278464256de1a6c727019e`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ca2e27b815a4a40cfebb2d3e9e35f746c5458629933fdb650f2fe0af8725c7`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f958027197f946bc5c344b5c6d11ee5563140eba9b62b50ebd81ff37e58c0cc2`  
		Last Modified: Tue, 25 Oct 2022 22:08:54 GMT  
		Size: 104.0 MB (103976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a1b379b05f9273bfb87896fa46bf209006cfc9e82c69f9a47067ca2d74aa5`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3b15e7b12a9239bb2946201d3c6989b08423aa83930600af3b36a69b572e5e`  
		Last Modified: Tue, 25 Oct 2022 22:09:16 GMT  
		Size: 95.5 MB (95469663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b453065d137014d9afd7b61bab790935a460401456f9bdcebf6dd134f5d37fc`  
		Last Modified: Tue, 25 Oct 2022 22:09:05 GMT  
		Size: 295.6 KB (295639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2316db5066b2f905bf3ef20d6f817416f350af05c67a3c8d3273d52234b41e4`  
		Last Modified: Tue, 25 Oct 2022 22:09:04 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c024b89761df7b88cd9ede63829964f10f26f025bc3e49c423b1ab95263630`  
		Last Modified: Tue, 25 Oct 2022 22:09:08 GMT  
		Size: 22.4 MB (22433878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:a77dcc38d9454e8a3d10971146eeb7a13bc36a0e97e8c97cade9ac090d9959aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:8bacb2ad63d34e815a7983fd8001a3f4183c28384feb5538e6dce2ec715eb7d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141660031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a32cd2767cb289a14d77fd1f6dd451fa60a7f107555bf2bc9a71dfe8dc5ac8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 07:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:34:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:34:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:34:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be1f7ccd647190e134f58b7bdaddc42b6477dff97e50567b748bc31b6303f00`  
		Last Modified: Tue, 25 Oct 2022 08:02:27 GMT  
		Size: 106.2 MB (106227052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd97e132a97f3e5517dacc0f9b6598427f1966b8505acab43d41575f53d2ee8`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bd98c1e23890289ecd4c1c3dcabb9871dd202d4e596196345862d17810dea087
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137337380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b6bffeab8857cd2edb8dd6c91809c31e3962be3f8132941040595a48cf1c1c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:02 GMT
ADD file:515177312f20fb1814b89bfccfe695fa2354bbb6d43fdb6e018bf5b1acc17e9f in / 
# Tue, 25 Oct 2022 05:55:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:40:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:41:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 21:43:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:43:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:43:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:43:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:56a2caa6b2c66e01954c1a013b37ea359b6e6af8989dbfb958124b6318771af4`  
		Last Modified: Tue, 25 Oct 2022 05:56:14 GMT  
		Size: 28.4 MB (28382489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191d2d5931f4547389f96db79cb360ca3fdcf9f2d51c390b6958348a8a67c347`  
		Last Modified: Tue, 25 Oct 2022 22:08:40 GMT  
		Size: 1.2 MB (1176430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c085abd75940b2d68ae65386a432f481580f2ba06963b1e8c435bf4a06943d1`  
		Last Modified: Tue, 25 Oct 2022 22:08:38 GMT  
		Size: 3.8 MB (3799950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efa6f1ee27186437a210a19aa7cac0243bca4bf8e278464256de1a6c727019e`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ca2e27b815a4a40cfebb2d3e9e35f746c5458629933fdb650f2fe0af8725c7`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f958027197f946bc5c344b5c6d11ee5563140eba9b62b50ebd81ff37e58c0cc2`  
		Last Modified: Tue, 25 Oct 2022 22:08:54 GMT  
		Size: 104.0 MB (103976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a1b379b05f9273bfb87896fa46bf209006cfc9e82c69f9a47067ca2d74aa5`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:a77dcc38d9454e8a3d10971146eeb7a13bc36a0e97e8c97cade9ac090d9959aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:8bacb2ad63d34e815a7983fd8001a3f4183c28384feb5538e6dce2ec715eb7d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141660031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a32cd2767cb289a14d77fd1f6dd451fa60a7f107555bf2bc9a71dfe8dc5ac8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 07:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:34:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:34:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:34:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be1f7ccd647190e134f58b7bdaddc42b6477dff97e50567b748bc31b6303f00`  
		Last Modified: Tue, 25 Oct 2022 08:02:27 GMT  
		Size: 106.2 MB (106227052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd97e132a97f3e5517dacc0f9b6598427f1966b8505acab43d41575f53d2ee8`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bd98c1e23890289ecd4c1c3dcabb9871dd202d4e596196345862d17810dea087
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137337380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b6bffeab8857cd2edb8dd6c91809c31e3962be3f8132941040595a48cf1c1c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:02 GMT
ADD file:515177312f20fb1814b89bfccfe695fa2354bbb6d43fdb6e018bf5b1acc17e9f in / 
# Tue, 25 Oct 2022 05:55:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:40:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:41:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 21:43:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:43:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:43:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:43:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:56a2caa6b2c66e01954c1a013b37ea359b6e6af8989dbfb958124b6318771af4`  
		Last Modified: Tue, 25 Oct 2022 05:56:14 GMT  
		Size: 28.4 MB (28382489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191d2d5931f4547389f96db79cb360ca3fdcf9f2d51c390b6958348a8a67c347`  
		Last Modified: Tue, 25 Oct 2022 22:08:40 GMT  
		Size: 1.2 MB (1176430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c085abd75940b2d68ae65386a432f481580f2ba06963b1e8c435bf4a06943d1`  
		Last Modified: Tue, 25 Oct 2022 22:08:38 GMT  
		Size: 3.8 MB (3799950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efa6f1ee27186437a210a19aa7cac0243bca4bf8e278464256de1a6c727019e`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ca2e27b815a4a40cfebb2d3e9e35f746c5458629933fdb650f2fe0af8725c7`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f958027197f946bc5c344b5c6d11ee5563140eba9b62b50ebd81ff37e58c0cc2`  
		Last Modified: Tue, 25 Oct 2022 22:08:54 GMT  
		Size: 104.0 MB (103976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a1b379b05f9273bfb87896fa46bf209006cfc9e82c69f9a47067ca2d74aa5`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:latest`

```console
$ docker pull ros@sha256:50bcdf7a659f810c5a353ed3da0b1ce32b6d9d8f07422de32034518aefea9863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:0a802223f0f42ce6c021e103c88cebb39d34b33e6f27b6c5eeb664a4384581ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262845111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f340563a38bb44aee9bda8c1ce81c0eb80dde4b3d82200d63cafbf34e511942`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 07:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:34:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:34:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:34:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:35:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:35:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:35:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be1f7ccd647190e134f58b7bdaddc42b6477dff97e50567b748bc31b6303f00`  
		Last Modified: Tue, 25 Oct 2022 08:02:27 GMT  
		Size: 106.2 MB (106227052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd97e132a97f3e5517dacc0f9b6598427f1966b8505acab43d41575f53d2ee8`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd54d8e71568daecc9e521d17654239410a7a8d6895fb3167bb3e4b8735f5e5`  
		Last Modified: Tue, 25 Oct 2022 08:02:52 GMT  
		Size: 97.9 MB (97878471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d389ad8893cc3f537cfc3608c72ea4279d8ef1edc81ecdf82f4dbbdf4b8b604`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 295.6 KB (295633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d846403b95a3d13902aed833ac91f24ab2628f08871623f59fc2ef029c73ab2c`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710da595552b7d9324d2e432bcf0437dc8b7f054bf7ae402a6f33c2d5cbc281c`  
		Last Modified: Tue, 25 Oct 2022 08:02:42 GMT  
		Size: 23.0 MB (23008535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e6d1e6c4518e267f9642f3097c08f57026bb5b23a07518200df6e3aecab64c00
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255538972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63521c990d674cda3c67249e6cfdcec14a99b82c74773fb5d1db4f07f726ab5c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:02 GMT
ADD file:515177312f20fb1814b89bfccfe695fa2354bbb6d43fdb6e018bf5b1acc17e9f in / 
# Tue, 25 Oct 2022 05:55:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:40:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:41:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 21:43:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:43:02 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:43:02 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:43:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:44:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:44:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:44:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:45:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56a2caa6b2c66e01954c1a013b37ea359b6e6af8989dbfb958124b6318771af4`  
		Last Modified: Tue, 25 Oct 2022 05:56:14 GMT  
		Size: 28.4 MB (28382489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191d2d5931f4547389f96db79cb360ca3fdcf9f2d51c390b6958348a8a67c347`  
		Last Modified: Tue, 25 Oct 2022 22:08:40 GMT  
		Size: 1.2 MB (1176430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c085abd75940b2d68ae65386a432f481580f2ba06963b1e8c435bf4a06943d1`  
		Last Modified: Tue, 25 Oct 2022 22:08:38 GMT  
		Size: 3.8 MB (3799950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efa6f1ee27186437a210a19aa7cac0243bca4bf8e278464256de1a6c727019e`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ca2e27b815a4a40cfebb2d3e9e35f746c5458629933fdb650f2fe0af8725c7`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f958027197f946bc5c344b5c6d11ee5563140eba9b62b50ebd81ff37e58c0cc2`  
		Last Modified: Tue, 25 Oct 2022 22:08:54 GMT  
		Size: 104.0 MB (103976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a1b379b05f9273bfb87896fa46bf209006cfc9e82c69f9a47067ca2d74aa5`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3b15e7b12a9239bb2946201d3c6989b08423aa83930600af3b36a69b572e5e`  
		Last Modified: Tue, 25 Oct 2022 22:09:16 GMT  
		Size: 95.5 MB (95469663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b453065d137014d9afd7b61bab790935a460401456f9bdcebf6dd134f5d37fc`  
		Last Modified: Tue, 25 Oct 2022 22:09:05 GMT  
		Size: 295.6 KB (295639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2316db5066b2f905bf3ef20d6f817416f350af05c67a3c8d3273d52234b41e4`  
		Last Modified: Tue, 25 Oct 2022 22:09:04 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c024b89761df7b88cd9ede63829964f10f26f025bc3e49c423b1ab95263630`  
		Last Modified: Tue, 25 Oct 2022 22:09:08 GMT  
		Size: 22.4 MB (22433878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic`

```console
$ docker pull ros@sha256:ea0345d70e87af214824b2435ac702f04b851c7ebdffbcb1576443b789638e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic` - linux; amd64

```console
$ docker pull ros@sha256:a7201ea28800aff6b84b5fc7ab4fd80b61bc58dc006b9c2cdca6ec7be32cf6ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 MB (437538991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898998df3ed57ef16b7e130a5148adf56b94754f794c70d6f6b5c670eb939dbf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:51:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 06:51:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 06:55:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:55:51 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 06:55:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 06:55:51 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:56:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:56:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 06:58:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1955214fb5b152d9d9fa8ce9a39b19a4e6e8ea487bc617e76c0b7b33e1881bc`  
		Last Modified: Tue, 25 Oct 2022 07:50:06 GMT  
		Size: 831.1 KB (831118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389880aa1534b94319b44ef0d7e8e52ae108ec326dc1efe1cf0e4e749a4190a`  
		Last Modified: Tue, 25 Oct 2022 07:50:04 GMT  
		Size: 4.9 MB (4877285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db68a36d4b9f8fa036da9f0c51e74b6d27dffd9d39317f42638ee84b29322668`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b325e4aad15f84b511f749de8e3b84dc88f98909bbfdd1961ac0e84f7d273f16`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ad76754b2b5a9699fc604ac8d1393dd3d6dfe21df82c8e930da67ffd6f6708`  
		Last Modified: Tue, 25 Oct 2022 07:50:52 GMT  
		Size: 259.6 MB (259567997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1318baf5e3f70ccdc707f97c58bf69e65917aadaa98ec26b67d1d2695572fa`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb834ce8392143178e871793c61a9bd2ac4e34031627b0f8d8453a1f1d836a1`  
		Last Modified: Tue, 25 Oct 2022 07:51:13 GMT  
		Size: 70.3 MB (70260436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874278d4c37ef6d13abdb486dd6dfd9900b104ad68492eb5ba5df13c5c947b37`  
		Last Modified: Tue, 25 Oct 2022 07:51:03 GMT  
		Size: 289.2 KB (289160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236595b9f2b064d0593cf222d04423eaa11b12eaa5c8e78974d822f22c23287`  
		Last Modified: Tue, 25 Oct 2022 07:51:19 GMT  
		Size: 75.0 MB (74998649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm variant v7

```console
$ docker pull ros@sha256:a45ac6c100b50466ddc1d7e743fa1245f7fd98846f6029690aea97d10f221e45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (385994420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39885270420308b747b47cac016d290e8ce997f48e27902594c0fb48214d0fa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:46:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:46:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Oct 2022 06:48:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:48:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:48:10 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:48:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:49:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25a09f0aff0cba5b24d07bd5b4c417734fbce77148b7b62042ac54dc95c068`  
		Last Modified: Thu, 06 Oct 2022 06:58:00 GMT  
		Size: 831.1 KB (831144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14397641aa51f3c3aa6ed2c352f3417b3bce0ebaca231e20759c931e3fe38560`  
		Last Modified: Thu, 06 Oct 2022 06:57:58 GMT  
		Size: 4.1 MB (4087217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2d98c80683d1808b546f8ca1a247aecedcea1e9d2460d95343238dfabc896`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670273ddac9f5d6d6c7da9986d18661e88bbbc0126833dcd54f90992f9c9484d`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6664b634c5bf87720b15e47366d33bea9fefdd0032f110f86c336e5ae31a0e`  
		Last Modified: Thu, 06 Oct 2022 06:58:45 GMT  
		Size: 239.0 MB (239013225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074569eb7528b8c52dc9fd001aac258a83c59faaf1830e646c00899e79c3a889`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c925a21a964fb8486223de78f9a2d457f125c75f70114336548d871ef3aa6e97`  
		Last Modified: Thu, 06 Oct 2022 06:59:08 GMT  
		Size: 54.7 MB (54719854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176e6a18e2f88225c6c13f76a00ecd1530583b434fa9c482eee0a2179245adbd`  
		Last Modified: Thu, 06 Oct 2022 06:58:57 GMT  
		Size: 287.8 KB (287786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ace293972247ef40871f854b48d8ab1be13f2c1d04bc8c2d37a6be30a82a5e`  
		Last Modified: Thu, 06 Oct 2022 06:59:13 GMT  
		Size: 64.7 MB (64747626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a3bc1386512161551014d974ef7a92ab093f9740745a129aaf585129950f409a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.2 MB (412168880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9021aea3f107f10bf15a3e04d0ebc412e3119eea741be23df0d0b94c222f3b7f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:56 GMT
ADD file:585011162da73734395f2ef251ad89b72cfed0101c7da2435fac55061f99b516 in / 
# Tue, 25 Oct 2022 05:54:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 20:56:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 20:56:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 20:56:59 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 20:57:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 20:57:00 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 20:57:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 20:57:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 21:01:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:01:22 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:01:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:01:22 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:02:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:02:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:03:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a217cb16e35b382d60a7ab454a8c4db0fbe5e0aeec4b4c346e51eb1e77d34f8c`  
		Last Modified: Tue, 25 Oct 2022 05:55:45 GMT  
		Size: 23.7 MB (23735856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716808bd159516452cc1fc4db13d26965a5ea97f8fd507504f2abbd039e6b49d`  
		Last Modified: Tue, 25 Oct 2022 21:59:17 GMT  
		Size: 832.1 KB (832133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba094397f1fa2e72e998a82343d0614edda5257c98110b93a24af381630d3d31`  
		Last Modified: Tue, 25 Oct 2022 21:59:16 GMT  
		Size: 4.5 MB (4461373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282853d155ba0f593cc03d8773b2943181fe800a9fd446c6f8e70272937f7b9`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8dfb3f0f683701a85906157d325487eef9df7b6c559e3789449d02a6141051`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a20849d29bb87d6b2a985fcc31e046ea130cae04137e9d346ad8322cab86170`  
		Last Modified: Tue, 25 Oct 2022 21:59:49 GMT  
		Size: 252.5 MB (252526710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90dfe4568d11bee7e54df662800278a22a50ea4a63904f366d46a49ee17f6a4`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f778aa7fa96e398ee7887d76161f1c151b67c7d0888a48c9512e86d37ba7c532`  
		Last Modified: Tue, 25 Oct 2022 22:00:07 GMT  
		Size: 63.1 MB (63091592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da590a11132a9292f690e41ddd35c007c4ad4da0e52655fad6f6ef220d97f9b7`  
		Last Modified: Tue, 25 Oct 2022 22:00:00 GMT  
		Size: 289.2 KB (289154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cb1026663e1c31e2f46024240399e38da1fd0da606460b86316cba8196c55a`  
		Last Modified: Tue, 25 Oct 2022 22:00:11 GMT  
		Size: 67.2 MB (67230215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-perception`

```console
$ docker pull ros@sha256:3e23cdc0ee62fc68a3ab005ce4450439bb80ed6552c27868b8eaf4acbff5c4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-perception` - linux; amd64

```console
$ docker pull ros@sha256:760356bd129ecac893a2c56afe72c845c57258ec8d238e58be69eef50afcce0b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.9 MB (742894003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0abbf16914f8244ac1927554743a188b63ed7ab5c73d268af3cce4073bf7d27`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:51:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 06:51:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 06:55:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:55:51 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 06:55:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 06:55:51 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:56:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:56:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 06:58:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1955214fb5b152d9d9fa8ce9a39b19a4e6e8ea487bc617e76c0b7b33e1881bc`  
		Last Modified: Tue, 25 Oct 2022 07:50:06 GMT  
		Size: 831.1 KB (831118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389880aa1534b94319b44ef0d7e8e52ae108ec326dc1efe1cf0e4e749a4190a`  
		Last Modified: Tue, 25 Oct 2022 07:50:04 GMT  
		Size: 4.9 MB (4877285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db68a36d4b9f8fa036da9f0c51e74b6d27dffd9d39317f42638ee84b29322668`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b325e4aad15f84b511f749de8e3b84dc88f98909bbfdd1961ac0e84f7d273f16`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ad76754b2b5a9699fc604ac8d1393dd3d6dfe21df82c8e930da67ffd6f6708`  
		Last Modified: Tue, 25 Oct 2022 07:50:52 GMT  
		Size: 259.6 MB (259567997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1318baf5e3f70ccdc707f97c58bf69e65917aadaa98ec26b67d1d2695572fa`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb834ce8392143178e871793c61a9bd2ac4e34031627b0f8d8453a1f1d836a1`  
		Last Modified: Tue, 25 Oct 2022 07:51:13 GMT  
		Size: 70.3 MB (70260436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874278d4c37ef6d13abdb486dd6dfd9900b104ad68492eb5ba5df13c5c947b37`  
		Last Modified: Tue, 25 Oct 2022 07:51:03 GMT  
		Size: 289.2 KB (289160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236595b9f2b064d0593cf222d04423eaa11b12eaa5c8e78974d822f22c23287`  
		Last Modified: Tue, 25 Oct 2022 07:51:19 GMT  
		Size: 75.0 MB (74998649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5938790ff52815fa00897b4584fc3cff933821fac6b497b443f30e51552f900e`  
		Last Modified: Tue, 25 Oct 2022 07:52:42 GMT  
		Size: 305.4 MB (305355012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:d4a2aed0652e148c3323aaf63d7bdbec3ab1a6cd6d46d0b5c259509134524bd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.0 MB (646023839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf1034097743a12d2ccc90d1828450af36facdf6c4a85c762d45f098854d328`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:46:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:46:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Oct 2022 06:48:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:48:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:48:10 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:48:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:49:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:51:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25a09f0aff0cba5b24d07bd5b4c417734fbce77148b7b62042ac54dc95c068`  
		Last Modified: Thu, 06 Oct 2022 06:58:00 GMT  
		Size: 831.1 KB (831144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14397641aa51f3c3aa6ed2c352f3417b3bce0ebaca231e20759c931e3fe38560`  
		Last Modified: Thu, 06 Oct 2022 06:57:58 GMT  
		Size: 4.1 MB (4087217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2d98c80683d1808b546f8ca1a247aecedcea1e9d2460d95343238dfabc896`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670273ddac9f5d6d6c7da9986d18661e88bbbc0126833dcd54f90992f9c9484d`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6664b634c5bf87720b15e47366d33bea9fefdd0032f110f86c336e5ae31a0e`  
		Last Modified: Thu, 06 Oct 2022 06:58:45 GMT  
		Size: 239.0 MB (239013225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074569eb7528b8c52dc9fd001aac258a83c59faaf1830e646c00899e79c3a889`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c925a21a964fb8486223de78f9a2d457f125c75f70114336548d871ef3aa6e97`  
		Last Modified: Thu, 06 Oct 2022 06:59:08 GMT  
		Size: 54.7 MB (54719854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176e6a18e2f88225c6c13f76a00ecd1530583b434fa9c482eee0a2179245adbd`  
		Last Modified: Thu, 06 Oct 2022 06:58:57 GMT  
		Size: 287.8 KB (287786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ace293972247ef40871f854b48d8ab1be13f2c1d04bc8c2d37a6be30a82a5e`  
		Last Modified: Thu, 06 Oct 2022 06:59:13 GMT  
		Size: 64.7 MB (64747626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b175cc34aa53aebf1e1d4adce550c8bce2cfb95ce33879a16e5f7646f701ba`  
		Last Modified: Thu, 06 Oct 2022 07:00:25 GMT  
		Size: 260.0 MB (260029419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7809a857fa2d5937dd531dc6039e24134bba59233db5ed5d3120cc50f20f2f93
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.8 MB (703837400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e338d4cfe1123c4dd3b263398b0d267137e181241fc40cd1a6fb767ffe3dd78`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:56 GMT
ADD file:585011162da73734395f2ef251ad89b72cfed0101c7da2435fac55061f99b516 in / 
# Tue, 25 Oct 2022 05:54:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 20:56:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 20:56:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 20:56:59 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 20:57:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 20:57:00 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 20:57:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 20:57:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 21:01:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:01:22 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:01:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:01:22 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:02:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:02:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:03:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:10:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a217cb16e35b382d60a7ab454a8c4db0fbe5e0aeec4b4c346e51eb1e77d34f8c`  
		Last Modified: Tue, 25 Oct 2022 05:55:45 GMT  
		Size: 23.7 MB (23735856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716808bd159516452cc1fc4db13d26965a5ea97f8fd507504f2abbd039e6b49d`  
		Last Modified: Tue, 25 Oct 2022 21:59:17 GMT  
		Size: 832.1 KB (832133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba094397f1fa2e72e998a82343d0614edda5257c98110b93a24af381630d3d31`  
		Last Modified: Tue, 25 Oct 2022 21:59:16 GMT  
		Size: 4.5 MB (4461373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282853d155ba0f593cc03d8773b2943181fe800a9fd446c6f8e70272937f7b9`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8dfb3f0f683701a85906157d325487eef9df7b6c559e3789449d02a6141051`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a20849d29bb87d6b2a985fcc31e046ea130cae04137e9d346ad8322cab86170`  
		Last Modified: Tue, 25 Oct 2022 21:59:49 GMT  
		Size: 252.5 MB (252526710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90dfe4568d11bee7e54df662800278a22a50ea4a63904f366d46a49ee17f6a4`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f778aa7fa96e398ee7887d76161f1c151b67c7d0888a48c9512e86d37ba7c532`  
		Last Modified: Tue, 25 Oct 2022 22:00:07 GMT  
		Size: 63.1 MB (63091592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da590a11132a9292f690e41ddd35c007c4ad4da0e52655fad6f6ef220d97f9b7`  
		Last Modified: Tue, 25 Oct 2022 22:00:00 GMT  
		Size: 289.2 KB (289154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cb1026663e1c31e2f46024240399e38da1fd0da606460b86316cba8196c55a`  
		Last Modified: Tue, 25 Oct 2022 22:00:11 GMT  
		Size: 67.2 MB (67230215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d15817f04bd3a686b3a1d656bf22fa94a4a7522e64e30e5d667807bf05b3051`  
		Last Modified: Tue, 25 Oct 2022 22:01:14 GMT  
		Size: 291.7 MB (291668520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-perception-bionic`

```console
$ docker pull ros@sha256:3e23cdc0ee62fc68a3ab005ce4450439bb80ed6552c27868b8eaf4acbff5c4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-perception-bionic` - linux; amd64

```console
$ docker pull ros@sha256:760356bd129ecac893a2c56afe72c845c57258ec8d238e58be69eef50afcce0b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.9 MB (742894003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0abbf16914f8244ac1927554743a188b63ed7ab5c73d268af3cce4073bf7d27`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:51:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 06:51:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 06:55:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:55:51 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 06:55:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 06:55:51 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:56:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:56:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 06:58:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1955214fb5b152d9d9fa8ce9a39b19a4e6e8ea487bc617e76c0b7b33e1881bc`  
		Last Modified: Tue, 25 Oct 2022 07:50:06 GMT  
		Size: 831.1 KB (831118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389880aa1534b94319b44ef0d7e8e52ae108ec326dc1efe1cf0e4e749a4190a`  
		Last Modified: Tue, 25 Oct 2022 07:50:04 GMT  
		Size: 4.9 MB (4877285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db68a36d4b9f8fa036da9f0c51e74b6d27dffd9d39317f42638ee84b29322668`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b325e4aad15f84b511f749de8e3b84dc88f98909bbfdd1961ac0e84f7d273f16`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ad76754b2b5a9699fc604ac8d1393dd3d6dfe21df82c8e930da67ffd6f6708`  
		Last Modified: Tue, 25 Oct 2022 07:50:52 GMT  
		Size: 259.6 MB (259567997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1318baf5e3f70ccdc707f97c58bf69e65917aadaa98ec26b67d1d2695572fa`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb834ce8392143178e871793c61a9bd2ac4e34031627b0f8d8453a1f1d836a1`  
		Last Modified: Tue, 25 Oct 2022 07:51:13 GMT  
		Size: 70.3 MB (70260436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874278d4c37ef6d13abdb486dd6dfd9900b104ad68492eb5ba5df13c5c947b37`  
		Last Modified: Tue, 25 Oct 2022 07:51:03 GMT  
		Size: 289.2 KB (289160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236595b9f2b064d0593cf222d04423eaa11b12eaa5c8e78974d822f22c23287`  
		Last Modified: Tue, 25 Oct 2022 07:51:19 GMT  
		Size: 75.0 MB (74998649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5938790ff52815fa00897b4584fc3cff933821fac6b497b443f30e51552f900e`  
		Last Modified: Tue, 25 Oct 2022 07:52:42 GMT  
		Size: 305.4 MB (305355012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:d4a2aed0652e148c3323aaf63d7bdbec3ab1a6cd6d46d0b5c259509134524bd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.0 MB (646023839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf1034097743a12d2ccc90d1828450af36facdf6c4a85c762d45f098854d328`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:46:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:46:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Oct 2022 06:48:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:48:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:48:10 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:48:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:49:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:51:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25a09f0aff0cba5b24d07bd5b4c417734fbce77148b7b62042ac54dc95c068`  
		Last Modified: Thu, 06 Oct 2022 06:58:00 GMT  
		Size: 831.1 KB (831144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14397641aa51f3c3aa6ed2c352f3417b3bce0ebaca231e20759c931e3fe38560`  
		Last Modified: Thu, 06 Oct 2022 06:57:58 GMT  
		Size: 4.1 MB (4087217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2d98c80683d1808b546f8ca1a247aecedcea1e9d2460d95343238dfabc896`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670273ddac9f5d6d6c7da9986d18661e88bbbc0126833dcd54f90992f9c9484d`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6664b634c5bf87720b15e47366d33bea9fefdd0032f110f86c336e5ae31a0e`  
		Last Modified: Thu, 06 Oct 2022 06:58:45 GMT  
		Size: 239.0 MB (239013225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074569eb7528b8c52dc9fd001aac258a83c59faaf1830e646c00899e79c3a889`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c925a21a964fb8486223de78f9a2d457f125c75f70114336548d871ef3aa6e97`  
		Last Modified: Thu, 06 Oct 2022 06:59:08 GMT  
		Size: 54.7 MB (54719854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176e6a18e2f88225c6c13f76a00ecd1530583b434fa9c482eee0a2179245adbd`  
		Last Modified: Thu, 06 Oct 2022 06:58:57 GMT  
		Size: 287.8 KB (287786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ace293972247ef40871f854b48d8ab1be13f2c1d04bc8c2d37a6be30a82a5e`  
		Last Modified: Thu, 06 Oct 2022 06:59:13 GMT  
		Size: 64.7 MB (64747626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b175cc34aa53aebf1e1d4adce550c8bce2cfb95ce33879a16e5f7646f701ba`  
		Last Modified: Thu, 06 Oct 2022 07:00:25 GMT  
		Size: 260.0 MB (260029419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7809a857fa2d5937dd531dc6039e24134bba59233db5ed5d3120cc50f20f2f93
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.8 MB (703837400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e338d4cfe1123c4dd3b263398b0d267137e181241fc40cd1a6fb767ffe3dd78`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:56 GMT
ADD file:585011162da73734395f2ef251ad89b72cfed0101c7da2435fac55061f99b516 in / 
# Tue, 25 Oct 2022 05:54:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 20:56:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 20:56:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 20:56:59 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 20:57:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 20:57:00 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 20:57:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 20:57:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 21:01:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:01:22 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:01:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:01:22 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:02:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:02:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:03:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:10:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a217cb16e35b382d60a7ab454a8c4db0fbe5e0aeec4b4c346e51eb1e77d34f8c`  
		Last Modified: Tue, 25 Oct 2022 05:55:45 GMT  
		Size: 23.7 MB (23735856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716808bd159516452cc1fc4db13d26965a5ea97f8fd507504f2abbd039e6b49d`  
		Last Modified: Tue, 25 Oct 2022 21:59:17 GMT  
		Size: 832.1 KB (832133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba094397f1fa2e72e998a82343d0614edda5257c98110b93a24af381630d3d31`  
		Last Modified: Tue, 25 Oct 2022 21:59:16 GMT  
		Size: 4.5 MB (4461373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282853d155ba0f593cc03d8773b2943181fe800a9fd446c6f8e70272937f7b9`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8dfb3f0f683701a85906157d325487eef9df7b6c559e3789449d02a6141051`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a20849d29bb87d6b2a985fcc31e046ea130cae04137e9d346ad8322cab86170`  
		Last Modified: Tue, 25 Oct 2022 21:59:49 GMT  
		Size: 252.5 MB (252526710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90dfe4568d11bee7e54df662800278a22a50ea4a63904f366d46a49ee17f6a4`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f778aa7fa96e398ee7887d76161f1c151b67c7d0888a48c9512e86d37ba7c532`  
		Last Modified: Tue, 25 Oct 2022 22:00:07 GMT  
		Size: 63.1 MB (63091592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da590a11132a9292f690e41ddd35c007c4ad4da0e52655fad6f6ef220d97f9b7`  
		Last Modified: Tue, 25 Oct 2022 22:00:00 GMT  
		Size: 289.2 KB (289154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cb1026663e1c31e2f46024240399e38da1fd0da606460b86316cba8196c55a`  
		Last Modified: Tue, 25 Oct 2022 22:00:11 GMT  
		Size: 67.2 MB (67230215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d15817f04bd3a686b3a1d656bf22fa94a4a7522e64e30e5d667807bf05b3051`  
		Last Modified: Tue, 25 Oct 2022 22:01:14 GMT  
		Size: 291.7 MB (291668520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-robot`

```console
$ docker pull ros@sha256:85120492e1d5a2cf7fb779569276ea31cabfbda5e6660785c12c2d1f464c9359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot` - linux; amd64

```console
$ docker pull ros@sha256:7fb936bf3f4c1f768981550fbafaa6e7b7b43f00d4d95b05798c4f78962cb349
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.6 MB (448624983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56880250050883f30db34a14ba89363854f201ded84b8f75d95611f26b8a787`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:51:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 06:51:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 06:55:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:55:51 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 06:55:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 06:55:51 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:56:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:56:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 06:58:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1955214fb5b152d9d9fa8ce9a39b19a4e6e8ea487bc617e76c0b7b33e1881bc`  
		Last Modified: Tue, 25 Oct 2022 07:50:06 GMT  
		Size: 831.1 KB (831118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389880aa1534b94319b44ef0d7e8e52ae108ec326dc1efe1cf0e4e749a4190a`  
		Last Modified: Tue, 25 Oct 2022 07:50:04 GMT  
		Size: 4.9 MB (4877285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db68a36d4b9f8fa036da9f0c51e74b6d27dffd9d39317f42638ee84b29322668`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b325e4aad15f84b511f749de8e3b84dc88f98909bbfdd1961ac0e84f7d273f16`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ad76754b2b5a9699fc604ac8d1393dd3d6dfe21df82c8e930da67ffd6f6708`  
		Last Modified: Tue, 25 Oct 2022 07:50:52 GMT  
		Size: 259.6 MB (259567997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1318baf5e3f70ccdc707f97c58bf69e65917aadaa98ec26b67d1d2695572fa`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb834ce8392143178e871793c61a9bd2ac4e34031627b0f8d8453a1f1d836a1`  
		Last Modified: Tue, 25 Oct 2022 07:51:13 GMT  
		Size: 70.3 MB (70260436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874278d4c37ef6d13abdb486dd6dfd9900b104ad68492eb5ba5df13c5c947b37`  
		Last Modified: Tue, 25 Oct 2022 07:51:03 GMT  
		Size: 289.2 KB (289160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236595b9f2b064d0593cf222d04423eaa11b12eaa5c8e78974d822f22c23287`  
		Last Modified: Tue, 25 Oct 2022 07:51:19 GMT  
		Size: 75.0 MB (74998649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04787df350a9858b29dcd5d866d17be1b134ac05697019c51a96201ec3a86463`  
		Last Modified: Tue, 25 Oct 2022 07:51:34 GMT  
		Size: 11.1 MB (11085992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:f41d68e783b7d250adc47fdf91c2d70b5bf9549309e96c6a3aeff32e79def5ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.1 MB (396117676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032becfc9cbe10179ba32714f7356484cde7fb78dd08f85f8380cc46ca85a675`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:46:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:46:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Oct 2022 06:48:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:48:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:48:10 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:48:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:49:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25a09f0aff0cba5b24d07bd5b4c417734fbce77148b7b62042ac54dc95c068`  
		Last Modified: Thu, 06 Oct 2022 06:58:00 GMT  
		Size: 831.1 KB (831144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14397641aa51f3c3aa6ed2c352f3417b3bce0ebaca231e20759c931e3fe38560`  
		Last Modified: Thu, 06 Oct 2022 06:57:58 GMT  
		Size: 4.1 MB (4087217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2d98c80683d1808b546f8ca1a247aecedcea1e9d2460d95343238dfabc896`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670273ddac9f5d6d6c7da9986d18661e88bbbc0126833dcd54f90992f9c9484d`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6664b634c5bf87720b15e47366d33bea9fefdd0032f110f86c336e5ae31a0e`  
		Last Modified: Thu, 06 Oct 2022 06:58:45 GMT  
		Size: 239.0 MB (239013225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074569eb7528b8c52dc9fd001aac258a83c59faaf1830e646c00899e79c3a889`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c925a21a964fb8486223de78f9a2d457f125c75f70114336548d871ef3aa6e97`  
		Last Modified: Thu, 06 Oct 2022 06:59:08 GMT  
		Size: 54.7 MB (54719854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176e6a18e2f88225c6c13f76a00ecd1530583b434fa9c482eee0a2179245adbd`  
		Last Modified: Thu, 06 Oct 2022 06:58:57 GMT  
		Size: 287.8 KB (287786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ace293972247ef40871f854b48d8ab1be13f2c1d04bc8c2d37a6be30a82a5e`  
		Last Modified: Thu, 06 Oct 2022 06:59:13 GMT  
		Size: 64.7 MB (64747626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335010a557901b56ebbeceac85af817dc563c72e83fe5f3c9d82d92e761187fe`  
		Last Modified: Thu, 06 Oct 2022 06:59:30 GMT  
		Size: 10.1 MB (10123256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2826cb95ef557c971ab9ff9e05ac0d9bf8e5803e9fcab9c4ea183188916e8899
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.9 MB (422909619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6553320dee30456380867da2c2c527fe0a5dcf416fa8f246f11a3c100295005a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:56 GMT
ADD file:585011162da73734395f2ef251ad89b72cfed0101c7da2435fac55061f99b516 in / 
# Tue, 25 Oct 2022 05:54:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 20:56:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 20:56:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 20:56:59 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 20:57:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 20:57:00 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 20:57:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 20:57:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 21:01:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:01:22 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:01:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:01:22 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:02:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:02:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:03:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:04:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a217cb16e35b382d60a7ab454a8c4db0fbe5e0aeec4b4c346e51eb1e77d34f8c`  
		Last Modified: Tue, 25 Oct 2022 05:55:45 GMT  
		Size: 23.7 MB (23735856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716808bd159516452cc1fc4db13d26965a5ea97f8fd507504f2abbd039e6b49d`  
		Last Modified: Tue, 25 Oct 2022 21:59:17 GMT  
		Size: 832.1 KB (832133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba094397f1fa2e72e998a82343d0614edda5257c98110b93a24af381630d3d31`  
		Last Modified: Tue, 25 Oct 2022 21:59:16 GMT  
		Size: 4.5 MB (4461373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282853d155ba0f593cc03d8773b2943181fe800a9fd446c6f8e70272937f7b9`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8dfb3f0f683701a85906157d325487eef9df7b6c559e3789449d02a6141051`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a20849d29bb87d6b2a985fcc31e046ea130cae04137e9d346ad8322cab86170`  
		Last Modified: Tue, 25 Oct 2022 21:59:49 GMT  
		Size: 252.5 MB (252526710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90dfe4568d11bee7e54df662800278a22a50ea4a63904f366d46a49ee17f6a4`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f778aa7fa96e398ee7887d76161f1c151b67c7d0888a48c9512e86d37ba7c532`  
		Last Modified: Tue, 25 Oct 2022 22:00:07 GMT  
		Size: 63.1 MB (63091592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da590a11132a9292f690e41ddd35c007c4ad4da0e52655fad6f6ef220d97f9b7`  
		Last Modified: Tue, 25 Oct 2022 22:00:00 GMT  
		Size: 289.2 KB (289154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cb1026663e1c31e2f46024240399e38da1fd0da606460b86316cba8196c55a`  
		Last Modified: Tue, 25 Oct 2022 22:00:11 GMT  
		Size: 67.2 MB (67230215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3212a29689ef6acf47341018b771b6536b1f595d3096d92409420d7bce7996`  
		Last Modified: Tue, 25 Oct 2022 22:00:25 GMT  
		Size: 10.7 MB (10740739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-robot-bionic`

```console
$ docker pull ros@sha256:85120492e1d5a2cf7fb779569276ea31cabfbda5e6660785c12c2d1f464c9359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot-bionic` - linux; amd64

```console
$ docker pull ros@sha256:7fb936bf3f4c1f768981550fbafaa6e7b7b43f00d4d95b05798c4f78962cb349
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.6 MB (448624983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56880250050883f30db34a14ba89363854f201ded84b8f75d95611f26b8a787`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:51:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 06:51:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 06:55:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:55:51 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 06:55:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 06:55:51 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:56:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:56:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 06:58:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1955214fb5b152d9d9fa8ce9a39b19a4e6e8ea487bc617e76c0b7b33e1881bc`  
		Last Modified: Tue, 25 Oct 2022 07:50:06 GMT  
		Size: 831.1 KB (831118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389880aa1534b94319b44ef0d7e8e52ae108ec326dc1efe1cf0e4e749a4190a`  
		Last Modified: Tue, 25 Oct 2022 07:50:04 GMT  
		Size: 4.9 MB (4877285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db68a36d4b9f8fa036da9f0c51e74b6d27dffd9d39317f42638ee84b29322668`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b325e4aad15f84b511f749de8e3b84dc88f98909bbfdd1961ac0e84f7d273f16`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ad76754b2b5a9699fc604ac8d1393dd3d6dfe21df82c8e930da67ffd6f6708`  
		Last Modified: Tue, 25 Oct 2022 07:50:52 GMT  
		Size: 259.6 MB (259567997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1318baf5e3f70ccdc707f97c58bf69e65917aadaa98ec26b67d1d2695572fa`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb834ce8392143178e871793c61a9bd2ac4e34031627b0f8d8453a1f1d836a1`  
		Last Modified: Tue, 25 Oct 2022 07:51:13 GMT  
		Size: 70.3 MB (70260436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874278d4c37ef6d13abdb486dd6dfd9900b104ad68492eb5ba5df13c5c947b37`  
		Last Modified: Tue, 25 Oct 2022 07:51:03 GMT  
		Size: 289.2 KB (289160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236595b9f2b064d0593cf222d04423eaa11b12eaa5c8e78974d822f22c23287`  
		Last Modified: Tue, 25 Oct 2022 07:51:19 GMT  
		Size: 75.0 MB (74998649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04787df350a9858b29dcd5d866d17be1b134ac05697019c51a96201ec3a86463`  
		Last Modified: Tue, 25 Oct 2022 07:51:34 GMT  
		Size: 11.1 MB (11085992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:f41d68e783b7d250adc47fdf91c2d70b5bf9549309e96c6a3aeff32e79def5ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.1 MB (396117676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032becfc9cbe10179ba32714f7356484cde7fb78dd08f85f8380cc46ca85a675`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:46:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:46:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Oct 2022 06:48:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:48:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:48:10 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:48:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:49:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25a09f0aff0cba5b24d07bd5b4c417734fbce77148b7b62042ac54dc95c068`  
		Last Modified: Thu, 06 Oct 2022 06:58:00 GMT  
		Size: 831.1 KB (831144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14397641aa51f3c3aa6ed2c352f3417b3bce0ebaca231e20759c931e3fe38560`  
		Last Modified: Thu, 06 Oct 2022 06:57:58 GMT  
		Size: 4.1 MB (4087217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2d98c80683d1808b546f8ca1a247aecedcea1e9d2460d95343238dfabc896`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670273ddac9f5d6d6c7da9986d18661e88bbbc0126833dcd54f90992f9c9484d`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6664b634c5bf87720b15e47366d33bea9fefdd0032f110f86c336e5ae31a0e`  
		Last Modified: Thu, 06 Oct 2022 06:58:45 GMT  
		Size: 239.0 MB (239013225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074569eb7528b8c52dc9fd001aac258a83c59faaf1830e646c00899e79c3a889`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c925a21a964fb8486223de78f9a2d457f125c75f70114336548d871ef3aa6e97`  
		Last Modified: Thu, 06 Oct 2022 06:59:08 GMT  
		Size: 54.7 MB (54719854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176e6a18e2f88225c6c13f76a00ecd1530583b434fa9c482eee0a2179245adbd`  
		Last Modified: Thu, 06 Oct 2022 06:58:57 GMT  
		Size: 287.8 KB (287786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ace293972247ef40871f854b48d8ab1be13f2c1d04bc8c2d37a6be30a82a5e`  
		Last Modified: Thu, 06 Oct 2022 06:59:13 GMT  
		Size: 64.7 MB (64747626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335010a557901b56ebbeceac85af817dc563c72e83fe5f3c9d82d92e761187fe`  
		Last Modified: Thu, 06 Oct 2022 06:59:30 GMT  
		Size: 10.1 MB (10123256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2826cb95ef557c971ab9ff9e05ac0d9bf8e5803e9fcab9c4ea183188916e8899
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.9 MB (422909619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6553320dee30456380867da2c2c527fe0a5dcf416fa8f246f11a3c100295005a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:56 GMT
ADD file:585011162da73734395f2ef251ad89b72cfed0101c7da2435fac55061f99b516 in / 
# Tue, 25 Oct 2022 05:54:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 20:56:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 20:56:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 20:56:59 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 20:57:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 20:57:00 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 20:57:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 20:57:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 21:01:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:01:22 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:01:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:01:22 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:02:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:02:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:03:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:04:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a217cb16e35b382d60a7ab454a8c4db0fbe5e0aeec4b4c346e51eb1e77d34f8c`  
		Last Modified: Tue, 25 Oct 2022 05:55:45 GMT  
		Size: 23.7 MB (23735856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716808bd159516452cc1fc4db13d26965a5ea97f8fd507504f2abbd039e6b49d`  
		Last Modified: Tue, 25 Oct 2022 21:59:17 GMT  
		Size: 832.1 KB (832133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba094397f1fa2e72e998a82343d0614edda5257c98110b93a24af381630d3d31`  
		Last Modified: Tue, 25 Oct 2022 21:59:16 GMT  
		Size: 4.5 MB (4461373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282853d155ba0f593cc03d8773b2943181fe800a9fd446c6f8e70272937f7b9`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8dfb3f0f683701a85906157d325487eef9df7b6c559e3789449d02a6141051`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a20849d29bb87d6b2a985fcc31e046ea130cae04137e9d346ad8322cab86170`  
		Last Modified: Tue, 25 Oct 2022 21:59:49 GMT  
		Size: 252.5 MB (252526710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90dfe4568d11bee7e54df662800278a22a50ea4a63904f366d46a49ee17f6a4`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f778aa7fa96e398ee7887d76161f1c151b67c7d0888a48c9512e86d37ba7c532`  
		Last Modified: Tue, 25 Oct 2022 22:00:07 GMT  
		Size: 63.1 MB (63091592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da590a11132a9292f690e41ddd35c007c4ad4da0e52655fad6f6ef220d97f9b7`  
		Last Modified: Tue, 25 Oct 2022 22:00:00 GMT  
		Size: 289.2 KB (289154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cb1026663e1c31e2f46024240399e38da1fd0da606460b86316cba8196c55a`  
		Last Modified: Tue, 25 Oct 2022 22:00:11 GMT  
		Size: 67.2 MB (67230215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3212a29689ef6acf47341018b771b6536b1f595d3096d92409420d7bce7996`  
		Last Modified: Tue, 25 Oct 2022 22:00:25 GMT  
		Size: 10.7 MB (10740739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-base`

```console
$ docker pull ros@sha256:ea0345d70e87af214824b2435ac702f04b851c7ebdffbcb1576443b789638e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:a7201ea28800aff6b84b5fc7ab4fd80b61bc58dc006b9c2cdca6ec7be32cf6ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 MB (437538991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898998df3ed57ef16b7e130a5148adf56b94754f794c70d6f6b5c670eb939dbf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:51:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 06:51:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 06:55:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:55:51 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 06:55:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 06:55:51 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:56:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:56:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 06:58:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1955214fb5b152d9d9fa8ce9a39b19a4e6e8ea487bc617e76c0b7b33e1881bc`  
		Last Modified: Tue, 25 Oct 2022 07:50:06 GMT  
		Size: 831.1 KB (831118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389880aa1534b94319b44ef0d7e8e52ae108ec326dc1efe1cf0e4e749a4190a`  
		Last Modified: Tue, 25 Oct 2022 07:50:04 GMT  
		Size: 4.9 MB (4877285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db68a36d4b9f8fa036da9f0c51e74b6d27dffd9d39317f42638ee84b29322668`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b325e4aad15f84b511f749de8e3b84dc88f98909bbfdd1961ac0e84f7d273f16`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ad76754b2b5a9699fc604ac8d1393dd3d6dfe21df82c8e930da67ffd6f6708`  
		Last Modified: Tue, 25 Oct 2022 07:50:52 GMT  
		Size: 259.6 MB (259567997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1318baf5e3f70ccdc707f97c58bf69e65917aadaa98ec26b67d1d2695572fa`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb834ce8392143178e871793c61a9bd2ac4e34031627b0f8d8453a1f1d836a1`  
		Last Modified: Tue, 25 Oct 2022 07:51:13 GMT  
		Size: 70.3 MB (70260436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874278d4c37ef6d13abdb486dd6dfd9900b104ad68492eb5ba5df13c5c947b37`  
		Last Modified: Tue, 25 Oct 2022 07:51:03 GMT  
		Size: 289.2 KB (289160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236595b9f2b064d0593cf222d04423eaa11b12eaa5c8e78974d822f22c23287`  
		Last Modified: Tue, 25 Oct 2022 07:51:19 GMT  
		Size: 75.0 MB (74998649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:a45ac6c100b50466ddc1d7e743fa1245f7fd98846f6029690aea97d10f221e45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (385994420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39885270420308b747b47cac016d290e8ce997f48e27902594c0fb48214d0fa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:46:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:46:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Oct 2022 06:48:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:48:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:48:10 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:48:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:49:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25a09f0aff0cba5b24d07bd5b4c417734fbce77148b7b62042ac54dc95c068`  
		Last Modified: Thu, 06 Oct 2022 06:58:00 GMT  
		Size: 831.1 KB (831144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14397641aa51f3c3aa6ed2c352f3417b3bce0ebaca231e20759c931e3fe38560`  
		Last Modified: Thu, 06 Oct 2022 06:57:58 GMT  
		Size: 4.1 MB (4087217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2d98c80683d1808b546f8ca1a247aecedcea1e9d2460d95343238dfabc896`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670273ddac9f5d6d6c7da9986d18661e88bbbc0126833dcd54f90992f9c9484d`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6664b634c5bf87720b15e47366d33bea9fefdd0032f110f86c336e5ae31a0e`  
		Last Modified: Thu, 06 Oct 2022 06:58:45 GMT  
		Size: 239.0 MB (239013225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074569eb7528b8c52dc9fd001aac258a83c59faaf1830e646c00899e79c3a889`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c925a21a964fb8486223de78f9a2d457f125c75f70114336548d871ef3aa6e97`  
		Last Modified: Thu, 06 Oct 2022 06:59:08 GMT  
		Size: 54.7 MB (54719854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176e6a18e2f88225c6c13f76a00ecd1530583b434fa9c482eee0a2179245adbd`  
		Last Modified: Thu, 06 Oct 2022 06:58:57 GMT  
		Size: 287.8 KB (287786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ace293972247ef40871f854b48d8ab1be13f2c1d04bc8c2d37a6be30a82a5e`  
		Last Modified: Thu, 06 Oct 2022 06:59:13 GMT  
		Size: 64.7 MB (64747626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a3bc1386512161551014d974ef7a92ab093f9740745a129aaf585129950f409a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.2 MB (412168880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9021aea3f107f10bf15a3e04d0ebc412e3119eea741be23df0d0b94c222f3b7f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:56 GMT
ADD file:585011162da73734395f2ef251ad89b72cfed0101c7da2435fac55061f99b516 in / 
# Tue, 25 Oct 2022 05:54:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 20:56:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 20:56:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 20:56:59 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 20:57:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 20:57:00 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 20:57:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 20:57:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 21:01:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:01:22 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:01:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:01:22 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:02:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:02:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:03:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a217cb16e35b382d60a7ab454a8c4db0fbe5e0aeec4b4c346e51eb1e77d34f8c`  
		Last Modified: Tue, 25 Oct 2022 05:55:45 GMT  
		Size: 23.7 MB (23735856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716808bd159516452cc1fc4db13d26965a5ea97f8fd507504f2abbd039e6b49d`  
		Last Modified: Tue, 25 Oct 2022 21:59:17 GMT  
		Size: 832.1 KB (832133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba094397f1fa2e72e998a82343d0614edda5257c98110b93a24af381630d3d31`  
		Last Modified: Tue, 25 Oct 2022 21:59:16 GMT  
		Size: 4.5 MB (4461373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282853d155ba0f593cc03d8773b2943181fe800a9fd446c6f8e70272937f7b9`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8dfb3f0f683701a85906157d325487eef9df7b6c559e3789449d02a6141051`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a20849d29bb87d6b2a985fcc31e046ea130cae04137e9d346ad8322cab86170`  
		Last Modified: Tue, 25 Oct 2022 21:59:49 GMT  
		Size: 252.5 MB (252526710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90dfe4568d11bee7e54df662800278a22a50ea4a63904f366d46a49ee17f6a4`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f778aa7fa96e398ee7887d76161f1c151b67c7d0888a48c9512e86d37ba7c532`  
		Last Modified: Tue, 25 Oct 2022 22:00:07 GMT  
		Size: 63.1 MB (63091592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da590a11132a9292f690e41ddd35c007c4ad4da0e52655fad6f6ef220d97f9b7`  
		Last Modified: Tue, 25 Oct 2022 22:00:00 GMT  
		Size: 289.2 KB (289154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cb1026663e1c31e2f46024240399e38da1fd0da606460b86316cba8196c55a`  
		Last Modified: Tue, 25 Oct 2022 22:00:11 GMT  
		Size: 67.2 MB (67230215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-base-bionic`

```console
$ docker pull ros@sha256:ea0345d70e87af214824b2435ac702f04b851c7ebdffbcb1576443b789638e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base-bionic` - linux; amd64

```console
$ docker pull ros@sha256:a7201ea28800aff6b84b5fc7ab4fd80b61bc58dc006b9c2cdca6ec7be32cf6ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 MB (437538991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898998df3ed57ef16b7e130a5148adf56b94754f794c70d6f6b5c670eb939dbf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:51:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 06:51:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 06:55:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:55:51 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 06:55:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 06:55:51 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:56:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:56:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 06:58:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1955214fb5b152d9d9fa8ce9a39b19a4e6e8ea487bc617e76c0b7b33e1881bc`  
		Last Modified: Tue, 25 Oct 2022 07:50:06 GMT  
		Size: 831.1 KB (831118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389880aa1534b94319b44ef0d7e8e52ae108ec326dc1efe1cf0e4e749a4190a`  
		Last Modified: Tue, 25 Oct 2022 07:50:04 GMT  
		Size: 4.9 MB (4877285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db68a36d4b9f8fa036da9f0c51e74b6d27dffd9d39317f42638ee84b29322668`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b325e4aad15f84b511f749de8e3b84dc88f98909bbfdd1961ac0e84f7d273f16`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ad76754b2b5a9699fc604ac8d1393dd3d6dfe21df82c8e930da67ffd6f6708`  
		Last Modified: Tue, 25 Oct 2022 07:50:52 GMT  
		Size: 259.6 MB (259567997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1318baf5e3f70ccdc707f97c58bf69e65917aadaa98ec26b67d1d2695572fa`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb834ce8392143178e871793c61a9bd2ac4e34031627b0f8d8453a1f1d836a1`  
		Last Modified: Tue, 25 Oct 2022 07:51:13 GMT  
		Size: 70.3 MB (70260436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874278d4c37ef6d13abdb486dd6dfd9900b104ad68492eb5ba5df13c5c947b37`  
		Last Modified: Tue, 25 Oct 2022 07:51:03 GMT  
		Size: 289.2 KB (289160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236595b9f2b064d0593cf222d04423eaa11b12eaa5c8e78974d822f22c23287`  
		Last Modified: Tue, 25 Oct 2022 07:51:19 GMT  
		Size: 75.0 MB (74998649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:a45ac6c100b50466ddc1d7e743fa1245f7fd98846f6029690aea97d10f221e45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (385994420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39885270420308b747b47cac016d290e8ce997f48e27902594c0fb48214d0fa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:46:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:46:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Oct 2022 06:48:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:48:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:48:10 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:48:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:49:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25a09f0aff0cba5b24d07bd5b4c417734fbce77148b7b62042ac54dc95c068`  
		Last Modified: Thu, 06 Oct 2022 06:58:00 GMT  
		Size: 831.1 KB (831144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14397641aa51f3c3aa6ed2c352f3417b3bce0ebaca231e20759c931e3fe38560`  
		Last Modified: Thu, 06 Oct 2022 06:57:58 GMT  
		Size: 4.1 MB (4087217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2d98c80683d1808b546f8ca1a247aecedcea1e9d2460d95343238dfabc896`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670273ddac9f5d6d6c7da9986d18661e88bbbc0126833dcd54f90992f9c9484d`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6664b634c5bf87720b15e47366d33bea9fefdd0032f110f86c336e5ae31a0e`  
		Last Modified: Thu, 06 Oct 2022 06:58:45 GMT  
		Size: 239.0 MB (239013225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074569eb7528b8c52dc9fd001aac258a83c59faaf1830e646c00899e79c3a889`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c925a21a964fb8486223de78f9a2d457f125c75f70114336548d871ef3aa6e97`  
		Last Modified: Thu, 06 Oct 2022 06:59:08 GMT  
		Size: 54.7 MB (54719854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176e6a18e2f88225c6c13f76a00ecd1530583b434fa9c482eee0a2179245adbd`  
		Last Modified: Thu, 06 Oct 2022 06:58:57 GMT  
		Size: 287.8 KB (287786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ace293972247ef40871f854b48d8ab1be13f2c1d04bc8c2d37a6be30a82a5e`  
		Last Modified: Thu, 06 Oct 2022 06:59:13 GMT  
		Size: 64.7 MB (64747626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a3bc1386512161551014d974ef7a92ab093f9740745a129aaf585129950f409a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.2 MB (412168880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9021aea3f107f10bf15a3e04d0ebc412e3119eea741be23df0d0b94c222f3b7f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:56 GMT
ADD file:585011162da73734395f2ef251ad89b72cfed0101c7da2435fac55061f99b516 in / 
# Tue, 25 Oct 2022 05:54:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 20:56:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 20:56:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 20:56:59 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 20:57:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 20:57:00 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 20:57:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 20:57:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 21:01:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:01:22 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:01:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:01:22 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:02:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:02:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:03:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a217cb16e35b382d60a7ab454a8c4db0fbe5e0aeec4b4c346e51eb1e77d34f8c`  
		Last Modified: Tue, 25 Oct 2022 05:55:45 GMT  
		Size: 23.7 MB (23735856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716808bd159516452cc1fc4db13d26965a5ea97f8fd507504f2abbd039e6b49d`  
		Last Modified: Tue, 25 Oct 2022 21:59:17 GMT  
		Size: 832.1 KB (832133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba094397f1fa2e72e998a82343d0614edda5257c98110b93a24af381630d3d31`  
		Last Modified: Tue, 25 Oct 2022 21:59:16 GMT  
		Size: 4.5 MB (4461373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282853d155ba0f593cc03d8773b2943181fe800a9fd446c6f8e70272937f7b9`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8dfb3f0f683701a85906157d325487eef9df7b6c559e3789449d02a6141051`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a20849d29bb87d6b2a985fcc31e046ea130cae04137e9d346ad8322cab86170`  
		Last Modified: Tue, 25 Oct 2022 21:59:49 GMT  
		Size: 252.5 MB (252526710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90dfe4568d11bee7e54df662800278a22a50ea4a63904f366d46a49ee17f6a4`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f778aa7fa96e398ee7887d76161f1c151b67c7d0888a48c9512e86d37ba7c532`  
		Last Modified: Tue, 25 Oct 2022 22:00:07 GMT  
		Size: 63.1 MB (63091592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da590a11132a9292f690e41ddd35c007c4ad4da0e52655fad6f6ef220d97f9b7`  
		Last Modified: Tue, 25 Oct 2022 22:00:00 GMT  
		Size: 289.2 KB (289154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cb1026663e1c31e2f46024240399e38da1fd0da606460b86316cba8196c55a`  
		Last Modified: Tue, 25 Oct 2022 22:00:11 GMT  
		Size: 67.2 MB (67230215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-core`

```console
$ docker pull ros@sha256:dc0e7285be861be778da729878eb2ffc34cfc0b195a94d8d540b973496a28191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:4823a905ffe0b3e7d527d857d533d78fc707ace416fed369a38da35f98b535bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (291990746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b750019b37ee79ded291459fd57709578c21c1a3c552e25109bf1f41e0d8dd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:51:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 06:51:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 06:55:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:55:51 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 06:55:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 06:55:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1955214fb5b152d9d9fa8ce9a39b19a4e6e8ea487bc617e76c0b7b33e1881bc`  
		Last Modified: Tue, 25 Oct 2022 07:50:06 GMT  
		Size: 831.1 KB (831118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389880aa1534b94319b44ef0d7e8e52ae108ec326dc1efe1cf0e4e749a4190a`  
		Last Modified: Tue, 25 Oct 2022 07:50:04 GMT  
		Size: 4.9 MB (4877285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db68a36d4b9f8fa036da9f0c51e74b6d27dffd9d39317f42638ee84b29322668`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b325e4aad15f84b511f749de8e3b84dc88f98909bbfdd1961ac0e84f7d273f16`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ad76754b2b5a9699fc604ac8d1393dd3d6dfe21df82c8e930da67ffd6f6708`  
		Last Modified: Tue, 25 Oct 2022 07:50:52 GMT  
		Size: 259.6 MB (259567997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1318baf5e3f70ccdc707f97c58bf69e65917aadaa98ec26b67d1d2695572fa`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:11cbb2f864a289726b9510d1a9b4e6e7414dfacb9a9d782b9d1e4754293f2056
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266239154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d83c28f326a67014793ddf881b3e99269c547c3a86ced293cec9f9fca7d46c0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:46:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:46:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Oct 2022 06:48:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:48:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:48:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25a09f0aff0cba5b24d07bd5b4c417734fbce77148b7b62042ac54dc95c068`  
		Last Modified: Thu, 06 Oct 2022 06:58:00 GMT  
		Size: 831.1 KB (831144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14397641aa51f3c3aa6ed2c352f3417b3bce0ebaca231e20759c931e3fe38560`  
		Last Modified: Thu, 06 Oct 2022 06:57:58 GMT  
		Size: 4.1 MB (4087217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2d98c80683d1808b546f8ca1a247aecedcea1e9d2460d95343238dfabc896`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670273ddac9f5d6d6c7da9986d18661e88bbbc0126833dcd54f90992f9c9484d`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6664b634c5bf87720b15e47366d33bea9fefdd0032f110f86c336e5ae31a0e`  
		Last Modified: Thu, 06 Oct 2022 06:58:45 GMT  
		Size: 239.0 MB (239013225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074569eb7528b8c52dc9fd001aac258a83c59faaf1830e646c00899e79c3a889`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0c361609706c9aee43282132738b66d3471f861629c71d8d949be9738ad6bb87
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 MB (281557919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c264a0eff7c5acbeca6ee4599d1de01b6c8d56f44c806d6564b60b2ee5d0fc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:56 GMT
ADD file:585011162da73734395f2ef251ad89b72cfed0101c7da2435fac55061f99b516 in / 
# Tue, 25 Oct 2022 05:54:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 20:56:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 20:56:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 20:56:59 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 20:57:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 20:57:00 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 20:57:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 20:57:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 21:01:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:01:22 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:01:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:01:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a217cb16e35b382d60a7ab454a8c4db0fbe5e0aeec4b4c346e51eb1e77d34f8c`  
		Last Modified: Tue, 25 Oct 2022 05:55:45 GMT  
		Size: 23.7 MB (23735856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716808bd159516452cc1fc4db13d26965a5ea97f8fd507504f2abbd039e6b49d`  
		Last Modified: Tue, 25 Oct 2022 21:59:17 GMT  
		Size: 832.1 KB (832133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba094397f1fa2e72e998a82343d0614edda5257c98110b93a24af381630d3d31`  
		Last Modified: Tue, 25 Oct 2022 21:59:16 GMT  
		Size: 4.5 MB (4461373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282853d155ba0f593cc03d8773b2943181fe800a9fd446c6f8e70272937f7b9`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8dfb3f0f683701a85906157d325487eef9df7b6c559e3789449d02a6141051`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a20849d29bb87d6b2a985fcc31e046ea130cae04137e9d346ad8322cab86170`  
		Last Modified: Tue, 25 Oct 2022 21:59:49 GMT  
		Size: 252.5 MB (252526710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90dfe4568d11bee7e54df662800278a22a50ea4a63904f366d46a49ee17f6a4`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-core-bionic`

```console
$ docker pull ros@sha256:dc0e7285be861be778da729878eb2ffc34cfc0b195a94d8d540b973496a28191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:4823a905ffe0b3e7d527d857d533d78fc707ace416fed369a38da35f98b535bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (291990746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b750019b37ee79ded291459fd57709578c21c1a3c552e25109bf1f41e0d8dd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:51:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 06:51:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 06:55:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:55:51 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 06:55:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 06:55:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1955214fb5b152d9d9fa8ce9a39b19a4e6e8ea487bc617e76c0b7b33e1881bc`  
		Last Modified: Tue, 25 Oct 2022 07:50:06 GMT  
		Size: 831.1 KB (831118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389880aa1534b94319b44ef0d7e8e52ae108ec326dc1efe1cf0e4e749a4190a`  
		Last Modified: Tue, 25 Oct 2022 07:50:04 GMT  
		Size: 4.9 MB (4877285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db68a36d4b9f8fa036da9f0c51e74b6d27dffd9d39317f42638ee84b29322668`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b325e4aad15f84b511f749de8e3b84dc88f98909bbfdd1961ac0e84f7d273f16`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ad76754b2b5a9699fc604ac8d1393dd3d6dfe21df82c8e930da67ffd6f6708`  
		Last Modified: Tue, 25 Oct 2022 07:50:52 GMT  
		Size: 259.6 MB (259567997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1318baf5e3f70ccdc707f97c58bf69e65917aadaa98ec26b67d1d2695572fa`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:11cbb2f864a289726b9510d1a9b4e6e7414dfacb9a9d782b9d1e4754293f2056
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266239154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d83c28f326a67014793ddf881b3e99269c547c3a86ced293cec9f9fca7d46c0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:46:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:46:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Oct 2022 06:48:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:48:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:48:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25a09f0aff0cba5b24d07bd5b4c417734fbce77148b7b62042ac54dc95c068`  
		Last Modified: Thu, 06 Oct 2022 06:58:00 GMT  
		Size: 831.1 KB (831144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14397641aa51f3c3aa6ed2c352f3417b3bce0ebaca231e20759c931e3fe38560`  
		Last Modified: Thu, 06 Oct 2022 06:57:58 GMT  
		Size: 4.1 MB (4087217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2d98c80683d1808b546f8ca1a247aecedcea1e9d2460d95343238dfabc896`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670273ddac9f5d6d6c7da9986d18661e88bbbc0126833dcd54f90992f9c9484d`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6664b634c5bf87720b15e47366d33bea9fefdd0032f110f86c336e5ae31a0e`  
		Last Modified: Thu, 06 Oct 2022 06:58:45 GMT  
		Size: 239.0 MB (239013225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074569eb7528b8c52dc9fd001aac258a83c59faaf1830e646c00899e79c3a889`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0c361609706c9aee43282132738b66d3471f861629c71d8d949be9738ad6bb87
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 MB (281557919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c264a0eff7c5acbeca6ee4599d1de01b6c8d56f44c806d6564b60b2ee5d0fc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:56 GMT
ADD file:585011162da73734395f2ef251ad89b72cfed0101c7da2435fac55061f99b516 in / 
# Tue, 25 Oct 2022 05:54:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 20:56:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 20:56:58 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 20:56:59 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 20:57:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 20:57:00 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 20:57:00 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 20:57:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 21:01:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:01:22 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:01:22 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:01:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a217cb16e35b382d60a7ab454a8c4db0fbe5e0aeec4b4c346e51eb1e77d34f8c`  
		Last Modified: Tue, 25 Oct 2022 05:55:45 GMT  
		Size: 23.7 MB (23735856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716808bd159516452cc1fc4db13d26965a5ea97f8fd507504f2abbd039e6b49d`  
		Last Modified: Tue, 25 Oct 2022 21:59:17 GMT  
		Size: 832.1 KB (832133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba094397f1fa2e72e998a82343d0614edda5257c98110b93a24af381630d3d31`  
		Last Modified: Tue, 25 Oct 2022 21:59:16 GMT  
		Size: 4.5 MB (4461373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282853d155ba0f593cc03d8773b2943181fe800a9fd446c6f8e70272937f7b9`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8dfb3f0f683701a85906157d325487eef9df7b6c559e3789449d02a6141051`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a20849d29bb87d6b2a985fcc31e046ea130cae04137e9d346ad8322cab86170`  
		Last Modified: Tue, 25 Oct 2022 21:59:49 GMT  
		Size: 252.5 MB (252526710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90dfe4568d11bee7e54df662800278a22a50ea4a63904f366d46a49ee17f6a4`  
		Last Modified: Tue, 25 Oct 2022 21:59:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic`

```console
$ docker pull ros@sha256:2f00fb3ac6187568298b4392ec718c27858dc34bacc4dd940a2cc6f2826fcd4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:34cbfe55d811fe7c57add8b3d6f01ba9c209258ef1b4029cec5118dcd21e358f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343179990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6d7ab7e066ec3cc62a3c2bfe041ba6a0a444f0b66da68886d72c1906c5004a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:04:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:07:31 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:07:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:07:31 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:08:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:08:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcba2703cc13554dd6ac252966be0f9f0a9d6e79ee879b5e0289457bc632f55`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617320b8300618f53ec135b976c7f3a733354c5ef799b7c969108d82a8509f8`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065fe084d225480619420eb81fce25e1ea4e12e4f4b95002773742fc0e01d67`  
		Last Modified: Tue, 25 Oct 2022 07:53:37 GMT  
		Size: 177.0 MB (177008909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f66f6a9e5d5690a6fcd01f03ca5ef0146410fa911f6fccb17d73db1bbec814`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcd60406762b57a7de1c5c937562c8a145da66c5f0d5716f70f5c5ae115ab71`  
		Last Modified: Tue, 25 Oct 2022 07:53:56 GMT  
		Size: 50.9 MB (50940379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb29d90361859f6ac155a32b08124b4fecb3b64649f15b68b7d6b59f22d70d4`  
		Last Modified: Tue, 25 Oct 2022 07:53:47 GMT  
		Size: 332.1 KB (332101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055f4ec67f38d1b1c161894d68208d46a4d5822664774d4554aaf150f243341c`  
		Last Modified: Tue, 25 Oct 2022 07:54:01 GMT  
		Size: 79.6 MB (79603171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:282eece3c6e182e825057bcb769c29ec38c0a3e9b2c9cb0b913ede9dec5a8ccd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289297974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727b6d344ef45add4b6b86083e60223e9bb9840f5052ac125292637db637ef91`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:52:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:52:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 06 Oct 2022 06:53:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:16 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:53:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:53:16 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:53:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ab6ac546133bf21e51dc29641d455c42144b184821f494258ff1ec514556c`  
		Last Modified: Thu, 06 Oct 2022 07:00:40 GMT  
		Size: 1.2 MB (1163905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706759f53c150848596edb49143a211c7e072793acea609cc8e9c0f267c4e3e`  
		Last Modified: Thu, 06 Oct 2022 07:00:38 GMT  
		Size: 4.7 MB (4675577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b0360f8c716b3c493ff9708abd3c165f9de06193430830ea64d829b1a6ac2`  
		Last Modified: Thu, 06 Oct 2022 07:00:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd789251f14b7842f745c35075b3e7f88a5aa3fb3b005a3bd0fde7d8f285d7f`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24248fc7fc767d03259bb795d6c177495b4f61cdb1ddcc6a6bb9bb7dcd5958db`  
		Last Modified: Thu, 06 Oct 2022 07:01:15 GMT  
		Size: 157.6 MB (157550749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1b296e1c261f003a529641cc88d1393116b3a0b1f7853da9463a2e9c16df7c`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1461e09b998de0d3b7ae285e2a3bb8bcb1b889f8a12f832e208d7ec8d3bfe847`  
		Last Modified: Thu, 06 Oct 2022 07:01:36 GMT  
		Size: 40.5 MB (40505592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e355cb57c65a1dc870c88f7e383d6a76770d5f6563b605a9a96dc5ceb24b3a`  
		Last Modified: Thu, 06 Oct 2022 07:01:28 GMT  
		Size: 329.9 KB (329943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b0b621043424762e62d798dd71533b7835ccd3741e94dcdc7fbbdd3ca4f723`  
		Last Modified: Thu, 06 Oct 2022 07:01:40 GMT  
		Size: 60.5 MB (60479707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:01d2a5693cbb33946e8b06971fe471d2fb165267fdbcb711dabe777d24337749
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.9 MB (322853760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8198d039a3796669f31af0d2cd9fe7c58a960e811af29f1768be002666b9167a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 21:11:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:11:42 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 21:14:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:14:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:14:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:14:39 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:15:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:15:26 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:17:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7354b266abeda9b5bfbca97ad1c6887d2a277d69ff8c607591a279459548ac7`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d614279c49f19055c903676e10afd41c8a3cd40f35d8b708fb499f7b5eeb965f`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c1b3c16d04da075eb127cecb646f3fbb43b07575ac781c7f670ca3f1885796`  
		Last Modified: Tue, 25 Oct 2022 22:01:55 GMT  
		Size: 171.4 MB (171447425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ac303ffe5e80a8c48e68fb479034e19261f5b6990dd5100bc6ddb1c7cd38ff`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4148c35466d56fca5bdd1144c7cc49f7c57ff22d51ce5c197995f215040f68d6`  
		Last Modified: Tue, 25 Oct 2022 22:02:11 GMT  
		Size: 45.2 MB (45204375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b385026becc2dcce049f0ab39c7d58c6459f28965efe78e7ee77336f82328a45`  
		Last Modified: Tue, 25 Oct 2022 22:02:05 GMT  
		Size: 332.1 KB (332102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d152eaa0a13418a883f576ea85d8893f1cdcafe87fc965ff14ee47fd4e076e7`  
		Last Modified: Tue, 25 Oct 2022 22:02:14 GMT  
		Size: 72.0 MB (71974237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:46cae435f6f7ea8d7043e84fd95a8b98bdf95c4dd950fbc08741298fb7bb1de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:cbbb6aa7e54b07b867ea1c6fefab9c1bd83f795f6e3a30a499c0a1f595db15c4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.1 MB (835147503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d806f6ce0fd63436af5228a1d9a4209bb5f7f8de53205864e5319df8784e227`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:04:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:07:31 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:07:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:07:31 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:08:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:08:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:16:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcba2703cc13554dd6ac252966be0f9f0a9d6e79ee879b5e0289457bc632f55`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617320b8300618f53ec135b976c7f3a733354c5ef799b7c969108d82a8509f8`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065fe084d225480619420eb81fce25e1ea4e12e4f4b95002773742fc0e01d67`  
		Last Modified: Tue, 25 Oct 2022 07:53:37 GMT  
		Size: 177.0 MB (177008909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f66f6a9e5d5690a6fcd01f03ca5ef0146410fa911f6fccb17d73db1bbec814`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcd60406762b57a7de1c5c937562c8a145da66c5f0d5716f70f5c5ae115ab71`  
		Last Modified: Tue, 25 Oct 2022 07:53:56 GMT  
		Size: 50.9 MB (50940379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb29d90361859f6ac155a32b08124b4fecb3b64649f15b68b7d6b59f22d70d4`  
		Last Modified: Tue, 25 Oct 2022 07:53:47 GMT  
		Size: 332.1 KB (332101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055f4ec67f38d1b1c161894d68208d46a4d5822664774d4554aaf150f243341c`  
		Last Modified: Tue, 25 Oct 2022 07:54:01 GMT  
		Size: 79.6 MB (79603171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96304f40d98ec3ee8f481818e18af495a0d8da05d780423f6da8294be3c5fcc1`  
		Last Modified: Tue, 25 Oct 2022 07:55:56 GMT  
		Size: 492.0 MB (491967513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:d3a05ef88d081e15785fcfe16ff2c65f1202d8e5ec15369b110b406ff066c6bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.2 MB (726177866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2302d2ee97aca1cc80e68f815cc9e06f1b146c7567089608a5feb883d948ea4a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:52:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:52:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 06 Oct 2022 06:53:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:16 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:53:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:53:16 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:53:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:57:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ab6ac546133bf21e51dc29641d455c42144b184821f494258ff1ec514556c`  
		Last Modified: Thu, 06 Oct 2022 07:00:40 GMT  
		Size: 1.2 MB (1163905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706759f53c150848596edb49143a211c7e072793acea609cc8e9c0f267c4e3e`  
		Last Modified: Thu, 06 Oct 2022 07:00:38 GMT  
		Size: 4.7 MB (4675577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b0360f8c716b3c493ff9708abd3c165f9de06193430830ea64d829b1a6ac2`  
		Last Modified: Thu, 06 Oct 2022 07:00:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd789251f14b7842f745c35075b3e7f88a5aa3fb3b005a3bd0fde7d8f285d7f`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24248fc7fc767d03259bb795d6c177495b4f61cdb1ddcc6a6bb9bb7dcd5958db`  
		Last Modified: Thu, 06 Oct 2022 07:01:15 GMT  
		Size: 157.6 MB (157550749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1b296e1c261f003a529641cc88d1393116b3a0b1f7853da9463a2e9c16df7c`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1461e09b998de0d3b7ae285e2a3bb8bcb1b889f8a12f832e208d7ec8d3bfe847`  
		Last Modified: Thu, 06 Oct 2022 07:01:36 GMT  
		Size: 40.5 MB (40505592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e355cb57c65a1dc870c88f7e383d6a76770d5f6563b605a9a96dc5ceb24b3a`  
		Last Modified: Thu, 06 Oct 2022 07:01:28 GMT  
		Size: 329.9 KB (329943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b0b621043424762e62d798dd71533b7835ccd3741e94dcdc7fbbdd3ca4f723`  
		Last Modified: Thu, 06 Oct 2022 07:01:40 GMT  
		Size: 60.5 MB (60479707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed30924832b5259516fe54fa5708a8ae36898b16de1c94f0898baa3d5d3b84a`  
		Last Modified: Thu, 06 Oct 2022 07:03:20 GMT  
		Size: 436.9 MB (436879892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6a56e4c46dd57c138947ba191f82579cbebc7bc8be157b4afdc98279d0c2824a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.4 MB (785391798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e9ded839737165910ae71f3043672969d898b0aea25743168af6643850474c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 21:11:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:11:42 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 21:14:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:14:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:14:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:14:39 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:15:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:15:26 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:17:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:25:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7354b266abeda9b5bfbca97ad1c6887d2a277d69ff8c607591a279459548ac7`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d614279c49f19055c903676e10afd41c8a3cd40f35d8b708fb499f7b5eeb965f`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c1b3c16d04da075eb127cecb646f3fbb43b07575ac781c7f670ca3f1885796`  
		Last Modified: Tue, 25 Oct 2022 22:01:55 GMT  
		Size: 171.4 MB (171447425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ac303ffe5e80a8c48e68fb479034e19261f5b6990dd5100bc6ddb1c7cd38ff`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4148c35466d56fca5bdd1144c7cc49f7c57ff22d51ce5c197995f215040f68d6`  
		Last Modified: Tue, 25 Oct 2022 22:02:11 GMT  
		Size: 45.2 MB (45204375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b385026becc2dcce049f0ab39c7d58c6459f28965efe78e7ee77336f82328a45`  
		Last Modified: Tue, 25 Oct 2022 22:02:05 GMT  
		Size: 332.1 KB (332102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d152eaa0a13418a883f576ea85d8893f1cdcafe87fc965ff14ee47fd4e076e7`  
		Last Modified: Tue, 25 Oct 2022 22:02:14 GMT  
		Size: 72.0 MB (71974237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35aa43327036965b93b120edc9468bb69de8263d58440de8ffc83cab8e59a269`  
		Last Modified: Tue, 25 Oct 2022 22:03:38 GMT  
		Size: 462.5 MB (462538038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-buster`

```console
$ docker pull ros@sha256:7e22170e8bd40258f4897d9f08b143705f6aceefbfb4f99808aa55ed3322273f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-perception-buster` - linux; amd64

```console
$ docker pull ros@sha256:c958d3e0d30b8a78337d7ca918ba7121ae3773ff0a059854735268ec24a7123d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **951.4 MB (951441437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9db43d92b60e5b392a3e50febed01db2bf45270fe34bc49262c432ebef789b3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:02 GMT
ADD file:259be79d94a2549a667ad08a093fe18f15a6c93d66a0723292f49294e31fc7a1 in / 
# Tue, 25 Oct 2022 01:44:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:17:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:17:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:17:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:17:27 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:17:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:17:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:18:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:18:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:18:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:18:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:19:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:19:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:20:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fd31ec14dccdcda8f2472547f1a94ef0a23b8dabb764cd7b1d48aeee0afea7c8`  
		Last Modified: Tue, 25 Oct 2022 01:48:15 GMT  
		Size: 50.4 MB (50447742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7bb5a8d4409ae76ed240704c8628d248a907ec454b12a0f653fa5180822f32`  
		Last Modified: Tue, 25 Oct 2022 07:56:14 GMT  
		Size: 10.9 MB (10896941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9831692d445c53ad6706089a3b147d293d3267dd486b27109a911c9da182ed31`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2beecf1c3569265300a22936ddda05e835f0c83b2193ea68b4d60f2882113cd`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834cb0e33271e58107ddec676304ba095210344f2ee4310bb860d12b941b510c`  
		Last Modified: Tue, 25 Oct 2022 07:56:46 GMT  
		Size: 239.2 MB (239209563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdd4ac8f13eeeb7f19f875b6a9191a3aedf9fd8006aae02db37664d36f51883`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f066880bf184688bbe3b3bce165ab3ad72850aae130b41b408020b47003491`  
		Last Modified: Tue, 25 Oct 2022 07:57:07 GMT  
		Size: 86.6 MB (86586144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c12225f8506452bbdfb135687a0e9642f4fd2bec37dacde2ff8e68f0031c8`  
		Last Modified: Tue, 25 Oct 2022 07:56:53 GMT  
		Size: 326.7 KB (326687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cb66701beaeeb105d227e3c100dab245e25d8e913dcb72fb68145181a9140f`  
		Last Modified: Tue, 25 Oct 2022 07:57:05 GMT  
		Size: 76.0 MB (75978159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f63a0255662de5afdca2ec51999af441f9c0591a5fcd779d7dd8fb7d38c5790`  
		Last Modified: Tue, 25 Oct 2022 07:58:52 GMT  
		Size: 488.0 MB (487993789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ee1b92f77252b3083bd127ec8aa1c76a2c454641b524359be69bc1e7949de58d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **868.2 MB (868217557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a49242fdf68650f6969de209830fd386aa06e87cb5ddb0a779714faaba78e1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:07 GMT
ADD file:21afa32c0395cc5046d09741d6821d21cfd9b77bce46ebcfc8fd9aca57c73648 in / 
# Tue, 25 Oct 2022 05:46:08 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:25:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:25:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 21:25:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:25:32 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:25:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:25:32 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 21:27:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:27:07 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:27:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:27:07 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:27:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:27:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:28:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:32:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3ba81f4c3c21f92780061ee116827d64ac4edbcd02b056845c2aaa3097b730ed`  
		Last Modified: Tue, 25 Oct 2022 05:49:24 GMT  
		Size: 49.2 MB (49233280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d908f4a3bf1681c533c1f96d98947d2633d0dcaba9dfd301e3012eccad131bc6`  
		Last Modified: Tue, 25 Oct 2022 22:03:50 GMT  
		Size: 10.9 MB (10902593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83583a72ce25a255e794a38648eb0801f9216da38498d62ffb9804978957d95`  
		Last Modified: Tue, 25 Oct 2022 22:03:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1a43410632b0d298d4c6dd3c98b00cf2db2e6c8f50916bd61fcb89cda1d392`  
		Last Modified: Tue, 25 Oct 2022 22:03:48 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae854a5636ab767fe777452319631201aee587f29bea10e23ec81f5b368c445e`  
		Last Modified: Tue, 25 Oct 2022 22:04:20 GMT  
		Size: 184.4 MB (184376816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ab694da339128addba43dd72984d8b40529266d26831ea594d60a8e3cd25b3`  
		Last Modified: Tue, 25 Oct 2022 22:03:48 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b981c9cfec0e372d9f2e94116b59186d02a91e10dd99e9a8a10431e4e413f65`  
		Last Modified: Tue, 25 Oct 2022 22:04:37 GMT  
		Size: 84.4 MB (84372303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f047284ff16936b6148e2a2a68062d6263f473b9a42b4c1c0f1aa1fb42ed60c8`  
		Last Modified: Tue, 25 Oct 2022 22:04:28 GMT  
		Size: 326.7 KB (326683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de179756dba0e248264ebf803f000dce4ddada0cbe200f61a3fbeaf9c6a7e9e`  
		Last Modified: Tue, 25 Oct 2022 22:04:36 GMT  
		Size: 74.1 MB (74089547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16498b836fc2399503b84eb7c0c674a6e3152b721b939d78a718128d86cf268`  
		Last Modified: Tue, 25 Oct 2022 22:05:55 GMT  
		Size: 464.9 MB (464913925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:46cae435f6f7ea8d7043e84fd95a8b98bdf95c4dd950fbc08741298fb7bb1de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:cbbb6aa7e54b07b867ea1c6fefab9c1bd83f795f6e3a30a499c0a1f595db15c4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.1 MB (835147503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d806f6ce0fd63436af5228a1d9a4209bb5f7f8de53205864e5319df8784e227`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:04:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:07:31 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:07:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:07:31 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:08:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:08:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:16:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcba2703cc13554dd6ac252966be0f9f0a9d6e79ee879b5e0289457bc632f55`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617320b8300618f53ec135b976c7f3a733354c5ef799b7c969108d82a8509f8`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065fe084d225480619420eb81fce25e1ea4e12e4f4b95002773742fc0e01d67`  
		Last Modified: Tue, 25 Oct 2022 07:53:37 GMT  
		Size: 177.0 MB (177008909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f66f6a9e5d5690a6fcd01f03ca5ef0146410fa911f6fccb17d73db1bbec814`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcd60406762b57a7de1c5c937562c8a145da66c5f0d5716f70f5c5ae115ab71`  
		Last Modified: Tue, 25 Oct 2022 07:53:56 GMT  
		Size: 50.9 MB (50940379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb29d90361859f6ac155a32b08124b4fecb3b64649f15b68b7d6b59f22d70d4`  
		Last Modified: Tue, 25 Oct 2022 07:53:47 GMT  
		Size: 332.1 KB (332101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055f4ec67f38d1b1c161894d68208d46a4d5822664774d4554aaf150f243341c`  
		Last Modified: Tue, 25 Oct 2022 07:54:01 GMT  
		Size: 79.6 MB (79603171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96304f40d98ec3ee8f481818e18af495a0d8da05d780423f6da8294be3c5fcc1`  
		Last Modified: Tue, 25 Oct 2022 07:55:56 GMT  
		Size: 492.0 MB (491967513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:d3a05ef88d081e15785fcfe16ff2c65f1202d8e5ec15369b110b406ff066c6bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.2 MB (726177866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2302d2ee97aca1cc80e68f815cc9e06f1b146c7567089608a5feb883d948ea4a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:52:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:52:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 06 Oct 2022 06:53:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:16 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:53:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:53:16 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:53:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:57:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ab6ac546133bf21e51dc29641d455c42144b184821f494258ff1ec514556c`  
		Last Modified: Thu, 06 Oct 2022 07:00:40 GMT  
		Size: 1.2 MB (1163905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706759f53c150848596edb49143a211c7e072793acea609cc8e9c0f267c4e3e`  
		Last Modified: Thu, 06 Oct 2022 07:00:38 GMT  
		Size: 4.7 MB (4675577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b0360f8c716b3c493ff9708abd3c165f9de06193430830ea64d829b1a6ac2`  
		Last Modified: Thu, 06 Oct 2022 07:00:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd789251f14b7842f745c35075b3e7f88a5aa3fb3b005a3bd0fde7d8f285d7f`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24248fc7fc767d03259bb795d6c177495b4f61cdb1ddcc6a6bb9bb7dcd5958db`  
		Last Modified: Thu, 06 Oct 2022 07:01:15 GMT  
		Size: 157.6 MB (157550749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1b296e1c261f003a529641cc88d1393116b3a0b1f7853da9463a2e9c16df7c`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1461e09b998de0d3b7ae285e2a3bb8bcb1b889f8a12f832e208d7ec8d3bfe847`  
		Last Modified: Thu, 06 Oct 2022 07:01:36 GMT  
		Size: 40.5 MB (40505592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e355cb57c65a1dc870c88f7e383d6a76770d5f6563b605a9a96dc5ceb24b3a`  
		Last Modified: Thu, 06 Oct 2022 07:01:28 GMT  
		Size: 329.9 KB (329943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b0b621043424762e62d798dd71533b7835ccd3741e94dcdc7fbbdd3ca4f723`  
		Last Modified: Thu, 06 Oct 2022 07:01:40 GMT  
		Size: 60.5 MB (60479707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed30924832b5259516fe54fa5708a8ae36898b16de1c94f0898baa3d5d3b84a`  
		Last Modified: Thu, 06 Oct 2022 07:03:20 GMT  
		Size: 436.9 MB (436879892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6a56e4c46dd57c138947ba191f82579cbebc7bc8be157b4afdc98279d0c2824a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.4 MB (785391798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e9ded839737165910ae71f3043672969d898b0aea25743168af6643850474c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 21:11:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:11:42 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 21:14:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:14:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:14:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:14:39 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:15:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:15:26 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:17:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:25:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7354b266abeda9b5bfbca97ad1c6887d2a277d69ff8c607591a279459548ac7`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d614279c49f19055c903676e10afd41c8a3cd40f35d8b708fb499f7b5eeb965f`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c1b3c16d04da075eb127cecb646f3fbb43b07575ac781c7f670ca3f1885796`  
		Last Modified: Tue, 25 Oct 2022 22:01:55 GMT  
		Size: 171.4 MB (171447425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ac303ffe5e80a8c48e68fb479034e19261f5b6990dd5100bc6ddb1c7cd38ff`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4148c35466d56fca5bdd1144c7cc49f7c57ff22d51ce5c197995f215040f68d6`  
		Last Modified: Tue, 25 Oct 2022 22:02:11 GMT  
		Size: 45.2 MB (45204375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b385026becc2dcce049f0ab39c7d58c6459f28965efe78e7ee77336f82328a45`  
		Last Modified: Tue, 25 Oct 2022 22:02:05 GMT  
		Size: 332.1 KB (332102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d152eaa0a13418a883f576ea85d8893f1cdcafe87fc965ff14ee47fd4e076e7`  
		Last Modified: Tue, 25 Oct 2022 22:02:14 GMT  
		Size: 72.0 MB (71974237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35aa43327036965b93b120edc9468bb69de8263d58440de8ffc83cab8e59a269`  
		Last Modified: Tue, 25 Oct 2022 22:03:38 GMT  
		Size: 462.5 MB (462538038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:9dbaa194472da645623e6d409612905be929185d5e3181d2940e6f4cf2b15714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:f2cb64c09356a71a17270f40ae8e9d42d242509547d47b395d46e04fbfaa5c93
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359041151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aae48c851939de656e19f202234d0491e2bf82aa82870ab8070c404b34a0bda`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:04:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:07:31 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:07:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:07:31 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:08:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:08:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:10:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcba2703cc13554dd6ac252966be0f9f0a9d6e79ee879b5e0289457bc632f55`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617320b8300618f53ec135b976c7f3a733354c5ef799b7c969108d82a8509f8`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065fe084d225480619420eb81fce25e1ea4e12e4f4b95002773742fc0e01d67`  
		Last Modified: Tue, 25 Oct 2022 07:53:37 GMT  
		Size: 177.0 MB (177008909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f66f6a9e5d5690a6fcd01f03ca5ef0146410fa911f6fccb17d73db1bbec814`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcd60406762b57a7de1c5c937562c8a145da66c5f0d5716f70f5c5ae115ab71`  
		Last Modified: Tue, 25 Oct 2022 07:53:56 GMT  
		Size: 50.9 MB (50940379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb29d90361859f6ac155a32b08124b4fecb3b64649f15b68b7d6b59f22d70d4`  
		Last Modified: Tue, 25 Oct 2022 07:53:47 GMT  
		Size: 332.1 KB (332101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055f4ec67f38d1b1c161894d68208d46a4d5822664774d4554aaf150f243341c`  
		Last Modified: Tue, 25 Oct 2022 07:54:01 GMT  
		Size: 79.6 MB (79603171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a67e64bc6cfc11803ed4fdb948911a3d1d22b6f40e7ed61cd815d62c050a4fc`  
		Last Modified: Tue, 25 Oct 2022 07:54:17 GMT  
		Size: 15.9 MB (15861161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:931a8f67e0e7779bbadc154d28cb081ecc3163db2b77ac9539c413644b6ceff5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303363136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205efb50cd40a2dadaee4531776d2a257c8fce1a9728465df5468491f976aac3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:52:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:52:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 06 Oct 2022 06:53:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:16 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:53:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:53:16 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:53:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:54:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ab6ac546133bf21e51dc29641d455c42144b184821f494258ff1ec514556c`  
		Last Modified: Thu, 06 Oct 2022 07:00:40 GMT  
		Size: 1.2 MB (1163905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706759f53c150848596edb49143a211c7e072793acea609cc8e9c0f267c4e3e`  
		Last Modified: Thu, 06 Oct 2022 07:00:38 GMT  
		Size: 4.7 MB (4675577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b0360f8c716b3c493ff9708abd3c165f9de06193430830ea64d829b1a6ac2`  
		Last Modified: Thu, 06 Oct 2022 07:00:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd789251f14b7842f745c35075b3e7f88a5aa3fb3b005a3bd0fde7d8f285d7f`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24248fc7fc767d03259bb795d6c177495b4f61cdb1ddcc6a6bb9bb7dcd5958db`  
		Last Modified: Thu, 06 Oct 2022 07:01:15 GMT  
		Size: 157.6 MB (157550749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1b296e1c261f003a529641cc88d1393116b3a0b1f7853da9463a2e9c16df7c`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1461e09b998de0d3b7ae285e2a3bb8bcb1b889f8a12f832e208d7ec8d3bfe847`  
		Last Modified: Thu, 06 Oct 2022 07:01:36 GMT  
		Size: 40.5 MB (40505592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e355cb57c65a1dc870c88f7e383d6a76770d5f6563b605a9a96dc5ceb24b3a`  
		Last Modified: Thu, 06 Oct 2022 07:01:28 GMT  
		Size: 329.9 KB (329943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b0b621043424762e62d798dd71533b7835ccd3741e94dcdc7fbbdd3ca4f723`  
		Last Modified: Thu, 06 Oct 2022 07:01:40 GMT  
		Size: 60.5 MB (60479707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4213011fc7a49cf580c896c00969f42891823b1dbe5356b6a627e03ac4bd6e13`  
		Last Modified: Thu, 06 Oct 2022 07:01:58 GMT  
		Size: 14.1 MB (14065162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:35c0807c3a9674796b7ff7b819fbd159fc13f69dc3034a817a170c98c29ebee6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338307578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb6fdbc1a68f4521e7fb3e4b2a4c8d83f26b47cd5b4233095f12c3dd95ec6a1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 21:11:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:11:42 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 21:14:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:14:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:14:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:14:39 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:15:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:15:26 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:17:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:17:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7354b266abeda9b5bfbca97ad1c6887d2a277d69ff8c607591a279459548ac7`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d614279c49f19055c903676e10afd41c8a3cd40f35d8b708fb499f7b5eeb965f`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c1b3c16d04da075eb127cecb646f3fbb43b07575ac781c7f670ca3f1885796`  
		Last Modified: Tue, 25 Oct 2022 22:01:55 GMT  
		Size: 171.4 MB (171447425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ac303ffe5e80a8c48e68fb479034e19261f5b6990dd5100bc6ddb1c7cd38ff`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4148c35466d56fca5bdd1144c7cc49f7c57ff22d51ce5c197995f215040f68d6`  
		Last Modified: Tue, 25 Oct 2022 22:02:11 GMT  
		Size: 45.2 MB (45204375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b385026becc2dcce049f0ab39c7d58c6459f28965efe78e7ee77336f82328a45`  
		Last Modified: Tue, 25 Oct 2022 22:02:05 GMT  
		Size: 332.1 KB (332102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d152eaa0a13418a883f576ea85d8893f1cdcafe87fc965ff14ee47fd4e076e7`  
		Last Modified: Tue, 25 Oct 2022 22:02:14 GMT  
		Size: 72.0 MB (71974237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1ae12efe38c9f33d969d096b063141edbfda6df668fbb72467712d72e825b5`  
		Last Modified: Tue, 25 Oct 2022 22:02:29 GMT  
		Size: 15.5 MB (15453818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:a614d790d60c866839315e5357c1722a0a37532d2a4f28fb4af7ba8aecf70ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:1df3c892d86fd452b24e82eaee409fa376a344437411ebcc64174f683cc20db5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.9 MB (484899656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe1b1975f4b9abbde15c6fa7066017b6b11ed67f9bed0616d47b9d8eaa078533`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:02 GMT
ADD file:259be79d94a2549a667ad08a093fe18f15a6c93d66a0723292f49294e31fc7a1 in / 
# Tue, 25 Oct 2022 01:44:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:17:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:17:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:17:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:17:27 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:17:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:17:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:18:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:18:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:18:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:18:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:19:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:19:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:20:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:20:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fd31ec14dccdcda8f2472547f1a94ef0a23b8dabb764cd7b1d48aeee0afea7c8`  
		Last Modified: Tue, 25 Oct 2022 01:48:15 GMT  
		Size: 50.4 MB (50447742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7bb5a8d4409ae76ed240704c8628d248a907ec454b12a0f653fa5180822f32`  
		Last Modified: Tue, 25 Oct 2022 07:56:14 GMT  
		Size: 10.9 MB (10896941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9831692d445c53ad6706089a3b147d293d3267dd486b27109a911c9da182ed31`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2beecf1c3569265300a22936ddda05e835f0c83b2193ea68b4d60f2882113cd`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834cb0e33271e58107ddec676304ba095210344f2ee4310bb860d12b941b510c`  
		Last Modified: Tue, 25 Oct 2022 07:56:46 GMT  
		Size: 239.2 MB (239209563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdd4ac8f13eeeb7f19f875b6a9191a3aedf9fd8006aae02db37664d36f51883`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f066880bf184688bbe3b3bce165ab3ad72850aae130b41b408020b47003491`  
		Last Modified: Tue, 25 Oct 2022 07:57:07 GMT  
		Size: 86.6 MB (86586144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c12225f8506452bbdfb135687a0e9642f4fd2bec37dacde2ff8e68f0031c8`  
		Last Modified: Tue, 25 Oct 2022 07:56:53 GMT  
		Size: 326.7 KB (326687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cb66701beaeeb105d227e3c100dab245e25d8e913dcb72fb68145181a9140f`  
		Last Modified: Tue, 25 Oct 2022 07:57:05 GMT  
		Size: 76.0 MB (75978159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e243b3e8516342ad34ac067531d9d7545ff8c35ac1742dfad88b051b3b043db`  
		Last Modified: Tue, 25 Oct 2022 07:57:18 GMT  
		Size: 21.5 MB (21452008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:19922028f6b49d6d09a7dcf2dfdfb0602fffdd7564000927baa07171288ff7bc
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.4 MB (424420034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0fd3595ce9dd62353737ecf7cbd4bba02f47897cf8991c41ae3a5f9aed63bc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:07 GMT
ADD file:21afa32c0395cc5046d09741d6821d21cfd9b77bce46ebcfc8fd9aca57c73648 in / 
# Tue, 25 Oct 2022 05:46:08 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:25:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:25:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 21:25:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:25:32 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:25:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:25:32 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 21:27:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:27:07 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:27:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:27:07 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:27:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:27:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:28:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:29:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3ba81f4c3c21f92780061ee116827d64ac4edbcd02b056845c2aaa3097b730ed`  
		Last Modified: Tue, 25 Oct 2022 05:49:24 GMT  
		Size: 49.2 MB (49233280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d908f4a3bf1681c533c1f96d98947d2633d0dcaba9dfd301e3012eccad131bc6`  
		Last Modified: Tue, 25 Oct 2022 22:03:50 GMT  
		Size: 10.9 MB (10902593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83583a72ce25a255e794a38648eb0801f9216da38498d62ffb9804978957d95`  
		Last Modified: Tue, 25 Oct 2022 22:03:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1a43410632b0d298d4c6dd3c98b00cf2db2e6c8f50916bd61fcb89cda1d392`  
		Last Modified: Tue, 25 Oct 2022 22:03:48 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae854a5636ab767fe777452319631201aee587f29bea10e23ec81f5b368c445e`  
		Last Modified: Tue, 25 Oct 2022 22:04:20 GMT  
		Size: 184.4 MB (184376816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ab694da339128addba43dd72984d8b40529266d26831ea594d60a8e3cd25b3`  
		Last Modified: Tue, 25 Oct 2022 22:03:48 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b981c9cfec0e372d9f2e94116b59186d02a91e10dd99e9a8a10431e4e413f65`  
		Last Modified: Tue, 25 Oct 2022 22:04:37 GMT  
		Size: 84.4 MB (84372303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f047284ff16936b6148e2a2a68062d6263f473b9a42b4c1c0f1aa1fb42ed60c8`  
		Last Modified: Tue, 25 Oct 2022 22:04:28 GMT  
		Size: 326.7 KB (326683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de179756dba0e248264ebf803f000dce4ddada0cbe200f61a3fbeaf9c6a7e9e`  
		Last Modified: Tue, 25 Oct 2022 22:04:36 GMT  
		Size: 74.1 MB (74089547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907d729e88d33d7e3b8823bd9b2711a8c01c6365ee6549670e0fe8d8c1bbdfd6`  
		Last Modified: Tue, 25 Oct 2022 22:04:48 GMT  
		Size: 21.1 MB (21116402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:9dbaa194472da645623e6d409612905be929185d5e3181d2940e6f4cf2b15714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:f2cb64c09356a71a17270f40ae8e9d42d242509547d47b395d46e04fbfaa5c93
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359041151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aae48c851939de656e19f202234d0491e2bf82aa82870ab8070c404b34a0bda`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:04:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:07:31 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:07:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:07:31 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:08:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:08:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:10:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcba2703cc13554dd6ac252966be0f9f0a9d6e79ee879b5e0289457bc632f55`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617320b8300618f53ec135b976c7f3a733354c5ef799b7c969108d82a8509f8`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065fe084d225480619420eb81fce25e1ea4e12e4f4b95002773742fc0e01d67`  
		Last Modified: Tue, 25 Oct 2022 07:53:37 GMT  
		Size: 177.0 MB (177008909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f66f6a9e5d5690a6fcd01f03ca5ef0146410fa911f6fccb17d73db1bbec814`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcd60406762b57a7de1c5c937562c8a145da66c5f0d5716f70f5c5ae115ab71`  
		Last Modified: Tue, 25 Oct 2022 07:53:56 GMT  
		Size: 50.9 MB (50940379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb29d90361859f6ac155a32b08124b4fecb3b64649f15b68b7d6b59f22d70d4`  
		Last Modified: Tue, 25 Oct 2022 07:53:47 GMT  
		Size: 332.1 KB (332101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055f4ec67f38d1b1c161894d68208d46a4d5822664774d4554aaf150f243341c`  
		Last Modified: Tue, 25 Oct 2022 07:54:01 GMT  
		Size: 79.6 MB (79603171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a67e64bc6cfc11803ed4fdb948911a3d1d22b6f40e7ed61cd815d62c050a4fc`  
		Last Modified: Tue, 25 Oct 2022 07:54:17 GMT  
		Size: 15.9 MB (15861161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:931a8f67e0e7779bbadc154d28cb081ecc3163db2b77ac9539c413644b6ceff5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303363136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205efb50cd40a2dadaee4531776d2a257c8fce1a9728465df5468491f976aac3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:52:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:52:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 06 Oct 2022 06:53:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:16 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:53:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:53:16 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:53:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:54:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ab6ac546133bf21e51dc29641d455c42144b184821f494258ff1ec514556c`  
		Last Modified: Thu, 06 Oct 2022 07:00:40 GMT  
		Size: 1.2 MB (1163905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706759f53c150848596edb49143a211c7e072793acea609cc8e9c0f267c4e3e`  
		Last Modified: Thu, 06 Oct 2022 07:00:38 GMT  
		Size: 4.7 MB (4675577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b0360f8c716b3c493ff9708abd3c165f9de06193430830ea64d829b1a6ac2`  
		Last Modified: Thu, 06 Oct 2022 07:00:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd789251f14b7842f745c35075b3e7f88a5aa3fb3b005a3bd0fde7d8f285d7f`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24248fc7fc767d03259bb795d6c177495b4f61cdb1ddcc6a6bb9bb7dcd5958db`  
		Last Modified: Thu, 06 Oct 2022 07:01:15 GMT  
		Size: 157.6 MB (157550749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1b296e1c261f003a529641cc88d1393116b3a0b1f7853da9463a2e9c16df7c`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1461e09b998de0d3b7ae285e2a3bb8bcb1b889f8a12f832e208d7ec8d3bfe847`  
		Last Modified: Thu, 06 Oct 2022 07:01:36 GMT  
		Size: 40.5 MB (40505592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e355cb57c65a1dc870c88f7e383d6a76770d5f6563b605a9a96dc5ceb24b3a`  
		Last Modified: Thu, 06 Oct 2022 07:01:28 GMT  
		Size: 329.9 KB (329943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b0b621043424762e62d798dd71533b7835ccd3741e94dcdc7fbbdd3ca4f723`  
		Last Modified: Thu, 06 Oct 2022 07:01:40 GMT  
		Size: 60.5 MB (60479707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4213011fc7a49cf580c896c00969f42891823b1dbe5356b6a627e03ac4bd6e13`  
		Last Modified: Thu, 06 Oct 2022 07:01:58 GMT  
		Size: 14.1 MB (14065162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:35c0807c3a9674796b7ff7b819fbd159fc13f69dc3034a817a170c98c29ebee6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338307578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb6fdbc1a68f4521e7fb3e4b2a4c8d83f26b47cd5b4233095f12c3dd95ec6a1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 21:11:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:11:42 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 21:14:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:14:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:14:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:14:39 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:15:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:15:26 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:17:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:17:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7354b266abeda9b5bfbca97ad1c6887d2a277d69ff8c607591a279459548ac7`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d614279c49f19055c903676e10afd41c8a3cd40f35d8b708fb499f7b5eeb965f`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c1b3c16d04da075eb127cecb646f3fbb43b07575ac781c7f670ca3f1885796`  
		Last Modified: Tue, 25 Oct 2022 22:01:55 GMT  
		Size: 171.4 MB (171447425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ac303ffe5e80a8c48e68fb479034e19261f5b6990dd5100bc6ddb1c7cd38ff`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4148c35466d56fca5bdd1144c7cc49f7c57ff22d51ce5c197995f215040f68d6`  
		Last Modified: Tue, 25 Oct 2022 22:02:11 GMT  
		Size: 45.2 MB (45204375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b385026becc2dcce049f0ab39c7d58c6459f28965efe78e7ee77336f82328a45`  
		Last Modified: Tue, 25 Oct 2022 22:02:05 GMT  
		Size: 332.1 KB (332102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d152eaa0a13418a883f576ea85d8893f1cdcafe87fc965ff14ee47fd4e076e7`  
		Last Modified: Tue, 25 Oct 2022 22:02:14 GMT  
		Size: 72.0 MB (71974237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1ae12efe38c9f33d969d096b063141edbfda6df668fbb72467712d72e825b5`  
		Last Modified: Tue, 25 Oct 2022 22:02:29 GMT  
		Size: 15.5 MB (15453818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:2f00fb3ac6187568298b4392ec718c27858dc34bacc4dd940a2cc6f2826fcd4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:34cbfe55d811fe7c57add8b3d6f01ba9c209258ef1b4029cec5118dcd21e358f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343179990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6d7ab7e066ec3cc62a3c2bfe041ba6a0a444f0b66da68886d72c1906c5004a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:04:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:07:31 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:07:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:07:31 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:08:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:08:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcba2703cc13554dd6ac252966be0f9f0a9d6e79ee879b5e0289457bc632f55`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617320b8300618f53ec135b976c7f3a733354c5ef799b7c969108d82a8509f8`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065fe084d225480619420eb81fce25e1ea4e12e4f4b95002773742fc0e01d67`  
		Last Modified: Tue, 25 Oct 2022 07:53:37 GMT  
		Size: 177.0 MB (177008909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f66f6a9e5d5690a6fcd01f03ca5ef0146410fa911f6fccb17d73db1bbec814`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcd60406762b57a7de1c5c937562c8a145da66c5f0d5716f70f5c5ae115ab71`  
		Last Modified: Tue, 25 Oct 2022 07:53:56 GMT  
		Size: 50.9 MB (50940379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb29d90361859f6ac155a32b08124b4fecb3b64649f15b68b7d6b59f22d70d4`  
		Last Modified: Tue, 25 Oct 2022 07:53:47 GMT  
		Size: 332.1 KB (332101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055f4ec67f38d1b1c161894d68208d46a4d5822664774d4554aaf150f243341c`  
		Last Modified: Tue, 25 Oct 2022 07:54:01 GMT  
		Size: 79.6 MB (79603171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:282eece3c6e182e825057bcb769c29ec38c0a3e9b2c9cb0b913ede9dec5a8ccd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289297974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727b6d344ef45add4b6b86083e60223e9bb9840f5052ac125292637db637ef91`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:52:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:52:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 06 Oct 2022 06:53:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:16 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:53:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:53:16 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:53:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ab6ac546133bf21e51dc29641d455c42144b184821f494258ff1ec514556c`  
		Last Modified: Thu, 06 Oct 2022 07:00:40 GMT  
		Size: 1.2 MB (1163905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706759f53c150848596edb49143a211c7e072793acea609cc8e9c0f267c4e3e`  
		Last Modified: Thu, 06 Oct 2022 07:00:38 GMT  
		Size: 4.7 MB (4675577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b0360f8c716b3c493ff9708abd3c165f9de06193430830ea64d829b1a6ac2`  
		Last Modified: Thu, 06 Oct 2022 07:00:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd789251f14b7842f745c35075b3e7f88a5aa3fb3b005a3bd0fde7d8f285d7f`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24248fc7fc767d03259bb795d6c177495b4f61cdb1ddcc6a6bb9bb7dcd5958db`  
		Last Modified: Thu, 06 Oct 2022 07:01:15 GMT  
		Size: 157.6 MB (157550749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1b296e1c261f003a529641cc88d1393116b3a0b1f7853da9463a2e9c16df7c`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1461e09b998de0d3b7ae285e2a3bb8bcb1b889f8a12f832e208d7ec8d3bfe847`  
		Last Modified: Thu, 06 Oct 2022 07:01:36 GMT  
		Size: 40.5 MB (40505592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e355cb57c65a1dc870c88f7e383d6a76770d5f6563b605a9a96dc5ceb24b3a`  
		Last Modified: Thu, 06 Oct 2022 07:01:28 GMT  
		Size: 329.9 KB (329943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b0b621043424762e62d798dd71533b7835ccd3741e94dcdc7fbbdd3ca4f723`  
		Last Modified: Thu, 06 Oct 2022 07:01:40 GMT  
		Size: 60.5 MB (60479707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:01d2a5693cbb33946e8b06971fe471d2fb165267fdbcb711dabe777d24337749
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.9 MB (322853760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8198d039a3796669f31af0d2cd9fe7c58a960e811af29f1768be002666b9167a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 21:11:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:11:42 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 21:14:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:14:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:14:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:14:39 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:15:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:15:26 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:17:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7354b266abeda9b5bfbca97ad1c6887d2a277d69ff8c607591a279459548ac7`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d614279c49f19055c903676e10afd41c8a3cd40f35d8b708fb499f7b5eeb965f`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c1b3c16d04da075eb127cecb646f3fbb43b07575ac781c7f670ca3f1885796`  
		Last Modified: Tue, 25 Oct 2022 22:01:55 GMT  
		Size: 171.4 MB (171447425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ac303ffe5e80a8c48e68fb479034e19261f5b6990dd5100bc6ddb1c7cd38ff`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4148c35466d56fca5bdd1144c7cc49f7c57ff22d51ce5c197995f215040f68d6`  
		Last Modified: Tue, 25 Oct 2022 22:02:11 GMT  
		Size: 45.2 MB (45204375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b385026becc2dcce049f0ab39c7d58c6459f28965efe78e7ee77336f82328a45`  
		Last Modified: Tue, 25 Oct 2022 22:02:05 GMT  
		Size: 332.1 KB (332102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d152eaa0a13418a883f576ea85d8893f1cdcafe87fc965ff14ee47fd4e076e7`  
		Last Modified: Tue, 25 Oct 2022 22:02:14 GMT  
		Size: 72.0 MB (71974237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:4963d81fa53f3fde4c142e189e724ea6fce303fdc0507fc155234146d8df5db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:953694421478b83fbba6976e01a5b90cad68357b90f6529b7d2ef1b3446a00c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.4 MB (463447648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761281453a86dd6f2a1f49082e6d95a477f3f57b89d6a5be4bfd28b811b19c6e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:02 GMT
ADD file:259be79d94a2549a667ad08a093fe18f15a6c93d66a0723292f49294e31fc7a1 in / 
# Tue, 25 Oct 2022 01:44:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:17:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:17:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:17:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:17:27 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:17:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:17:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:18:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:18:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:18:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:18:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:19:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:19:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:20:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fd31ec14dccdcda8f2472547f1a94ef0a23b8dabb764cd7b1d48aeee0afea7c8`  
		Last Modified: Tue, 25 Oct 2022 01:48:15 GMT  
		Size: 50.4 MB (50447742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7bb5a8d4409ae76ed240704c8628d248a907ec454b12a0f653fa5180822f32`  
		Last Modified: Tue, 25 Oct 2022 07:56:14 GMT  
		Size: 10.9 MB (10896941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9831692d445c53ad6706089a3b147d293d3267dd486b27109a911c9da182ed31`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2beecf1c3569265300a22936ddda05e835f0c83b2193ea68b4d60f2882113cd`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834cb0e33271e58107ddec676304ba095210344f2ee4310bb860d12b941b510c`  
		Last Modified: Tue, 25 Oct 2022 07:56:46 GMT  
		Size: 239.2 MB (239209563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdd4ac8f13eeeb7f19f875b6a9191a3aedf9fd8006aae02db37664d36f51883`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f066880bf184688bbe3b3bce165ab3ad72850aae130b41b408020b47003491`  
		Last Modified: Tue, 25 Oct 2022 07:57:07 GMT  
		Size: 86.6 MB (86586144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c12225f8506452bbdfb135687a0e9642f4fd2bec37dacde2ff8e68f0031c8`  
		Last Modified: Tue, 25 Oct 2022 07:56:53 GMT  
		Size: 326.7 KB (326687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cb66701beaeeb105d227e3c100dab245e25d8e913dcb72fb68145181a9140f`  
		Last Modified: Tue, 25 Oct 2022 07:57:05 GMT  
		Size: 76.0 MB (75978159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dafb622bd0ec9c3b26dbddbfbea7811f23b16c2763a7cfedff27ce00dc3291fb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.3 MB (403303632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907dceb9ca2faa0d1ce52ae69c6569c16777514bca500657a2c0643760f5fcbc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:07 GMT
ADD file:21afa32c0395cc5046d09741d6821d21cfd9b77bce46ebcfc8fd9aca57c73648 in / 
# Tue, 25 Oct 2022 05:46:08 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:25:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:25:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 21:25:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:25:32 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:25:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:25:32 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 21:27:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:27:07 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:27:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:27:07 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:27:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:27:45 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:28:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3ba81f4c3c21f92780061ee116827d64ac4edbcd02b056845c2aaa3097b730ed`  
		Last Modified: Tue, 25 Oct 2022 05:49:24 GMT  
		Size: 49.2 MB (49233280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d908f4a3bf1681c533c1f96d98947d2633d0dcaba9dfd301e3012eccad131bc6`  
		Last Modified: Tue, 25 Oct 2022 22:03:50 GMT  
		Size: 10.9 MB (10902593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83583a72ce25a255e794a38648eb0801f9216da38498d62ffb9804978957d95`  
		Last Modified: Tue, 25 Oct 2022 22:03:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1a43410632b0d298d4c6dd3c98b00cf2db2e6c8f50916bd61fcb89cda1d392`  
		Last Modified: Tue, 25 Oct 2022 22:03:48 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae854a5636ab767fe777452319631201aee587f29bea10e23ec81f5b368c445e`  
		Last Modified: Tue, 25 Oct 2022 22:04:20 GMT  
		Size: 184.4 MB (184376816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ab694da339128addba43dd72984d8b40529266d26831ea594d60a8e3cd25b3`  
		Last Modified: Tue, 25 Oct 2022 22:03:48 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b981c9cfec0e372d9f2e94116b59186d02a91e10dd99e9a8a10431e4e413f65`  
		Last Modified: Tue, 25 Oct 2022 22:04:37 GMT  
		Size: 84.4 MB (84372303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f047284ff16936b6148e2a2a68062d6263f473b9a42b4c1c0f1aa1fb42ed60c8`  
		Last Modified: Tue, 25 Oct 2022 22:04:28 GMT  
		Size: 326.7 KB (326683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de179756dba0e248264ebf803f000dce4ddada0cbe200f61a3fbeaf9c6a7e9e`  
		Last Modified: Tue, 25 Oct 2022 22:04:36 GMT  
		Size: 74.1 MB (74089547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:2f00fb3ac6187568298b4392ec718c27858dc34bacc4dd940a2cc6f2826fcd4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:34cbfe55d811fe7c57add8b3d6f01ba9c209258ef1b4029cec5118dcd21e358f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343179990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6d7ab7e066ec3cc62a3c2bfe041ba6a0a444f0b66da68886d72c1906c5004a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:04:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:07:31 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:07:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:07:31 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:08:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:08:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcba2703cc13554dd6ac252966be0f9f0a9d6e79ee879b5e0289457bc632f55`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617320b8300618f53ec135b976c7f3a733354c5ef799b7c969108d82a8509f8`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065fe084d225480619420eb81fce25e1ea4e12e4f4b95002773742fc0e01d67`  
		Last Modified: Tue, 25 Oct 2022 07:53:37 GMT  
		Size: 177.0 MB (177008909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f66f6a9e5d5690a6fcd01f03ca5ef0146410fa911f6fccb17d73db1bbec814`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcd60406762b57a7de1c5c937562c8a145da66c5f0d5716f70f5c5ae115ab71`  
		Last Modified: Tue, 25 Oct 2022 07:53:56 GMT  
		Size: 50.9 MB (50940379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb29d90361859f6ac155a32b08124b4fecb3b64649f15b68b7d6b59f22d70d4`  
		Last Modified: Tue, 25 Oct 2022 07:53:47 GMT  
		Size: 332.1 KB (332101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055f4ec67f38d1b1c161894d68208d46a4d5822664774d4554aaf150f243341c`  
		Last Modified: Tue, 25 Oct 2022 07:54:01 GMT  
		Size: 79.6 MB (79603171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:282eece3c6e182e825057bcb769c29ec38c0a3e9b2c9cb0b913ede9dec5a8ccd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289297974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727b6d344ef45add4b6b86083e60223e9bb9840f5052ac125292637db637ef91`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:52:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:52:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 06 Oct 2022 06:53:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:16 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:53:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:53:16 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:53:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ab6ac546133bf21e51dc29641d455c42144b184821f494258ff1ec514556c`  
		Last Modified: Thu, 06 Oct 2022 07:00:40 GMT  
		Size: 1.2 MB (1163905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706759f53c150848596edb49143a211c7e072793acea609cc8e9c0f267c4e3e`  
		Last Modified: Thu, 06 Oct 2022 07:00:38 GMT  
		Size: 4.7 MB (4675577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b0360f8c716b3c493ff9708abd3c165f9de06193430830ea64d829b1a6ac2`  
		Last Modified: Thu, 06 Oct 2022 07:00:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd789251f14b7842f745c35075b3e7f88a5aa3fb3b005a3bd0fde7d8f285d7f`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24248fc7fc767d03259bb795d6c177495b4f61cdb1ddcc6a6bb9bb7dcd5958db`  
		Last Modified: Thu, 06 Oct 2022 07:01:15 GMT  
		Size: 157.6 MB (157550749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1b296e1c261f003a529641cc88d1393116b3a0b1f7853da9463a2e9c16df7c`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1461e09b998de0d3b7ae285e2a3bb8bcb1b889f8a12f832e208d7ec8d3bfe847`  
		Last Modified: Thu, 06 Oct 2022 07:01:36 GMT  
		Size: 40.5 MB (40505592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e355cb57c65a1dc870c88f7e383d6a76770d5f6563b605a9a96dc5ceb24b3a`  
		Last Modified: Thu, 06 Oct 2022 07:01:28 GMT  
		Size: 329.9 KB (329943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b0b621043424762e62d798dd71533b7835ccd3741e94dcdc7fbbdd3ca4f723`  
		Last Modified: Thu, 06 Oct 2022 07:01:40 GMT  
		Size: 60.5 MB (60479707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:01d2a5693cbb33946e8b06971fe471d2fb165267fdbcb711dabe777d24337749
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.9 MB (322853760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8198d039a3796669f31af0d2cd9fe7c58a960e811af29f1768be002666b9167a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 21:11:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:11:42 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 21:14:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:14:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:14:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:14:39 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:15:21 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:15:26 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:17:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7354b266abeda9b5bfbca97ad1c6887d2a277d69ff8c607591a279459548ac7`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d614279c49f19055c903676e10afd41c8a3cd40f35d8b708fb499f7b5eeb965f`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c1b3c16d04da075eb127cecb646f3fbb43b07575ac781c7f670ca3f1885796`  
		Last Modified: Tue, 25 Oct 2022 22:01:55 GMT  
		Size: 171.4 MB (171447425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ac303ffe5e80a8c48e68fb479034e19261f5b6990dd5100bc6ddb1c7cd38ff`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4148c35466d56fca5bdd1144c7cc49f7c57ff22d51ce5c197995f215040f68d6`  
		Last Modified: Tue, 25 Oct 2022 22:02:11 GMT  
		Size: 45.2 MB (45204375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b385026becc2dcce049f0ab39c7d58c6459f28965efe78e7ee77336f82328a45`  
		Last Modified: Tue, 25 Oct 2022 22:02:05 GMT  
		Size: 332.1 KB (332102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d152eaa0a13418a883f576ea85d8893f1cdcafe87fc965ff14ee47fd4e076e7`  
		Last Modified: Tue, 25 Oct 2022 22:02:14 GMT  
		Size: 72.0 MB (71974237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:73ba67c09c6ab756c57a1d8654d692f3055a8c7ec54b06f120e5b4f877e968ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:846f250f6dd222e44ee17b7f871875e20abd569082de6299b1d3fb89b4a60ee9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212304339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c78d80b5cf8bf8109d294a84172eb5bc1f718d08607ed579e63932bac8cfa9d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:04:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:07:31 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:07:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:07:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcba2703cc13554dd6ac252966be0f9f0a9d6e79ee879b5e0289457bc632f55`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617320b8300618f53ec135b976c7f3a733354c5ef799b7c969108d82a8509f8`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065fe084d225480619420eb81fce25e1ea4e12e4f4b95002773742fc0e01d67`  
		Last Modified: Tue, 25 Oct 2022 07:53:37 GMT  
		Size: 177.0 MB (177008909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f66f6a9e5d5690a6fcd01f03ca5ef0146410fa911f6fccb17d73db1bbec814`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:67ea8f522d8e90ade44c0d45a623b182c7dbb9f48f4b567f1079e6d3136ca48c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187982732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7c3f4179402fe66a367adbf02ca6941b11a372f4111ef176ab7c3c7de1f500`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:52:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:52:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 06 Oct 2022 06:53:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:16 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:53:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:53:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ab6ac546133bf21e51dc29641d455c42144b184821f494258ff1ec514556c`  
		Last Modified: Thu, 06 Oct 2022 07:00:40 GMT  
		Size: 1.2 MB (1163905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706759f53c150848596edb49143a211c7e072793acea609cc8e9c0f267c4e3e`  
		Last Modified: Thu, 06 Oct 2022 07:00:38 GMT  
		Size: 4.7 MB (4675577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b0360f8c716b3c493ff9708abd3c165f9de06193430830ea64d829b1a6ac2`  
		Last Modified: Thu, 06 Oct 2022 07:00:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd789251f14b7842f745c35075b3e7f88a5aa3fb3b005a3bd0fde7d8f285d7f`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24248fc7fc767d03259bb795d6c177495b4f61cdb1ddcc6a6bb9bb7dcd5958db`  
		Last Modified: Thu, 06 Oct 2022 07:01:15 GMT  
		Size: 157.6 MB (157550749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1b296e1c261f003a529641cc88d1393116b3a0b1f7853da9463a2e9c16df7c`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:89a530ed26b46eee46941dbadbb46db7466d5e5ce9d18d067dc815b0d3052467
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205343046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cbd10085e3bd8e389031b83d712cb3a42365b13f88c647a9ee795d92151879d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 21:11:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:11:42 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 21:14:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:14:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:14:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:14:39 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7354b266abeda9b5bfbca97ad1c6887d2a277d69ff8c607591a279459548ac7`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d614279c49f19055c903676e10afd41c8a3cd40f35d8b708fb499f7b5eeb965f`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c1b3c16d04da075eb127cecb646f3fbb43b07575ac781c7f670ca3f1885796`  
		Last Modified: Tue, 25 Oct 2022 22:01:55 GMT  
		Size: 171.4 MB (171447425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ac303ffe5e80a8c48e68fb479034e19261f5b6990dd5100bc6ddb1c7cd38ff`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:56d410a83013d84d98a3539261b99621c9291634042c945d6b1d043a8ccb78c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:53efc571f64b54efd30784d514c0fa3bd40c8d6b08ea7d4af6aa443dfc6685fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300556658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6517633704986256d83bc929f469d3f13adec737859a7b4c1e04b3251f94a064`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:02 GMT
ADD file:259be79d94a2549a667ad08a093fe18f15a6c93d66a0723292f49294e31fc7a1 in / 
# Tue, 25 Oct 2022 01:44:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:17:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:17:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:17:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:17:27 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:17:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:17:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:18:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:18:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:18:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:18:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fd31ec14dccdcda8f2472547f1a94ef0a23b8dabb764cd7b1d48aeee0afea7c8`  
		Last Modified: Tue, 25 Oct 2022 01:48:15 GMT  
		Size: 50.4 MB (50447742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7bb5a8d4409ae76ed240704c8628d248a907ec454b12a0f653fa5180822f32`  
		Last Modified: Tue, 25 Oct 2022 07:56:14 GMT  
		Size: 10.9 MB (10896941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9831692d445c53ad6706089a3b147d293d3267dd486b27109a911c9da182ed31`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2beecf1c3569265300a22936ddda05e835f0c83b2193ea68b4d60f2882113cd`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834cb0e33271e58107ddec676304ba095210344f2ee4310bb860d12b941b510c`  
		Last Modified: Tue, 25 Oct 2022 07:56:46 GMT  
		Size: 239.2 MB (239209563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdd4ac8f13eeeb7f19f875b6a9191a3aedf9fd8006aae02db37664d36f51883`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7e17dba0821da8f0d9cf96341d9952fbf39bb10cef5bf4b06590218f8aceb279
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244515099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59bccc2eb39c6d0a333f561f5701aba1e9988ef9f63967351c2b9b1e91e8948`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:07 GMT
ADD file:21afa32c0395cc5046d09741d6821d21cfd9b77bce46ebcfc8fd9aca57c73648 in / 
# Tue, 25 Oct 2022 05:46:08 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:25:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:25:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 21:25:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:25:32 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:25:32 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:25:32 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 21:27:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:27:07 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:27:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:27:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3ba81f4c3c21f92780061ee116827d64ac4edbcd02b056845c2aaa3097b730ed`  
		Last Modified: Tue, 25 Oct 2022 05:49:24 GMT  
		Size: 49.2 MB (49233280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d908f4a3bf1681c533c1f96d98947d2633d0dcaba9dfd301e3012eccad131bc6`  
		Last Modified: Tue, 25 Oct 2022 22:03:50 GMT  
		Size: 10.9 MB (10902593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83583a72ce25a255e794a38648eb0801f9216da38498d62ffb9804978957d95`  
		Last Modified: Tue, 25 Oct 2022 22:03:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1a43410632b0d298d4c6dd3c98b00cf2db2e6c8f50916bd61fcb89cda1d392`  
		Last Modified: Tue, 25 Oct 2022 22:03:48 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae854a5636ab767fe777452319631201aee587f29bea10e23ec81f5b368c445e`  
		Last Modified: Tue, 25 Oct 2022 22:04:20 GMT  
		Size: 184.4 MB (184376816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ab694da339128addba43dd72984d8b40529266d26831ea594d60a8e3cd25b3`  
		Last Modified: Tue, 25 Oct 2022 22:03:48 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:73ba67c09c6ab756c57a1d8654d692f3055a8c7ec54b06f120e5b4f877e968ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:846f250f6dd222e44ee17b7f871875e20abd569082de6299b1d3fb89b4a60ee9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212304339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c78d80b5cf8bf8109d294a84172eb5bc1f718d08607ed579e63932bac8cfa9d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:04:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:07:31 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:07:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:07:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcba2703cc13554dd6ac252966be0f9f0a9d6e79ee879b5e0289457bc632f55`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617320b8300618f53ec135b976c7f3a733354c5ef799b7c969108d82a8509f8`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065fe084d225480619420eb81fce25e1ea4e12e4f4b95002773742fc0e01d67`  
		Last Modified: Tue, 25 Oct 2022 07:53:37 GMT  
		Size: 177.0 MB (177008909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f66f6a9e5d5690a6fcd01f03ca5ef0146410fa911f6fccb17d73db1bbec814`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:67ea8f522d8e90ade44c0d45a623b182c7dbb9f48f4b567f1079e6d3136ca48c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187982732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7c3f4179402fe66a367adbf02ca6941b11a372f4111ef176ab7c3c7de1f500`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:52:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:52:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 06 Oct 2022 06:53:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:16 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:53:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:53:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ab6ac546133bf21e51dc29641d455c42144b184821f494258ff1ec514556c`  
		Last Modified: Thu, 06 Oct 2022 07:00:40 GMT  
		Size: 1.2 MB (1163905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706759f53c150848596edb49143a211c7e072793acea609cc8e9c0f267c4e3e`  
		Last Modified: Thu, 06 Oct 2022 07:00:38 GMT  
		Size: 4.7 MB (4675577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b0360f8c716b3c493ff9708abd3c165f9de06193430830ea64d829b1a6ac2`  
		Last Modified: Thu, 06 Oct 2022 07:00:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd789251f14b7842f745c35075b3e7f88a5aa3fb3b005a3bd0fde7d8f285d7f`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24248fc7fc767d03259bb795d6c177495b4f61cdb1ddcc6a6bb9bb7dcd5958db`  
		Last Modified: Thu, 06 Oct 2022 07:01:15 GMT  
		Size: 157.6 MB (157550749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1b296e1c261f003a529641cc88d1393116b3a0b1f7853da9463a2e9c16df7c`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:89a530ed26b46eee46941dbadbb46db7466d5e5ce9d18d067dc815b0d3052467
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205343046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cbd10085e3bd8e389031b83d712cb3a42365b13f88c647a9ee795d92151879d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:11:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:11:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 21:11:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:11:42 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:11:43 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 21:14:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:14:39 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 21:14:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:14:39 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9660e190ed5a21f6a47fc8cfa949892297824fc48480ba11a5119f126a25b4`  
		Last Modified: Tue, 25 Oct 2022 22:01:28 GMT  
		Size: 1.2 MB (1165046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b01fcd3ecd6496f537d89e10c06e3e8b4c184964ea86d849208d9347132cde`  
		Last Modified: Tue, 25 Oct 2022 22:01:26 GMT  
		Size: 5.5 MB (5532164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7354b266abeda9b5bfbca97ad1c6887d2a277d69ff8c607591a279459548ac7`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d614279c49f19055c903676e10afd41c8a3cd40f35d8b708fb499f7b5eeb965f`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c1b3c16d04da075eb127cecb646f3fbb43b07575ac781c7f670ca3f1885796`  
		Last Modified: Tue, 25 Oct 2022 22:01:55 GMT  
		Size: 171.4 MB (171447425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ac303ffe5e80a8c48e68fb479034e19261f5b6990dd5100bc6ddb1c7cd38ff`  
		Last Modified: Tue, 25 Oct 2022 22:01:25 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling`

```console
$ docker pull ros@sha256:ba2900d9b86070f8a8b21e1ee55938b572b8078fd27f83c2e23af84ba8e6efed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:44bdbd819383462c025ea361c9c8427375ba5c38201356b93c5827ae7b1ebf8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263221662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef1ef5ce96f4a5c4ee7e03559ae7c8da886e0ac2f52a705eb33428dce931`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:45:02 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 07:45:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:45:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:45:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:45:48 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:46:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:46:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:46:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:46:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7767abbf3782738860e3bb5ede4f627dba0211161ae5cfa4a72cf1dd43c58be4`  
		Last Modified: Tue, 25 Oct 2022 08:05:34 GMT  
		Size: 106.4 MB (106391215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8106ab6bf436bb06edcea0071debbc4b31d730b8cc8ca4d7fd6af8bd19ea702a`  
		Last Modified: Tue, 25 Oct 2022 08:05:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb38b610c9d923dbe6bbe532a0559a4064856d0105bf842e52ce1ad4ff11e8b`  
		Last Modified: Tue, 25 Oct 2022 08:05:58 GMT  
		Size: 97.9 MB (97879015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faad8ca67596a7af7c25ade2313bccb1e13db2a2646e408a7171bdcce0e48b6`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 289.2 KB (289222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e4659981956310c677c0249ba2e2eba19ae8b8670034f1b14176d899fde8b0`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af086c324a03d7da5c2309c2b4691d12e9153d09eb5464a8a4442fa3a8c24ae`  
		Last Modified: Tue, 25 Oct 2022 08:05:49 GMT  
		Size: 23.2 MB (23226799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7ec4b6c8e80c1361ce865eb097a692f932f89b4e311f6b683ea806a870db1490
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255895766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a4f5f6cf0080d4581a14dd3b5e879c6d87b8aea0966d9de50bc9d313cc40f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:02 GMT
ADD file:515177312f20fb1814b89bfccfe695fa2354bbb6d43fdb6e018bf5b1acc17e9f in / 
# Tue, 25 Oct 2022 05:55:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:40:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:41:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:55:07 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 21:55:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:55:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:55:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:55:43 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:56:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:56:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:56:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:56:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56a2caa6b2c66e01954c1a013b37ea359b6e6af8989dbfb958124b6318771af4`  
		Last Modified: Tue, 25 Oct 2022 05:56:14 GMT  
		Size: 28.4 MB (28382489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191d2d5931f4547389f96db79cb360ca3fdcf9f2d51c390b6958348a8a67c347`  
		Last Modified: Tue, 25 Oct 2022 22:08:40 GMT  
		Size: 1.2 MB (1176430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c085abd75940b2d68ae65386a432f481580f2ba06963b1e8c435bf4a06943d1`  
		Last Modified: Tue, 25 Oct 2022 22:08:38 GMT  
		Size: 3.8 MB (3799950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efa6f1ee27186437a210a19aa7cac0243bca4bf8e278464256de1a6c727019e`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ca2e27b815a4a40cfebb2d3e9e35f746c5458629933fdb650f2fe0af8725c7`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed727913da2df4c85f543bb622ca8250788089578111439f22bb714798459b3`  
		Last Modified: Tue, 25 Oct 2022 22:11:22 GMT  
		Size: 104.1 MB (104123415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9583f3a54ad44a88d2f8f3cef0123a92cfd2d0812bc3b17ae46dee50616c62cc`  
		Last Modified: Tue, 25 Oct 2022 22:11:05 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2894b1d29796d37211f1faac9997114b1d9ac24cb16aa7b37a55e7e053dfe5c4`  
		Last Modified: Tue, 25 Oct 2022 22:11:44 GMT  
		Size: 95.5 MB (95469739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb51cac7761444f42be6933140a6f38701364f808935260001a5e6de62b856a`  
		Last Modified: Tue, 25 Oct 2022 22:11:33 GMT  
		Size: 289.2 KB (289217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0a1dcd2273219e84ecf67eca79433d30c31344c46ac2fd9599a574a40114f3`  
		Last Modified: Tue, 25 Oct 2022 22:11:32 GMT  
		Size: 2.4 KB (2417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebfdea86c967860b279ac03d6a5c556c40da6dc586face59732850ca052e284`  
		Last Modified: Tue, 25 Oct 2022 22:11:36 GMT  
		Size: 22.6 MB (22649690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:8ffd2eec34c1595e747f73919b7b2eb4f7c536d383cbbd19ff2cd33672e2e969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:5b6c57eef6e1d7715608064ff21c0dda63c00346cf7aff24cb7d14e7cc1cfa5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1088048490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a22bed2655671151456cb87328451adae485aa8e08b1dbf61ce345483c70dce`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:45:02 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 07:45:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:45:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:45:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:45:48 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:46:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:46:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:46:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:46:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:48:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7767abbf3782738860e3bb5ede4f627dba0211161ae5cfa4a72cf1dd43c58be4`  
		Last Modified: Tue, 25 Oct 2022 08:05:34 GMT  
		Size: 106.4 MB (106391215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8106ab6bf436bb06edcea0071debbc4b31d730b8cc8ca4d7fd6af8bd19ea702a`  
		Last Modified: Tue, 25 Oct 2022 08:05:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb38b610c9d923dbe6bbe532a0559a4064856d0105bf842e52ce1ad4ff11e8b`  
		Last Modified: Tue, 25 Oct 2022 08:05:58 GMT  
		Size: 97.9 MB (97879015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faad8ca67596a7af7c25ade2313bccb1e13db2a2646e408a7171bdcce0e48b6`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 289.2 KB (289222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e4659981956310c677c0249ba2e2eba19ae8b8670034f1b14176d899fde8b0`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af086c324a03d7da5c2309c2b4691d12e9153d09eb5464a8a4442fa3a8c24ae`  
		Last Modified: Tue, 25 Oct 2022 08:05:49 GMT  
		Size: 23.2 MB (23226799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57143ed7f731779085a0e57d22932271e243520fd47318ed7ccf08cd50211152`  
		Last Modified: Tue, 25 Oct 2022 08:07:51 GMT  
		Size: 824.8 MB (824826828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f43bef87315efebf16422ccfebe6b8366a1bf1d431d8789128fc8d289b10ceaf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1038301133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2208bc0701c962aa607e1c384fe787bd5ccf177a7dfd210023c80bdfadafab`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:02 GMT
ADD file:515177312f20fb1814b89bfccfe695fa2354bbb6d43fdb6e018bf5b1acc17e9f in / 
# Tue, 25 Oct 2022 05:55:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:40:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:41:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:55:07 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 21:55:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:55:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:55:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:55:43 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:56:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:56:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:56:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:56:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:58:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56a2caa6b2c66e01954c1a013b37ea359b6e6af8989dbfb958124b6318771af4`  
		Last Modified: Tue, 25 Oct 2022 05:56:14 GMT  
		Size: 28.4 MB (28382489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191d2d5931f4547389f96db79cb360ca3fdcf9f2d51c390b6958348a8a67c347`  
		Last Modified: Tue, 25 Oct 2022 22:08:40 GMT  
		Size: 1.2 MB (1176430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c085abd75940b2d68ae65386a432f481580f2ba06963b1e8c435bf4a06943d1`  
		Last Modified: Tue, 25 Oct 2022 22:08:38 GMT  
		Size: 3.8 MB (3799950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efa6f1ee27186437a210a19aa7cac0243bca4bf8e278464256de1a6c727019e`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ca2e27b815a4a40cfebb2d3e9e35f746c5458629933fdb650f2fe0af8725c7`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed727913da2df4c85f543bb622ca8250788089578111439f22bb714798459b3`  
		Last Modified: Tue, 25 Oct 2022 22:11:22 GMT  
		Size: 104.1 MB (104123415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9583f3a54ad44a88d2f8f3cef0123a92cfd2d0812bc3b17ae46dee50616c62cc`  
		Last Modified: Tue, 25 Oct 2022 22:11:05 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2894b1d29796d37211f1faac9997114b1d9ac24cb16aa7b37a55e7e053dfe5c4`  
		Last Modified: Tue, 25 Oct 2022 22:11:44 GMT  
		Size: 95.5 MB (95469739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb51cac7761444f42be6933140a6f38701364f808935260001a5e6de62b856a`  
		Last Modified: Tue, 25 Oct 2022 22:11:33 GMT  
		Size: 289.2 KB (289217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0a1dcd2273219e84ecf67eca79433d30c31344c46ac2fd9599a574a40114f3`  
		Last Modified: Tue, 25 Oct 2022 22:11:32 GMT  
		Size: 2.4 KB (2417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebfdea86c967860b279ac03d6a5c556c40da6dc586face59732850ca052e284`  
		Last Modified: Tue, 25 Oct 2022 22:11:36 GMT  
		Size: 22.6 MB (22649690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ebe977e9b8257a2674fee21fd63af1c08eac5e57e2ada34b1822c9c0cdb80e`  
		Last Modified: Tue, 25 Oct 2022 22:13:20 GMT  
		Size: 782.4 MB (782405367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception-jammy`

```console
$ docker pull ros@sha256:8ffd2eec34c1595e747f73919b7b2eb4f7c536d383cbbd19ff2cd33672e2e969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:5b6c57eef6e1d7715608064ff21c0dda63c00346cf7aff24cb7d14e7cc1cfa5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1088048490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a22bed2655671151456cb87328451adae485aa8e08b1dbf61ce345483c70dce`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:45:02 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 07:45:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:45:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:45:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:45:48 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:46:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:46:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:46:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:46:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:48:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7767abbf3782738860e3bb5ede4f627dba0211161ae5cfa4a72cf1dd43c58be4`  
		Last Modified: Tue, 25 Oct 2022 08:05:34 GMT  
		Size: 106.4 MB (106391215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8106ab6bf436bb06edcea0071debbc4b31d730b8cc8ca4d7fd6af8bd19ea702a`  
		Last Modified: Tue, 25 Oct 2022 08:05:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb38b610c9d923dbe6bbe532a0559a4064856d0105bf842e52ce1ad4ff11e8b`  
		Last Modified: Tue, 25 Oct 2022 08:05:58 GMT  
		Size: 97.9 MB (97879015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faad8ca67596a7af7c25ade2313bccb1e13db2a2646e408a7171bdcce0e48b6`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 289.2 KB (289222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e4659981956310c677c0249ba2e2eba19ae8b8670034f1b14176d899fde8b0`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af086c324a03d7da5c2309c2b4691d12e9153d09eb5464a8a4442fa3a8c24ae`  
		Last Modified: Tue, 25 Oct 2022 08:05:49 GMT  
		Size: 23.2 MB (23226799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57143ed7f731779085a0e57d22932271e243520fd47318ed7ccf08cd50211152`  
		Last Modified: Tue, 25 Oct 2022 08:07:51 GMT  
		Size: 824.8 MB (824826828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f43bef87315efebf16422ccfebe6b8366a1bf1d431d8789128fc8d289b10ceaf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1038301133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2208bc0701c962aa607e1c384fe787bd5ccf177a7dfd210023c80bdfadafab`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:02 GMT
ADD file:515177312f20fb1814b89bfccfe695fa2354bbb6d43fdb6e018bf5b1acc17e9f in / 
# Tue, 25 Oct 2022 05:55:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:40:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:41:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:55:07 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 21:55:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:55:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:55:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:55:43 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:56:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:56:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:56:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:56:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:58:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56a2caa6b2c66e01954c1a013b37ea359b6e6af8989dbfb958124b6318771af4`  
		Last Modified: Tue, 25 Oct 2022 05:56:14 GMT  
		Size: 28.4 MB (28382489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191d2d5931f4547389f96db79cb360ca3fdcf9f2d51c390b6958348a8a67c347`  
		Last Modified: Tue, 25 Oct 2022 22:08:40 GMT  
		Size: 1.2 MB (1176430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c085abd75940b2d68ae65386a432f481580f2ba06963b1e8c435bf4a06943d1`  
		Last Modified: Tue, 25 Oct 2022 22:08:38 GMT  
		Size: 3.8 MB (3799950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efa6f1ee27186437a210a19aa7cac0243bca4bf8e278464256de1a6c727019e`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ca2e27b815a4a40cfebb2d3e9e35f746c5458629933fdb650f2fe0af8725c7`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed727913da2df4c85f543bb622ca8250788089578111439f22bb714798459b3`  
		Last Modified: Tue, 25 Oct 2022 22:11:22 GMT  
		Size: 104.1 MB (104123415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9583f3a54ad44a88d2f8f3cef0123a92cfd2d0812bc3b17ae46dee50616c62cc`  
		Last Modified: Tue, 25 Oct 2022 22:11:05 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2894b1d29796d37211f1faac9997114b1d9ac24cb16aa7b37a55e7e053dfe5c4`  
		Last Modified: Tue, 25 Oct 2022 22:11:44 GMT  
		Size: 95.5 MB (95469739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb51cac7761444f42be6933140a6f38701364f808935260001a5e6de62b856a`  
		Last Modified: Tue, 25 Oct 2022 22:11:33 GMT  
		Size: 289.2 KB (289217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0a1dcd2273219e84ecf67eca79433d30c31344c46ac2fd9599a574a40114f3`  
		Last Modified: Tue, 25 Oct 2022 22:11:32 GMT  
		Size: 2.4 KB (2417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebfdea86c967860b279ac03d6a5c556c40da6dc586face59732850ca052e284`  
		Last Modified: Tue, 25 Oct 2022 22:11:36 GMT  
		Size: 22.6 MB (22649690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ebe977e9b8257a2674fee21fd63af1c08eac5e57e2ada34b1822c9c0cdb80e`  
		Last Modified: Tue, 25 Oct 2022 22:13:20 GMT  
		Size: 782.4 MB (782405367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:ba2900d9b86070f8a8b21e1ee55938b572b8078fd27f83c2e23af84ba8e6efed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:44bdbd819383462c025ea361c9c8427375ba5c38201356b93c5827ae7b1ebf8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263221662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef1ef5ce96f4a5c4ee7e03559ae7c8da886e0ac2f52a705eb33428dce931`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:45:02 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 07:45:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:45:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:45:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:45:48 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:46:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:46:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:46:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:46:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7767abbf3782738860e3bb5ede4f627dba0211161ae5cfa4a72cf1dd43c58be4`  
		Last Modified: Tue, 25 Oct 2022 08:05:34 GMT  
		Size: 106.4 MB (106391215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8106ab6bf436bb06edcea0071debbc4b31d730b8cc8ca4d7fd6af8bd19ea702a`  
		Last Modified: Tue, 25 Oct 2022 08:05:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb38b610c9d923dbe6bbe532a0559a4064856d0105bf842e52ce1ad4ff11e8b`  
		Last Modified: Tue, 25 Oct 2022 08:05:58 GMT  
		Size: 97.9 MB (97879015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faad8ca67596a7af7c25ade2313bccb1e13db2a2646e408a7171bdcce0e48b6`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 289.2 KB (289222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e4659981956310c677c0249ba2e2eba19ae8b8670034f1b14176d899fde8b0`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af086c324a03d7da5c2309c2b4691d12e9153d09eb5464a8a4442fa3a8c24ae`  
		Last Modified: Tue, 25 Oct 2022 08:05:49 GMT  
		Size: 23.2 MB (23226799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7ec4b6c8e80c1361ce865eb097a692f932f89b4e311f6b683ea806a870db1490
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255895766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a4f5f6cf0080d4581a14dd3b5e879c6d87b8aea0966d9de50bc9d313cc40f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:02 GMT
ADD file:515177312f20fb1814b89bfccfe695fa2354bbb6d43fdb6e018bf5b1acc17e9f in / 
# Tue, 25 Oct 2022 05:55:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:40:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:41:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:55:07 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 21:55:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:55:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:55:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:55:43 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:56:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:56:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:56:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:56:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56a2caa6b2c66e01954c1a013b37ea359b6e6af8989dbfb958124b6318771af4`  
		Last Modified: Tue, 25 Oct 2022 05:56:14 GMT  
		Size: 28.4 MB (28382489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191d2d5931f4547389f96db79cb360ca3fdcf9f2d51c390b6958348a8a67c347`  
		Last Modified: Tue, 25 Oct 2022 22:08:40 GMT  
		Size: 1.2 MB (1176430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c085abd75940b2d68ae65386a432f481580f2ba06963b1e8c435bf4a06943d1`  
		Last Modified: Tue, 25 Oct 2022 22:08:38 GMT  
		Size: 3.8 MB (3799950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efa6f1ee27186437a210a19aa7cac0243bca4bf8e278464256de1a6c727019e`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ca2e27b815a4a40cfebb2d3e9e35f746c5458629933fdb650f2fe0af8725c7`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed727913da2df4c85f543bb622ca8250788089578111439f22bb714798459b3`  
		Last Modified: Tue, 25 Oct 2022 22:11:22 GMT  
		Size: 104.1 MB (104123415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9583f3a54ad44a88d2f8f3cef0123a92cfd2d0812bc3b17ae46dee50616c62cc`  
		Last Modified: Tue, 25 Oct 2022 22:11:05 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2894b1d29796d37211f1faac9997114b1d9ac24cb16aa7b37a55e7e053dfe5c4`  
		Last Modified: Tue, 25 Oct 2022 22:11:44 GMT  
		Size: 95.5 MB (95469739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb51cac7761444f42be6933140a6f38701364f808935260001a5e6de62b856a`  
		Last Modified: Tue, 25 Oct 2022 22:11:33 GMT  
		Size: 289.2 KB (289217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0a1dcd2273219e84ecf67eca79433d30c31344c46ac2fd9599a574a40114f3`  
		Last Modified: Tue, 25 Oct 2022 22:11:32 GMT  
		Size: 2.4 KB (2417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebfdea86c967860b279ac03d6a5c556c40da6dc586face59732850ca052e284`  
		Last Modified: Tue, 25 Oct 2022 22:11:36 GMT  
		Size: 22.6 MB (22649690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base-jammy`

```console
$ docker pull ros@sha256:ba2900d9b86070f8a8b21e1ee55938b572b8078fd27f83c2e23af84ba8e6efed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:44bdbd819383462c025ea361c9c8427375ba5c38201356b93c5827ae7b1ebf8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263221662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef1ef5ce96f4a5c4ee7e03559ae7c8da886e0ac2f52a705eb33428dce931`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:45:02 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 07:45:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:45:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:45:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:45:48 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:46:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:46:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:46:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:46:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7767abbf3782738860e3bb5ede4f627dba0211161ae5cfa4a72cf1dd43c58be4`  
		Last Modified: Tue, 25 Oct 2022 08:05:34 GMT  
		Size: 106.4 MB (106391215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8106ab6bf436bb06edcea0071debbc4b31d730b8cc8ca4d7fd6af8bd19ea702a`  
		Last Modified: Tue, 25 Oct 2022 08:05:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb38b610c9d923dbe6bbe532a0559a4064856d0105bf842e52ce1ad4ff11e8b`  
		Last Modified: Tue, 25 Oct 2022 08:05:58 GMT  
		Size: 97.9 MB (97879015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faad8ca67596a7af7c25ade2313bccb1e13db2a2646e408a7171bdcce0e48b6`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 289.2 KB (289222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e4659981956310c677c0249ba2e2eba19ae8b8670034f1b14176d899fde8b0`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af086c324a03d7da5c2309c2b4691d12e9153d09eb5464a8a4442fa3a8c24ae`  
		Last Modified: Tue, 25 Oct 2022 08:05:49 GMT  
		Size: 23.2 MB (23226799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:7ec4b6c8e80c1361ce865eb097a692f932f89b4e311f6b683ea806a870db1490
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255895766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a4f5f6cf0080d4581a14dd3b5e879c6d87b8aea0966d9de50bc9d313cc40f6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:02 GMT
ADD file:515177312f20fb1814b89bfccfe695fa2354bbb6d43fdb6e018bf5b1acc17e9f in / 
# Tue, 25 Oct 2022 05:55:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:40:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:41:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:55:07 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 21:55:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:55:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:55:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:55:43 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:56:01 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:56:05 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 21:56:11 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 21:56:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:56a2caa6b2c66e01954c1a013b37ea359b6e6af8989dbfb958124b6318771af4`  
		Last Modified: Tue, 25 Oct 2022 05:56:14 GMT  
		Size: 28.4 MB (28382489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191d2d5931f4547389f96db79cb360ca3fdcf9f2d51c390b6958348a8a67c347`  
		Last Modified: Tue, 25 Oct 2022 22:08:40 GMT  
		Size: 1.2 MB (1176430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c085abd75940b2d68ae65386a432f481580f2ba06963b1e8c435bf4a06943d1`  
		Last Modified: Tue, 25 Oct 2022 22:08:38 GMT  
		Size: 3.8 MB (3799950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efa6f1ee27186437a210a19aa7cac0243bca4bf8e278464256de1a6c727019e`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ca2e27b815a4a40cfebb2d3e9e35f746c5458629933fdb650f2fe0af8725c7`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed727913da2df4c85f543bb622ca8250788089578111439f22bb714798459b3`  
		Last Modified: Tue, 25 Oct 2022 22:11:22 GMT  
		Size: 104.1 MB (104123415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9583f3a54ad44a88d2f8f3cef0123a92cfd2d0812bc3b17ae46dee50616c62cc`  
		Last Modified: Tue, 25 Oct 2022 22:11:05 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2894b1d29796d37211f1faac9997114b1d9ac24cb16aa7b37a55e7e053dfe5c4`  
		Last Modified: Tue, 25 Oct 2022 22:11:44 GMT  
		Size: 95.5 MB (95469739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb51cac7761444f42be6933140a6f38701364f808935260001a5e6de62b856a`  
		Last Modified: Tue, 25 Oct 2022 22:11:33 GMT  
		Size: 289.2 KB (289217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0a1dcd2273219e84ecf67eca79433d30c31344c46ac2fd9599a574a40114f3`  
		Last Modified: Tue, 25 Oct 2022 22:11:32 GMT  
		Size: 2.4 KB (2417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebfdea86c967860b279ac03d6a5c556c40da6dc586face59732850ca052e284`  
		Last Modified: Tue, 25 Oct 2022 22:11:36 GMT  
		Size: 22.6 MB (22649690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:57b32c08542d04a1ef48e53f0790a9378d625d8f4313829ffd6dd3054831529d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:f4058c67b7489efe0031cbb8086a4f21cbb8ee27bf043cdcd9009a62c840324f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141824194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20a7abc7499d2145cffd08fccb8263da40b4180e7b811d23faada47f7f2c2ab`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:45:02 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 07:45:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:45:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:45:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:45:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7767abbf3782738860e3bb5ede4f627dba0211161ae5cfa4a72cf1dd43c58be4`  
		Last Modified: Tue, 25 Oct 2022 08:05:34 GMT  
		Size: 106.4 MB (106391215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8106ab6bf436bb06edcea0071debbc4b31d730b8cc8ca4d7fd6af8bd19ea702a`  
		Last Modified: Tue, 25 Oct 2022 08:05:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c245087d427a7ec6d34d974d8abd19c07f0ebf30b817b252371ecf03fa4b0fb7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137484703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dfe6dbf3ec72bc109c826c11f44000d67b108313ec26ae1365ae341441583c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:02 GMT
ADD file:515177312f20fb1814b89bfccfe695fa2354bbb6d43fdb6e018bf5b1acc17e9f in / 
# Tue, 25 Oct 2022 05:55:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:40:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:41:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:55:07 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 21:55:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:55:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:55:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:55:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:56a2caa6b2c66e01954c1a013b37ea359b6e6af8989dbfb958124b6318771af4`  
		Last Modified: Tue, 25 Oct 2022 05:56:14 GMT  
		Size: 28.4 MB (28382489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191d2d5931f4547389f96db79cb360ca3fdcf9f2d51c390b6958348a8a67c347`  
		Last Modified: Tue, 25 Oct 2022 22:08:40 GMT  
		Size: 1.2 MB (1176430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c085abd75940b2d68ae65386a432f481580f2ba06963b1e8c435bf4a06943d1`  
		Last Modified: Tue, 25 Oct 2022 22:08:38 GMT  
		Size: 3.8 MB (3799950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efa6f1ee27186437a210a19aa7cac0243bca4bf8e278464256de1a6c727019e`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ca2e27b815a4a40cfebb2d3e9e35f746c5458629933fdb650f2fe0af8725c7`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed727913da2df4c85f543bb622ca8250788089578111439f22bb714798459b3`  
		Last Modified: Tue, 25 Oct 2022 22:11:22 GMT  
		Size: 104.1 MB (104123415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9583f3a54ad44a88d2f8f3cef0123a92cfd2d0812bc3b17ae46dee50616c62cc`  
		Last Modified: Tue, 25 Oct 2022 22:11:05 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core-jammy`

```console
$ docker pull ros@sha256:57b32c08542d04a1ef48e53f0790a9378d625d8f4313829ffd6dd3054831529d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:f4058c67b7489efe0031cbb8086a4f21cbb8ee27bf043cdcd9009a62c840324f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141824194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20a7abc7499d2145cffd08fccb8263da40b4180e7b811d23faada47f7f2c2ab`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:45:02 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 07:45:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:45:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:45:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:45:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7767abbf3782738860e3bb5ede4f627dba0211161ae5cfa4a72cf1dd43c58be4`  
		Last Modified: Tue, 25 Oct 2022 08:05:34 GMT  
		Size: 106.4 MB (106391215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8106ab6bf436bb06edcea0071debbc4b31d730b8cc8ca4d7fd6af8bd19ea702a`  
		Last Modified: Tue, 25 Oct 2022 08:05:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c245087d427a7ec6d34d974d8abd19c07f0ebf30b817b252371ecf03fa4b0fb7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137484703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dfe6dbf3ec72bc109c826c11f44000d67b108313ec26ae1365ae341441583c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:02 GMT
ADD file:515177312f20fb1814b89bfccfe695fa2354bbb6d43fdb6e018bf5b1acc17e9f in / 
# Tue, 25 Oct 2022 05:55:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 21:40:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:41:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 21:41:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 21:41:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 21:55:07 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 21:55:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 21:55:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 21:55:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 21:55:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:56a2caa6b2c66e01954c1a013b37ea359b6e6af8989dbfb958124b6318771af4`  
		Last Modified: Tue, 25 Oct 2022 05:56:14 GMT  
		Size: 28.4 MB (28382489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191d2d5931f4547389f96db79cb360ca3fdcf9f2d51c390b6958348a8a67c347`  
		Last Modified: Tue, 25 Oct 2022 22:08:40 GMT  
		Size: 1.2 MB (1176430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c085abd75940b2d68ae65386a432f481580f2ba06963b1e8c435bf4a06943d1`  
		Last Modified: Tue, 25 Oct 2022 22:08:38 GMT  
		Size: 3.8 MB (3799950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efa6f1ee27186437a210a19aa7cac0243bca4bf8e278464256de1a6c727019e`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ca2e27b815a4a40cfebb2d3e9e35f746c5458629933fdb650f2fe0af8725c7`  
		Last Modified: Tue, 25 Oct 2022 22:08:37 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed727913da2df4c85f543bb622ca8250788089578111439f22bb714798459b3`  
		Last Modified: Tue, 25 Oct 2022 22:11:22 GMT  
		Size: 104.1 MB (104123415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9583f3a54ad44a88d2f8f3cef0123a92cfd2d0812bc3b17ae46dee50616c62cc`  
		Last Modified: Tue, 25 Oct 2022 22:11:05 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
