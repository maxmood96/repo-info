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
$ docker pull ros@sha256:afd8508e9f193cf3d3fe298f68a14e4f4ac80527cb0bc5ff6943c4300d950e99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:foxy` - linux; amd64

```console
$ docker pull ros@sha256:1555cf64b24b344baeb5af796878a8b4f2051c3f38c88cc162dd46ee104e8226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254968863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc76cc006e617b12323eed3c811587b1714b6f7b41ecae986c2d939807d0100`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
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
	-	`sha256:905dfb1bab3312147382cf593a88dfd91dcde255426f42b174c0a00cbfee3d49`  
		Last Modified: Fri, 06 Jun 2025 22:49:29 GMT  
		Size: 1.2 MB (1194819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bf200ef89210ac612db81e54c264d517b910910145ae871d765696f0b2599d`  
		Last Modified: Fri, 06 Jun 2025 22:49:29 GMT  
		Size: 5.4 MB (5363903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f4f1b29220d6398d0c70e5bf4d323cf24bc1b2b4587f6b1b9a02658100661b`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc09efa67422b34d4c77e03962a93fb1c22f91239484ef3e692b04953247ee3d`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fdc4be6b715533df3810ad59eb7a493b1ad5a0fcd129ace37d611a85328e0d7`  
		Last Modified: Fri, 06 Jun 2025 22:49:35 GMT  
		Size: 125.6 MB (125595150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd83c03f807b7ea0994bf1035dc345d86aa658f5159998acc62e1c70a214182`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9aec951983b4c0ff57c8185a118737d2aa6abd2979e54efa7007c42e388e3ce`  
		Last Modified: Fri, 06 Jun 2025 23:09:21 GMT  
		Size: 73.3 MB (73323708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a36983631da54649d3973eca83d8f7b9bdff7368406fac4f29468e0bb26c3b`  
		Last Modified: Fri, 06 Jun 2025 23:09:19 GMT  
		Size: 301.2 KB (301159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87633dc1f860b5a814b4544ede1903f1dc53029e982d7bc3b4b6dc51e679c0f1`  
		Last Modified: Fri, 06 Jun 2025 23:09:19 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f026747287ad82fbc819b8c857e70adb1d75218fc3f41221b1591bf802e9d0`  
		Last Modified: Sat, 07 Jun 2025 02:12:32 GMT  
		Size: 21.7 MB (21672857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy` - unknown; unknown

```console
$ docker pull ros@sha256:43ed1b9a60d768ff82cc5df477a2fd2d487148f2a0e514daed7bca4cba295e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22643474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a24c1e03c14698278a3bd385e83c37d021a5750bc0cc12b39d4ce57ef71341`

```dockerfile
```

-	Layers:
	-	`sha256:0c7f62558466bf857633ef7626050e6cbb7c77b8dfa7dba89463c82e5f4af2d3`  
		Last Modified: Sat, 07 Jun 2025 01:19:24 GMT  
		Size: 22.6 MB (22626355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65e2aae5698e322871b42ae00b147c2953c832c98d1fa28241763a7164ec12c4`  
		Last Modified: Sat, 07 Jun 2025 01:19:25 GMT  
		Size: 17.1 KB (17119 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:foxy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:487e2b121107be08d3dcfb759fdb0bc25f1622902a7b6fedb85236a602b4d789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229776472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce8a3d24ba5fc59286d4d98bf1349762b4946e63eecc2f6418de304af3f76b7`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
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
	-	`sha256:3da64ed2bb66a6ce3d36adf9712e73c205cbae57442bbdb8365c1c16617e0183`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 5.3 MB (5344104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a127babc495b469c32a2537669b10def6004f278427e28a9ad21e1eaad81c`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 4.0 KB (3983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd563e74b9280d17b11bae86038561c7184eda5ae05a08570ac236ede7caab26`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f376c0b3101d22149ca2d878d920aa16f69ba90b157b102210f0b0216b96c6`  
		Last Modified: Fri, 06 Jun 2025 23:12:25 GMT  
		Size: 108.9 MB (108878978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8bbf8c8a1cae034a096fd542d615567aabad879961709c67a9d412fa9cb10c`  
		Last Modified: Fri, 06 Jun 2025 23:12:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0828ae3bcc02cebe074457715b9015f612b41f3505eec2d509eb84191059d1`  
		Last Modified: Sat, 07 Jun 2025 00:45:00 GMT  
		Size: 67.7 MB (67674946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0008d8e892d97a7ab8afd15de5401052d67d5d1a11424408fe9bdf6f8facd4ea`  
		Last Modified: Sat, 07 Jun 2025 00:44:57 GMT  
		Size: 301.2 KB (301159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195e8afc91b0fc0fc13a30cd50b392436315c3301fc5dd8378e1bad63c83b178`  
		Last Modified: Sat, 07 Jun 2025 00:44:58 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7067dec2b246676b2e5d3e65aa8474d14fed126303588ae5ebd0040f9b0c2`  
		Last Modified: Sat, 07 Jun 2025 00:45:00 GMT  
		Size: 20.4 MB (20398057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy` - unknown; unknown

```console
$ docker pull ros@sha256:633ba80f46ca8fc360c6e93718a0f1006c287c8686db18b94cf9b54933a0d868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21563319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a424bdf2cc314396cca76f67161f150f45a995d96282b4256b5ad6cd5e25c277`

```dockerfile
```

-	Layers:
	-	`sha256:641f149cbb13fed4a2d3b7cf31a8214f520e730368002d5ee11037d2d7fc11f1`  
		Last Modified: Sat, 07 Jun 2025 01:19:39 GMT  
		Size: 21.5 MB (21546063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6850a9c9bc9c1da1ad6c90721c65cecef6622936daac15d6f1a08d200cb0e34`  
		Last Modified: Sat, 07 Jun 2025 01:19:40 GMT  
		Size: 17.3 KB (17256 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:foxy-ros-base`

```console
$ docker pull ros@sha256:afd8508e9f193cf3d3fe298f68a14e4f4ac80527cb0bc5ff6943c4300d950e99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:foxy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:1555cf64b24b344baeb5af796878a8b4f2051c3f38c88cc162dd46ee104e8226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254968863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc76cc006e617b12323eed3c811587b1714b6f7b41ecae986c2d939807d0100`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
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
	-	`sha256:905dfb1bab3312147382cf593a88dfd91dcde255426f42b174c0a00cbfee3d49`  
		Last Modified: Fri, 06 Jun 2025 22:49:29 GMT  
		Size: 1.2 MB (1194819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bf200ef89210ac612db81e54c264d517b910910145ae871d765696f0b2599d`  
		Last Modified: Fri, 06 Jun 2025 22:49:29 GMT  
		Size: 5.4 MB (5363903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f4f1b29220d6398d0c70e5bf4d323cf24bc1b2b4587f6b1b9a02658100661b`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc09efa67422b34d4c77e03962a93fb1c22f91239484ef3e692b04953247ee3d`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fdc4be6b715533df3810ad59eb7a493b1ad5a0fcd129ace37d611a85328e0d7`  
		Last Modified: Fri, 06 Jun 2025 22:49:35 GMT  
		Size: 125.6 MB (125595150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd83c03f807b7ea0994bf1035dc345d86aa658f5159998acc62e1c70a214182`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9aec951983b4c0ff57c8185a118737d2aa6abd2979e54efa7007c42e388e3ce`  
		Last Modified: Fri, 06 Jun 2025 23:09:21 GMT  
		Size: 73.3 MB (73323708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a36983631da54649d3973eca83d8f7b9bdff7368406fac4f29468e0bb26c3b`  
		Last Modified: Fri, 06 Jun 2025 23:09:19 GMT  
		Size: 301.2 KB (301159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87633dc1f860b5a814b4544ede1903f1dc53029e982d7bc3b4b6dc51e679c0f1`  
		Last Modified: Fri, 06 Jun 2025 23:09:19 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f026747287ad82fbc819b8c857e70adb1d75218fc3f41221b1591bf802e9d0`  
		Last Modified: Sat, 07 Jun 2025 02:12:32 GMT  
		Size: 21.7 MB (21672857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:43ed1b9a60d768ff82cc5df477a2fd2d487148f2a0e514daed7bca4cba295e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22643474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a24c1e03c14698278a3bd385e83c37d021a5750bc0cc12b39d4ce57ef71341`

```dockerfile
```

-	Layers:
	-	`sha256:0c7f62558466bf857633ef7626050e6cbb7c77b8dfa7dba89463c82e5f4af2d3`  
		Last Modified: Sat, 07 Jun 2025 01:19:24 GMT  
		Size: 22.6 MB (22626355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65e2aae5698e322871b42ae00b147c2953c832c98d1fa28241763a7164ec12c4`  
		Last Modified: Sat, 07 Jun 2025 01:19:25 GMT  
		Size: 17.1 KB (17119 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:foxy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:487e2b121107be08d3dcfb759fdb0bc25f1622902a7b6fedb85236a602b4d789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229776472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce8a3d24ba5fc59286d4d98bf1349762b4946e63eecc2f6418de304af3f76b7`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
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
	-	`sha256:3da64ed2bb66a6ce3d36adf9712e73c205cbae57442bbdb8365c1c16617e0183`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 5.3 MB (5344104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a127babc495b469c32a2537669b10def6004f278427e28a9ad21e1eaad81c`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 4.0 KB (3983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd563e74b9280d17b11bae86038561c7184eda5ae05a08570ac236ede7caab26`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f376c0b3101d22149ca2d878d920aa16f69ba90b157b102210f0b0216b96c6`  
		Last Modified: Fri, 06 Jun 2025 23:12:25 GMT  
		Size: 108.9 MB (108878978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8bbf8c8a1cae034a096fd542d615567aabad879961709c67a9d412fa9cb10c`  
		Last Modified: Fri, 06 Jun 2025 23:12:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0828ae3bcc02cebe074457715b9015f612b41f3505eec2d509eb84191059d1`  
		Last Modified: Sat, 07 Jun 2025 00:45:00 GMT  
		Size: 67.7 MB (67674946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0008d8e892d97a7ab8afd15de5401052d67d5d1a11424408fe9bdf6f8facd4ea`  
		Last Modified: Sat, 07 Jun 2025 00:44:57 GMT  
		Size: 301.2 KB (301159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195e8afc91b0fc0fc13a30cd50b392436315c3301fc5dd8378e1bad63c83b178`  
		Last Modified: Sat, 07 Jun 2025 00:44:58 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7067dec2b246676b2e5d3e65aa8474d14fed126303588ae5ebd0040f9b0c2`  
		Last Modified: Sat, 07 Jun 2025 00:45:00 GMT  
		Size: 20.4 MB (20398057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:633ba80f46ca8fc360c6e93718a0f1006c287c8686db18b94cf9b54933a0d868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21563319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a424bdf2cc314396cca76f67161f150f45a995d96282b4256b5ad6cd5e25c277`

```dockerfile
```

-	Layers:
	-	`sha256:641f149cbb13fed4a2d3b7cf31a8214f520e730368002d5ee11037d2d7fc11f1`  
		Last Modified: Sat, 07 Jun 2025 01:19:39 GMT  
		Size: 21.5 MB (21546063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6850a9c9bc9c1da1ad6c90721c65cecef6622936daac15d6f1a08d200cb0e34`  
		Last Modified: Sat, 07 Jun 2025 01:19:40 GMT  
		Size: 17.3 KB (17256 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:foxy-ros-base-focal`

```console
$ docker pull ros@sha256:afd8508e9f193cf3d3fe298f68a14e4f4ac80527cb0bc5ff6943c4300d950e99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:foxy-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:1555cf64b24b344baeb5af796878a8b4f2051c3f38c88cc162dd46ee104e8226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254968863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc76cc006e617b12323eed3c811587b1714b6f7b41ecae986c2d939807d0100`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
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
	-	`sha256:905dfb1bab3312147382cf593a88dfd91dcde255426f42b174c0a00cbfee3d49`  
		Last Modified: Fri, 06 Jun 2025 22:49:29 GMT  
		Size: 1.2 MB (1194819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bf200ef89210ac612db81e54c264d517b910910145ae871d765696f0b2599d`  
		Last Modified: Fri, 06 Jun 2025 22:49:29 GMT  
		Size: 5.4 MB (5363903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f4f1b29220d6398d0c70e5bf4d323cf24bc1b2b4587f6b1b9a02658100661b`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc09efa67422b34d4c77e03962a93fb1c22f91239484ef3e692b04953247ee3d`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fdc4be6b715533df3810ad59eb7a493b1ad5a0fcd129ace37d611a85328e0d7`  
		Last Modified: Fri, 06 Jun 2025 22:49:35 GMT  
		Size: 125.6 MB (125595150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd83c03f807b7ea0994bf1035dc345d86aa658f5159998acc62e1c70a214182`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9aec951983b4c0ff57c8185a118737d2aa6abd2979e54efa7007c42e388e3ce`  
		Last Modified: Fri, 06 Jun 2025 23:09:21 GMT  
		Size: 73.3 MB (73323708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a36983631da54649d3973eca83d8f7b9bdff7368406fac4f29468e0bb26c3b`  
		Last Modified: Fri, 06 Jun 2025 23:09:19 GMT  
		Size: 301.2 KB (301159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87633dc1f860b5a814b4544ede1903f1dc53029e982d7bc3b4b6dc51e679c0f1`  
		Last Modified: Fri, 06 Jun 2025 23:09:19 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f026747287ad82fbc819b8c857e70adb1d75218fc3f41221b1591bf802e9d0`  
		Last Modified: Sat, 07 Jun 2025 02:12:32 GMT  
		Size: 21.7 MB (21672857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:43ed1b9a60d768ff82cc5df477a2fd2d487148f2a0e514daed7bca4cba295e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22643474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a24c1e03c14698278a3bd385e83c37d021a5750bc0cc12b39d4ce57ef71341`

```dockerfile
```

-	Layers:
	-	`sha256:0c7f62558466bf857633ef7626050e6cbb7c77b8dfa7dba89463c82e5f4af2d3`  
		Last Modified: Sat, 07 Jun 2025 01:19:24 GMT  
		Size: 22.6 MB (22626355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65e2aae5698e322871b42ae00b147c2953c832c98d1fa28241763a7164ec12c4`  
		Last Modified: Sat, 07 Jun 2025 01:19:25 GMT  
		Size: 17.1 KB (17119 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:foxy-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:487e2b121107be08d3dcfb759fdb0bc25f1622902a7b6fedb85236a602b4d789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229776472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce8a3d24ba5fc59286d4d98bf1349762b4946e63eecc2f6418de304af3f76b7`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
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
	-	`sha256:3da64ed2bb66a6ce3d36adf9712e73c205cbae57442bbdb8365c1c16617e0183`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 5.3 MB (5344104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a127babc495b469c32a2537669b10def6004f278427e28a9ad21e1eaad81c`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 4.0 KB (3983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd563e74b9280d17b11bae86038561c7184eda5ae05a08570ac236ede7caab26`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f376c0b3101d22149ca2d878d920aa16f69ba90b157b102210f0b0216b96c6`  
		Last Modified: Fri, 06 Jun 2025 23:12:25 GMT  
		Size: 108.9 MB (108878978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8bbf8c8a1cae034a096fd542d615567aabad879961709c67a9d412fa9cb10c`  
		Last Modified: Fri, 06 Jun 2025 23:12:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0828ae3bcc02cebe074457715b9015f612b41f3505eec2d509eb84191059d1`  
		Last Modified: Sat, 07 Jun 2025 00:45:00 GMT  
		Size: 67.7 MB (67674946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0008d8e892d97a7ab8afd15de5401052d67d5d1a11424408fe9bdf6f8facd4ea`  
		Last Modified: Sat, 07 Jun 2025 00:44:57 GMT  
		Size: 301.2 KB (301159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195e8afc91b0fc0fc13a30cd50b392436315c3301fc5dd8378e1bad63c83b178`  
		Last Modified: Sat, 07 Jun 2025 00:44:58 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7067dec2b246676b2e5d3e65aa8474d14fed126303588ae5ebd0040f9b0c2`  
		Last Modified: Sat, 07 Jun 2025 00:45:00 GMT  
		Size: 20.4 MB (20398057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:633ba80f46ca8fc360c6e93718a0f1006c287c8686db18b94cf9b54933a0d868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21563319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a424bdf2cc314396cca76f67161f150f45a995d96282b4256b5ad6cd5e25c277`

```dockerfile
```

-	Layers:
	-	`sha256:641f149cbb13fed4a2d3b7cf31a8214f520e730368002d5ee11037d2d7fc11f1`  
		Last Modified: Sat, 07 Jun 2025 01:19:39 GMT  
		Size: 21.5 MB (21546063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6850a9c9bc9c1da1ad6c90721c65cecef6622936daac15d6f1a08d200cb0e34`  
		Last Modified: Sat, 07 Jun 2025 01:19:40 GMT  
		Size: 17.3 KB (17256 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:foxy-ros-core`

```console
$ docker pull ros@sha256:233f8425f29a42bfbd95de9acf216921191cbc3d5421ee41139ec4946b80d258
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:foxy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:bde7c8b6d345de454b5dac6f5249c55bc7a5cc7a2c2986cbe4b87faff74fff67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159668678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad133bd4ef06f61336eaf87844a7d4d40482b853caa2f74682322914076a9e1e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 06:00:32 GMT
ARG RELEASE
# Fri, 01 Dec 2023 06:00:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 06:00:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 06:00:32 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 01 Dec 2023 06:00:32 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo "deb http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV ROS_DISTRO=foxy
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905dfb1bab3312147382cf593a88dfd91dcde255426f42b174c0a00cbfee3d49`  
		Last Modified: Fri, 06 Jun 2025 22:49:29 GMT  
		Size: 1.2 MB (1194819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bf200ef89210ac612db81e54c264d517b910910145ae871d765696f0b2599d`  
		Last Modified: Fri, 06 Jun 2025 22:49:29 GMT  
		Size: 5.4 MB (5363903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f4f1b29220d6398d0c70e5bf4d323cf24bc1b2b4587f6b1b9a02658100661b`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc09efa67422b34d4c77e03962a93fb1c22f91239484ef3e692b04953247ee3d`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fdc4be6b715533df3810ad59eb7a493b1ad5a0fcd129ace37d611a85328e0d7`  
		Last Modified: Fri, 06 Jun 2025 22:49:35 GMT  
		Size: 125.6 MB (125595150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd83c03f807b7ea0994bf1035dc345d86aa658f5159998acc62e1c70a214182`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:ea74b1607fc4dd1a8f37902c6ebe4faef897ca6c038ccbba0f66427232b7844f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18628064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea580783e9d8620d49f8daa117bd8ddcb2a6ea4178f22c318539d1acf6f53579`

```dockerfile
```

-	Layers:
	-	`sha256:06018cbdae5b90c89e6bee62965594d9d4aa5bf5746638138d8dd2476b3d5d38`  
		Last Modified: Sat, 07 Jun 2025 01:19:32 GMT  
		Size: 18.6 MB (18612948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f39e5d5101c1bb0ec4c1b76d33068788647bddbc3a45cfd2a02db9440f53ea7`  
		Last Modified: Sat, 07 Jun 2025 01:19:33 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:foxy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bd8104dd64efbcc029bdd091ff0f48d2ae1534af3a078aa1ebf0884052daf4bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141399846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc117f8978792a3b3742858bfdaa5357fa37bac5abdce2de50bbfbcd4c2d431`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 06:00:32 GMT
ARG RELEASE
# Fri, 01 Dec 2023 06:00:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 06:00:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 06:00:32 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 01 Dec 2023 06:00:32 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo "deb http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV ROS_DISTRO=foxy
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:32 GMT
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
	-	`sha256:3da64ed2bb66a6ce3d36adf9712e73c205cbae57442bbdb8365c1c16617e0183`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 5.3 MB (5344104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a127babc495b469c32a2537669b10def6004f278427e28a9ad21e1eaad81c`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 4.0 KB (3983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd563e74b9280d17b11bae86038561c7184eda5ae05a08570ac236ede7caab26`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f376c0b3101d22149ca2d878d920aa16f69ba90b157b102210f0b0216b96c6`  
		Last Modified: Fri, 06 Jun 2025 23:12:25 GMT  
		Size: 108.9 MB (108878978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8bbf8c8a1cae034a096fd542d615567aabad879961709c67a9d412fa9cb10c`  
		Last Modified: Fri, 06 Jun 2025 23:12:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:814dd8552cf538bd3e2b4136a218e10b7e798a9fff5fc58a999f66419ece5f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17546520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d19296288acc8269f4632218eab94f56376679f69743854981d09361034737`

```dockerfile
```

-	Layers:
	-	`sha256:fbe35413fbf6cd78b976514fb78fc21327f4c016ab9c7e0cb68df7a9ffd89c58`  
		Last Modified: Sat, 07 Jun 2025 01:19:46 GMT  
		Size: 17.5 MB (17531270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7a234ca656e538fc6a75900ffb7883e26bbed0b16d27b333ee8dccdbab3177`  
		Last Modified: Sat, 07 Jun 2025 01:19:47 GMT  
		Size: 15.2 KB (15250 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:foxy-ros-core-focal`

```console
$ docker pull ros@sha256:233f8425f29a42bfbd95de9acf216921191cbc3d5421ee41139ec4946b80d258
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:foxy-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:bde7c8b6d345de454b5dac6f5249c55bc7a5cc7a2c2986cbe4b87faff74fff67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159668678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad133bd4ef06f61336eaf87844a7d4d40482b853caa2f74682322914076a9e1e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 06:00:32 GMT
ARG RELEASE
# Fri, 01 Dec 2023 06:00:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 06:00:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 06:00:32 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 01 Dec 2023 06:00:32 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo "deb http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV ROS_DISTRO=foxy
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905dfb1bab3312147382cf593a88dfd91dcde255426f42b174c0a00cbfee3d49`  
		Last Modified: Fri, 06 Jun 2025 22:49:29 GMT  
		Size: 1.2 MB (1194819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bf200ef89210ac612db81e54c264d517b910910145ae871d765696f0b2599d`  
		Last Modified: Fri, 06 Jun 2025 22:49:29 GMT  
		Size: 5.4 MB (5363903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f4f1b29220d6398d0c70e5bf4d323cf24bc1b2b4587f6b1b9a02658100661b`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc09efa67422b34d4c77e03962a93fb1c22f91239484ef3e692b04953247ee3d`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fdc4be6b715533df3810ad59eb7a493b1ad5a0fcd129ace37d611a85328e0d7`  
		Last Modified: Fri, 06 Jun 2025 22:49:35 GMT  
		Size: 125.6 MB (125595150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd83c03f807b7ea0994bf1035dc345d86aa658f5159998acc62e1c70a214182`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:ea74b1607fc4dd1a8f37902c6ebe4faef897ca6c038ccbba0f66427232b7844f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18628064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea580783e9d8620d49f8daa117bd8ddcb2a6ea4178f22c318539d1acf6f53579`

```dockerfile
```

-	Layers:
	-	`sha256:06018cbdae5b90c89e6bee62965594d9d4aa5bf5746638138d8dd2476b3d5d38`  
		Last Modified: Sat, 07 Jun 2025 01:19:32 GMT  
		Size: 18.6 MB (18612948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f39e5d5101c1bb0ec4c1b76d33068788647bddbc3a45cfd2a02db9440f53ea7`  
		Last Modified: Sat, 07 Jun 2025 01:19:33 GMT  
		Size: 15.1 KB (15116 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:foxy-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:bd8104dd64efbcc029bdd091ff0f48d2ae1534af3a078aa1ebf0884052daf4bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141399846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc117f8978792a3b3742858bfdaa5357fa37bac5abdce2de50bbfbcd4c2d431`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 06:00:32 GMT
ARG RELEASE
# Fri, 01 Dec 2023 06:00:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 06:00:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 06:00:32 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 01 Dec 2023 06:00:32 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo "deb http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV ROS_DISTRO=foxy
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:32 GMT
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
	-	`sha256:3da64ed2bb66a6ce3d36adf9712e73c205cbae57442bbdb8365c1c16617e0183`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 5.3 MB (5344104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a127babc495b469c32a2537669b10def6004f278427e28a9ad21e1eaad81c`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 4.0 KB (3983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd563e74b9280d17b11bae86038561c7184eda5ae05a08570ac236ede7caab26`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f376c0b3101d22149ca2d878d920aa16f69ba90b157b102210f0b0216b96c6`  
		Last Modified: Fri, 06 Jun 2025 23:12:25 GMT  
		Size: 108.9 MB (108878978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8bbf8c8a1cae034a096fd542d615567aabad879961709c67a9d412fa9cb10c`  
		Last Modified: Fri, 06 Jun 2025 23:12:21 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:foxy-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:814dd8552cf538bd3e2b4136a218e10b7e798a9fff5fc58a999f66419ece5f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17546520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d19296288acc8269f4632218eab94f56376679f69743854981d09361034737`

```dockerfile
```

-	Layers:
	-	`sha256:fbe35413fbf6cd78b976514fb78fc21327f4c016ab9c7e0cb68df7a9ffd89c58`  
		Last Modified: Sat, 07 Jun 2025 01:19:46 GMT  
		Size: 17.5 MB (17531270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7a234ca656e538fc6a75900ffb7883e26bbed0b16d27b333ee8dccdbab3177`  
		Last Modified: Sat, 07 Jun 2025 01:19:47 GMT  
		Size: 15.2 KB (15250 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:foxy-ros1-bridge`

```console
$ docker pull ros@sha256:3df748a354582095c6d1a9263027bacd179cdf828157534d6442635095d8c356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:d0dca420c0e34068187d847e901f1b7ad8a453144bcc1ff331c67ee99ed60b0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.6 MB (354556761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1455d101c5c71ff7bf511dfd66d07a8691f54dc2aea6233dad8243b3b8f76aea`
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
# Sat, 09 Dec 2023 03:55:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:55:18 GMT
RUN echo "deb http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:55:18 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:55:18 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:55:18 GMT
ENV ROS_DISTRO=foxy
# Sat, 09 Dec 2023 03:57:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:57:23 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 09 Dec 2023 03:57:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:57:23 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:58:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:58:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 03:58:39 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:59:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:59:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 09 Dec 2023 03:59:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 09 Dec 2023 03:59:35 GMT
ENV ROS1_DISTRO=noetic
# Sat, 09 Dec 2023 03:59:35 GMT
ENV ROS2_DISTRO=foxy
# Sat, 09 Dec 2023 04:01:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.16.0-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:01:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.7-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:01:34 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:30ecab32a3b65c6ec04c63a65b90e627b49d1297d8793896ed50b656377d8a06`  
		Last Modified: Fri, 13 Dec 2024 20:02:48 GMT  
		Size: 28.6 MB (28584029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc1327734170da8c4ae4171fb4248189d0691d6b4a3f01b09239c3e34688651`  
		Last Modified: Fri, 13 Dec 2024 16:03:32 GMT  
		Size: 1.2 MB (1198788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77125e61032dbbcd43c015fe756de97b5661bdbbf4f5219588148f651ae900c1`  
		Last Modified: Fri, 13 Dec 2024 15:58:55 GMT  
		Size: 5.6 MB (5553989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cfdb297cb2e56f5144d6a03d94e416f7101347779b1dac8d072ddb965d0b5`  
		Last Modified: Fri, 13 Dec 2024 15:58:54 GMT  
		Size: 3.6 KB (3622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f8d76fdc12cd19e368e2e5b21e5d481559248fe3c64da35af018355d18977f`  
		Last Modified: Fri, 13 Dec 2024 19:02:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf35df53ba113fe177d0183f4f445e060ccef226ed32cd3aa6f3f4f4de6774d`  
		Last Modified: Fri, 13 Dec 2024 16:59:40 GMT  
		Size: 125.5 MB (125548513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756e62193488345e83b7f3bc2f2f5886a4e5f412e64e38fa594af820c9163a82`  
		Last Modified: Fri, 13 Dec 2024 16:03:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cebe9015ddead423a6b6692f059bcec1ee4a7135ac384b80dfddfd44c52f05`  
		Last Modified: Fri, 13 Dec 2024 15:54:13 GMT  
		Size: 73.5 MB (73519978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbd79866e649ea889791009144a2b64171483730cbc5851b85dadfe2dccc0d3`  
		Last Modified: Fri, 13 Dec 2024 16:59:31 GMT  
		Size: 271.1 KB (271061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29aa10f749f0e3485f98a7d6b1d1cc10f3c1165d1bf4afee0905d2aff8744e2e`  
		Last Modified: Fri, 13 Dec 2024 17:30:05 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74769e56d216fe1fa3364194dbaf8bdff6904a92bf9947f4e9255eb7f2368db`  
		Last Modified: Fri, 13 Dec 2024 17:09:31 GMT  
		Size: 21.7 MB (21683234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057ff5f003438bbf1a70b54ad3107bf12e5b462d8a68fc840e4d9dcd45138f2d`  
		Last Modified: Sat, 14 Dec 2024 10:42:21 GMT  
		Size: 5.4 KB (5404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbbc004a620e1e7fdfba67fe5bb2771bfa5d70dc58cf73166680dd158a889ee`  
		Last Modified: Fri, 13 Dec 2024 16:59:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c71f7f8c767245b2da788a8cf7dceea44db9385146db02309651a27bd5cd3a2`  
		Last Modified: Fri, 13 Dec 2024 16:59:40 GMT  
		Size: 76.5 MB (76492172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a57cdbb28b729ddfa83268c455ba85c6e54031fa38d939dff072bfd24873d32`  
		Last Modified: Sun, 15 Dec 2024 21:26:29 GMT  
		Size: 21.7 MB (21692589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c741ae3129549281c8610a35bfe3e10b39f0874fae2d38987b04a2063d2e6a4a`  
		Last Modified: Fri, 13 Dec 2024 16:59:37 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d1a6c46f9a144df8fff76353189b6acf19dd65ef1b487758a56b7960266d7347
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322212818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc6569dc3c3df330b1505026894f9f64ef725899f310877ea859d9511057c35`
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
# Sat, 09 Dec 2023 03:18:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:18:16 GMT
RUN echo "deb http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:18:17 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:18:17 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:18:17 GMT
ENV ROS_DISTRO=foxy
# Sat, 09 Dec 2023 03:20:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:20:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 09 Dec 2023 03:20:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:20:29 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:21:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:21:27 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 03:21:30 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:22:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:22:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 09 Dec 2023 03:22:32 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 09 Dec 2023 03:22:32 GMT
ENV ROS1_DISTRO=noetic
# Sat, 09 Dec 2023 03:22:32 GMT
ENV ROS2_DISTRO=foxy
# Sat, 09 Dec 2023 03:23:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.16.0-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:24:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.7-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:24:03 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:5d2acf9ee7cfde47b6ce997317767b8fa9bf8d93b8297016db9e093d06aa913d`  
		Last Modified: Fri, 13 Dec 2024 17:20:51 GMT  
		Size: 27.2 MB (27203865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2aa78ed8ad18394d7ae521e83b2810fec9fbb7d95aa074d794bb43e6e2bbfb`  
		Last Modified: Mon, 16 Dec 2024 02:12:36 GMT  
		Size: 1.2 MB (1198781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f106a95fef578814e019c4ac69f1cf32b15d5f85da2729a7ab2487c5d3505d`  
		Last Modified: Sat, 14 Dec 2024 00:59:42 GMT  
		Size: 5.5 MB (5532202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2293949a62535f558d267574d694fe0b0e9498fce13b94a8a2e83b00a4d86669`  
		Last Modified: Mon, 16 Dec 2024 02:05:56 GMT  
		Size: 3.6 KB (3625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a9aa07ed44d01bc5e93b12e2d7956a74afaa4429287652b3977b63f637eb95`  
		Last Modified: Sun, 15 Dec 2024 13:36:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c6bf64f4814b4883be6b658102c6e1626f806dd4da742884c5abaee2a0ef41`  
		Last Modified: Mon, 16 Dec 2024 01:37:36 GMT  
		Size: 108.9 MB (108868171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690afa1d3835689299293b326bad874dae11c7272f40b31361519f157bafc83d`  
		Last Modified: Sat, 14 Dec 2024 00:59:42 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7872575e51da68e3230da2c297adc491d124bf859b36958f1bbb8426f35ba1be`  
		Last Modified: Sat, 14 Dec 2024 00:59:51 GMT  
		Size: 67.9 MB (67873751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc82c8b47ed2a55171cb49066a548ce009f33651de5c18b9dc2086aabacfadc`  
		Last Modified: Sat, 14 Dec 2024 14:21:09 GMT  
		Size: 271.1 KB (271064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cda9fbaf443befc328955ce52a4dd2c785013d6799696a4312ceb7d63ac4649`  
		Last Modified: Sat, 14 Dec 2024 00:59:43 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e0e60e385c86f6ec04d573e8b226dc2ba301f5c10fdf44e7abb07e631cfaec`  
		Last Modified: Mon, 16 Dec 2024 00:44:59 GMT  
		Size: 20.4 MB (20408514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d4172bb37850053590c8bbf0338196240ede633d066a382295a21572b1fc8b`  
		Last Modified: Mon, 30 Dec 2024 08:06:22 GMT  
		Size: 5.4 KB (5403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c292a706f58ad87895b431b677d07c737296e8c792c8c10511ee7a5de6c971c0`  
		Last Modified: Mon, 17 Feb 2025 17:48:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a2e04f638e8e4d5c997363cd45c5a87919e4bc2b68a9b96359ce78a414bfdd`  
		Last Modified: Tue, 17 Dec 2024 08:59:21 GMT  
		Size: 76.5 MB (76512109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3ed3d56043a07cf4529a0f627c33bb37cb2dee51fbae9033aacaf67a91297a`  
		Last Modified: Tue, 17 Dec 2024 08:59:16 GMT  
		Size: 14.3 MB (14331997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd141cd9a723fb1f5d673bb205f80a3201cb973960b759d0f8fd8c7faafd91a0`  
		Last Modified: Mon, 17 Feb 2025 17:48:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:3df748a354582095c6d1a9263027bacd179cdf828157534d6442635095d8c356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:d0dca420c0e34068187d847e901f1b7ad8a453144bcc1ff331c67ee99ed60b0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.6 MB (354556761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1455d101c5c71ff7bf511dfd66d07a8691f54dc2aea6233dad8243b3b8f76aea`
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
# Sat, 09 Dec 2023 03:55:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:55:18 GMT
RUN echo "deb http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:55:18 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:55:18 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:55:18 GMT
ENV ROS_DISTRO=foxy
# Sat, 09 Dec 2023 03:57:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:57:23 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 09 Dec 2023 03:57:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:57:23 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:58:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:58:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 03:58:39 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:59:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:59:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 09 Dec 2023 03:59:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 09 Dec 2023 03:59:35 GMT
ENV ROS1_DISTRO=noetic
# Sat, 09 Dec 2023 03:59:35 GMT
ENV ROS2_DISTRO=foxy
# Sat, 09 Dec 2023 04:01:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.16.0-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:01:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.7-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:01:34 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:30ecab32a3b65c6ec04c63a65b90e627b49d1297d8793896ed50b656377d8a06`  
		Last Modified: Fri, 13 Dec 2024 20:02:48 GMT  
		Size: 28.6 MB (28584029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc1327734170da8c4ae4171fb4248189d0691d6b4a3f01b09239c3e34688651`  
		Last Modified: Fri, 13 Dec 2024 16:03:32 GMT  
		Size: 1.2 MB (1198788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77125e61032dbbcd43c015fe756de97b5661bdbbf4f5219588148f651ae900c1`  
		Last Modified: Fri, 13 Dec 2024 15:58:55 GMT  
		Size: 5.6 MB (5553989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cfdb297cb2e56f5144d6a03d94e416f7101347779b1dac8d072ddb965d0b5`  
		Last Modified: Fri, 13 Dec 2024 15:58:54 GMT  
		Size: 3.6 KB (3622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f8d76fdc12cd19e368e2e5b21e5d481559248fe3c64da35af018355d18977f`  
		Last Modified: Fri, 13 Dec 2024 19:02:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf35df53ba113fe177d0183f4f445e060ccef226ed32cd3aa6f3f4f4de6774d`  
		Last Modified: Fri, 13 Dec 2024 16:59:40 GMT  
		Size: 125.5 MB (125548513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756e62193488345e83b7f3bc2f2f5886a4e5f412e64e38fa594af820c9163a82`  
		Last Modified: Fri, 13 Dec 2024 16:03:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cebe9015ddead423a6b6692f059bcec1ee4a7135ac384b80dfddfd44c52f05`  
		Last Modified: Fri, 13 Dec 2024 15:54:13 GMT  
		Size: 73.5 MB (73519978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbd79866e649ea889791009144a2b64171483730cbc5851b85dadfe2dccc0d3`  
		Last Modified: Fri, 13 Dec 2024 16:59:31 GMT  
		Size: 271.1 KB (271061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29aa10f749f0e3485f98a7d6b1d1cc10f3c1165d1bf4afee0905d2aff8744e2e`  
		Last Modified: Fri, 13 Dec 2024 17:30:05 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74769e56d216fe1fa3364194dbaf8bdff6904a92bf9947f4e9255eb7f2368db`  
		Last Modified: Fri, 13 Dec 2024 17:09:31 GMT  
		Size: 21.7 MB (21683234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057ff5f003438bbf1a70b54ad3107bf12e5b462d8a68fc840e4d9dcd45138f2d`  
		Last Modified: Sat, 14 Dec 2024 10:42:21 GMT  
		Size: 5.4 KB (5404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbbc004a620e1e7fdfba67fe5bb2771bfa5d70dc58cf73166680dd158a889ee`  
		Last Modified: Fri, 13 Dec 2024 16:59:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c71f7f8c767245b2da788a8cf7dceea44db9385146db02309651a27bd5cd3a2`  
		Last Modified: Fri, 13 Dec 2024 16:59:40 GMT  
		Size: 76.5 MB (76492172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a57cdbb28b729ddfa83268c455ba85c6e54031fa38d939dff072bfd24873d32`  
		Last Modified: Sun, 15 Dec 2024 21:26:29 GMT  
		Size: 21.7 MB (21692589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c741ae3129549281c8610a35bfe3e10b39f0874fae2d38987b04a2063d2e6a4a`  
		Last Modified: Fri, 13 Dec 2024 16:59:37 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d1a6c46f9a144df8fff76353189b6acf19dd65ef1b487758a56b7960266d7347
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322212818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc6569dc3c3df330b1505026894f9f64ef725899f310877ea859d9511057c35`
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
# Sat, 09 Dec 2023 03:18:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:18:16 GMT
RUN echo "deb http://snapshots.ros.org/foxy/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:18:17 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:18:17 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:18:17 GMT
ENV ROS_DISTRO=foxy
# Sat, 09 Dec 2023 03:20:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:20:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 09 Dec 2023 03:20:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:20:29 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:21:23 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:21:27 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 03:21:30 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:22:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:22:31 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 09 Dec 2023 03:22:32 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 09 Dec 2023 03:22:32 GMT
ENV ROS1_DISTRO=noetic
# Sat, 09 Dec 2023 03:22:32 GMT
ENV ROS2_DISTRO=foxy
# Sat, 09 Dec 2023 03:23:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.16.0-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:24:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.7-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:24:03 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:5d2acf9ee7cfde47b6ce997317767b8fa9bf8d93b8297016db9e093d06aa913d`  
		Last Modified: Fri, 13 Dec 2024 17:20:51 GMT  
		Size: 27.2 MB (27203865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2aa78ed8ad18394d7ae521e83b2810fec9fbb7d95aa074d794bb43e6e2bbfb`  
		Last Modified: Mon, 16 Dec 2024 02:12:36 GMT  
		Size: 1.2 MB (1198781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f106a95fef578814e019c4ac69f1cf32b15d5f85da2729a7ab2487c5d3505d`  
		Last Modified: Sat, 14 Dec 2024 00:59:42 GMT  
		Size: 5.5 MB (5532202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2293949a62535f558d267574d694fe0b0e9498fce13b94a8a2e83b00a4d86669`  
		Last Modified: Mon, 16 Dec 2024 02:05:56 GMT  
		Size: 3.6 KB (3625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a9aa07ed44d01bc5e93b12e2d7956a74afaa4429287652b3977b63f637eb95`  
		Last Modified: Sun, 15 Dec 2024 13:36:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c6bf64f4814b4883be6b658102c6e1626f806dd4da742884c5abaee2a0ef41`  
		Last Modified: Mon, 16 Dec 2024 01:37:36 GMT  
		Size: 108.9 MB (108868171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690afa1d3835689299293b326bad874dae11c7272f40b31361519f157bafc83d`  
		Last Modified: Sat, 14 Dec 2024 00:59:42 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7872575e51da68e3230da2c297adc491d124bf859b36958f1bbb8426f35ba1be`  
		Last Modified: Sat, 14 Dec 2024 00:59:51 GMT  
		Size: 67.9 MB (67873751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc82c8b47ed2a55171cb49066a548ce009f33651de5c18b9dc2086aabacfadc`  
		Last Modified: Sat, 14 Dec 2024 14:21:09 GMT  
		Size: 271.1 KB (271064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cda9fbaf443befc328955ce52a4dd2c785013d6799696a4312ceb7d63ac4649`  
		Last Modified: Sat, 14 Dec 2024 00:59:43 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e0e60e385c86f6ec04d573e8b226dc2ba301f5c10fdf44e7abb07e631cfaec`  
		Last Modified: Mon, 16 Dec 2024 00:44:59 GMT  
		Size: 20.4 MB (20408514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d4172bb37850053590c8bbf0338196240ede633d066a382295a21572b1fc8b`  
		Last Modified: Mon, 30 Dec 2024 08:06:22 GMT  
		Size: 5.4 KB (5403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c292a706f58ad87895b431b677d07c737296e8c792c8c10511ee7a5de6c971c0`  
		Last Modified: Mon, 17 Feb 2025 17:48:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a2e04f638e8e4d5c997363cd45c5a87919e4bc2b68a9b96359ce78a414bfdd`  
		Last Modified: Tue, 17 Dec 2024 08:59:21 GMT  
		Size: 76.5 MB (76512109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3ed3d56043a07cf4529a0f627c33bb37cb2dee51fbae9033aacaf67a91297a`  
		Last Modified: Tue, 17 Dec 2024 08:59:16 GMT  
		Size: 14.3 MB (14331997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd141cd9a723fb1f5d673bb205f80a3201cb973960b759d0f8fd8c7faafd91a0`  
		Last Modified: Mon, 17 Feb 2025 17:48:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic`

```console
$ docker pull ros@sha256:c9d2f75092d231e91bb82bec267fe20955a4929890027feb453a4b08f489487d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:galactic` - linux; amd64

```console
$ docker pull ros@sha256:98f9e5f7859236b18f9d5956c211b1e65ecf2be0eecb7d5e1d7e1ea78af9d450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (238975790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ffcc5430a28e01427c334f5dc1dc19cf3c71cb22a017b4741bfab6d53fe3e22`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
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
	-	`sha256:945134a43cf5436bcd4c4fabbe5f8689d89a7e3813c2be30f673ddd81f849543`  
		Last Modified: Fri, 06 Jun 2025 22:49:26 GMT  
		Size: 1.2 MB (1194815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddc9e11a6f24d45a0fd6c2fd537bb5c96fcfe7ad0f2a5534cc8f35938605463`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 5.4 MB (5363955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f4f1b29220d6398d0c70e5bf4d323cf24bc1b2b4587f6b1b9a02658100661b`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49802bd0654544e040c6c148afac52b1bc2758819ccf7844589f6ea1f8d42935`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4547639f65f5b71b189c02bc2917e674ef90e9b6aac3744e8961e9ae71488bc0`  
		Last Modified: Fri, 06 Jun 2025 22:49:32 GMT  
		Size: 109.2 MB (109184147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd83c03f807b7ea0994bf1035dc345d86aa658f5159998acc62e1c70a214182`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd6130c854a7c7deccae5be3df2133266053727e77edb5553b49a3f07c39cf8`  
		Last Modified: Sat, 07 Jun 2025 01:24:00 GMT  
		Size: 73.3 MB (73268699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92773102787c1ed83158d901c443a22e72710fd2821edf229d354302d9bb6589`  
		Last Modified: Fri, 06 Jun 2025 23:25:24 GMT  
		Size: 308.6 KB (308613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cd060b418219001fd791439bf81ed5acda05148f2f046a379087a3659e4e07`  
		Last Modified: Fri, 06 Jun 2025 23:25:27 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b4106c64a336d4312d21c00493611465eda6a53262564b5789d93a322c8dcd`  
		Last Modified: Sat, 07 Jun 2025 01:23:56 GMT  
		Size: 22.1 MB (22138284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic` - unknown; unknown

```console
$ docker pull ros@sha256:b6d203e67d5964510ea58905e769ea3610c57338b8759e49541de4b399f62172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21772917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e255e579a924496a78e3a0b9c24bb53224f9c53a53f5012d77e3eb8f1a8039`

```dockerfile
```

-	Layers:
	-	`sha256:41c025e72d1e802ebc408a6d258c99ea6c3318a4927da14afb47025422cb5e65`  
		Last Modified: Sat, 07 Jun 2025 01:19:43 GMT  
		Size: 21.8 MB (21755730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20f696845da6b6223f1206047b3b3d059e483bf237a4341fcfbd2c7e7a0575c`  
		Last Modified: Sat, 07 Jun 2025 01:19:44 GMT  
		Size: 17.2 KB (17187 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:galactic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eaedd5322112f1fb29519d09baf756a224d84e287455e6a8b5dbff053a356dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226604103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9792d43dba722882763614064989ed09b6ca0125ab49161f2051ad6cd7705a5a`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
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
	-	`sha256:3da64ed2bb66a6ce3d36adf9712e73c205cbae57442bbdb8365c1c16617e0183`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 5.3 MB (5344104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a127babc495b469c32a2537669b10def6004f278427e28a9ad21e1eaad81c`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 4.0 KB (3983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0c8192db141ffbb5140fe411c5eced3897890db3b1fcea32de47823cb1e9f5`  
		Last Modified: Fri, 06 Jun 2025 23:24:52 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d05758778f2814758f8af46ee68fc371f4c70c37e44d6667bd998a6a401889`  
		Last Modified: Sat, 07 Jun 2025 23:59:04 GMT  
		Size: 104.7 MB (104674775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d724ca4312a3680a73d9b733e052cdc81fc0456386fb1c596c2520fc09de111`  
		Last Modified: Fri, 06 Jun 2025 23:24:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75b490757b30dade46f2da5ace5d4729ad05bfce3c989747b9cc271a60d8696`  
		Last Modified: Sat, 07 Jun 2025 11:54:37 GMT  
		Size: 67.6 MB (67616740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749f0fee2ade4717f94fb8fbca0c15d03895ca738793e29f7de8aa9122e3793e`  
		Last Modified: Sat, 07 Jun 2025 01:12:38 GMT  
		Size: 308.6 KB (308611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058d1b759c544dc86e0206d68eb46690ce0bff76dbb7c93936c619d810f074c9`  
		Last Modified: Sat, 07 Jun 2025 01:12:41 GMT  
		Size: 2.5 KB (2475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2ab5088ca56b495d0591758e096786563c29f23898224f755dd1dab7398fac`  
		Last Modified: Sat, 07 Jun 2025 11:54:44 GMT  
		Size: 21.5 MB (21480630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic` - unknown; unknown

```console
$ docker pull ros@sha256:b474cae5bff3cb1f75e809fbf49e95a76e43a09f544121b0448388aa4ac65f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21793637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3746a18bfc50b6d25389611b5050dd370b3817c466b99140219a01d8c3fa8c5e`

```dockerfile
```

-	Layers:
	-	`sha256:464f23f22d6008437b37547ff8cfdeb68eef5764f21caaf5ad74ab98a9b664b2`  
		Last Modified: Sat, 07 Jun 2025 01:20:04 GMT  
		Size: 21.8 MB (21776313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15a4879757c50c2079366e7fd0020cceb1f8ca7b673c7e8178057aaf539069bb`  
		Last Modified: Sat, 07 Jun 2025 01:20:05 GMT  
		Size: 17.3 KB (17324 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:galactic-ros-base`

```console
$ docker pull ros@sha256:c9d2f75092d231e91bb82bec267fe20955a4929890027feb453a4b08f489487d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:galactic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:98f9e5f7859236b18f9d5956c211b1e65ecf2be0eecb7d5e1d7e1ea78af9d450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (238975790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ffcc5430a28e01427c334f5dc1dc19cf3c71cb22a017b4741bfab6d53fe3e22`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
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
	-	`sha256:945134a43cf5436bcd4c4fabbe5f8689d89a7e3813c2be30f673ddd81f849543`  
		Last Modified: Fri, 06 Jun 2025 22:49:26 GMT  
		Size: 1.2 MB (1194815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddc9e11a6f24d45a0fd6c2fd537bb5c96fcfe7ad0f2a5534cc8f35938605463`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 5.4 MB (5363955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f4f1b29220d6398d0c70e5bf4d323cf24bc1b2b4587f6b1b9a02658100661b`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49802bd0654544e040c6c148afac52b1bc2758819ccf7844589f6ea1f8d42935`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4547639f65f5b71b189c02bc2917e674ef90e9b6aac3744e8961e9ae71488bc0`  
		Last Modified: Fri, 06 Jun 2025 22:49:32 GMT  
		Size: 109.2 MB (109184147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd83c03f807b7ea0994bf1035dc345d86aa658f5159998acc62e1c70a214182`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd6130c854a7c7deccae5be3df2133266053727e77edb5553b49a3f07c39cf8`  
		Last Modified: Sat, 07 Jun 2025 01:24:00 GMT  
		Size: 73.3 MB (73268699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92773102787c1ed83158d901c443a22e72710fd2821edf229d354302d9bb6589`  
		Last Modified: Fri, 06 Jun 2025 23:25:24 GMT  
		Size: 308.6 KB (308613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cd060b418219001fd791439bf81ed5acda05148f2f046a379087a3659e4e07`  
		Last Modified: Fri, 06 Jun 2025 23:25:27 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b4106c64a336d4312d21c00493611465eda6a53262564b5789d93a322c8dcd`  
		Last Modified: Sat, 07 Jun 2025 01:23:56 GMT  
		Size: 22.1 MB (22138284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:b6d203e67d5964510ea58905e769ea3610c57338b8759e49541de4b399f62172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21772917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e255e579a924496a78e3a0b9c24bb53224f9c53a53f5012d77e3eb8f1a8039`

```dockerfile
```

-	Layers:
	-	`sha256:41c025e72d1e802ebc408a6d258c99ea6c3318a4927da14afb47025422cb5e65`  
		Last Modified: Sat, 07 Jun 2025 01:19:43 GMT  
		Size: 21.8 MB (21755730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20f696845da6b6223f1206047b3b3d059e483bf237a4341fcfbd2c7e7a0575c`  
		Last Modified: Sat, 07 Jun 2025 01:19:44 GMT  
		Size: 17.2 KB (17187 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:galactic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eaedd5322112f1fb29519d09baf756a224d84e287455e6a8b5dbff053a356dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226604103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9792d43dba722882763614064989ed09b6ca0125ab49161f2051ad6cd7705a5a`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
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
	-	`sha256:3da64ed2bb66a6ce3d36adf9712e73c205cbae57442bbdb8365c1c16617e0183`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 5.3 MB (5344104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a127babc495b469c32a2537669b10def6004f278427e28a9ad21e1eaad81c`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 4.0 KB (3983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0c8192db141ffbb5140fe411c5eced3897890db3b1fcea32de47823cb1e9f5`  
		Last Modified: Fri, 06 Jun 2025 23:24:52 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d05758778f2814758f8af46ee68fc371f4c70c37e44d6667bd998a6a401889`  
		Last Modified: Sat, 07 Jun 2025 23:59:04 GMT  
		Size: 104.7 MB (104674775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d724ca4312a3680a73d9b733e052cdc81fc0456386fb1c596c2520fc09de111`  
		Last Modified: Fri, 06 Jun 2025 23:24:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75b490757b30dade46f2da5ace5d4729ad05bfce3c989747b9cc271a60d8696`  
		Last Modified: Sat, 07 Jun 2025 11:54:37 GMT  
		Size: 67.6 MB (67616740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749f0fee2ade4717f94fb8fbca0c15d03895ca738793e29f7de8aa9122e3793e`  
		Last Modified: Sat, 07 Jun 2025 01:12:38 GMT  
		Size: 308.6 KB (308611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058d1b759c544dc86e0206d68eb46690ce0bff76dbb7c93936c619d810f074c9`  
		Last Modified: Sat, 07 Jun 2025 01:12:41 GMT  
		Size: 2.5 KB (2475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2ab5088ca56b495d0591758e096786563c29f23898224f755dd1dab7398fac`  
		Last Modified: Sat, 07 Jun 2025 11:54:44 GMT  
		Size: 21.5 MB (21480630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:b474cae5bff3cb1f75e809fbf49e95a76e43a09f544121b0448388aa4ac65f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21793637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3746a18bfc50b6d25389611b5050dd370b3817c466b99140219a01d8c3fa8c5e`

```dockerfile
```

-	Layers:
	-	`sha256:464f23f22d6008437b37547ff8cfdeb68eef5764f21caaf5ad74ab98a9b664b2`  
		Last Modified: Sat, 07 Jun 2025 01:20:04 GMT  
		Size: 21.8 MB (21776313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15a4879757c50c2079366e7fd0020cceb1f8ca7b673c7e8178057aaf539069bb`  
		Last Modified: Sat, 07 Jun 2025 01:20:05 GMT  
		Size: 17.3 KB (17324 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:galactic-ros-base-focal`

```console
$ docker pull ros@sha256:c9d2f75092d231e91bb82bec267fe20955a4929890027feb453a4b08f489487d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:galactic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:98f9e5f7859236b18f9d5956c211b1e65ecf2be0eecb7d5e1d7e1ea78af9d450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (238975790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ffcc5430a28e01427c334f5dc1dc19cf3c71cb22a017b4741bfab6d53fe3e22`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
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
	-	`sha256:945134a43cf5436bcd4c4fabbe5f8689d89a7e3813c2be30f673ddd81f849543`  
		Last Modified: Fri, 06 Jun 2025 22:49:26 GMT  
		Size: 1.2 MB (1194815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddc9e11a6f24d45a0fd6c2fd537bb5c96fcfe7ad0f2a5534cc8f35938605463`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 5.4 MB (5363955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f4f1b29220d6398d0c70e5bf4d323cf24bc1b2b4587f6b1b9a02658100661b`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49802bd0654544e040c6c148afac52b1bc2758819ccf7844589f6ea1f8d42935`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4547639f65f5b71b189c02bc2917e674ef90e9b6aac3744e8961e9ae71488bc0`  
		Last Modified: Fri, 06 Jun 2025 22:49:32 GMT  
		Size: 109.2 MB (109184147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd83c03f807b7ea0994bf1035dc345d86aa658f5159998acc62e1c70a214182`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd6130c854a7c7deccae5be3df2133266053727e77edb5553b49a3f07c39cf8`  
		Last Modified: Sat, 07 Jun 2025 01:24:00 GMT  
		Size: 73.3 MB (73268699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92773102787c1ed83158d901c443a22e72710fd2821edf229d354302d9bb6589`  
		Last Modified: Fri, 06 Jun 2025 23:25:24 GMT  
		Size: 308.6 KB (308613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cd060b418219001fd791439bf81ed5acda05148f2f046a379087a3659e4e07`  
		Last Modified: Fri, 06 Jun 2025 23:25:27 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b4106c64a336d4312d21c00493611465eda6a53262564b5789d93a322c8dcd`  
		Last Modified: Sat, 07 Jun 2025 01:23:56 GMT  
		Size: 22.1 MB (22138284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:b6d203e67d5964510ea58905e769ea3610c57338b8759e49541de4b399f62172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21772917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e255e579a924496a78e3a0b9c24bb53224f9c53a53f5012d77e3eb8f1a8039`

```dockerfile
```

-	Layers:
	-	`sha256:41c025e72d1e802ebc408a6d258c99ea6c3318a4927da14afb47025422cb5e65`  
		Last Modified: Sat, 07 Jun 2025 01:19:43 GMT  
		Size: 21.8 MB (21755730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20f696845da6b6223f1206047b3b3d059e483bf237a4341fcfbd2c7e7a0575c`  
		Last Modified: Sat, 07 Jun 2025 01:19:44 GMT  
		Size: 17.2 KB (17187 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:galactic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eaedd5322112f1fb29519d09baf756a224d84e287455e6a8b5dbff053a356dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226604103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9792d43dba722882763614064989ed09b6ca0125ab49161f2051ad6cd7705a5a`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Tue, 25 May 2021 09:27:44 GMT
RUN echo "deb http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
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
	-	`sha256:3da64ed2bb66a6ce3d36adf9712e73c205cbae57442bbdb8365c1c16617e0183`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 5.3 MB (5344104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a127babc495b469c32a2537669b10def6004f278427e28a9ad21e1eaad81c`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 4.0 KB (3983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0c8192db141ffbb5140fe411c5eced3897890db3b1fcea32de47823cb1e9f5`  
		Last Modified: Fri, 06 Jun 2025 23:24:52 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d05758778f2814758f8af46ee68fc371f4c70c37e44d6667bd998a6a401889`  
		Last Modified: Sat, 07 Jun 2025 23:59:04 GMT  
		Size: 104.7 MB (104674775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d724ca4312a3680a73d9b733e052cdc81fc0456386fb1c596c2520fc09de111`  
		Last Modified: Fri, 06 Jun 2025 23:24:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75b490757b30dade46f2da5ace5d4729ad05bfce3c989747b9cc271a60d8696`  
		Last Modified: Sat, 07 Jun 2025 11:54:37 GMT  
		Size: 67.6 MB (67616740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749f0fee2ade4717f94fb8fbca0c15d03895ca738793e29f7de8aa9122e3793e`  
		Last Modified: Sat, 07 Jun 2025 01:12:38 GMT  
		Size: 308.6 KB (308611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058d1b759c544dc86e0206d68eb46690ce0bff76dbb7c93936c619d810f074c9`  
		Last Modified: Sat, 07 Jun 2025 01:12:41 GMT  
		Size: 2.5 KB (2475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2ab5088ca56b495d0591758e096786563c29f23898224f755dd1dab7398fac`  
		Last Modified: Sat, 07 Jun 2025 11:54:44 GMT  
		Size: 21.5 MB (21480630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:b474cae5bff3cb1f75e809fbf49e95a76e43a09f544121b0448388aa4ac65f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21793637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3746a18bfc50b6d25389611b5050dd370b3817c466b99140219a01d8c3fa8c5e`

```dockerfile
```

-	Layers:
	-	`sha256:464f23f22d6008437b37547ff8cfdeb68eef5764f21caaf5ad74ab98a9b664b2`  
		Last Modified: Sat, 07 Jun 2025 01:20:04 GMT  
		Size: 21.8 MB (21776313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15a4879757c50c2079366e7fd0020cceb1f8ca7b673c7e8178057aaf539069bb`  
		Last Modified: Sat, 07 Jun 2025 01:20:05 GMT  
		Size: 17.3 KB (17324 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:galactic-ros-core`

```console
$ docker pull ros@sha256:8f5a6326be760da91c01175d40bd70ee1aa4a159c0c50f03eebd42fc7bc814e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:galactic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:548cb7cbc1f0f1bddf6119aaafd9c0f58d4c4d49979385f3506f508dcbc86f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143257724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b098d76410ec3458136c1083779e1b7d9632e00d5c54bb73bab856fda3b05240`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 06:00:32 GMT
ARG RELEASE
# Fri, 01 Dec 2023 06:00:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 06:00:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 06:00:32 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 01 Dec 2023 06:00:32 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo "deb http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV ROS_DISTRO=galactic
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945134a43cf5436bcd4c4fabbe5f8689d89a7e3813c2be30f673ddd81f849543`  
		Last Modified: Fri, 06 Jun 2025 22:49:26 GMT  
		Size: 1.2 MB (1194815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddc9e11a6f24d45a0fd6c2fd537bb5c96fcfe7ad0f2a5534cc8f35938605463`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 5.4 MB (5363955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f4f1b29220d6398d0c70e5bf4d323cf24bc1b2b4587f6b1b9a02658100661b`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49802bd0654544e040c6c148afac52b1bc2758819ccf7844589f6ea1f8d42935`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4547639f65f5b71b189c02bc2917e674ef90e9b6aac3744e8961e9ae71488bc0`  
		Last Modified: Fri, 06 Jun 2025 22:49:32 GMT  
		Size: 109.2 MB (109184147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd83c03f807b7ea0994bf1035dc345d86aa658f5159998acc62e1c70a214182`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:3d840b0b1e25ec3dfdd1e6aa095609a71c48c653e3bc5ead24e0af09555d6d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17529458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617872342dc41f43ce15777a293a32bf0c10e480474dd48736cce76463dab31d`

```dockerfile
```

-	Layers:
	-	`sha256:f9556e6b5d67234ddbb1027d5eafebb92f48afedc0ad3ab84d357cc5826a3e7f`  
		Last Modified: Sat, 07 Jun 2025 01:19:51 GMT  
		Size: 17.5 MB (17514286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ab891ec9bb5414a34308ecf2465716cafa4bc4982d8944350155dff3a264317`  
		Last Modified: Sat, 07 Jun 2025 01:19:52 GMT  
		Size: 15.2 KB (15172 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:galactic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6f5cd9da10e0131cae5062e66a561ed67c3085e7d9e70fb4d907e1ba97b2d915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137195647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59688edd96d9a55b6d48b8331191b191d9ead03102fdbe5c542840e57213422`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 06:00:32 GMT
ARG RELEASE
# Fri, 01 Dec 2023 06:00:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 06:00:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 06:00:32 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 01 Dec 2023 06:00:32 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo "deb http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV ROS_DISTRO=galactic
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:32 GMT
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
	-	`sha256:3da64ed2bb66a6ce3d36adf9712e73c205cbae57442bbdb8365c1c16617e0183`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 5.3 MB (5344104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a127babc495b469c32a2537669b10def6004f278427e28a9ad21e1eaad81c`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 4.0 KB (3983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0c8192db141ffbb5140fe411c5eced3897890db3b1fcea32de47823cb1e9f5`  
		Last Modified: Fri, 06 Jun 2025 23:24:52 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d05758778f2814758f8af46ee68fc371f4c70c37e44d6667bd998a6a401889`  
		Last Modified: Sat, 07 Jun 2025 23:59:04 GMT  
		Size: 104.7 MB (104674775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d724ca4312a3680a73d9b733e052cdc81fc0456386fb1c596c2520fc09de111`  
		Last Modified: Fri, 06 Jun 2025 23:24:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:ef5b00499c028f1c7e984c287ebdb0d972cb9f3219437caa066c276246817e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17521884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9ee7cfcbef04246e6b926052620d528750616ee431dc2c06308131090ee7d8`

```dockerfile
```

-	Layers:
	-	`sha256:b473b35e03df4ffd11151436147454b8ad88a0f1f1628f50dda41f95889d37f4`  
		Last Modified: Sat, 07 Jun 2025 01:20:06 GMT  
		Size: 17.5 MB (17506578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:873ee2c735e58d05673811da84537673af3746b02f8c667a92f71831778f6d56`  
		Last Modified: Sat, 07 Jun 2025 01:20:07 GMT  
		Size: 15.3 KB (15306 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:galactic-ros-core-focal`

```console
$ docker pull ros@sha256:8f5a6326be760da91c01175d40bd70ee1aa4a159c0c50f03eebd42fc7bc814e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `ros:galactic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:548cb7cbc1f0f1bddf6119aaafd9c0f58d4c4d49979385f3506f508dcbc86f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143257724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b098d76410ec3458136c1083779e1b7d9632e00d5c54bb73bab856fda3b05240`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 06:00:32 GMT
ARG RELEASE
# Fri, 01 Dec 2023 06:00:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 06:00:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 06:00:32 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 01 Dec 2023 06:00:32 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo "deb http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV ROS_DISTRO=galactic
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945134a43cf5436bcd4c4fabbe5f8689d89a7e3813c2be30f673ddd81f849543`  
		Last Modified: Fri, 06 Jun 2025 22:49:26 GMT  
		Size: 1.2 MB (1194815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddc9e11a6f24d45a0fd6c2fd537bb5c96fcfe7ad0f2a5534cc8f35938605463`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 5.4 MB (5363955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f4f1b29220d6398d0c70e5bf4d323cf24bc1b2b4587f6b1b9a02658100661b`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49802bd0654544e040c6c148afac52b1bc2758819ccf7844589f6ea1f8d42935`  
		Last Modified: Fri, 06 Jun 2025 22:49:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4547639f65f5b71b189c02bc2917e674ef90e9b6aac3744e8961e9ae71488bc0`  
		Last Modified: Fri, 06 Jun 2025 22:49:32 GMT  
		Size: 109.2 MB (109184147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd83c03f807b7ea0994bf1035dc345d86aa658f5159998acc62e1c70a214182`  
		Last Modified: Fri, 06 Jun 2025 22:49:28 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:3d840b0b1e25ec3dfdd1e6aa095609a71c48c653e3bc5ead24e0af09555d6d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17529458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617872342dc41f43ce15777a293a32bf0c10e480474dd48736cce76463dab31d`

```dockerfile
```

-	Layers:
	-	`sha256:f9556e6b5d67234ddbb1027d5eafebb92f48afedc0ad3ab84d357cc5826a3e7f`  
		Last Modified: Sat, 07 Jun 2025 01:19:51 GMT  
		Size: 17.5 MB (17514286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ab891ec9bb5414a34308ecf2465716cafa4bc4982d8944350155dff3a264317`  
		Last Modified: Sat, 07 Jun 2025 01:19:52 GMT  
		Size: 15.2 KB (15172 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:galactic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6f5cd9da10e0131cae5062e66a561ed67c3085e7d9e70fb4d907e1ba97b2d915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137195647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59688edd96d9a55b6d48b8331191b191d9ead03102fdbe5c542840e57213422`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Dec 2023 06:00:32 GMT
ARG RELEASE
# Fri, 01 Dec 2023 06:00:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 06:00:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 06:00:32 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 01 Dec 2023 06:00:32 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Fri, 01 Dec 2023 06:00:32 GMT
CMD ["/bin/bash"]
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
RUN echo "deb http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV LC_ALL=C.UTF-8
# Fri, 01 Dec 2023 06:00:32 GMT
ENV ROS_DISTRO=galactic
# Fri, 01 Dec 2023 06:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Fri, 01 Dec 2023 06:00:32 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 01 Dec 2023 06:00:32 GMT
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
	-	`sha256:3da64ed2bb66a6ce3d36adf9712e73c205cbae57442bbdb8365c1c16617e0183`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 5.3 MB (5344104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a127babc495b469c32a2537669b10def6004f278427e28a9ad21e1eaad81c`  
		Last Modified: Fri, 06 Jun 2025 23:12:20 GMT  
		Size: 4.0 KB (3983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0c8192db141ffbb5140fe411c5eced3897890db3b1fcea32de47823cb1e9f5`  
		Last Modified: Fri, 06 Jun 2025 23:24:52 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d05758778f2814758f8af46ee68fc371f4c70c37e44d6667bd998a6a401889`  
		Last Modified: Sat, 07 Jun 2025 23:59:04 GMT  
		Size: 104.7 MB (104674775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d724ca4312a3680a73d9b733e052cdc81fc0456386fb1c596c2520fc09de111`  
		Last Modified: Fri, 06 Jun 2025 23:24:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:galactic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:ef5b00499c028f1c7e984c287ebdb0d972cb9f3219437caa066c276246817e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17521884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9ee7cfcbef04246e6b926052620d528750616ee431dc2c06308131090ee7d8`

```dockerfile
```

-	Layers:
	-	`sha256:b473b35e03df4ffd11151436147454b8ad88a0f1f1628f50dda41f95889d37f4`  
		Last Modified: Sat, 07 Jun 2025 01:20:06 GMT  
		Size: 17.5 MB (17506578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:873ee2c735e58d05673811da84537673af3746b02f8c667a92f71831778f6d56`  
		Last Modified: Sat, 07 Jun 2025 01:20:07 GMT  
		Size: 15.3 KB (15306 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:galactic-ros1-bridge`

```console
$ docker pull ros@sha256:f4caef292184e90c294cd14636c2812efa0a9c18fe63021c3002a82509f1519a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:a2f06953930b0a209295138745d606b1936f0b0564106df9230e2a6612b8b9a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.7 MB (335739532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972da3292152b13c9d2c6b8c13315b189d7f9cff1fe58adac5d33a1bc5be2407`
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
# Sat, 09 Dec 2023 03:55:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 04:01:42 GMT
RUN echo "deb http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 04:01:42 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 04:01:42 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 04:01:42 GMT
ENV ROS_DISTRO=galactic
# Sat, 09 Dec 2023 04:02:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:02:33 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 09 Dec 2023 04:02:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 04:02:33 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 04:02:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:03:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 04:03:06 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 04:03:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:03:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 09 Dec 2023 04:03:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 09 Dec 2023 04:03:31 GMT
ENV ROS1_DISTRO=noetic
# Sat, 09 Dec 2023 04:03:31 GMT
ENV ROS2_DISTRO=galactic
# Sat, 09 Dec 2023 04:03:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.16.0-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:04:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.4-1*     ros-galactic-demo-nodes-py=0.14.4-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:04:10 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:30ecab32a3b65c6ec04c63a65b90e627b49d1297d8793896ed50b656377d8a06`  
		Last Modified: Fri, 13 Dec 2024 20:02:48 GMT  
		Size: 28.6 MB (28584029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc1327734170da8c4ae4171fb4248189d0691d6b4a3f01b09239c3e34688651`  
		Last Modified: Fri, 13 Dec 2024 16:03:32 GMT  
		Size: 1.2 MB (1198788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77125e61032dbbcd43c015fe756de97b5661bdbbf4f5219588148f651ae900c1`  
		Last Modified: Fri, 13 Dec 2024 15:58:55 GMT  
		Size: 5.6 MB (5553989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cfdb297cb2e56f5144d6a03d94e416f7101347779b1dac8d072ddb965d0b5`  
		Last Modified: Fri, 13 Dec 2024 15:58:54 GMT  
		Size: 3.6 KB (3622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ae93d7330b04913f411e004ee6e95c6f115a405deced6159ed0ae4c9987099`  
		Last Modified: Sun, 15 Dec 2024 01:28:21 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aadbc41c419150c402c40f1d1eed2da57691737b48cfabb2a85a677c999bdb79`  
		Last Modified: Fri, 13 Dec 2024 16:03:41 GMT  
		Size: 109.2 MB (109169623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f16c937df28690cec98c60ae445a5ad2e4d5c2868816a30a5d8859297cd824c`  
		Last Modified: Fri, 13 Dec 2024 16:03:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491e9e6abb4a9e20e09b6c4e4a30c80e408608a98793f29587a4d6f27eced1e3`  
		Last Modified: Sun, 15 Dec 2024 01:28:30 GMT  
		Size: 73.5 MB (73462168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b21021fd9b9e6faa1b78a6061fb9d053fe7c15d2241f597844b39fd421ecca`  
		Last Modified: Mon, 16 Dec 2024 06:38:10 GMT  
		Size: 279.0 KB (278988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b4e77c324c9b353c1655c675dc3e15d5690491f12eb6cc3f7983b7541e3ee`  
		Last Modified: Fri, 13 Dec 2024 15:44:11 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8d940467045531264741a07da79cb54953c596a4a949f3a20bb49f0e647f93`  
		Last Modified: Fri, 13 Dec 2024 15:58:55 GMT  
		Size: 22.1 MB (22140300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a4ad6250fdd606f65fe888d9aeeae5cb468c07f8b0a609f4bb0f7e3e036953`  
		Last Modified: Mon, 16 Dec 2024 07:47:13 GMT  
		Size: 5.4 KB (5405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa839d68c2779d2c21b487d0e59c1c818f020b889e6019c78caa3626e48458d8`  
		Last Modified: Mon, 16 Dec 2024 10:08:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62f7f6251bccfdf666858e6a457027bff3aee9e402b196a7e93519b6a230a7d`  
		Last Modified: Mon, 16 Dec 2024 10:08:44 GMT  
		Size: 78.8 MB (78845967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf377c92f3fc74e02dc633002b07ec3f6b1fbda80d373c592630677be0a45f4`  
		Last Modified: Mon, 16 Dec 2024 10:08:48 GMT  
		Size: 16.5 MB (16493310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff95dbe602ee48c3060f917022573dfd5abc52c081264a6eaa8b7c2904654a0`  
		Last Modified: Mon, 16 Dec 2024 10:08:37 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1612b2093f25d491c55d95cc50e98f9c70e45c1f3770e7295d4e6c5c4b878582
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.0 MB (322971458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac58377f8466e6f1526903cc312deda40e2eea7bebf48c85a2d637266a5f82a5`
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
# Sat, 09 Dec 2023 03:18:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:24:08 GMT
RUN echo "deb http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:24:09 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:24:09 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:24:09 GMT
ENV ROS_DISTRO=galactic
# Sat, 09 Dec 2023 03:24:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:25:01 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 09 Dec 2023 03:25:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:25:02 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:25:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:25:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 03:25:30 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:25:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:25:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 09 Dec 2023 03:25:55 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 09 Dec 2023 03:25:55 GMT
ENV ROS1_DISTRO=noetic
# Sat, 09 Dec 2023 03:25:55 GMT
ENV ROS2_DISTRO=galactic
# Sat, 09 Dec 2023 03:26:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.16.0-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:26:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.4-1*     ros-galactic-demo-nodes-py=0.14.4-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:26:27 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:5d2acf9ee7cfde47b6ce997317767b8fa9bf8d93b8297016db9e093d06aa913d`  
		Last Modified: Fri, 13 Dec 2024 17:20:51 GMT  
		Size: 27.2 MB (27203865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2aa78ed8ad18394d7ae521e83b2810fec9fbb7d95aa074d794bb43e6e2bbfb`  
		Last Modified: Mon, 16 Dec 2024 02:12:36 GMT  
		Size: 1.2 MB (1198781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f106a95fef578814e019c4ac69f1cf32b15d5f85da2729a7ab2487c5d3505d`  
		Last Modified: Sat, 14 Dec 2024 00:59:42 GMT  
		Size: 5.5 MB (5532202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2293949a62535f558d267574d694fe0b0e9498fce13b94a8a2e83b00a4d86669`  
		Last Modified: Mon, 16 Dec 2024 02:05:56 GMT  
		Size: 3.6 KB (3625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19e6106ec9b9e87d61a209dae736d5a55521179a1e971b3e19fbf6e6cf862b0`  
		Last Modified: Thu, 26 Dec 2024 08:20:09 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38dd4c4d79e02de926140a561865bc9b24c63a07e419305ab0a1deae10efadf8`  
		Last Modified: Fri, 03 Jan 2025 13:19:18 GMT  
		Size: 104.7 MB (104684595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b236153245646eabf2f747172467aceaec88d3f377325803397c5ea67e5fd6e4`  
		Last Modified: Mon, 16 Dec 2024 14:07:27 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25521cd7c38d4702acc35bf86286dd8ec0b25b29688062df02aa6a6e40b0aeb7`  
		Last Modified: Thu, 19 Dec 2024 13:42:41 GMT  
		Size: 67.8 MB (67820715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd225e47b2314091e4a77693b5adde09531a56c382944dcdf26fca1a9945ea9`  
		Last Modified: Mon, 16 Dec 2024 14:07:46 GMT  
		Size: 279.0 KB (278989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5facdfbd066e270842cecd5e7b2804fff0a51adcc271885cb5b96a58a90a8b2f`  
		Last Modified: Thu, 19 Dec 2024 13:42:38 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d9da6baa7ccdaef0b14c4f0599c9e580f7a4e2ec3439bbe0d5f1512901e72e`  
		Last Modified: Mon, 16 Dec 2024 07:09:56 GMT  
		Size: 21.5 MB (21481488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf3f2d3f902424fa2e5e82a830345f1bf72ad3c82a63f8ca46697e7edc7db75`  
		Last Modified: Wed, 19 Feb 2025 03:01:28 GMT  
		Size: 5.4 KB (5399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7eccd88a94f9e4bf8fbc013fc95ef5ee569265cfa57eb403d08eee628154e6f`  
		Last Modified: Wed, 12 Feb 2025 00:27:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad198325fabb7033faed92791501d458083ad53178e95679c991883331768c2c`  
		Last Modified: Wed, 19 Feb 2025 03:01:42 GMT  
		Size: 78.7 MB (78745423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bcee0cd0a03a0d245a95f48999570b936cf0370ff10f5f7ccb61adaf15b0b3`  
		Last Modified: Sat, 09 Dec 2023 04:07:16 GMT  
		Size: 16.0 MB (16013019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1020862ac6a704344c0c4453c4b2f2d2afda6aee0b57898df747ddd1e6b43c04`  
		Last Modified: Wed, 12 Feb 2025 00:27:30 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros1-bridge-focal`

```console
$ docker pull ros@sha256:f4caef292184e90c294cd14636c2812efa0a9c18fe63021c3002a82509f1519a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:a2f06953930b0a209295138745d606b1936f0b0564106df9230e2a6612b8b9a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.7 MB (335739532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972da3292152b13c9d2c6b8c13315b189d7f9cff1fe58adac5d33a1bc5be2407`
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
# Sat, 09 Dec 2023 03:55:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 04:01:42 GMT
RUN echo "deb http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 04:01:42 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 04:01:42 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 04:01:42 GMT
ENV ROS_DISTRO=galactic
# Sat, 09 Dec 2023 04:02:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:02:33 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 09 Dec 2023 04:02:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 04:02:33 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 04:02:58 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:03:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 04:03:06 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 04:03:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:03:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 09 Dec 2023 04:03:31 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 09 Dec 2023 04:03:31 GMT
ENV ROS1_DISTRO=noetic
# Sat, 09 Dec 2023 04:03:31 GMT
ENV ROS2_DISTRO=galactic
# Sat, 09 Dec 2023 04:03:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.16.0-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:04:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.4-1*     ros-galactic-demo-nodes-py=0.14.4-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 04:04:10 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:30ecab32a3b65c6ec04c63a65b90e627b49d1297d8793896ed50b656377d8a06`  
		Last Modified: Fri, 13 Dec 2024 20:02:48 GMT  
		Size: 28.6 MB (28584029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc1327734170da8c4ae4171fb4248189d0691d6b4a3f01b09239c3e34688651`  
		Last Modified: Fri, 13 Dec 2024 16:03:32 GMT  
		Size: 1.2 MB (1198788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77125e61032dbbcd43c015fe756de97b5661bdbbf4f5219588148f651ae900c1`  
		Last Modified: Fri, 13 Dec 2024 15:58:55 GMT  
		Size: 5.6 MB (5553989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9cfdb297cb2e56f5144d6a03d94e416f7101347779b1dac8d072ddb965d0b5`  
		Last Modified: Fri, 13 Dec 2024 15:58:54 GMT  
		Size: 3.6 KB (3622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ae93d7330b04913f411e004ee6e95c6f115a405deced6159ed0ae4c9987099`  
		Last Modified: Sun, 15 Dec 2024 01:28:21 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aadbc41c419150c402c40f1d1eed2da57691737b48cfabb2a85a677c999bdb79`  
		Last Modified: Fri, 13 Dec 2024 16:03:41 GMT  
		Size: 109.2 MB (109169623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f16c937df28690cec98c60ae445a5ad2e4d5c2868816a30a5d8859297cd824c`  
		Last Modified: Fri, 13 Dec 2024 16:03:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491e9e6abb4a9e20e09b6c4e4a30c80e408608a98793f29587a4d6f27eced1e3`  
		Last Modified: Sun, 15 Dec 2024 01:28:30 GMT  
		Size: 73.5 MB (73462168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b21021fd9b9e6faa1b78a6061fb9d053fe7c15d2241f597844b39fd421ecca`  
		Last Modified: Mon, 16 Dec 2024 06:38:10 GMT  
		Size: 279.0 KB (278988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b4e77c324c9b353c1655c675dc3e15d5690491f12eb6cc3f7983b7541e3ee`  
		Last Modified: Fri, 13 Dec 2024 15:44:11 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8d940467045531264741a07da79cb54953c596a4a949f3a20bb49f0e647f93`  
		Last Modified: Fri, 13 Dec 2024 15:58:55 GMT  
		Size: 22.1 MB (22140300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a4ad6250fdd606f65fe888d9aeeae5cb468c07f8b0a609f4bb0f7e3e036953`  
		Last Modified: Mon, 16 Dec 2024 07:47:13 GMT  
		Size: 5.4 KB (5405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa839d68c2779d2c21b487d0e59c1c818f020b889e6019c78caa3626e48458d8`  
		Last Modified: Mon, 16 Dec 2024 10:08:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62f7f6251bccfdf666858e6a457027bff3aee9e402b196a7e93519b6a230a7d`  
		Last Modified: Mon, 16 Dec 2024 10:08:44 GMT  
		Size: 78.8 MB (78845967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf377c92f3fc74e02dc633002b07ec3f6b1fbda80d373c592630677be0a45f4`  
		Last Modified: Mon, 16 Dec 2024 10:08:48 GMT  
		Size: 16.5 MB (16493310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff95dbe602ee48c3060f917022573dfd5abc52c081264a6eaa8b7c2904654a0`  
		Last Modified: Mon, 16 Dec 2024 10:08:37 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1612b2093f25d491c55d95cc50e98f9c70e45c1f3770e7295d4e6c5c4b878582
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.0 MB (322971458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac58377f8466e6f1526903cc312deda40e2eea7bebf48c85a2d637266a5f82a5`
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
# Sat, 09 Dec 2023 03:18:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 4B63CF8FDE49746E98FA01DDAD19BAB3CBF125EA
# Sat, 09 Dec 2023 03:24:08 GMT
RUN echo "deb http://snapshots.ros.org/galactic/final/ubuntu focal main" > /etc/apt/sources.list.d/ros2-snapshots.list
# Sat, 09 Dec 2023 03:24:09 GMT
ENV LANG=C.UTF-8
# Sat, 09 Dec 2023 03:24:09 GMT
ENV LC_ALL=C.UTF-8
# Sat, 09 Dec 2023 03:24:09 GMT
ENV ROS_DISTRO=galactic
# Sat, 09 Dec 2023 03:24:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:25:01 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Sat, 09 Dec 2023 03:25:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Sat, 09 Dec 2023 03:25:02 GMT
CMD ["bash"]
# Sat, 09 Dec 2023 03:25:20 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:25:25 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Sat, 09 Dec 2023 03:25:30 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Sat, 09 Dec 2023 03:25:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:25:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Sat, 09 Dec 2023 03:25:55 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Sat, 09 Dec 2023 03:25:55 GMT
ENV ROS1_DISTRO=noetic
# Sat, 09 Dec 2023 03:25:55 GMT
ENV ROS2_DISTRO=galactic
# Sat, 09 Dec 2023 03:26:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.16.0-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:26:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.4-1*     ros-galactic-demo-nodes-py=0.14.4-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 09 Dec 2023 03:26:27 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:5d2acf9ee7cfde47b6ce997317767b8fa9bf8d93b8297016db9e093d06aa913d`  
		Last Modified: Fri, 13 Dec 2024 17:20:51 GMT  
		Size: 27.2 MB (27203865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2aa78ed8ad18394d7ae521e83b2810fec9fbb7d95aa074d794bb43e6e2bbfb`  
		Last Modified: Mon, 16 Dec 2024 02:12:36 GMT  
		Size: 1.2 MB (1198781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f106a95fef578814e019c4ac69f1cf32b15d5f85da2729a7ab2487c5d3505d`  
		Last Modified: Sat, 14 Dec 2024 00:59:42 GMT  
		Size: 5.5 MB (5532202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2293949a62535f558d267574d694fe0b0e9498fce13b94a8a2e83b00a4d86669`  
		Last Modified: Mon, 16 Dec 2024 02:05:56 GMT  
		Size: 3.6 KB (3625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19e6106ec9b9e87d61a209dae736d5a55521179a1e971b3e19fbf6e6cf862b0`  
		Last Modified: Thu, 26 Dec 2024 08:20:09 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38dd4c4d79e02de926140a561865bc9b24c63a07e419305ab0a1deae10efadf8`  
		Last Modified: Fri, 03 Jan 2025 13:19:18 GMT  
		Size: 104.7 MB (104684595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b236153245646eabf2f747172467aceaec88d3f377325803397c5ea67e5fd6e4`  
		Last Modified: Mon, 16 Dec 2024 14:07:27 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25521cd7c38d4702acc35bf86286dd8ec0b25b29688062df02aa6a6e40b0aeb7`  
		Last Modified: Thu, 19 Dec 2024 13:42:41 GMT  
		Size: 67.8 MB (67820715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd225e47b2314091e4a77693b5adde09531a56c382944dcdf26fca1a9945ea9`  
		Last Modified: Mon, 16 Dec 2024 14:07:46 GMT  
		Size: 279.0 KB (278989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5facdfbd066e270842cecd5e7b2804fff0a51adcc271885cb5b96a58a90a8b2f`  
		Last Modified: Thu, 19 Dec 2024 13:42:38 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d9da6baa7ccdaef0b14c4f0599c9e580f7a4e2ec3439bbe0d5f1512901e72e`  
		Last Modified: Mon, 16 Dec 2024 07:09:56 GMT  
		Size: 21.5 MB (21481488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf3f2d3f902424fa2e5e82a830345f1bf72ad3c82a63f8ca46697e7edc7db75`  
		Last Modified: Wed, 19 Feb 2025 03:01:28 GMT  
		Size: 5.4 KB (5399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7eccd88a94f9e4bf8fbc013fc95ef5ee569265cfa57eb403d08eee628154e6f`  
		Last Modified: Wed, 12 Feb 2025 00:27:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad198325fabb7033faed92791501d458083ad53178e95679c991883331768c2c`  
		Last Modified: Wed, 19 Feb 2025 03:01:42 GMT  
		Size: 78.7 MB (78745423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bcee0cd0a03a0d245a95f48999570b936cf0370ff10f5f7ccb61adaf15b0b3`  
		Last Modified: Sat, 09 Dec 2023 04:07:16 GMT  
		Size: 16.0 MB (16013019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1020862ac6a704344c0c4453c4b2f2d2afda6aee0b57898df747ddd1e6b43c04`  
		Last Modified: Wed, 12 Feb 2025 00:27:30 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull ros@sha256:6465a56f03f72033905bd7c537d29848c14c78e087bab45ea30181f3ca06ded3
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
$ docker pull ros@sha256:274cafb4228a90240a38e98eb7b469071d8912de039db739bc5a683b0008e345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263117266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c445e4e9450d813702fa00d57b2bace32ecd24a584b6093d57ca2cf4b06fd2e9`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:fe5f39a48dd5e32631ed16c88dce9f258413e07a4bd18febf0fe86116fd84718`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 1.2 MB (1194707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e85c211102ab44bb27f6fae9285c9d5372b02fa7957fef17cf88938d6c6fdfc`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 5.4 MB (5363878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6311663f122dccef631ec54a38cb7388fd50b5c2fe26207dbc65c9e1cce5709`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ea9a5fcfe3a513395e2980f864dad1efe2ad81c1932bec13e1ad6de300f85`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633e89e2c9ac48f8bf438c0688d6ec1409062328508ee6720565f4ba0be5e6a6`  
		Last Modified: Thu, 08 May 2025 17:05:34 GMT  
		Size: 177.1 MB (177069417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ccad8440f923e4cdaf8882f41787c599a4e976a9350b51b0f45aebcc9c70`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230eaefd6c1785cce75d62b2cd7f24ce3ece78e4978c84ad13f244b0761b531`  
		Last Modified: Thu, 08 May 2025 17:05:16 GMT  
		Size: 50.7 MB (50717459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d46fa073a9fd04739b1d191001dfc5ce09da96d8d4c0af8a03a7f9ca81c445`  
		Last Modified: Thu, 08 May 2025 17:05:12 GMT  
		Size: 342.6 KB (342568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f141accf2c2a408013c16f96d8aad85739eaff1ab8f872d1186c8c96d7dadce`  
		Last Modified: Thu, 08 May 2025 17:05:13 GMT  
		Size: 916.4 KB (916375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:894d6d306f4a156faef3730e7718f84b3f6a7e61a7ac87f59db565eb55c2b41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27620532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b93e73bd53bcf0cba37d3bb0c53db0aed971446443b64039246ecd9c552df9`

```dockerfile
```

-	Layers:
	-	`sha256:ae2cb33b1ab49a18cd94355d1e94171e5d5904a2f7886c1a45b833b63804f3be`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 27.6 MB (27606846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a19f11b316561bc9402681823319dbab7b17538ca6eab782b6c261f95d0e2708`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 13.7 KB (13686 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:7f06923620dcb14829611b10907cc82c55a7b333c9318bfeb53cd8ad907fc195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228333887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6480a80e46afc8bd51cd981ff94aa3fab93b996f1f7de2b88dc118703d16488`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:3596bc04094955644b548ea1c23b1a6bdc109275e65283ca4fd1f6a9a89d8626`  
		Last Modified: Sun, 18 May 2025 18:45:27 GMT  
		Size: 1.2 MB (1194711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93ea204140e85e488ee453c48b702ee6d1215d0c8a37917d51770766fa1863`  
		Last Modified: Sun, 18 May 2025 18:45:30 GMT  
		Size: 4.5 MB (4489374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f66ca89d4141b646b78981e712368d2a6c606146007a28fbafa1a7722f8fb5`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41353e856d62bf7da977152eeb11f65f00acf8fff54c22e92373a53045d67f`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20730724004eb01785b328d46ba7823f1c1692018c81e257b8f2c1f1e2f887`  
		Last Modified: Tue, 20 May 2025 09:31:42 GMT  
		Size: 157.6 MB (157555882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46fc9a00d6b061bc163a63a7b4ab2a3954a1181b3e35917e6ef4d73c581f37`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79409844b34fb92b857683485d70dfbd0be143a3204925a1d365ac95595758`  
		Last Modified: Sun, 18 May 2025 18:45:39 GMT  
		Size: 40.3 MB (40277695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226ef6ad1c100f52351ff305d7b4a124148ff932894cd872354fefce17c8f31`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 342.6 KB (342571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f761607f87c78ac5442bc670e7e9f423410c6fb081d3271d93253e4ba526d`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 847.1 KB (847126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:18e13ecba12a87f54a9f386ce6fec1aeeec342d51cebc59f93687d200660c0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27383622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a59e628885a870a5e4c547949eb356a8207eefb673574a207d30cc44edc84c`

```dockerfile
```

-	Layers:
	-	`sha256:8766d60d6a90fdccae930bfb00cf53eea623068ac6966e1518c6e114ae3fed15`  
		Last Modified: Wed, 09 Apr 2025 12:49:05 GMT  
		Size: 27.4 MB (27369842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d36c37521d0d18b0e266ef7e93c98217a617d45aee5ca476c23b1b6c605339c5`  
		Last Modified: Wed, 09 Apr 2025 12:49:04 GMT  
		Size: 13.8 KB (13780 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5626d190770d234143954698dddf98a9cb97a3429922bc05e310d034c5ee7006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250235697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1a8972be4098e73a367bc535112949e47c4dbd1e183fa1e6f87ea23060dcac`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:79b1b5c52d6e8060d576d30ef37b2dff7ac599a9acd3a50369427d2448b8707c`  
		Last Modified: Thu, 08 May 2025 19:41:35 GMT  
		Size: 1.2 MB (1194543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd8cbf95842dba0eabf002f3aea2635e781f046658cce5b7ba313fad10bde90`  
		Last Modified: Thu, 08 May 2025 19:41:34 GMT  
		Size: 5.3 MB (5344064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fe00290afb945b6813546d3926aea5a8ec0082d4a1dc0d63bb3086b1e2a8a1`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae42f08156cf5ed9de8bc1f6d53206b54a49718b831050ddbac5cee7fb21775`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1035cf4b45887b737d9db818d2873882f4ed775c8802ec12500a5a7eb61928`  
		Last Modified: Thu, 08 May 2025 19:41:57 GMT  
		Size: 171.5 MB (171486596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea9b1520ad4662c02b05f9d047e3831dc184c6a7323a71f1128591ca69f26d`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa074f57d5682580ed27d2a5cecc84542028a7dd9e838cb04deb0ba31b051878`  
		Last Modified: Thu, 08 May 2025 19:41:51 GMT  
		Size: 45.0 MB (44990177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e66974cba6bb44f651eb6e6ba3e0bc14e999155f94cb079f5c83af285435746`  
		Last Modified: Thu, 08 May 2025 19:41:31 GMT  
		Size: 342.6 KB (342564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7278c4ff3a25bd1a3c8f3fa178fa20f12c6609c591924217d492c7d76214d0`  
		Last Modified: Thu, 08 May 2025 19:41:31 GMT  
		Size: 897.6 KB (897624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic` - unknown; unknown

```console
$ docker pull ros@sha256:90249cede2082d3aca1db98135b1ab6e429caf1bbf08b4fa8bccdabcafd0925c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27570563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c578189226a60b3bda679cb5b90bde0c4f7744d0f14b14b8d36142d77e5d57c`

```dockerfile
```

-	Layers:
	-	`sha256:d75e6f47c4ab5594fbea0ec4966288fd99af3dd31e0e15bc514e31ce7c4a43ca`  
		Last Modified: Wed, 09 Apr 2025 15:45:44 GMT  
		Size: 27.6 MB (27556755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfa8fdd93e74bccd7e121aacd19ef9d4f55868eff3f212e02c656d6ece48bd74`  
		Last Modified: Wed, 09 Apr 2025 15:45:43 GMT  
		Size: 13.8 KB (13808 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:1af3db41095a745c30265af92c66042cfa77c0e752cfc8316b4227cadd70ba89
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
$ docker pull ros@sha256:ad53566f8860108545de1e7a9ec08674c6662a7040bc14285167f4b5e59ec6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **947.1 MB (947079134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d7c1b575a3a4be2b512a2a1347867dd7e52acd766a7e4ececf13911a30f813`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:fe5f39a48dd5e32631ed16c88dce9f258413e07a4bd18febf0fe86116fd84718`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 1.2 MB (1194707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e85c211102ab44bb27f6fae9285c9d5372b02fa7957fef17cf88938d6c6fdfc`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 5.4 MB (5363878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6311663f122dccef631ec54a38cb7388fd50b5c2fe26207dbc65c9e1cce5709`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ea9a5fcfe3a513395e2980f864dad1efe2ad81c1932bec13e1ad6de300f85`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633e89e2c9ac48f8bf438c0688d6ec1409062328508ee6720565f4ba0be5e6a6`  
		Last Modified: Thu, 08 May 2025 17:05:34 GMT  
		Size: 177.1 MB (177069417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ccad8440f923e4cdaf8882f41787c599a4e976a9350b51b0f45aebcc9c70`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230eaefd6c1785cce75d62b2cd7f24ce3ece78e4978c84ad13f244b0761b531`  
		Last Modified: Thu, 08 May 2025 17:05:16 GMT  
		Size: 50.7 MB (50717459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d46fa073a9fd04739b1d191001dfc5ce09da96d8d4c0af8a03a7f9ca81c445`  
		Last Modified: Thu, 08 May 2025 17:05:12 GMT  
		Size: 342.6 KB (342568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f141accf2c2a408013c16f96d8aad85739eaff1ab8f872d1186c8c96d7dadce`  
		Last Modified: Thu, 08 May 2025 17:05:13 GMT  
		Size: 916.4 KB (916375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59e8c3b14c608ecb2e865a0de678b74f5794f6d1027a965462403f1b83582b0`  
		Last Modified: Fri, 09 May 2025 00:01:33 GMT  
		Size: 684.0 MB (683961868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:c42c6cd3b6ece2f67cdfd1c894fdc6a4473a4435191fe53345e7cbcdb2c2e60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52718030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e1e5cf94431d2ab4a6c9405cce7c8686d06afa3ef4cfd860f028e3f27d7f67`

```dockerfile
```

-	Layers:
	-	`sha256:2cad68b96b92d88b145401da2716d5827c0f781f72f1005117185c9918ca388d`  
		Last Modified: Wed, 09 Apr 2025 03:15:29 GMT  
		Size: 52.7 MB (52708657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf99da4e34c7a38b9050b7d5debf517fb04bab793919f282acd327df3707f666`  
		Last Modified: Wed, 09 Apr 2025 03:15:27 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:e369bf14da3d93f9be6ad671f4681b2b488f5f0056278a79723286d2ed2d239f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.2 MB (725206547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424465548bb231bcb31875ce6e38c94dcfbef64f744da6db98b9817377cb28ce`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:3596bc04094955644b548ea1c23b1a6bdc109275e65283ca4fd1f6a9a89d8626`  
		Last Modified: Sun, 18 May 2025 18:45:27 GMT  
		Size: 1.2 MB (1194711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93ea204140e85e488ee453c48b702ee6d1215d0c8a37917d51770766fa1863`  
		Last Modified: Sun, 18 May 2025 18:45:30 GMT  
		Size: 4.5 MB (4489374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f66ca89d4141b646b78981e712368d2a6c606146007a28fbafa1a7722f8fb5`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41353e856d62bf7da977152eeb11f65f00acf8fff54c22e92373a53045d67f`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20730724004eb01785b328d46ba7823f1c1692018c81e257b8f2c1f1e2f887`  
		Last Modified: Tue, 20 May 2025 09:31:42 GMT  
		Size: 157.6 MB (157555882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46fc9a00d6b061bc163a63a7b4ab2a3954a1181b3e35917e6ef4d73c581f37`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79409844b34fb92b857683485d70dfbd0be143a3204925a1d365ac95595758`  
		Last Modified: Sun, 18 May 2025 18:45:39 GMT  
		Size: 40.3 MB (40277695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226ef6ad1c100f52351ff305d7b4a124148ff932894cd872354fefce17c8f31`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 342.6 KB (342571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f761607f87c78ac5442bc670e7e9f423410c6fb081d3271d93253e4ba526d`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 847.1 KB (847126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22052e0f4af1fa1026f671cc3091c7c92fc31d9da9086335d89ec24f1c013474`  
		Last Modified: Wed, 04 Jun 2025 10:52:21 GMT  
		Size: 496.9 MB (496872660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:1fbf1d0fe5a65fae05c1ee79bb1d59394c0124d36e81e95300cf6b280254b382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51466276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08cf80209972ecf4daf80b36ce0363eab1a75c5f046a99fe0518fb41a37470a9`

```dockerfile
```

-	Layers:
	-	`sha256:350b1e9cb0d117c5c2ba18f2ba57f6d6ba9d0e72c5c2e793bad9e8f84b8e72e7`  
		Last Modified: Wed, 09 Apr 2025 13:45:50 GMT  
		Size: 51.5 MB (51456843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98581e073cf87a2627f231fe098612edf517b2e20ad820129c446e3afc1f74fb`  
		Last Modified: Wed, 09 Apr 2025 13:45:48 GMT  
		Size: 9.4 KB (9433 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cfcdafb6ae6c5e1c85e054202ee9571e286b88fe215dcad96e2920cf7f3bf7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **902.0 MB (902042260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e17c4f0db3b8edd25decb5455db77a82b8508882492faacbd0032b51909045e`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:79b1b5c52d6e8060d576d30ef37b2dff7ac599a9acd3a50369427d2448b8707c`  
		Last Modified: Thu, 08 May 2025 19:41:35 GMT  
		Size: 1.2 MB (1194543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd8cbf95842dba0eabf002f3aea2635e781f046658cce5b7ba313fad10bde90`  
		Last Modified: Thu, 08 May 2025 19:41:34 GMT  
		Size: 5.3 MB (5344064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fe00290afb945b6813546d3926aea5a8ec0082d4a1dc0d63bb3086b1e2a8a1`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae42f08156cf5ed9de8bc1f6d53206b54a49718b831050ddbac5cee7fb21775`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1035cf4b45887b737d9db818d2873882f4ed775c8802ec12500a5a7eb61928`  
		Last Modified: Thu, 08 May 2025 19:41:57 GMT  
		Size: 171.5 MB (171486596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea9b1520ad4662c02b05f9d047e3831dc184c6a7323a71f1128591ca69f26d`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa074f57d5682580ed27d2a5cecc84542028a7dd9e838cb04deb0ba31b051878`  
		Last Modified: Thu, 08 May 2025 19:41:51 GMT  
		Size: 45.0 MB (44990177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e66974cba6bb44f651eb6e6ba3e0bc14e999155f94cb079f5c83af285435746`  
		Last Modified: Thu, 08 May 2025 19:41:31 GMT  
		Size: 342.6 KB (342564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7278c4ff3a25bd1a3c8f3fa178fa20f12c6609c591924217d492c7d76214d0`  
		Last Modified: Thu, 08 May 2025 19:41:31 GMT  
		Size: 897.6 KB (897624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8498e3ff194372ace8e0d6adab098ede6183b5fc569779a0da961fce617ec1aa`  
		Last Modified: Fri, 09 May 2025 00:33:55 GMT  
		Size: 651.8 MB (651806563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception` - unknown; unknown

```console
$ docker pull ros@sha256:e53bdc49d292ca610d7c65ea39ca39d81e6e3db349619076484eb33e90501621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52577752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99522e5bf9afe7bc5271fb30273274c04615e345ca72b41c861478851d82d7b`

```dockerfile
```

-	Layers:
	-	`sha256:0fab2f8af0fefd387cd98b46db31acb42237fcb69539a5c90c9b6a494e6789e4`  
		Last Modified: Wed, 09 Apr 2025 18:53:13 GMT  
		Size: 52.6 MB (52568298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efbb944e96c1e06942dbdd8eb1150a055a3c839522f5cd6454f7096b5409e75b`  
		Last Modified: Wed, 09 Apr 2025 18:53:11 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:1af3db41095a745c30265af92c66042cfa77c0e752cfc8316b4227cadd70ba89
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
$ docker pull ros@sha256:ad53566f8860108545de1e7a9ec08674c6662a7040bc14285167f4b5e59ec6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **947.1 MB (947079134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d7c1b575a3a4be2b512a2a1347867dd7e52acd766a7e4ececf13911a30f813`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:fe5f39a48dd5e32631ed16c88dce9f258413e07a4bd18febf0fe86116fd84718`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 1.2 MB (1194707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e85c211102ab44bb27f6fae9285c9d5372b02fa7957fef17cf88938d6c6fdfc`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 5.4 MB (5363878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6311663f122dccef631ec54a38cb7388fd50b5c2fe26207dbc65c9e1cce5709`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ea9a5fcfe3a513395e2980f864dad1efe2ad81c1932bec13e1ad6de300f85`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633e89e2c9ac48f8bf438c0688d6ec1409062328508ee6720565f4ba0be5e6a6`  
		Last Modified: Thu, 08 May 2025 17:05:34 GMT  
		Size: 177.1 MB (177069417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ccad8440f923e4cdaf8882f41787c599a4e976a9350b51b0f45aebcc9c70`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230eaefd6c1785cce75d62b2cd7f24ce3ece78e4978c84ad13f244b0761b531`  
		Last Modified: Thu, 08 May 2025 17:05:16 GMT  
		Size: 50.7 MB (50717459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d46fa073a9fd04739b1d191001dfc5ce09da96d8d4c0af8a03a7f9ca81c445`  
		Last Modified: Thu, 08 May 2025 17:05:12 GMT  
		Size: 342.6 KB (342568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f141accf2c2a408013c16f96d8aad85739eaff1ab8f872d1186c8c96d7dadce`  
		Last Modified: Thu, 08 May 2025 17:05:13 GMT  
		Size: 916.4 KB (916375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59e8c3b14c608ecb2e865a0de678b74f5794f6d1027a965462403f1b83582b0`  
		Last Modified: Fri, 09 May 2025 00:01:33 GMT  
		Size: 684.0 MB (683961868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:c42c6cd3b6ece2f67cdfd1c894fdc6a4473a4435191fe53345e7cbcdb2c2e60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52718030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e1e5cf94431d2ab4a6c9405cce7c8686d06afa3ef4cfd860f028e3f27d7f67`

```dockerfile
```

-	Layers:
	-	`sha256:2cad68b96b92d88b145401da2716d5827c0f781f72f1005117185c9918ca388d`  
		Last Modified: Wed, 09 Apr 2025 03:15:29 GMT  
		Size: 52.7 MB (52708657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf99da4e34c7a38b9050b7d5debf517fb04bab793919f282acd327df3707f666`  
		Last Modified: Wed, 09 Apr 2025 03:15:27 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:e369bf14da3d93f9be6ad671f4681b2b488f5f0056278a79723286d2ed2d239f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.2 MB (725206547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424465548bb231bcb31875ce6e38c94dcfbef64f744da6db98b9817377cb28ce`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:3596bc04094955644b548ea1c23b1a6bdc109275e65283ca4fd1f6a9a89d8626`  
		Last Modified: Sun, 18 May 2025 18:45:27 GMT  
		Size: 1.2 MB (1194711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93ea204140e85e488ee453c48b702ee6d1215d0c8a37917d51770766fa1863`  
		Last Modified: Sun, 18 May 2025 18:45:30 GMT  
		Size: 4.5 MB (4489374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f66ca89d4141b646b78981e712368d2a6c606146007a28fbafa1a7722f8fb5`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41353e856d62bf7da977152eeb11f65f00acf8fff54c22e92373a53045d67f`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20730724004eb01785b328d46ba7823f1c1692018c81e257b8f2c1f1e2f887`  
		Last Modified: Tue, 20 May 2025 09:31:42 GMT  
		Size: 157.6 MB (157555882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46fc9a00d6b061bc163a63a7b4ab2a3954a1181b3e35917e6ef4d73c581f37`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79409844b34fb92b857683485d70dfbd0be143a3204925a1d365ac95595758`  
		Last Modified: Sun, 18 May 2025 18:45:39 GMT  
		Size: 40.3 MB (40277695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226ef6ad1c100f52351ff305d7b4a124148ff932894cd872354fefce17c8f31`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 342.6 KB (342571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f761607f87c78ac5442bc670e7e9f423410c6fb081d3271d93253e4ba526d`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 847.1 KB (847126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22052e0f4af1fa1026f671cc3091c7c92fc31d9da9086335d89ec24f1c013474`  
		Last Modified: Wed, 04 Jun 2025 10:52:21 GMT  
		Size: 496.9 MB (496872660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:1fbf1d0fe5a65fae05c1ee79bb1d59394c0124d36e81e95300cf6b280254b382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51466276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08cf80209972ecf4daf80b36ce0363eab1a75c5f046a99fe0518fb41a37470a9`

```dockerfile
```

-	Layers:
	-	`sha256:350b1e9cb0d117c5c2ba18f2ba57f6d6ba9d0e72c5c2e793bad9e8f84b8e72e7`  
		Last Modified: Wed, 09 Apr 2025 13:45:50 GMT  
		Size: 51.5 MB (51456843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98581e073cf87a2627f231fe098612edf517b2e20ad820129c446e3afc1f74fb`  
		Last Modified: Wed, 09 Apr 2025 13:45:48 GMT  
		Size: 9.4 KB (9433 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cfcdafb6ae6c5e1c85e054202ee9571e286b88fe215dcad96e2920cf7f3bf7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **902.0 MB (902042260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e17c4f0db3b8edd25decb5455db77a82b8508882492faacbd0032b51909045e`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:79b1b5c52d6e8060d576d30ef37b2dff7ac599a9acd3a50369427d2448b8707c`  
		Last Modified: Thu, 08 May 2025 19:41:35 GMT  
		Size: 1.2 MB (1194543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd8cbf95842dba0eabf002f3aea2635e781f046658cce5b7ba313fad10bde90`  
		Last Modified: Thu, 08 May 2025 19:41:34 GMT  
		Size: 5.3 MB (5344064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fe00290afb945b6813546d3926aea5a8ec0082d4a1dc0d63bb3086b1e2a8a1`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae42f08156cf5ed9de8bc1f6d53206b54a49718b831050ddbac5cee7fb21775`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1035cf4b45887b737d9db818d2873882f4ed775c8802ec12500a5a7eb61928`  
		Last Modified: Thu, 08 May 2025 19:41:57 GMT  
		Size: 171.5 MB (171486596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea9b1520ad4662c02b05f9d047e3831dc184c6a7323a71f1128591ca69f26d`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa074f57d5682580ed27d2a5cecc84542028a7dd9e838cb04deb0ba31b051878`  
		Last Modified: Thu, 08 May 2025 19:41:51 GMT  
		Size: 45.0 MB (44990177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e66974cba6bb44f651eb6e6ba3e0bc14e999155f94cb079f5c83af285435746`  
		Last Modified: Thu, 08 May 2025 19:41:31 GMT  
		Size: 342.6 KB (342564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7278c4ff3a25bd1a3c8f3fa178fa20f12c6609c591924217d492c7d76214d0`  
		Last Modified: Thu, 08 May 2025 19:41:31 GMT  
		Size: 897.6 KB (897624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8498e3ff194372ace8e0d6adab098ede6183b5fc569779a0da961fce617ec1aa`  
		Last Modified: Fri, 09 May 2025 00:33:55 GMT  
		Size: 651.8 MB (651806563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-perception-focal` - unknown; unknown

```console
$ docker pull ros@sha256:e53bdc49d292ca610d7c65ea39ca39d81e6e3db349619076484eb33e90501621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52577752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99522e5bf9afe7bc5271fb30273274c04615e345ca72b41c861478851d82d7b`

```dockerfile
```

-	Layers:
	-	`sha256:0fab2f8af0fefd387cd98b46db31acb42237fcb69539a5c90c9b6a494e6789e4`  
		Last Modified: Wed, 09 Apr 2025 18:53:13 GMT  
		Size: 52.6 MB (52568298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efbb944e96c1e06942dbdd8eb1150a055a3c839522f5cd6454f7096b5409e75b`  
		Last Modified: Wed, 09 Apr 2025 18:53:11 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:8a8402ac39bc8d0be5b9b261d691c9e970340507a1974929a9f1e7a6b0f54e3d
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
$ docker pull ros@sha256:588666ac574852c0f1e259190bd806ae1b99ccc6619005bc24910c151627d1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (280042321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a03753484f8bbac88f933035da74157dfb24e98d5563aaea5b3af4313dbb369`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:fe5f39a48dd5e32631ed16c88dce9f258413e07a4bd18febf0fe86116fd84718`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 1.2 MB (1194707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e85c211102ab44bb27f6fae9285c9d5372b02fa7957fef17cf88938d6c6fdfc`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 5.4 MB (5363878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6311663f122dccef631ec54a38cb7388fd50b5c2fe26207dbc65c9e1cce5709`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ea9a5fcfe3a513395e2980f864dad1efe2ad81c1932bec13e1ad6de300f85`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633e89e2c9ac48f8bf438c0688d6ec1409062328508ee6720565f4ba0be5e6a6`  
		Last Modified: Thu, 08 May 2025 17:05:34 GMT  
		Size: 177.1 MB (177069417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ccad8440f923e4cdaf8882f41787c599a4e976a9350b51b0f45aebcc9c70`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230eaefd6c1785cce75d62b2cd7f24ce3ece78e4978c84ad13f244b0761b531`  
		Last Modified: Thu, 08 May 2025 17:05:16 GMT  
		Size: 50.7 MB (50717459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d46fa073a9fd04739b1d191001dfc5ce09da96d8d4c0af8a03a7f9ca81c445`  
		Last Modified: Thu, 08 May 2025 17:05:12 GMT  
		Size: 342.6 KB (342568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f141accf2c2a408013c16f96d8aad85739eaff1ab8f872d1186c8c96d7dadce`  
		Last Modified: Thu, 08 May 2025 17:05:13 GMT  
		Size: 916.4 KB (916375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdca47db82ecc28269b7fa68385af6120c48afac7a12c7f0bf95e28dbf6686ee`  
		Last Modified: Thu, 08 May 2025 17:21:13 GMT  
		Size: 16.9 MB (16925055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:e33bfdee69c472d8bb814caec0491e35a8e073bf211b390190568141f5b7c44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29512790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4623b560e03238cf86606821f7e0c697279853c8a048aa0a90ad881dcbc5522c`

```dockerfile
```

-	Layers:
	-	`sha256:29c4cb4ef7b34b8d9940a27971d2cfd5b9fa4febd04f8b4db127d4e1915acb0b`  
		Last Modified: Wed, 09 Apr 2025 03:11:52 GMT  
		Size: 29.5 MB (29503464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee60d0a4acbc42cd0154cd6d608c3a47d7092fc6da7c4ce3dc2f11ed155102d7`  
		Last Modified: Wed, 09 Apr 2025 03:11:51 GMT  
		Size: 9.3 KB (9326 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:247ba19cb640d3a017c255d5541301625006985570bba1f05720f7ecef9074f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243357623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db32f83b400706cf730c41647acfbe4fdc88306c1407aacb9119bde20cfc438`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:3596bc04094955644b548ea1c23b1a6bdc109275e65283ca4fd1f6a9a89d8626`  
		Last Modified: Sun, 18 May 2025 18:45:27 GMT  
		Size: 1.2 MB (1194711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93ea204140e85e488ee453c48b702ee6d1215d0c8a37917d51770766fa1863`  
		Last Modified: Sun, 18 May 2025 18:45:30 GMT  
		Size: 4.5 MB (4489374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f66ca89d4141b646b78981e712368d2a6c606146007a28fbafa1a7722f8fb5`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41353e856d62bf7da977152eeb11f65f00acf8fff54c22e92373a53045d67f`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20730724004eb01785b328d46ba7823f1c1692018c81e257b8f2c1f1e2f887`  
		Last Modified: Tue, 20 May 2025 09:31:42 GMT  
		Size: 157.6 MB (157555882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46fc9a00d6b061bc163a63a7b4ab2a3954a1181b3e35917e6ef4d73c581f37`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79409844b34fb92b857683485d70dfbd0be143a3204925a1d365ac95595758`  
		Last Modified: Sun, 18 May 2025 18:45:39 GMT  
		Size: 40.3 MB (40277695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226ef6ad1c100f52351ff305d7b4a124148ff932894cd872354fefce17c8f31`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 342.6 KB (342571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f761607f87c78ac5442bc670e7e9f423410c6fb081d3271d93253e4ba526d`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 847.1 KB (847126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce917e8cec917422e9b6a79f9f49112806fda0cdaab6fce81b17bf63c04f209`  
		Last Modified: Wed, 09 Apr 2025 13:33:42 GMT  
		Size: 15.0 MB (15023736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:626b755c3618c71ae52bd438d05ec6a346a47b35e9711c9388564dc93da89c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.3 MB (29267106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec5ef38941e671f87b984b4f5304b2e2fdc2e9b2a7d5e768e9541cd6eb84876`

```dockerfile
```

-	Layers:
	-	`sha256:a8d06991796052382e033ebfa50cf0b80e437ffc3ba2325350464f47b9f0b403`  
		Last Modified: Wed, 09 Apr 2025 13:33:42 GMT  
		Size: 29.3 MB (29257720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:456bf4bb66d9bbece5d2fe1cbb27ba6703dfb4db9c4c1696359ed701022b9af5`  
		Last Modified: Wed, 09 Apr 2025 13:33:41 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fd8eaa825e35a53b192e94ea3ba2eab3bdcc643490951ba174bef67c7ff79832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266760448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61658de4f350c408e30eb759999297306caf15df5319b470cfe4352a3d4fa324`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:79b1b5c52d6e8060d576d30ef37b2dff7ac599a9acd3a50369427d2448b8707c`  
		Last Modified: Thu, 08 May 2025 19:41:35 GMT  
		Size: 1.2 MB (1194543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd8cbf95842dba0eabf002f3aea2635e781f046658cce5b7ba313fad10bde90`  
		Last Modified: Thu, 08 May 2025 19:41:34 GMT  
		Size: 5.3 MB (5344064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fe00290afb945b6813546d3926aea5a8ec0082d4a1dc0d63bb3086b1e2a8a1`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae42f08156cf5ed9de8bc1f6d53206b54a49718b831050ddbac5cee7fb21775`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1035cf4b45887b737d9db818d2873882f4ed775c8802ec12500a5a7eb61928`  
		Last Modified: Thu, 08 May 2025 19:41:57 GMT  
		Size: 171.5 MB (171486596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea9b1520ad4662c02b05f9d047e3831dc184c6a7323a71f1128591ca69f26d`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa074f57d5682580ed27d2a5cecc84542028a7dd9e838cb04deb0ba31b051878`  
		Last Modified: Thu, 08 May 2025 19:41:51 GMT  
		Size: 45.0 MB (44990177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e66974cba6bb44f651eb6e6ba3e0bc14e999155f94cb079f5c83af285435746`  
		Last Modified: Thu, 08 May 2025 19:41:31 GMT  
		Size: 342.6 KB (342564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7278c4ff3a25bd1a3c8f3fa178fa20f12c6609c591924217d492c7d76214d0`  
		Last Modified: Thu, 08 May 2025 19:41:31 GMT  
		Size: 897.6 KB (897624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfc18e7f8f3ae2ac59eca56e522da5ed43f809e3579b4b75a48316034dc1e44`  
		Last Modified: Thu, 08 May 2025 23:21:51 GMT  
		Size: 16.5 MB (16524751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot` - unknown; unknown

```console
$ docker pull ros@sha256:30c0ba04fe310f092169fdff39ed518bacd834606fcf538560502f7342d8a4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29461629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26885debb52feb76793555af5cb2ddbeb619a1f6c7e4a755bea97f7562e2c9d4`

```dockerfile
```

-	Layers:
	-	`sha256:727d7b00a4d318636171b5fec68d750197abb14a42696eeed770eae6d211718b`  
		Last Modified: Wed, 09 Apr 2025 18:41:38 GMT  
		Size: 29.5 MB (29452223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f67eea5ebd299fbd5b2b27021fc5f37a22e5d4fef3370f153efd7844dbbd781`  
		Last Modified: Wed, 09 Apr 2025 18:41:36 GMT  
		Size: 9.4 KB (9406 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:8a8402ac39bc8d0be5b9b261d691c9e970340507a1974929a9f1e7a6b0f54e3d
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
$ docker pull ros@sha256:588666ac574852c0f1e259190bd806ae1b99ccc6619005bc24910c151627d1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (280042321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a03753484f8bbac88f933035da74157dfb24e98d5563aaea5b3af4313dbb369`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:fe5f39a48dd5e32631ed16c88dce9f258413e07a4bd18febf0fe86116fd84718`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 1.2 MB (1194707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e85c211102ab44bb27f6fae9285c9d5372b02fa7957fef17cf88938d6c6fdfc`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 5.4 MB (5363878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6311663f122dccef631ec54a38cb7388fd50b5c2fe26207dbc65c9e1cce5709`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ea9a5fcfe3a513395e2980f864dad1efe2ad81c1932bec13e1ad6de300f85`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633e89e2c9ac48f8bf438c0688d6ec1409062328508ee6720565f4ba0be5e6a6`  
		Last Modified: Thu, 08 May 2025 17:05:34 GMT  
		Size: 177.1 MB (177069417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ccad8440f923e4cdaf8882f41787c599a4e976a9350b51b0f45aebcc9c70`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230eaefd6c1785cce75d62b2cd7f24ce3ece78e4978c84ad13f244b0761b531`  
		Last Modified: Thu, 08 May 2025 17:05:16 GMT  
		Size: 50.7 MB (50717459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d46fa073a9fd04739b1d191001dfc5ce09da96d8d4c0af8a03a7f9ca81c445`  
		Last Modified: Thu, 08 May 2025 17:05:12 GMT  
		Size: 342.6 KB (342568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f141accf2c2a408013c16f96d8aad85739eaff1ab8f872d1186c8c96d7dadce`  
		Last Modified: Thu, 08 May 2025 17:05:13 GMT  
		Size: 916.4 KB (916375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdca47db82ecc28269b7fa68385af6120c48afac7a12c7f0bf95e28dbf6686ee`  
		Last Modified: Thu, 08 May 2025 17:21:13 GMT  
		Size: 16.9 MB (16925055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:e33bfdee69c472d8bb814caec0491e35a8e073bf211b390190568141f5b7c44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29512790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4623b560e03238cf86606821f7e0c697279853c8a048aa0a90ad881dcbc5522c`

```dockerfile
```

-	Layers:
	-	`sha256:29c4cb4ef7b34b8d9940a27971d2cfd5b9fa4febd04f8b4db127d4e1915acb0b`  
		Last Modified: Wed, 09 Apr 2025 03:11:52 GMT  
		Size: 29.5 MB (29503464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee60d0a4acbc42cd0154cd6d608c3a47d7092fc6da7c4ce3dc2f11ed155102d7`  
		Last Modified: Wed, 09 Apr 2025 03:11:51 GMT  
		Size: 9.3 KB (9326 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:247ba19cb640d3a017c255d5541301625006985570bba1f05720f7ecef9074f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243357623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db32f83b400706cf730c41647acfbe4fdc88306c1407aacb9119bde20cfc438`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:3596bc04094955644b548ea1c23b1a6bdc109275e65283ca4fd1f6a9a89d8626`  
		Last Modified: Sun, 18 May 2025 18:45:27 GMT  
		Size: 1.2 MB (1194711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93ea204140e85e488ee453c48b702ee6d1215d0c8a37917d51770766fa1863`  
		Last Modified: Sun, 18 May 2025 18:45:30 GMT  
		Size: 4.5 MB (4489374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f66ca89d4141b646b78981e712368d2a6c606146007a28fbafa1a7722f8fb5`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41353e856d62bf7da977152eeb11f65f00acf8fff54c22e92373a53045d67f`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20730724004eb01785b328d46ba7823f1c1692018c81e257b8f2c1f1e2f887`  
		Last Modified: Tue, 20 May 2025 09:31:42 GMT  
		Size: 157.6 MB (157555882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46fc9a00d6b061bc163a63a7b4ab2a3954a1181b3e35917e6ef4d73c581f37`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79409844b34fb92b857683485d70dfbd0be143a3204925a1d365ac95595758`  
		Last Modified: Sun, 18 May 2025 18:45:39 GMT  
		Size: 40.3 MB (40277695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226ef6ad1c100f52351ff305d7b4a124148ff932894cd872354fefce17c8f31`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 342.6 KB (342571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f761607f87c78ac5442bc670e7e9f423410c6fb081d3271d93253e4ba526d`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 847.1 KB (847126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce917e8cec917422e9b6a79f9f49112806fda0cdaab6fce81b17bf63c04f209`  
		Last Modified: Wed, 09 Apr 2025 13:33:42 GMT  
		Size: 15.0 MB (15023736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:626b755c3618c71ae52bd438d05ec6a346a47b35e9711c9388564dc93da89c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.3 MB (29267106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec5ef38941e671f87b984b4f5304b2e2fdc2e9b2a7d5e768e9541cd6eb84876`

```dockerfile
```

-	Layers:
	-	`sha256:a8d06991796052382e033ebfa50cf0b80e437ffc3ba2325350464f47b9f0b403`  
		Last Modified: Wed, 09 Apr 2025 13:33:42 GMT  
		Size: 29.3 MB (29257720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:456bf4bb66d9bbece5d2fe1cbb27ba6703dfb4db9c4c1696359ed701022b9af5`  
		Last Modified: Wed, 09 Apr 2025 13:33:41 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:fd8eaa825e35a53b192e94ea3ba2eab3bdcc643490951ba174bef67c7ff79832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266760448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61658de4f350c408e30eb759999297306caf15df5319b470cfe4352a3d4fa324`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:79b1b5c52d6e8060d576d30ef37b2dff7ac599a9acd3a50369427d2448b8707c`  
		Last Modified: Thu, 08 May 2025 19:41:35 GMT  
		Size: 1.2 MB (1194543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd8cbf95842dba0eabf002f3aea2635e781f046658cce5b7ba313fad10bde90`  
		Last Modified: Thu, 08 May 2025 19:41:34 GMT  
		Size: 5.3 MB (5344064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fe00290afb945b6813546d3926aea5a8ec0082d4a1dc0d63bb3086b1e2a8a1`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae42f08156cf5ed9de8bc1f6d53206b54a49718b831050ddbac5cee7fb21775`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1035cf4b45887b737d9db818d2873882f4ed775c8802ec12500a5a7eb61928`  
		Last Modified: Thu, 08 May 2025 19:41:57 GMT  
		Size: 171.5 MB (171486596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea9b1520ad4662c02b05f9d047e3831dc184c6a7323a71f1128591ca69f26d`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa074f57d5682580ed27d2a5cecc84542028a7dd9e838cb04deb0ba31b051878`  
		Last Modified: Thu, 08 May 2025 19:41:51 GMT  
		Size: 45.0 MB (44990177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e66974cba6bb44f651eb6e6ba3e0bc14e999155f94cb079f5c83af285435746`  
		Last Modified: Thu, 08 May 2025 19:41:31 GMT  
		Size: 342.6 KB (342564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7278c4ff3a25bd1a3c8f3fa178fa20f12c6609c591924217d492c7d76214d0`  
		Last Modified: Thu, 08 May 2025 19:41:31 GMT  
		Size: 897.6 KB (897624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfc18e7f8f3ae2ac59eca56e522da5ed43f809e3579b4b75a48316034dc1e44`  
		Last Modified: Thu, 08 May 2025 23:21:51 GMT  
		Size: 16.5 MB (16524751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-robot-focal` - unknown; unknown

```console
$ docker pull ros@sha256:30c0ba04fe310f092169fdff39ed518bacd834606fcf538560502f7342d8a4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29461629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26885debb52feb76793555af5cb2ddbeb619a1f6c7e4a755bea97f7562e2c9d4`

```dockerfile
```

-	Layers:
	-	`sha256:727d7b00a4d318636171b5fec68d750197abb14a42696eeed770eae6d211718b`  
		Last Modified: Wed, 09 Apr 2025 18:41:38 GMT  
		Size: 29.5 MB (29452223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f67eea5ebd299fbd5b2b27021fc5f37a22e5d4fef3370f153efd7844dbbd781`  
		Last Modified: Wed, 09 Apr 2025 18:41:36 GMT  
		Size: 9.4 KB (9406 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:6465a56f03f72033905bd7c537d29848c14c78e087bab45ea30181f3ca06ded3
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
$ docker pull ros@sha256:274cafb4228a90240a38e98eb7b469071d8912de039db739bc5a683b0008e345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263117266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c445e4e9450d813702fa00d57b2bace32ecd24a584b6093d57ca2cf4b06fd2e9`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:fe5f39a48dd5e32631ed16c88dce9f258413e07a4bd18febf0fe86116fd84718`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 1.2 MB (1194707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e85c211102ab44bb27f6fae9285c9d5372b02fa7957fef17cf88938d6c6fdfc`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 5.4 MB (5363878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6311663f122dccef631ec54a38cb7388fd50b5c2fe26207dbc65c9e1cce5709`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ea9a5fcfe3a513395e2980f864dad1efe2ad81c1932bec13e1ad6de300f85`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633e89e2c9ac48f8bf438c0688d6ec1409062328508ee6720565f4ba0be5e6a6`  
		Last Modified: Thu, 08 May 2025 17:05:34 GMT  
		Size: 177.1 MB (177069417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ccad8440f923e4cdaf8882f41787c599a4e976a9350b51b0f45aebcc9c70`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230eaefd6c1785cce75d62b2cd7f24ce3ece78e4978c84ad13f244b0761b531`  
		Last Modified: Thu, 08 May 2025 17:05:16 GMT  
		Size: 50.7 MB (50717459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d46fa073a9fd04739b1d191001dfc5ce09da96d8d4c0af8a03a7f9ca81c445`  
		Last Modified: Thu, 08 May 2025 17:05:12 GMT  
		Size: 342.6 KB (342568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f141accf2c2a408013c16f96d8aad85739eaff1ab8f872d1186c8c96d7dadce`  
		Last Modified: Thu, 08 May 2025 17:05:13 GMT  
		Size: 916.4 KB (916375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:894d6d306f4a156faef3730e7718f84b3f6a7e61a7ac87f59db565eb55c2b41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27620532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b93e73bd53bcf0cba37d3bb0c53db0aed971446443b64039246ecd9c552df9`

```dockerfile
```

-	Layers:
	-	`sha256:ae2cb33b1ab49a18cd94355d1e94171e5d5904a2f7886c1a45b833b63804f3be`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 27.6 MB (27606846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a19f11b316561bc9402681823319dbab7b17538ca6eab782b6c261f95d0e2708`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 13.7 KB (13686 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:7f06923620dcb14829611b10907cc82c55a7b333c9318bfeb53cd8ad907fc195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228333887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6480a80e46afc8bd51cd981ff94aa3fab93b996f1f7de2b88dc118703d16488`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:3596bc04094955644b548ea1c23b1a6bdc109275e65283ca4fd1f6a9a89d8626`  
		Last Modified: Sun, 18 May 2025 18:45:27 GMT  
		Size: 1.2 MB (1194711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93ea204140e85e488ee453c48b702ee6d1215d0c8a37917d51770766fa1863`  
		Last Modified: Sun, 18 May 2025 18:45:30 GMT  
		Size: 4.5 MB (4489374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f66ca89d4141b646b78981e712368d2a6c606146007a28fbafa1a7722f8fb5`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41353e856d62bf7da977152eeb11f65f00acf8fff54c22e92373a53045d67f`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20730724004eb01785b328d46ba7823f1c1692018c81e257b8f2c1f1e2f887`  
		Last Modified: Tue, 20 May 2025 09:31:42 GMT  
		Size: 157.6 MB (157555882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46fc9a00d6b061bc163a63a7b4ab2a3954a1181b3e35917e6ef4d73c581f37`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79409844b34fb92b857683485d70dfbd0be143a3204925a1d365ac95595758`  
		Last Modified: Sun, 18 May 2025 18:45:39 GMT  
		Size: 40.3 MB (40277695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226ef6ad1c100f52351ff305d7b4a124148ff932894cd872354fefce17c8f31`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 342.6 KB (342571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f761607f87c78ac5442bc670e7e9f423410c6fb081d3271d93253e4ba526d`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 847.1 KB (847126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:18e13ecba12a87f54a9f386ce6fec1aeeec342d51cebc59f93687d200660c0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27383622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a59e628885a870a5e4c547949eb356a8207eefb673574a207d30cc44edc84c`

```dockerfile
```

-	Layers:
	-	`sha256:8766d60d6a90fdccae930bfb00cf53eea623068ac6966e1518c6e114ae3fed15`  
		Last Modified: Wed, 09 Apr 2025 12:49:05 GMT  
		Size: 27.4 MB (27369842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d36c37521d0d18b0e266ef7e93c98217a617d45aee5ca476c23b1b6c605339c5`  
		Last Modified: Wed, 09 Apr 2025 12:49:04 GMT  
		Size: 13.8 KB (13780 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5626d190770d234143954698dddf98a9cb97a3429922bc05e310d034c5ee7006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250235697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1a8972be4098e73a367bc535112949e47c4dbd1e183fa1e6f87ea23060dcac`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:79b1b5c52d6e8060d576d30ef37b2dff7ac599a9acd3a50369427d2448b8707c`  
		Last Modified: Thu, 08 May 2025 19:41:35 GMT  
		Size: 1.2 MB (1194543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd8cbf95842dba0eabf002f3aea2635e781f046658cce5b7ba313fad10bde90`  
		Last Modified: Thu, 08 May 2025 19:41:34 GMT  
		Size: 5.3 MB (5344064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fe00290afb945b6813546d3926aea5a8ec0082d4a1dc0d63bb3086b1e2a8a1`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae42f08156cf5ed9de8bc1f6d53206b54a49718b831050ddbac5cee7fb21775`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1035cf4b45887b737d9db818d2873882f4ed775c8802ec12500a5a7eb61928`  
		Last Modified: Thu, 08 May 2025 19:41:57 GMT  
		Size: 171.5 MB (171486596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea9b1520ad4662c02b05f9d047e3831dc184c6a7323a71f1128591ca69f26d`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa074f57d5682580ed27d2a5cecc84542028a7dd9e838cb04deb0ba31b051878`  
		Last Modified: Thu, 08 May 2025 19:41:51 GMT  
		Size: 45.0 MB (44990177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e66974cba6bb44f651eb6e6ba3e0bc14e999155f94cb079f5c83af285435746`  
		Last Modified: Thu, 08 May 2025 19:41:31 GMT  
		Size: 342.6 KB (342564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7278c4ff3a25bd1a3c8f3fa178fa20f12c6609c591924217d492c7d76214d0`  
		Last Modified: Thu, 08 May 2025 19:41:31 GMT  
		Size: 897.6 KB (897624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base` - unknown; unknown

```console
$ docker pull ros@sha256:90249cede2082d3aca1db98135b1ab6e429caf1bbf08b4fa8bccdabcafd0925c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27570563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c578189226a60b3bda679cb5b90bde0c4f7744d0f14b14b8d36142d77e5d57c`

```dockerfile
```

-	Layers:
	-	`sha256:d75e6f47c4ab5594fbea0ec4966288fd99af3dd31e0e15bc514e31ce7c4a43ca`  
		Last Modified: Wed, 09 Apr 2025 15:45:44 GMT  
		Size: 27.6 MB (27556755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfa8fdd93e74bccd7e121aacd19ef9d4f55868eff3f212e02c656d6ece48bd74`  
		Last Modified: Wed, 09 Apr 2025 15:45:43 GMT  
		Size: 13.8 KB (13808 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:6465a56f03f72033905bd7c537d29848c14c78e087bab45ea30181f3ca06ded3
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
$ docker pull ros@sha256:274cafb4228a90240a38e98eb7b469071d8912de039db739bc5a683b0008e345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263117266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c445e4e9450d813702fa00d57b2bace32ecd24a584b6093d57ca2cf4b06fd2e9`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:fe5f39a48dd5e32631ed16c88dce9f258413e07a4bd18febf0fe86116fd84718`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 1.2 MB (1194707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e85c211102ab44bb27f6fae9285c9d5372b02fa7957fef17cf88938d6c6fdfc`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 5.4 MB (5363878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6311663f122dccef631ec54a38cb7388fd50b5c2fe26207dbc65c9e1cce5709`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ea9a5fcfe3a513395e2980f864dad1efe2ad81c1932bec13e1ad6de300f85`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633e89e2c9ac48f8bf438c0688d6ec1409062328508ee6720565f4ba0be5e6a6`  
		Last Modified: Thu, 08 May 2025 17:05:34 GMT  
		Size: 177.1 MB (177069417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ccad8440f923e4cdaf8882f41787c599a4e976a9350b51b0f45aebcc9c70`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230eaefd6c1785cce75d62b2cd7f24ce3ece78e4978c84ad13f244b0761b531`  
		Last Modified: Thu, 08 May 2025 17:05:16 GMT  
		Size: 50.7 MB (50717459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d46fa073a9fd04739b1d191001dfc5ce09da96d8d4c0af8a03a7f9ca81c445`  
		Last Modified: Thu, 08 May 2025 17:05:12 GMT  
		Size: 342.6 KB (342568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f141accf2c2a408013c16f96d8aad85739eaff1ab8f872d1186c8c96d7dadce`  
		Last Modified: Thu, 08 May 2025 17:05:13 GMT  
		Size: 916.4 KB (916375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:894d6d306f4a156faef3730e7718f84b3f6a7e61a7ac87f59db565eb55c2b41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27620532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b93e73bd53bcf0cba37d3bb0c53db0aed971446443b64039246ecd9c552df9`

```dockerfile
```

-	Layers:
	-	`sha256:ae2cb33b1ab49a18cd94355d1e94171e5d5904a2f7886c1a45b833b63804f3be`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 27.6 MB (27606846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a19f11b316561bc9402681823319dbab7b17538ca6eab782b6c261f95d0e2708`  
		Last Modified: Wed, 09 Apr 2025 02:15:47 GMT  
		Size: 13.7 KB (13686 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:7f06923620dcb14829611b10907cc82c55a7b333c9318bfeb53cd8ad907fc195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228333887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6480a80e46afc8bd51cd981ff94aa3fab93b996f1f7de2b88dc118703d16488`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:3596bc04094955644b548ea1c23b1a6bdc109275e65283ca4fd1f6a9a89d8626`  
		Last Modified: Sun, 18 May 2025 18:45:27 GMT  
		Size: 1.2 MB (1194711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93ea204140e85e488ee453c48b702ee6d1215d0c8a37917d51770766fa1863`  
		Last Modified: Sun, 18 May 2025 18:45:30 GMT  
		Size: 4.5 MB (4489374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f66ca89d4141b646b78981e712368d2a6c606146007a28fbafa1a7722f8fb5`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41353e856d62bf7da977152eeb11f65f00acf8fff54c22e92373a53045d67f`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20730724004eb01785b328d46ba7823f1c1692018c81e257b8f2c1f1e2f887`  
		Last Modified: Tue, 20 May 2025 09:31:42 GMT  
		Size: 157.6 MB (157555882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46fc9a00d6b061bc163a63a7b4ab2a3954a1181b3e35917e6ef4d73c581f37`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79409844b34fb92b857683485d70dfbd0be143a3204925a1d365ac95595758`  
		Last Modified: Sun, 18 May 2025 18:45:39 GMT  
		Size: 40.3 MB (40277695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226ef6ad1c100f52351ff305d7b4a124148ff932894cd872354fefce17c8f31`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 342.6 KB (342571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f761607f87c78ac5442bc670e7e9f423410c6fb081d3271d93253e4ba526d`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 847.1 KB (847126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:18e13ecba12a87f54a9f386ce6fec1aeeec342d51cebc59f93687d200660c0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27383622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a59e628885a870a5e4c547949eb356a8207eefb673574a207d30cc44edc84c`

```dockerfile
```

-	Layers:
	-	`sha256:8766d60d6a90fdccae930bfb00cf53eea623068ac6966e1518c6e114ae3fed15`  
		Last Modified: Wed, 09 Apr 2025 12:49:05 GMT  
		Size: 27.4 MB (27369842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d36c37521d0d18b0e266ef7e93c98217a617d45aee5ca476c23b1b6c605339c5`  
		Last Modified: Wed, 09 Apr 2025 12:49:04 GMT  
		Size: 13.8 KB (13780 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5626d190770d234143954698dddf98a9cb97a3429922bc05e310d034c5ee7006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250235697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1a8972be4098e73a367bc535112949e47c4dbd1e183fa1e6f87ea23060dcac`
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
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Nov 2020 19:36:01 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
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
	-	`sha256:79b1b5c52d6e8060d576d30ef37b2dff7ac599a9acd3a50369427d2448b8707c`  
		Last Modified: Thu, 08 May 2025 19:41:35 GMT  
		Size: 1.2 MB (1194543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd8cbf95842dba0eabf002f3aea2635e781f046658cce5b7ba313fad10bde90`  
		Last Modified: Thu, 08 May 2025 19:41:34 GMT  
		Size: 5.3 MB (5344064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fe00290afb945b6813546d3926aea5a8ec0082d4a1dc0d63bb3086b1e2a8a1`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae42f08156cf5ed9de8bc1f6d53206b54a49718b831050ddbac5cee7fb21775`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1035cf4b45887b737d9db818d2873882f4ed775c8802ec12500a5a7eb61928`  
		Last Modified: Thu, 08 May 2025 19:41:57 GMT  
		Size: 171.5 MB (171486596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea9b1520ad4662c02b05f9d047e3831dc184c6a7323a71f1128591ca69f26d`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa074f57d5682580ed27d2a5cecc84542028a7dd9e838cb04deb0ba31b051878`  
		Last Modified: Thu, 08 May 2025 19:41:51 GMT  
		Size: 45.0 MB (44990177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e66974cba6bb44f651eb6e6ba3e0bc14e999155f94cb079f5c83af285435746`  
		Last Modified: Thu, 08 May 2025 19:41:31 GMT  
		Size: 342.6 KB (342564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7278c4ff3a25bd1a3c8f3fa178fa20f12c6609c591924217d492c7d76214d0`  
		Last Modified: Thu, 08 May 2025 19:41:31 GMT  
		Size: 897.6 KB (897624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-base-focal` - unknown; unknown

```console
$ docker pull ros@sha256:90249cede2082d3aca1db98135b1ab6e429caf1bbf08b4fa8bccdabcafd0925c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27570563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c578189226a60b3bda679cb5b90bde0c4f7744d0f14b14b8d36142d77e5d57c`

```dockerfile
```

-	Layers:
	-	`sha256:d75e6f47c4ab5594fbea0ec4966288fd99af3dd31e0e15bc514e31ce7c4a43ca`  
		Last Modified: Wed, 09 Apr 2025 15:45:44 GMT  
		Size: 27.6 MB (27556755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfa8fdd93e74bccd7e121aacd19ef9d4f55868eff3f212e02c656d6ece48bd74`  
		Last Modified: Wed, 09 Apr 2025 15:45:43 GMT  
		Size: 13.8 KB (13808 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:9879882c8bc0d413196d642b4d6472d48aca8e71904095165130b6ad997cb005
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
$ docker pull ros@sha256:e3ee73327a6c0b9fcc0d0417f497efd32bdd1fb805eedc6cb9ac569a74106ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211140864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4322e50775a7c49dcdea57f96c4f54a779e8ae843ab3585f21def61bd84b6e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=noetic
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5f39a48dd5e32631ed16c88dce9f258413e07a4bd18febf0fe86116fd84718`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 1.2 MB (1194707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e85c211102ab44bb27f6fae9285c9d5372b02fa7957fef17cf88938d6c6fdfc`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 5.4 MB (5363878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6311663f122dccef631ec54a38cb7388fd50b5c2fe26207dbc65c9e1cce5709`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ea9a5fcfe3a513395e2980f864dad1efe2ad81c1932bec13e1ad6de300f85`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633e89e2c9ac48f8bf438c0688d6ec1409062328508ee6720565f4ba0be5e6a6`  
		Last Modified: Thu, 08 May 2025 17:05:34 GMT  
		Size: 177.1 MB (177069417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ccad8440f923e4cdaf8882f41787c599a4e976a9350b51b0f45aebcc9c70`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:f4c31b8b90bd7e7521a693330759356bfd3a2a2a33e93163f474e52d8878c76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26143714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b714883d7de56c37684a771cbf4fc78714590ee1dd0648a263545c517f80e8cb`

```dockerfile
```

-	Layers:
	-	`sha256:1e714282d84d7ce6bd446b3b0a913a7fdc97e18fd7cba34d59d962e35b020bd2`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 26.1 MB (26127337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f9dc9e7dadf0400d5163e43754c73c9e03fb1674775b61a4727c541ea31a051`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 16.4 KB (16377 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:151b9235253426a0d8e7655e9bfbae714abe57ba72caeb42dec05744ba16c1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186866495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd4efad2dd6ff7af9c5ec58d3379e00fdad60531ffa040973347a4452589d9e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=noetic
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Thu, 08 May 2025 17:24:17 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3596bc04094955644b548ea1c23b1a6bdc109275e65283ca4fd1f6a9a89d8626`  
		Last Modified: Sun, 18 May 2025 18:45:27 GMT  
		Size: 1.2 MB (1194711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93ea204140e85e488ee453c48b702ee6d1215d0c8a37917d51770766fa1863`  
		Last Modified: Sun, 18 May 2025 18:45:30 GMT  
		Size: 4.5 MB (4489374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f66ca89d4141b646b78981e712368d2a6c606146007a28fbafa1a7722f8fb5`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41353e856d62bf7da977152eeb11f65f00acf8fff54c22e92373a53045d67f`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20730724004eb01785b328d46ba7823f1c1692018c81e257b8f2c1f1e2f887`  
		Last Modified: Tue, 20 May 2025 09:31:42 GMT  
		Size: 157.6 MB (157555882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46fc9a00d6b061bc163a63a7b4ab2a3954a1181b3e35917e6ef4d73c581f37`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:6e8b44927476ef189f622ca00c9fb5e9bb851eec69e78e75634e3eea58720b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26056807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba816d41d03aed709f0b2decbc51c6450d406ac842f5c800e17f053a9384bc5b`

```dockerfile
```

-	Layers:
	-	`sha256:a9ac5d1d21afcfb57c58e67437ba9a2f2e7941be62277aafa75e7edf5011dabe`  
		Last Modified: Wed, 09 Apr 2025 12:06:04 GMT  
		Size: 26.0 MB (26040318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fb27a049109432dba7aeb4f84280414ead6bbb0d9f67f35c6af454dc3dbf1ef`  
		Last Modified: Wed, 09 Apr 2025 12:06:02 GMT  
		Size: 16.5 KB (16489 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0f7de31ac9a71ebf9ebca0bf424fa4343ae519c76bd4b050de1f573191397a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (204005332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ac5c2cfabd3fd3599fb21adaea30c6dfa43fb474de5a21de1366025e0b43a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=noetic
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b1b5c52d6e8060d576d30ef37b2dff7ac599a9acd3a50369427d2448b8707c`  
		Last Modified: Thu, 08 May 2025 19:41:35 GMT  
		Size: 1.2 MB (1194543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd8cbf95842dba0eabf002f3aea2635e781f046658cce5b7ba313fad10bde90`  
		Last Modified: Thu, 08 May 2025 19:41:34 GMT  
		Size: 5.3 MB (5344064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fe00290afb945b6813546d3926aea5a8ec0082d4a1dc0d63bb3086b1e2a8a1`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae42f08156cf5ed9de8bc1f6d53206b54a49718b831050ddbac5cee7fb21775`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1035cf4b45887b737d9db818d2873882f4ed775c8802ec12500a5a7eb61928`  
		Last Modified: Thu, 08 May 2025 19:41:57 GMT  
		Size: 171.5 MB (171486596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea9b1520ad4662c02b05f9d047e3831dc184c6a7323a71f1128591ca69f26d`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core` - unknown; unknown

```console
$ docker pull ros@sha256:34f5d25371f8858ec64b5b90e6a02a87290490571242bb5f2eb693d20c242aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26065587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6116132cc84451c0715ce6d9193b941c50145a233232866fc290ccea8e9cb7e`

```dockerfile
```

-	Layers:
	-	`sha256:27167fa2a14e9cf15daff2f6310176e962d915900aacb47474061a6874ee4f24`  
		Last Modified: Wed, 09 Apr 2025 09:09:07 GMT  
		Size: 26.0 MB (26049070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec7aed39508320d33a62deae1dd7261a6270fcade2f287ea90dffb8f5004a26`  
		Last Modified: Wed, 09 Apr 2025 09:09:05 GMT  
		Size: 16.5 KB (16517 bytes)  
		MIME: application/vnd.in-toto+json

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:9879882c8bc0d413196d642b4d6472d48aca8e71904095165130b6ad997cb005
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
$ docker pull ros@sha256:e3ee73327a6c0b9fcc0d0417f497efd32bdd1fb805eedc6cb9ac569a74106ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211140864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4322e50775a7c49dcdea57f96c4f54a779e8ae843ab3585f21def61bd84b6e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=noetic
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5f39a48dd5e32631ed16c88dce9f258413e07a4bd18febf0fe86116fd84718`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 1.2 MB (1194707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e85c211102ab44bb27f6fae9285c9d5372b02fa7957fef17cf88938d6c6fdfc`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 5.4 MB (5363878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6311663f122dccef631ec54a38cb7388fd50b5c2fe26207dbc65c9e1cce5709`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333ea9a5fcfe3a513395e2980f864dad1efe2ad81c1932bec13e1ad6de300f85`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633e89e2c9ac48f8bf438c0688d6ec1409062328508ee6720565f4ba0be5e6a6`  
		Last Modified: Thu, 08 May 2025 17:05:34 GMT  
		Size: 177.1 MB (177069417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0ccad8440f923e4cdaf8882f41787c599a4e976a9350b51b0f45aebcc9c70`  
		Last Modified: Thu, 08 May 2025 17:05:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:f4c31b8b90bd7e7521a693330759356bfd3a2a2a33e93163f474e52d8878c76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26143714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b714883d7de56c37684a771cbf4fc78714590ee1dd0648a263545c517f80e8cb`

```dockerfile
```

-	Layers:
	-	`sha256:1e714282d84d7ce6bd446b3b0a913a7fdc97e18fd7cba34d59d962e35b020bd2`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 26.1 MB (26127337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f9dc9e7dadf0400d5163e43754c73c9e03fb1674775b61a4727c541ea31a051`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 16.4 KB (16377 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:151b9235253426a0d8e7655e9bfbae714abe57ba72caeb42dec05744ba16c1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186866495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd4efad2dd6ff7af9c5ec58d3379e00fdad60531ffa040973347a4452589d9e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=noetic
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Thu, 08 May 2025 17:24:17 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3596bc04094955644b548ea1c23b1a6bdc109275e65283ca4fd1f6a9a89d8626`  
		Last Modified: Sun, 18 May 2025 18:45:27 GMT  
		Size: 1.2 MB (1194711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93ea204140e85e488ee453c48b702ee6d1215d0c8a37917d51770766fa1863`  
		Last Modified: Sun, 18 May 2025 18:45:30 GMT  
		Size: 4.5 MB (4489374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f66ca89d4141b646b78981e712368d2a6c606146007a28fbafa1a7722f8fb5`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41353e856d62bf7da977152eeb11f65f00acf8fff54c22e92373a53045d67f`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20730724004eb01785b328d46ba7823f1c1692018c81e257b8f2c1f1e2f887`  
		Last Modified: Tue, 20 May 2025 09:31:42 GMT  
		Size: 157.6 MB (157555882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46fc9a00d6b061bc163a63a7b4ab2a3954a1181b3e35917e6ef4d73c581f37`  
		Last Modified: Fri, 09 May 2025 06:25:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:6e8b44927476ef189f622ca00c9fb5e9bb851eec69e78e75634e3eea58720b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26056807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba816d41d03aed709f0b2decbc51c6450d406ac842f5c800e17f053a9384bc5b`

```dockerfile
```

-	Layers:
	-	`sha256:a9ac5d1d21afcfb57c58e67437ba9a2f2e7941be62277aafa75e7edf5011dabe`  
		Last Modified: Wed, 09 Apr 2025 12:06:04 GMT  
		Size: 26.0 MB (26040318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fb27a049109432dba7aeb4f84280414ead6bbb0d9f67f35c6af454dc3dbf1ef`  
		Last Modified: Wed, 09 Apr 2025 12:06:02 GMT  
		Size: 16.5 KB (16489 bytes)  
		MIME: application/vnd.in-toto+json

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0f7de31ac9a71ebf9ebca0bf424fa4343ae519c76bd4b050de1f573191397a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (204005332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ac5c2cfabd3fd3599fb21adaea30c6dfa43fb474de5a21de1366025e0b43a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 10 Feb 2025 08:31:29 GMT
ARG RELEASE
# Mon, 10 Feb 2025 08:31:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 10 Feb 2025 08:31:29 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 10 Feb 2025 08:31:29 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["/bin/bash"]
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN set -eux;        key='C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654';        export GNUPGHOME="$(mktemp -d)";        gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key";        mkdir -p /usr/share/keyrings;        gpg --batch --export "$key" > /usr/share/keyrings/ros1-latest-archive-keyring.gpg;        gpgconf --kill all;        rm -rf "$GNUPGHOME" # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
RUN echo "deb [ signed-by=/usr/share/keyrings/ros1-latest-archive-keyring.gpg ] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LANG=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV LC_ALL=C.UTF-8
# Mon, 10 Feb 2025 08:31:29 GMT
ENV ROS_DISTRO=noetic
# Mon, 10 Feb 2025 08:31:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
COPY ./ros_entrypoint.sh / # buildkit
# Mon, 10 Feb 2025 08:31:29 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 10 Feb 2025 08:31:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b1b5c52d6e8060d576d30ef37b2dff7ac599a9acd3a50369427d2448b8707c`  
		Last Modified: Thu, 08 May 2025 19:41:35 GMT  
		Size: 1.2 MB (1194543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd8cbf95842dba0eabf002f3aea2635e781f046658cce5b7ba313fad10bde90`  
		Last Modified: Thu, 08 May 2025 19:41:34 GMT  
		Size: 5.3 MB (5344064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fe00290afb945b6813546d3926aea5a8ec0082d4a1dc0d63bb3086b1e2a8a1`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae42f08156cf5ed9de8bc1f6d53206b54a49718b831050ddbac5cee7fb21775`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1035cf4b45887b737d9db818d2873882f4ed775c8802ec12500a5a7eb61928`  
		Last Modified: Thu, 08 May 2025 19:41:57 GMT  
		Size: 171.5 MB (171486596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea9b1520ad4662c02b05f9d047e3831dc184c6a7323a71f1128591ca69f26d`  
		Last Modified: Thu, 08 May 2025 19:41:36 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ros:noetic-ros-core-focal` - unknown; unknown

```console
$ docker pull ros@sha256:34f5d25371f8858ec64b5b90e6a02a87290490571242bb5f2eb693d20c242aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26065587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6116132cc84451c0715ce6d9193b941c50145a233232866fc290ccea8e9cb7e`

```dockerfile
```

-	Layers:
	-	`sha256:27167fa2a14e9cf15daff2f6310176e962d915900aacb47474061a6874ee4f24`  
		Last Modified: Wed, 09 Apr 2025 09:09:07 GMT  
		Size: 26.0 MB (26049070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec7aed39508320d33a62deae1dd7261a6270fcade2f287ea90dffb8f5004a26`  
		Last Modified: Wed, 09 Apr 2025 09:09:05 GMT  
		Size: 16.5 KB (16517 bytes)  
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
