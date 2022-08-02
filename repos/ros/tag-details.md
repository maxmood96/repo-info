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
$ docker pull ros@sha256:32e86135cb8111e6f12523fa20a3c08d56026ddde04aed04c807db26ffd8db05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy` - linux; amd64

```console
$ docker pull ros@sha256:e613ea66938d881430319d733c0c434236d92cd21b543a5d83f9fc8296b2ccfa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250645508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a9cba3f8cf84a9d108082cb7daec5057b37820ac0c06e93c9936f776b3ac1b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:27:23 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:27:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 13:29:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:29:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:29:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:29:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:30:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:30:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:30:27 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:31:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7922b843c9985c018b28399cfe7cdf458b105aa857166116387fb59aea69773e`  
		Last Modified: Tue, 02 Aug 2022 14:01:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7d4dffb56dd34745f4b3d35b10fffeaa9fb9d3e4289645c3f872151b5ee3ae`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c52ae16f14310233a6e7249f0fa763fae9f5995610d370d531d882fff1f338d`  
		Last Modified: Tue, 02 Aug 2022 14:01:37 GMT  
		Size: 120.1 MB (120094593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbe4231b7280f383df6653740ce8b62eb7b3b26eb9b73063194fb33adaad0c5`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1860d019f8d83ce737fa22bbc20d50e8ad9ee06c8b790aecd7ad5f4f5b7b4217`  
		Last Modified: Tue, 02 Aug 2022 14:01:58 GMT  
		Size: 73.3 MB (73321236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4deaeff6a713d4b6767976eb346827c701fe347d528f6851b6092cdc151c65`  
		Last Modified: Tue, 02 Aug 2022 14:01:47 GMT  
		Size: 260.9 KB (260923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6111214e0f2e935ae823a1da2de08f1d686923dc249d6d4372d640bdbb42e92`  
		Last Modified: Tue, 02 Aug 2022 14:01:47 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eacb7c7081c45f56ff2d971ab52dbff21183ebd2588413f8c7e8a957b2fd35c`  
		Last Modified: Tue, 02 Aug 2022 14:01:50 GMT  
		Size: 21.7 MB (21663296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:21ac406bc29b75b76613bfbeeaaf50ea812ecb0ae0747b0a4c017ae8b7d24594
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (226048428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7c48b9d562076023020e2d5b4618b7394b41d20d86b7639ae4f5136c37e665`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:21:03 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 15:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:21:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:21:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:21:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:22:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:22:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:22:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:23:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c95a64572463fdd2d4da0ee7a97ef6c2697332b4ec60bd367e4cd19991e0e30`  
		Last Modified: Tue, 02 Aug 2022 15:46:46 GMT  
		Size: 104.3 MB (104269304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6081d9d7b2a4859859c99dbf1aad54f3b6ff971aab468768c5a4b82b1f9eb5f`  
		Last Modified: Tue, 02 Aug 2022 15:46:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384f02761631a00491d018951bf10473535158ed993973ee5a21534c0413691e`  
		Last Modified: Tue, 02 Aug 2022 15:47:08 GMT  
		Size: 67.4 MB (67448558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668918483f09cef23a428dc6fe3a5cbf56a08974b0c370421c3aaf02fbfdf045`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 260.9 KB (260876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bf6d2a082a0478f917366d67636027a403007d46b96d7f06a6b76eb4da6358`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 2.2 KB (2248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2892bdcdd7472d84ac2f6e5bdca785fda5551b8f2f9acb56309c2294fecef`  
		Last Modified: Tue, 02 Aug 2022 15:47:01 GMT  
		Size: 20.4 MB (20366890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-base`

```console
$ docker pull ros@sha256:32e86135cb8111e6f12523fa20a3c08d56026ddde04aed04c807db26ffd8db05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:e613ea66938d881430319d733c0c434236d92cd21b543a5d83f9fc8296b2ccfa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250645508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a9cba3f8cf84a9d108082cb7daec5057b37820ac0c06e93c9936f776b3ac1b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:27:23 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:27:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 13:29:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:29:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:29:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:29:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:30:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:30:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:30:27 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:31:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7922b843c9985c018b28399cfe7cdf458b105aa857166116387fb59aea69773e`  
		Last Modified: Tue, 02 Aug 2022 14:01:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7d4dffb56dd34745f4b3d35b10fffeaa9fb9d3e4289645c3f872151b5ee3ae`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c52ae16f14310233a6e7249f0fa763fae9f5995610d370d531d882fff1f338d`  
		Last Modified: Tue, 02 Aug 2022 14:01:37 GMT  
		Size: 120.1 MB (120094593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbe4231b7280f383df6653740ce8b62eb7b3b26eb9b73063194fb33adaad0c5`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1860d019f8d83ce737fa22bbc20d50e8ad9ee06c8b790aecd7ad5f4f5b7b4217`  
		Last Modified: Tue, 02 Aug 2022 14:01:58 GMT  
		Size: 73.3 MB (73321236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4deaeff6a713d4b6767976eb346827c701fe347d528f6851b6092cdc151c65`  
		Last Modified: Tue, 02 Aug 2022 14:01:47 GMT  
		Size: 260.9 KB (260923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6111214e0f2e935ae823a1da2de08f1d686923dc249d6d4372d640bdbb42e92`  
		Last Modified: Tue, 02 Aug 2022 14:01:47 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eacb7c7081c45f56ff2d971ab52dbff21183ebd2588413f8c7e8a957b2fd35c`  
		Last Modified: Tue, 02 Aug 2022 14:01:50 GMT  
		Size: 21.7 MB (21663296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:21ac406bc29b75b76613bfbeeaaf50ea812ecb0ae0747b0a4c017ae8b7d24594
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (226048428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7c48b9d562076023020e2d5b4618b7394b41d20d86b7639ae4f5136c37e665`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:21:03 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 15:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:21:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:21:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:21:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:22:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:22:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:22:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:23:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c95a64572463fdd2d4da0ee7a97ef6c2697332b4ec60bd367e4cd19991e0e30`  
		Last Modified: Tue, 02 Aug 2022 15:46:46 GMT  
		Size: 104.3 MB (104269304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6081d9d7b2a4859859c99dbf1aad54f3b6ff971aab468768c5a4b82b1f9eb5f`  
		Last Modified: Tue, 02 Aug 2022 15:46:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384f02761631a00491d018951bf10473535158ed993973ee5a21534c0413691e`  
		Last Modified: Tue, 02 Aug 2022 15:47:08 GMT  
		Size: 67.4 MB (67448558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668918483f09cef23a428dc6fe3a5cbf56a08974b0c370421c3aaf02fbfdf045`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 260.9 KB (260876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bf6d2a082a0478f917366d67636027a403007d46b96d7f06a6b76eb4da6358`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 2.2 KB (2248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2892bdcdd7472d84ac2f6e5bdca785fda5551b8f2f9acb56309c2294fecef`  
		Last Modified: Tue, 02 Aug 2022 15:47:01 GMT  
		Size: 20.4 MB (20366890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-base-focal`

```console
$ docker pull ros@sha256:32e86135cb8111e6f12523fa20a3c08d56026ddde04aed04c807db26ffd8db05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:e613ea66938d881430319d733c0c434236d92cd21b543a5d83f9fc8296b2ccfa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250645508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a9cba3f8cf84a9d108082cb7daec5057b37820ac0c06e93c9936f776b3ac1b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:27:23 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:27:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 13:29:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:29:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:29:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:29:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:30:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:30:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:30:27 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:31:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7922b843c9985c018b28399cfe7cdf458b105aa857166116387fb59aea69773e`  
		Last Modified: Tue, 02 Aug 2022 14:01:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7d4dffb56dd34745f4b3d35b10fffeaa9fb9d3e4289645c3f872151b5ee3ae`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c52ae16f14310233a6e7249f0fa763fae9f5995610d370d531d882fff1f338d`  
		Last Modified: Tue, 02 Aug 2022 14:01:37 GMT  
		Size: 120.1 MB (120094593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbe4231b7280f383df6653740ce8b62eb7b3b26eb9b73063194fb33adaad0c5`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1860d019f8d83ce737fa22bbc20d50e8ad9ee06c8b790aecd7ad5f4f5b7b4217`  
		Last Modified: Tue, 02 Aug 2022 14:01:58 GMT  
		Size: 73.3 MB (73321236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4deaeff6a713d4b6767976eb346827c701fe347d528f6851b6092cdc151c65`  
		Last Modified: Tue, 02 Aug 2022 14:01:47 GMT  
		Size: 260.9 KB (260923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6111214e0f2e935ae823a1da2de08f1d686923dc249d6d4372d640bdbb42e92`  
		Last Modified: Tue, 02 Aug 2022 14:01:47 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eacb7c7081c45f56ff2d971ab52dbff21183ebd2588413f8c7e8a957b2fd35c`  
		Last Modified: Tue, 02 Aug 2022 14:01:50 GMT  
		Size: 21.7 MB (21663296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:21ac406bc29b75b76613bfbeeaaf50ea812ecb0ae0747b0a4c017ae8b7d24594
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (226048428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7c48b9d562076023020e2d5b4618b7394b41d20d86b7639ae4f5136c37e665`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:21:03 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 15:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:21:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:21:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:21:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:22:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:22:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:22:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:23:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c95a64572463fdd2d4da0ee7a97ef6c2697332b4ec60bd367e4cd19991e0e30`  
		Last Modified: Tue, 02 Aug 2022 15:46:46 GMT  
		Size: 104.3 MB (104269304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6081d9d7b2a4859859c99dbf1aad54f3b6ff971aab468768c5a4b82b1f9eb5f`  
		Last Modified: Tue, 02 Aug 2022 15:46:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384f02761631a00491d018951bf10473535158ed993973ee5a21534c0413691e`  
		Last Modified: Tue, 02 Aug 2022 15:47:08 GMT  
		Size: 67.4 MB (67448558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668918483f09cef23a428dc6fe3a5cbf56a08974b0c370421c3aaf02fbfdf045`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 260.9 KB (260876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bf6d2a082a0478f917366d67636027a403007d46b96d7f06a6b76eb4da6358`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 2.2 KB (2248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2892bdcdd7472d84ac2f6e5bdca785fda5551b8f2f9acb56309c2294fecef`  
		Last Modified: Tue, 02 Aug 2022 15:47:01 GMT  
		Size: 20.4 MB (20366890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-core`

```console
$ docker pull ros@sha256:d2d734358fd4c8a5181711532c313ff0abacd147e02957b6dc38ed467928e371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:e9a6f94250188aa1cd747876d698d8e037e044a7328d9138df9a1d9ec80fb04a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155397788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1404fde45611b6070ef68bde148ebd15aa98b898d1476624a3a36ffdb0aaa42`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:27:23 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:27:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 13:29:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:29:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:29:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:29:19 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7922b843c9985c018b28399cfe7cdf458b105aa857166116387fb59aea69773e`  
		Last Modified: Tue, 02 Aug 2022 14:01:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7d4dffb56dd34745f4b3d35b10fffeaa9fb9d3e4289645c3f872151b5ee3ae`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c52ae16f14310233a6e7249f0fa763fae9f5995610d370d531d882fff1f338d`  
		Last Modified: Tue, 02 Aug 2022 14:01:37 GMT  
		Size: 120.1 MB (120094593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbe4231b7280f383df6653740ce8b62eb7b3b26eb9b73063194fb33adaad0c5`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4e3e2b4942f4ff2424e12fad581e08a73f65fd63a43ae6b30a25c31a1e57632a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137969856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37682e32a97b7ad60c3f515317757740553ccb72e600e5e2b2e5e9a1316276a4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:21:03 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 15:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:21:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:21:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:21:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c95a64572463fdd2d4da0ee7a97ef6c2697332b4ec60bd367e4cd19991e0e30`  
		Last Modified: Tue, 02 Aug 2022 15:46:46 GMT  
		Size: 104.3 MB (104269304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6081d9d7b2a4859859c99dbf1aad54f3b6ff971aab468768c5a4b82b1f9eb5f`  
		Last Modified: Tue, 02 Aug 2022 15:46:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-core-focal`

```console
$ docker pull ros@sha256:d2d734358fd4c8a5181711532c313ff0abacd147e02957b6dc38ed467928e371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:e9a6f94250188aa1cd747876d698d8e037e044a7328d9138df9a1d9ec80fb04a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155397788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1404fde45611b6070ef68bde148ebd15aa98b898d1476624a3a36ffdb0aaa42`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:27:23 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:27:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 13:29:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:29:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:29:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:29:19 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7922b843c9985c018b28399cfe7cdf458b105aa857166116387fb59aea69773e`  
		Last Modified: Tue, 02 Aug 2022 14:01:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7d4dffb56dd34745f4b3d35b10fffeaa9fb9d3e4289645c3f872151b5ee3ae`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c52ae16f14310233a6e7249f0fa763fae9f5995610d370d531d882fff1f338d`  
		Last Modified: Tue, 02 Aug 2022 14:01:37 GMT  
		Size: 120.1 MB (120094593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbe4231b7280f383df6653740ce8b62eb7b3b26eb9b73063194fb33adaad0c5`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4e3e2b4942f4ff2424e12fad581e08a73f65fd63a43ae6b30a25c31a1e57632a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137969856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37682e32a97b7ad60c3f515317757740553ccb72e600e5e2b2e5e9a1316276a4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:21:03 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 15:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:21:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:21:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:21:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c95a64572463fdd2d4da0ee7a97ef6c2697332b4ec60bd367e4cd19991e0e30`  
		Last Modified: Tue, 02 Aug 2022 15:46:46 GMT  
		Size: 104.3 MB (104269304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6081d9d7b2a4859859c99dbf1aad54f3b6ff971aab468768c5a4b82b1f9eb5f`  
		Last Modified: Tue, 02 Aug 2022 15:46:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros1-bridge`

```console
$ docker pull ros@sha256:0e185ff94ac73619b41fcbdddaa8508da917335aae03e3aae245010f76a869c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:26ff0b66e8070fb5883bc6d3e79e429be979ce4fbc5e78f5735ece8ff91cb000
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.6 MB (348611143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbea4c2c80151dacde3a8b0ffc4e53500e6be19da3c08f93ef911fa2bc15dad`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:27:23 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:27:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 13:29:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:29:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:29:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:29:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:30:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:30:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:30:27 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:31:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:31:24 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 13:31:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:31:26 GMT
ENV ROS1_DISTRO=noetic
# Tue, 02 Aug 2022 13:31:26 GMT
ENV ROS2_DISTRO=foxy
# Tue, 02 Aug 2022 13:32:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:32:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:32:49 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7922b843c9985c018b28399cfe7cdf458b105aa857166116387fb59aea69773e`  
		Last Modified: Tue, 02 Aug 2022 14:01:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7d4dffb56dd34745f4b3d35b10fffeaa9fb9d3e4289645c3f872151b5ee3ae`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c52ae16f14310233a6e7249f0fa763fae9f5995610d370d531d882fff1f338d`  
		Last Modified: Tue, 02 Aug 2022 14:01:37 GMT  
		Size: 120.1 MB (120094593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbe4231b7280f383df6653740ce8b62eb7b3b26eb9b73063194fb33adaad0c5`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1860d019f8d83ce737fa22bbc20d50e8ad9ee06c8b790aecd7ad5f4f5b7b4217`  
		Last Modified: Tue, 02 Aug 2022 14:01:58 GMT  
		Size: 73.3 MB (73321236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4deaeff6a713d4b6767976eb346827c701fe347d528f6851b6092cdc151c65`  
		Last Modified: Tue, 02 Aug 2022 14:01:47 GMT  
		Size: 260.9 KB (260923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6111214e0f2e935ae823a1da2de08f1d686923dc249d6d4372d640bdbb42e92`  
		Last Modified: Tue, 02 Aug 2022 14:01:47 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eacb7c7081c45f56ff2d971ab52dbff21183ebd2588413f8c7e8a957b2fd35c`  
		Last Modified: Tue, 02 Aug 2022 14:01:50 GMT  
		Size: 21.7 MB (21663296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286d636529f999eca09444b318ce3241d317e552f0a4f640b0c1031c9324e7e0`  
		Last Modified: Tue, 02 Aug 2022 14:02:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7c3f4a148e52800a0deda3bb24c15be7027cffdfb1f971d66d6671897590ae`  
		Last Modified: Tue, 02 Aug 2022 14:02:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637c665fa6f5986478cebe9e16d9818f4577a2b1579d903cd92409ef63ae5a7b`  
		Last Modified: Tue, 02 Aug 2022 14:02:26 GMT  
		Size: 76.4 MB (76429024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5363e563fb5b79bdebe0877b556c871de06f2c9c6837bf93b788c1191cf8a1`  
		Last Modified: Tue, 02 Aug 2022 14:02:16 GMT  
		Size: 21.5 MB (21535985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a857bad74b67654b2f1ab2d8ffbac122b18319ed2133b987de53f69657798f`  
		Last Modified: Tue, 02 Aug 2022 14:02:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e908c2d0016f5d0b80de3417ac4423550a10f52342b98bb9573ce1755a66d93e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.3 MB (316275648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07eb9def03493c71fa102c9e773ce7c768b6ce2584769d25759492121f77825e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:21:03 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 15:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:21:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:21:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:21:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:22:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:22:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:22:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:23:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:23:13 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:23:15 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:23:17 GMT
ENV ROS1_DISTRO=noetic
# Tue, 02 Aug 2022 15:23:18 GMT
ENV ROS2_DISTRO=foxy
# Tue, 02 Aug 2022 15:23:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:24:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:24:06 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c95a64572463fdd2d4da0ee7a97ef6c2697332b4ec60bd367e4cd19991e0e30`  
		Last Modified: Tue, 02 Aug 2022 15:46:46 GMT  
		Size: 104.3 MB (104269304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6081d9d7b2a4859859c99dbf1aad54f3b6ff971aab468768c5a4b82b1f9eb5f`  
		Last Modified: Tue, 02 Aug 2022 15:46:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384f02761631a00491d018951bf10473535158ed993973ee5a21534c0413691e`  
		Last Modified: Tue, 02 Aug 2022 15:47:08 GMT  
		Size: 67.4 MB (67448558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668918483f09cef23a428dc6fe3a5cbf56a08974b0c370421c3aaf02fbfdf045`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 260.9 KB (260876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bf6d2a082a0478f917366d67636027a403007d46b96d7f06a6b76eb4da6358`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 2.2 KB (2248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2892bdcdd7472d84ac2f6e5bdca785fda5551b8f2f9acb56309c2294fecef`  
		Last Modified: Tue, 02 Aug 2022 15:47:01 GMT  
		Size: 20.4 MB (20366890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbde1dfcc79d4a7217b8a62168774cb73c2d182e5e154b8bf035c2212d263fc`  
		Last Modified: Tue, 02 Aug 2022 15:47:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e84b0413c2629b20c17fe09106bfb54cbd61d076c1bfd09aba3cb192db7f7b6`  
		Last Modified: Tue, 02 Aug 2022 15:47:39 GMT  
		Size: 76.3 MB (76269498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e39c8f9bee1fefc9e6920baef31896530bf3cf37e7d7f1d16af3ace537f8a35`  
		Last Modified: Tue, 02 Aug 2022 15:47:27 GMT  
		Size: 14.0 MB (13957252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa581353eb222963439f599d8089571c19a9b3791d685d31ca76bababdbf27f`  
		Last Modified: Tue, 02 Aug 2022 15:47:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:0e185ff94ac73619b41fcbdddaa8508da917335aae03e3aae245010f76a869c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:26ff0b66e8070fb5883bc6d3e79e429be979ce4fbc5e78f5735ece8ff91cb000
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.6 MB (348611143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbea4c2c80151dacde3a8b0ffc4e53500e6be19da3c08f93ef911fa2bc15dad`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:27:23 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:27:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 13:29:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:29:19 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:29:19 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:29:19 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:30:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:30:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:30:27 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:31:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:31:24 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 13:31:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:31:26 GMT
ENV ROS1_DISTRO=noetic
# Tue, 02 Aug 2022 13:31:26 GMT
ENV ROS2_DISTRO=foxy
# Tue, 02 Aug 2022 13:32:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:32:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:32:49 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7922b843c9985c018b28399cfe7cdf458b105aa857166116387fb59aea69773e`  
		Last Modified: Tue, 02 Aug 2022 14:01:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7d4dffb56dd34745f4b3d35b10fffeaa9fb9d3e4289645c3f872151b5ee3ae`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c52ae16f14310233a6e7249f0fa763fae9f5995610d370d531d882fff1f338d`  
		Last Modified: Tue, 02 Aug 2022 14:01:37 GMT  
		Size: 120.1 MB (120094593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbe4231b7280f383df6653740ce8b62eb7b3b26eb9b73063194fb33adaad0c5`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1860d019f8d83ce737fa22bbc20d50e8ad9ee06c8b790aecd7ad5f4f5b7b4217`  
		Last Modified: Tue, 02 Aug 2022 14:01:58 GMT  
		Size: 73.3 MB (73321236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4deaeff6a713d4b6767976eb346827c701fe347d528f6851b6092cdc151c65`  
		Last Modified: Tue, 02 Aug 2022 14:01:47 GMT  
		Size: 260.9 KB (260923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6111214e0f2e935ae823a1da2de08f1d686923dc249d6d4372d640bdbb42e92`  
		Last Modified: Tue, 02 Aug 2022 14:01:47 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eacb7c7081c45f56ff2d971ab52dbff21183ebd2588413f8c7e8a957b2fd35c`  
		Last Modified: Tue, 02 Aug 2022 14:01:50 GMT  
		Size: 21.7 MB (21663296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286d636529f999eca09444b318ce3241d317e552f0a4f640b0c1031c9324e7e0`  
		Last Modified: Tue, 02 Aug 2022 14:02:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7c3f4a148e52800a0deda3bb24c15be7027cffdfb1f971d66d6671897590ae`  
		Last Modified: Tue, 02 Aug 2022 14:02:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637c665fa6f5986478cebe9e16d9818f4577a2b1579d903cd92409ef63ae5a7b`  
		Last Modified: Tue, 02 Aug 2022 14:02:26 GMT  
		Size: 76.4 MB (76429024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5363e563fb5b79bdebe0877b556c871de06f2c9c6837bf93b788c1191cf8a1`  
		Last Modified: Tue, 02 Aug 2022 14:02:16 GMT  
		Size: 21.5 MB (21535985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a857bad74b67654b2f1ab2d8ffbac122b18319ed2133b987de53f69657798f`  
		Last Modified: Tue, 02 Aug 2022 14:02:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e908c2d0016f5d0b80de3417ac4423550a10f52342b98bb9573ce1755a66d93e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.3 MB (316275648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07eb9def03493c71fa102c9e773ce7c768b6ce2584769d25759492121f77825e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:21:03 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 15:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:21:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:21:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:21:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:22:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:22:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:22:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:23:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:23:13 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:23:15 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:23:17 GMT
ENV ROS1_DISTRO=noetic
# Tue, 02 Aug 2022 15:23:18 GMT
ENV ROS2_DISTRO=foxy
# Tue, 02 Aug 2022 15:23:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:24:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:24:06 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c95a64572463fdd2d4da0ee7a97ef6c2697332b4ec60bd367e4cd19991e0e30`  
		Last Modified: Tue, 02 Aug 2022 15:46:46 GMT  
		Size: 104.3 MB (104269304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6081d9d7b2a4859859c99dbf1aad54f3b6ff971aab468768c5a4b82b1f9eb5f`  
		Last Modified: Tue, 02 Aug 2022 15:46:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384f02761631a00491d018951bf10473535158ed993973ee5a21534c0413691e`  
		Last Modified: Tue, 02 Aug 2022 15:47:08 GMT  
		Size: 67.4 MB (67448558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668918483f09cef23a428dc6fe3a5cbf56a08974b0c370421c3aaf02fbfdf045`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 260.9 KB (260876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bf6d2a082a0478f917366d67636027a403007d46b96d7f06a6b76eb4da6358`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 2.2 KB (2248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2892bdcdd7472d84ac2f6e5bdca785fda5551b8f2f9acb56309c2294fecef`  
		Last Modified: Tue, 02 Aug 2022 15:47:01 GMT  
		Size: 20.4 MB (20366890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbde1dfcc79d4a7217b8a62168774cb73c2d182e5e154b8bf035c2212d263fc`  
		Last Modified: Tue, 02 Aug 2022 15:47:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e84b0413c2629b20c17fe09106bfb54cbd61d076c1bfd09aba3cb192db7f7b6`  
		Last Modified: Tue, 02 Aug 2022 15:47:39 GMT  
		Size: 76.3 MB (76269498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e39c8f9bee1fefc9e6920baef31896530bf3cf37e7d7f1d16af3ace537f8a35`  
		Last Modified: Tue, 02 Aug 2022 15:47:27 GMT  
		Size: 14.0 MB (13957252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa581353eb222963439f599d8089571c19a9b3791d685d31ca76bababdbf27f`  
		Last Modified: Tue, 02 Aug 2022 15:47:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic`

```console
$ docker pull ros@sha256:b63cde11f0c07569e7d81bd7495993d35797ddf95f2c04de01f8ff641f580aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic` - linux; amd64

```console
$ docker pull ros@sha256:26b0b7d49c3e9fa792a6d7831b98aa6b1bb5add16002f347e5f8a165c3e30f0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234871613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157e48342c45913d631f527697b4b5919461c7ff6547f3e987af8ed95f4fc6ad`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:27:23 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:27:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:33:02 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 13:33:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:33:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:33:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:33:45 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:34:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:34:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:34:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:34:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7922b843c9985c018b28399cfe7cdf458b105aa857166116387fb59aea69773e`  
		Last Modified: Tue, 02 Aug 2022 14:01:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7d4dffb56dd34745f4b3d35b10fffeaa9fb9d3e4289645c3f872151b5ee3ae`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff5bc0f4410a9a4df17b2ba68d11b669ca1b5bfeb7de939c97e51d05b1b4dae`  
		Last Modified: Tue, 02 Aug 2022 14:03:03 GMT  
		Size: 103.9 MB (103883299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28a0c156e3f431ed899d85555fd6240ce1d49f9a40e54350b529a495823808f`  
		Last Modified: Tue, 02 Aug 2022 14:02:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba2bd50d7d05880919f8f6a90f132ff76c104c3edea5258199b2387889dc84a`  
		Last Modified: Tue, 02 Aug 2022 14:03:26 GMT  
		Size: 73.3 MB (73278242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d06c0f29101913e5f40d7fc33f4c270f9b4ef2279944a5308711d28664e4fca`  
		Last Modified: Tue, 02 Aug 2022 14:03:14 GMT  
		Size: 271.8 KB (271834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469a75f80a7f31bd5d819c55b008a36b5ac2069f8fa30f2cc7ea08afa5525a34`  
		Last Modified: Tue, 02 Aug 2022 14:03:14 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bc9b7ea12109f91d10341166fd078867c43304721c1f6a88e0c9e5de0f8dce`  
		Last Modified: Tue, 02 Aug 2022 14:03:19 GMT  
		Size: 22.1 MB (22132816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d75f46e141a80f9b7cff2cf238925c2af89d02ac8adef6b989645cc01ce2eef2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223132370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ac4a489929fe9fffc868878c7d4ec54fa785d4d765c1994394c108c9ab7395`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:24:13 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 15:25:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:25:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:25:07 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:25:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:25:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:26:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec24629b846176e31ddaaf8b24b1ddfa5c013c36a5adc644cc1ea9cbfaf1f0d`  
		Last Modified: Tue, 02 Aug 2022 15:48:08 GMT  
		Size: 100.3 MB (100301595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6c32d186e05482bc0d52ca6d3348f8f2135fe0ce5cb80694cbf0c402904ab`  
		Last Modified: Tue, 02 Aug 2022 15:47:51 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f1bc7aab31ae221d1d0a204692f57529cc52be37d783e9408e6091c9140e30`  
		Last Modified: Tue, 02 Aug 2022 15:48:30 GMT  
		Size: 67.4 MB (67403003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8728db5450b6ae980d219774ae0acd473093c7203a814add3754b37fa58d2f16`  
		Last Modified: Tue, 02 Aug 2022 15:48:20 GMT  
		Size: 271.8 KB (271758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b3c45ed46817bdd81a5f97bc0ac2f937e60aba727035f3fda0c52b1e8d3766`  
		Last Modified: Tue, 02 Aug 2022 15:48:20 GMT  
		Size: 2.2 KB (2208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb12350bd7ee355d38d341f83cd1fc612133c69ea151b66e1784eeb2e27e4a4`  
		Last Modified: Tue, 02 Aug 2022 15:48:23 GMT  
		Size: 21.5 MB (21453253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-base`

```console
$ docker pull ros@sha256:b63cde11f0c07569e7d81bd7495993d35797ddf95f2c04de01f8ff641f580aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:26b0b7d49c3e9fa792a6d7831b98aa6b1bb5add16002f347e5f8a165c3e30f0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234871613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157e48342c45913d631f527697b4b5919461c7ff6547f3e987af8ed95f4fc6ad`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:27:23 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:27:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:33:02 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 13:33:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:33:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:33:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:33:45 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:34:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:34:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:34:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:34:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7922b843c9985c018b28399cfe7cdf458b105aa857166116387fb59aea69773e`  
		Last Modified: Tue, 02 Aug 2022 14:01:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7d4dffb56dd34745f4b3d35b10fffeaa9fb9d3e4289645c3f872151b5ee3ae`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff5bc0f4410a9a4df17b2ba68d11b669ca1b5bfeb7de939c97e51d05b1b4dae`  
		Last Modified: Tue, 02 Aug 2022 14:03:03 GMT  
		Size: 103.9 MB (103883299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28a0c156e3f431ed899d85555fd6240ce1d49f9a40e54350b529a495823808f`  
		Last Modified: Tue, 02 Aug 2022 14:02:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba2bd50d7d05880919f8f6a90f132ff76c104c3edea5258199b2387889dc84a`  
		Last Modified: Tue, 02 Aug 2022 14:03:26 GMT  
		Size: 73.3 MB (73278242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d06c0f29101913e5f40d7fc33f4c270f9b4ef2279944a5308711d28664e4fca`  
		Last Modified: Tue, 02 Aug 2022 14:03:14 GMT  
		Size: 271.8 KB (271834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469a75f80a7f31bd5d819c55b008a36b5ac2069f8fa30f2cc7ea08afa5525a34`  
		Last Modified: Tue, 02 Aug 2022 14:03:14 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bc9b7ea12109f91d10341166fd078867c43304721c1f6a88e0c9e5de0f8dce`  
		Last Modified: Tue, 02 Aug 2022 14:03:19 GMT  
		Size: 22.1 MB (22132816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d75f46e141a80f9b7cff2cf238925c2af89d02ac8adef6b989645cc01ce2eef2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223132370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ac4a489929fe9fffc868878c7d4ec54fa785d4d765c1994394c108c9ab7395`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:24:13 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 15:25:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:25:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:25:07 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:25:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:25:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:26:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec24629b846176e31ddaaf8b24b1ddfa5c013c36a5adc644cc1ea9cbfaf1f0d`  
		Last Modified: Tue, 02 Aug 2022 15:48:08 GMT  
		Size: 100.3 MB (100301595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6c32d186e05482bc0d52ca6d3348f8f2135fe0ce5cb80694cbf0c402904ab`  
		Last Modified: Tue, 02 Aug 2022 15:47:51 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f1bc7aab31ae221d1d0a204692f57529cc52be37d783e9408e6091c9140e30`  
		Last Modified: Tue, 02 Aug 2022 15:48:30 GMT  
		Size: 67.4 MB (67403003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8728db5450b6ae980d219774ae0acd473093c7203a814add3754b37fa58d2f16`  
		Last Modified: Tue, 02 Aug 2022 15:48:20 GMT  
		Size: 271.8 KB (271758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b3c45ed46817bdd81a5f97bc0ac2f937e60aba727035f3fda0c52b1e8d3766`  
		Last Modified: Tue, 02 Aug 2022 15:48:20 GMT  
		Size: 2.2 KB (2208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb12350bd7ee355d38d341f83cd1fc612133c69ea151b66e1784eeb2e27e4a4`  
		Last Modified: Tue, 02 Aug 2022 15:48:23 GMT  
		Size: 21.5 MB (21453253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-base-focal`

```console
$ docker pull ros@sha256:b63cde11f0c07569e7d81bd7495993d35797ddf95f2c04de01f8ff641f580aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:26b0b7d49c3e9fa792a6d7831b98aa6b1bb5add16002f347e5f8a165c3e30f0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234871613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157e48342c45913d631f527697b4b5919461c7ff6547f3e987af8ed95f4fc6ad`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:27:23 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:27:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:33:02 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 13:33:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:33:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:33:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:33:45 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:34:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:34:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:34:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:34:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7922b843c9985c018b28399cfe7cdf458b105aa857166116387fb59aea69773e`  
		Last Modified: Tue, 02 Aug 2022 14:01:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7d4dffb56dd34745f4b3d35b10fffeaa9fb9d3e4289645c3f872151b5ee3ae`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff5bc0f4410a9a4df17b2ba68d11b669ca1b5bfeb7de939c97e51d05b1b4dae`  
		Last Modified: Tue, 02 Aug 2022 14:03:03 GMT  
		Size: 103.9 MB (103883299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28a0c156e3f431ed899d85555fd6240ce1d49f9a40e54350b529a495823808f`  
		Last Modified: Tue, 02 Aug 2022 14:02:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba2bd50d7d05880919f8f6a90f132ff76c104c3edea5258199b2387889dc84a`  
		Last Modified: Tue, 02 Aug 2022 14:03:26 GMT  
		Size: 73.3 MB (73278242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d06c0f29101913e5f40d7fc33f4c270f9b4ef2279944a5308711d28664e4fca`  
		Last Modified: Tue, 02 Aug 2022 14:03:14 GMT  
		Size: 271.8 KB (271834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469a75f80a7f31bd5d819c55b008a36b5ac2069f8fa30f2cc7ea08afa5525a34`  
		Last Modified: Tue, 02 Aug 2022 14:03:14 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bc9b7ea12109f91d10341166fd078867c43304721c1f6a88e0c9e5de0f8dce`  
		Last Modified: Tue, 02 Aug 2022 14:03:19 GMT  
		Size: 22.1 MB (22132816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d75f46e141a80f9b7cff2cf238925c2af89d02ac8adef6b989645cc01ce2eef2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223132370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ac4a489929fe9fffc868878c7d4ec54fa785d4d765c1994394c108c9ab7395`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:24:13 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 15:25:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:25:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:25:07 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:25:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:25:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:26:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec24629b846176e31ddaaf8b24b1ddfa5c013c36a5adc644cc1ea9cbfaf1f0d`  
		Last Modified: Tue, 02 Aug 2022 15:48:08 GMT  
		Size: 100.3 MB (100301595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6c32d186e05482bc0d52ca6d3348f8f2135fe0ce5cb80694cbf0c402904ab`  
		Last Modified: Tue, 02 Aug 2022 15:47:51 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f1bc7aab31ae221d1d0a204692f57529cc52be37d783e9408e6091c9140e30`  
		Last Modified: Tue, 02 Aug 2022 15:48:30 GMT  
		Size: 67.4 MB (67403003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8728db5450b6ae980d219774ae0acd473093c7203a814add3754b37fa58d2f16`  
		Last Modified: Tue, 02 Aug 2022 15:48:20 GMT  
		Size: 271.8 KB (271758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b3c45ed46817bdd81a5f97bc0ac2f937e60aba727035f3fda0c52b1e8d3766`  
		Last Modified: Tue, 02 Aug 2022 15:48:20 GMT  
		Size: 2.2 KB (2208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb12350bd7ee355d38d341f83cd1fc612133c69ea151b66e1784eeb2e27e4a4`  
		Last Modified: Tue, 02 Aug 2022 15:48:23 GMT  
		Size: 21.5 MB (21453253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-core`

```console
$ docker pull ros@sha256:bce8044af0e336f91440711a5504a2f39f06fb8277d876dbc45261c4ff96fc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:9b8050505cf6fe53e21c64db13c18aed1cbb5c950935538479c2d1927d0d103c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139186495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d4a8800f377afbf9fc0d29455b003c21165fd67a2d34034235a50d9d4a8b95`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:27:23 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:27:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:33:02 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 13:33:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:33:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:33:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:33:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7922b843c9985c018b28399cfe7cdf458b105aa857166116387fb59aea69773e`  
		Last Modified: Tue, 02 Aug 2022 14:01:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7d4dffb56dd34745f4b3d35b10fffeaa9fb9d3e4289645c3f872151b5ee3ae`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff5bc0f4410a9a4df17b2ba68d11b669ca1b5bfeb7de939c97e51d05b1b4dae`  
		Last Modified: Tue, 02 Aug 2022 14:03:03 GMT  
		Size: 103.9 MB (103883299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28a0c156e3f431ed899d85555fd6240ce1d49f9a40e54350b529a495823808f`  
		Last Modified: Tue, 02 Aug 2022 14:02:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d188c2c8fa40b0a33ea208fdfa152bc426266ed2bb7206b4a1cdc951f93f4506
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134002148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e49fda94cfbb24093edc051b459c556171662bdd4b4a1a5157bc9ceb1dfba1f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:24:13 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 15:25:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:25:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:25:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec24629b846176e31ddaaf8b24b1ddfa5c013c36a5adc644cc1ea9cbfaf1f0d`  
		Last Modified: Tue, 02 Aug 2022 15:48:08 GMT  
		Size: 100.3 MB (100301595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6c32d186e05482bc0d52ca6d3348f8f2135fe0ce5cb80694cbf0c402904ab`  
		Last Modified: Tue, 02 Aug 2022 15:47:51 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-core-focal`

```console
$ docker pull ros@sha256:bce8044af0e336f91440711a5504a2f39f06fb8277d876dbc45261c4ff96fc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:9b8050505cf6fe53e21c64db13c18aed1cbb5c950935538479c2d1927d0d103c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139186495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d4a8800f377afbf9fc0d29455b003c21165fd67a2d34034235a50d9d4a8b95`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:27:23 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:27:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:33:02 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 13:33:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:33:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:33:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:33:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7922b843c9985c018b28399cfe7cdf458b105aa857166116387fb59aea69773e`  
		Last Modified: Tue, 02 Aug 2022 14:01:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7d4dffb56dd34745f4b3d35b10fffeaa9fb9d3e4289645c3f872151b5ee3ae`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff5bc0f4410a9a4df17b2ba68d11b669ca1b5bfeb7de939c97e51d05b1b4dae`  
		Last Modified: Tue, 02 Aug 2022 14:03:03 GMT  
		Size: 103.9 MB (103883299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28a0c156e3f431ed899d85555fd6240ce1d49f9a40e54350b529a495823808f`  
		Last Modified: Tue, 02 Aug 2022 14:02:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d188c2c8fa40b0a33ea208fdfa152bc426266ed2bb7206b4a1cdc951f93f4506
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134002148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e49fda94cfbb24093edc051b459c556171662bdd4b4a1a5157bc9ceb1dfba1f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:24:13 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 15:25:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:25:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:25:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec24629b846176e31ddaaf8b24b1ddfa5c013c36a5adc644cc1ea9cbfaf1f0d`  
		Last Modified: Tue, 02 Aug 2022 15:48:08 GMT  
		Size: 100.3 MB (100301595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6c32d186e05482bc0d52ca6d3348f8f2135fe0ce5cb80694cbf0c402904ab`  
		Last Modified: Tue, 02 Aug 2022 15:47:51 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros1-bridge`

```console
$ docker pull ros@sha256:35fe74bb930498b5920bf9a469591481e79a4f23388acd977e47ba81dda690ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:147cab728b6776ab4f956f0bfd307ac8646af9c61107f93ad54549bee15642cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.0 MB (330039447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0b0f4fbe76b9774aaaff171e8a868d82675e13cc4ae26fd93b3725bc5cd897`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:27:23 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:27:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:33:02 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 13:33:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:33:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:33:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:33:45 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:34:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:34:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:34:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:34:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:34:39 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 13:34:40 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:34:40 GMT
ENV ROS1_DISTRO=noetic
# Tue, 02 Aug 2022 13:34:40 GMT
ENV ROS2_DISTRO=galactic
# Tue, 02 Aug 2022 13:35:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:17 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7922b843c9985c018b28399cfe7cdf458b105aa857166116387fb59aea69773e`  
		Last Modified: Tue, 02 Aug 2022 14:01:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7d4dffb56dd34745f4b3d35b10fffeaa9fb9d3e4289645c3f872151b5ee3ae`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff5bc0f4410a9a4df17b2ba68d11b669ca1b5bfeb7de939c97e51d05b1b4dae`  
		Last Modified: Tue, 02 Aug 2022 14:03:03 GMT  
		Size: 103.9 MB (103883299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28a0c156e3f431ed899d85555fd6240ce1d49f9a40e54350b529a495823808f`  
		Last Modified: Tue, 02 Aug 2022 14:02:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba2bd50d7d05880919f8f6a90f132ff76c104c3edea5258199b2387889dc84a`  
		Last Modified: Tue, 02 Aug 2022 14:03:26 GMT  
		Size: 73.3 MB (73278242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d06c0f29101913e5f40d7fc33f4c270f9b4ef2279944a5308711d28664e4fca`  
		Last Modified: Tue, 02 Aug 2022 14:03:14 GMT  
		Size: 271.8 KB (271834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469a75f80a7f31bd5d819c55b008a36b5ac2069f8fa30f2cc7ea08afa5525a34`  
		Last Modified: Tue, 02 Aug 2022 14:03:14 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bc9b7ea12109f91d10341166fd078867c43304721c1f6a88e0c9e5de0f8dce`  
		Last Modified: Tue, 02 Aug 2022 14:03:19 GMT  
		Size: 22.1 MB (22132816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e2f251f1be18e9fb2b6db36330a52f23588ca3fe197df909d52e01bbaf7ed2`  
		Last Modified: Tue, 02 Aug 2022 14:03:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b47309acdec21a52ec827e96d46c35254586a1424edd6f99a7f158f7a329f2`  
		Last Modified: Tue, 02 Aug 2022 14:03:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957e5c11db36799f600e24665cd1af78a91ec3c7aaf994390b56441ca3ad91d5`  
		Last Modified: Tue, 02 Aug 2022 14:04:00 GMT  
		Size: 78.7 MB (78703374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14e3868dbd8a3c44c7419b1384ebe2dbc7f455a0d433a11230334d736eed6a8`  
		Last Modified: Tue, 02 Aug 2022 14:03:43 GMT  
		Size: 16.5 MB (16463831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c634d47e9ca1f1b831cc123df1c366c3e694c0eaa33d27e57e988278f5c72a8b`  
		Last Modified: Tue, 02 Aug 2022 14:03:39 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:703a9eac69888790c5e9f9b0ad8b2fe7c4212aefb8f87b468de8dfa49b46c55d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317344219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba234e3a95450c339cd2fb32a7fe82c0b586bcd441cb1568fb85614cea506395`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:24:13 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 15:25:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:25:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:25:07 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:25:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:25:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:26:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:26:16 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:26:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:26:20 GMT
ENV ROS1_DISTRO=noetic
# Tue, 02 Aug 2022 15:26:21 GMT
ENV ROS2_DISTRO=galactic
# Tue, 02 Aug 2022 15:26:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:07 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec24629b846176e31ddaaf8b24b1ddfa5c013c36a5adc644cc1ea9cbfaf1f0d`  
		Last Modified: Tue, 02 Aug 2022 15:48:08 GMT  
		Size: 100.3 MB (100301595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6c32d186e05482bc0d52ca6d3348f8f2135fe0ce5cb80694cbf0c402904ab`  
		Last Modified: Tue, 02 Aug 2022 15:47:51 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f1bc7aab31ae221d1d0a204692f57529cc52be37d783e9408e6091c9140e30`  
		Last Modified: Tue, 02 Aug 2022 15:48:30 GMT  
		Size: 67.4 MB (67403003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8728db5450b6ae980d219774ae0acd473093c7203a814add3754b37fa58d2f16`  
		Last Modified: Tue, 02 Aug 2022 15:48:20 GMT  
		Size: 271.8 KB (271758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b3c45ed46817bdd81a5f97bc0ac2f937e60aba727035f3fda0c52b1e8d3766`  
		Last Modified: Tue, 02 Aug 2022 15:48:20 GMT  
		Size: 2.2 KB (2208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb12350bd7ee355d38d341f83cd1fc612133c69ea151b66e1784eeb2e27e4a4`  
		Last Modified: Tue, 02 Aug 2022 15:48:23 GMT  
		Size: 21.5 MB (21453253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88423f93f307272d4821bff3ed3a92da165133eeda2d669662750e2653e243c7`  
		Last Modified: Tue, 02 Aug 2022 15:48:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bf2097533a80b1e6a12df87577fe260936fdbfc07806dee784658e7e11a32d`  
		Last Modified: Tue, 02 Aug 2022 15:49:01 GMT  
		Size: 78.4 MB (78449708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a9110e723a98854f8a59ac27a6fb2d57d6f09837880d7ed1362ac4b6c1329b`  
		Last Modified: Tue, 02 Aug 2022 15:48:49 GMT  
		Size: 15.8 MB (15761670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3349b8ec1b44856e85ff8fbf4aebd2b687e480b88d9b9b84574936a10cb12c03`  
		Last Modified: Tue, 02 Aug 2022 15:48:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros1-bridge-focal`

```console
$ docker pull ros@sha256:35fe74bb930498b5920bf9a469591481e79a4f23388acd977e47ba81dda690ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:147cab728b6776ab4f956f0bfd307ac8646af9c61107f93ad54549bee15642cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.0 MB (330039447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0b0f4fbe76b9774aaaff171e8a868d82675e13cc4ae26fd93b3725bc5cd897`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:27:23 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:27:25 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:27:25 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:33:02 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 13:33:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:33:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:33:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:33:45 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:34:07 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:34:12 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:34:14 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:34:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:34:39 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 13:34:40 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:34:40 GMT
ENV ROS1_DISTRO=noetic
# Tue, 02 Aug 2022 13:34:40 GMT
ENV ROS2_DISTRO=galactic
# Tue, 02 Aug 2022 13:35:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:17 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7922b843c9985c018b28399cfe7cdf458b105aa857166116387fb59aea69773e`  
		Last Modified: Tue, 02 Aug 2022 14:01:16 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7d4dffb56dd34745f4b3d35b10fffeaa9fb9d3e4289645c3f872151b5ee3ae`  
		Last Modified: Tue, 02 Aug 2022 14:01:15 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff5bc0f4410a9a4df17b2ba68d11b669ca1b5bfeb7de939c97e51d05b1b4dae`  
		Last Modified: Tue, 02 Aug 2022 14:03:03 GMT  
		Size: 103.9 MB (103883299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28a0c156e3f431ed899d85555fd6240ce1d49f9a40e54350b529a495823808f`  
		Last Modified: Tue, 02 Aug 2022 14:02:37 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba2bd50d7d05880919f8f6a90f132ff76c104c3edea5258199b2387889dc84a`  
		Last Modified: Tue, 02 Aug 2022 14:03:26 GMT  
		Size: 73.3 MB (73278242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d06c0f29101913e5f40d7fc33f4c270f9b4ef2279944a5308711d28664e4fca`  
		Last Modified: Tue, 02 Aug 2022 14:03:14 GMT  
		Size: 271.8 KB (271834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469a75f80a7f31bd5d819c55b008a36b5ac2069f8fa30f2cc7ea08afa5525a34`  
		Last Modified: Tue, 02 Aug 2022 14:03:14 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bc9b7ea12109f91d10341166fd078867c43304721c1f6a88e0c9e5de0f8dce`  
		Last Modified: Tue, 02 Aug 2022 14:03:19 GMT  
		Size: 22.1 MB (22132816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e2f251f1be18e9fb2b6db36330a52f23588ca3fe197df909d52e01bbaf7ed2`  
		Last Modified: Tue, 02 Aug 2022 14:03:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b47309acdec21a52ec827e96d46c35254586a1424edd6f99a7f158f7a329f2`  
		Last Modified: Tue, 02 Aug 2022 14:03:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957e5c11db36799f600e24665cd1af78a91ec3c7aaf994390b56441ca3ad91d5`  
		Last Modified: Tue, 02 Aug 2022 14:04:00 GMT  
		Size: 78.7 MB (78703374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14e3868dbd8a3c44c7419b1384ebe2dbc7f455a0d433a11230334d736eed6a8`  
		Last Modified: Tue, 02 Aug 2022 14:03:43 GMT  
		Size: 16.5 MB (16463831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c634d47e9ca1f1b831cc123df1c366c3e694c0eaa33d27e57e988278f5c72a8b`  
		Last Modified: Tue, 02 Aug 2022 14:03:39 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:703a9eac69888790c5e9f9b0ad8b2fe7c4212aefb8f87b468de8dfa49b46c55d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317344219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba234e3a95450c339cd2fb32a7fe82c0b586bcd441cb1568fb85614cea506395`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:24:13 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 15:25:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:25:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:25:07 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:25:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:25:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:26:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:26:16 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:26:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:26:20 GMT
ENV ROS1_DISTRO=noetic
# Tue, 02 Aug 2022 15:26:21 GMT
ENV ROS2_DISTRO=galactic
# Tue, 02 Aug 2022 15:26:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:07 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec24629b846176e31ddaaf8b24b1ddfa5c013c36a5adc644cc1ea9cbfaf1f0d`  
		Last Modified: Tue, 02 Aug 2022 15:48:08 GMT  
		Size: 100.3 MB (100301595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6c32d186e05482bc0d52ca6d3348f8f2135fe0ce5cb80694cbf0c402904ab`  
		Last Modified: Tue, 02 Aug 2022 15:47:51 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f1bc7aab31ae221d1d0a204692f57529cc52be37d783e9408e6091c9140e30`  
		Last Modified: Tue, 02 Aug 2022 15:48:30 GMT  
		Size: 67.4 MB (67403003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8728db5450b6ae980d219774ae0acd473093c7203a814add3754b37fa58d2f16`  
		Last Modified: Tue, 02 Aug 2022 15:48:20 GMT  
		Size: 271.8 KB (271758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b3c45ed46817bdd81a5f97bc0ac2f937e60aba727035f3fda0c52b1e8d3766`  
		Last Modified: Tue, 02 Aug 2022 15:48:20 GMT  
		Size: 2.2 KB (2208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb12350bd7ee355d38d341f83cd1fc612133c69ea151b66e1784eeb2e27e4a4`  
		Last Modified: Tue, 02 Aug 2022 15:48:23 GMT  
		Size: 21.5 MB (21453253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88423f93f307272d4821bff3ed3a92da165133eeda2d669662750e2653e243c7`  
		Last Modified: Tue, 02 Aug 2022 15:48:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bf2097533a80b1e6a12df87577fe260936fdbfc07806dee784658e7e11a32d`  
		Last Modified: Tue, 02 Aug 2022 15:49:01 GMT  
		Size: 78.4 MB (78449708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a9110e723a98854f8a59ac27a6fb2d57d6f09837880d7ed1362ac4b6c1329b`  
		Last Modified: Tue, 02 Aug 2022 15:48:49 GMT  
		Size: 15.8 MB (15761670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3349b8ec1b44856e85ff8fbf4aebd2b687e480b88d9b9b84574936a10cb12c03`  
		Last Modified: Tue, 02 Aug 2022 15:48:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble`

```console
$ docker pull ros@sha256:cf52e93f9bbee5864f83052672561fb0f6dc54f027bbd68c8aae2635de39ca49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:e3f310e9de945ad756d03d0f2609e5ed8415bca86c08f6e57e65d23da982795d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262753999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb33e15a008f880229bac48f5056f5dbb3d3764ef55c0801a7880138e76a9f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:35:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:57 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:35:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 13:37:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:37:39 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:37:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:37:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:38:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:38:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:38:48 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:39:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5bfc5848603bd668295b5a975d71c189291f87f6598cf6dc5205c57efdc41f`  
		Last Modified: Tue, 02 Aug 2022 14:04:13 GMT  
		Size: 1.2 MB (1192245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c425ff1dadf43c340925189568bc8f392e60eec7d53b401bb72a710aa66135c`  
		Last Modified: Tue, 02 Aug 2022 14:04:11 GMT  
		Size: 3.8 MB (3827758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eae6de5e53443906b64a12ebc086b149ea851be37c5c514c6a4b7d1446ac6e`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b619038cdfe7b8c10e6820e8ebbfc5b3ab2e7bff0008f9498e10f48a3948ca`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b149af5857de5b95b05668990bef7749088ee5e72afac8e34e07edb55b26f2`  
		Last Modified: Tue, 02 Aug 2022 14:04:35 GMT  
		Size: 106.2 MB (106164552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292f52350cdcdfef6bb772303448c6d04258cef179310be8711a9b3f13cc4dad`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030d5567e60848fa47d516eccb165a83b9ba0e3ff50df104d90de5f4d8c1f540`  
		Last Modified: Tue, 02 Aug 2022 14:05:00 GMT  
		Size: 97.8 MB (97848680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123c6566c81129cd717b77b7656fdff7655520e8d6ca726554e3617f9926872a`  
		Last Modified: Tue, 02 Aug 2022 14:04:45 GMT  
		Size: 283.0 KB (283034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18091009f452ed85ae96624f6d932f8350ecafdedda1cc70e3d7ef55a044460`  
		Last Modified: Tue, 02 Aug 2022 14:04:46 GMT  
		Size: 2.2 KB (2249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388e81439f28e9eb3612a6c4f5d7c3f4538cb052e151c5017a4b507a1174d4ea`  
		Last Modified: Tue, 02 Aug 2022 14:04:50 GMT  
		Size: 23.0 MB (23006931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:acdf5cdb5849df6e1eae707a9d59dea052812be1d5941cdc23b5773fdbcf6657
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254989878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2561d52df82b07ddd78498fcf61efa619edf34b086a4ab5b50afb4e72d0ea9ed`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:27:39 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 15:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:28:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:28:31 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:29:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:29:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:29:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:29:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05fa5a00264cd775880db77d90a3ef55262e9fca2af5ce9b5829e8732057281`  
		Last Modified: Tue, 02 Aug 2022 15:49:30 GMT  
		Size: 103.9 MB (103889367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f851cc59237e6d46b391e74e170d98dfee8e2a0f1eeb69881e3ff47f20020f1e`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268f426f25631919b3a5f6d171d25f0b1c7eed19c2ff10805bfb5e2fd8acc246`  
		Last Modified: Tue, 02 Aug 2022 15:49:56 GMT  
		Size: 95.2 MB (95214628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c810faa1690af68f54ea46e1bdd750aac3e6e246a835ba0c70f85ce89614db`  
		Last Modified: Tue, 02 Aug 2022 15:49:43 GMT  
		Size: 283.0 KB (282977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5882ceb61cae13eccf9ebd03a7a30ce85f7bc53b71deb8705a7776522e6b03d6`  
		Last Modified: Tue, 02 Aug 2022 15:49:42 GMT  
		Size: 2.2 KB (2241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97be626b88d492edf0ca4cd8e116114811578dd05aea521639f25ccccdb848ad`  
		Last Modified: Tue, 02 Aug 2022 15:49:46 GMT  
		Size: 22.4 MB (22427651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception`

```console
$ docker pull ros@sha256:751e941a65c4deffee4c04c0c2add5006cd50d0a6a04396a2d9d4e779f9e3c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:1140315bd15e40bc9ffc0565c8d53175beaf5bfa24bf25ec8d09784399a944d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1086568827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a0ace6c3ceb5c9a6fcd3b781d39d498119eaca4b0fcef6192ba157d33edc53`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:35:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:57 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:35:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 13:37:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:37:39 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:37:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:37:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:38:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:38:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:38:48 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:39:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:47:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5bfc5848603bd668295b5a975d71c189291f87f6598cf6dc5205c57efdc41f`  
		Last Modified: Tue, 02 Aug 2022 14:04:13 GMT  
		Size: 1.2 MB (1192245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c425ff1dadf43c340925189568bc8f392e60eec7d53b401bb72a710aa66135c`  
		Last Modified: Tue, 02 Aug 2022 14:04:11 GMT  
		Size: 3.8 MB (3827758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eae6de5e53443906b64a12ebc086b149ea851be37c5c514c6a4b7d1446ac6e`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b619038cdfe7b8c10e6820e8ebbfc5b3ab2e7bff0008f9498e10f48a3948ca`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b149af5857de5b95b05668990bef7749088ee5e72afac8e34e07edb55b26f2`  
		Last Modified: Tue, 02 Aug 2022 14:04:35 GMT  
		Size: 106.2 MB (106164552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292f52350cdcdfef6bb772303448c6d04258cef179310be8711a9b3f13cc4dad`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030d5567e60848fa47d516eccb165a83b9ba0e3ff50df104d90de5f4d8c1f540`  
		Last Modified: Tue, 02 Aug 2022 14:05:00 GMT  
		Size: 97.8 MB (97848680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123c6566c81129cd717b77b7656fdff7655520e8d6ca726554e3617f9926872a`  
		Last Modified: Tue, 02 Aug 2022 14:04:45 GMT  
		Size: 283.0 KB (283034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18091009f452ed85ae96624f6d932f8350ecafdedda1cc70e3d7ef55a044460`  
		Last Modified: Tue, 02 Aug 2022 14:04:46 GMT  
		Size: 2.2 KB (2249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388e81439f28e9eb3612a6c4f5d7c3f4538cb052e151c5017a4b507a1174d4ea`  
		Last Modified: Tue, 02 Aug 2022 14:04:50 GMT  
		Size: 23.0 MB (23006931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400e7013c241689097f8df1159db9317a7aaa68c6a2798340cad47ea5a69cc49`  
		Last Modified: Tue, 02 Aug 2022 14:07:11 GMT  
		Size: 823.8 MB (823814828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:76edca30f7e1ef03392a3f02356d1ebdedc6fea03edf5b1e350ab5fb49312d5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1034227178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7917f192cc7d1bb83f4d903e2ba00b8edd6a3bfd6807f9e0e22e804008f2d6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:27:39 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 15:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:28:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:28:31 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:29:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:29:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:29:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:29:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:32:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05fa5a00264cd775880db77d90a3ef55262e9fca2af5ce9b5829e8732057281`  
		Last Modified: Tue, 02 Aug 2022 15:49:30 GMT  
		Size: 103.9 MB (103889367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f851cc59237e6d46b391e74e170d98dfee8e2a0f1eeb69881e3ff47f20020f1e`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268f426f25631919b3a5f6d171d25f0b1c7eed19c2ff10805bfb5e2fd8acc246`  
		Last Modified: Tue, 02 Aug 2022 15:49:56 GMT  
		Size: 95.2 MB (95214628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c810faa1690af68f54ea46e1bdd750aac3e6e246a835ba0c70f85ce89614db`  
		Last Modified: Tue, 02 Aug 2022 15:49:43 GMT  
		Size: 283.0 KB (282977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5882ceb61cae13eccf9ebd03a7a30ce85f7bc53b71deb8705a7776522e6b03d6`  
		Last Modified: Tue, 02 Aug 2022 15:49:42 GMT  
		Size: 2.2 KB (2241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97be626b88d492edf0ca4cd8e116114811578dd05aea521639f25ccccdb848ad`  
		Last Modified: Tue, 02 Aug 2022 15:49:46 GMT  
		Size: 22.4 MB (22427651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa124ac25d3a1a83ea306f40bce0401e51ccb7cb7df5d46a4434747b1685c1d`  
		Last Modified: Tue, 02 Aug 2022 15:51:52 GMT  
		Size: 779.2 MB (779237300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:751e941a65c4deffee4c04c0c2add5006cd50d0a6a04396a2d9d4e779f9e3c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:1140315bd15e40bc9ffc0565c8d53175beaf5bfa24bf25ec8d09784399a944d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1086568827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a0ace6c3ceb5c9a6fcd3b781d39d498119eaca4b0fcef6192ba157d33edc53`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:35:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:57 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:35:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 13:37:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:37:39 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:37:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:37:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:38:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:38:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:38:48 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:39:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:47:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5bfc5848603bd668295b5a975d71c189291f87f6598cf6dc5205c57efdc41f`  
		Last Modified: Tue, 02 Aug 2022 14:04:13 GMT  
		Size: 1.2 MB (1192245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c425ff1dadf43c340925189568bc8f392e60eec7d53b401bb72a710aa66135c`  
		Last Modified: Tue, 02 Aug 2022 14:04:11 GMT  
		Size: 3.8 MB (3827758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eae6de5e53443906b64a12ebc086b149ea851be37c5c514c6a4b7d1446ac6e`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b619038cdfe7b8c10e6820e8ebbfc5b3ab2e7bff0008f9498e10f48a3948ca`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b149af5857de5b95b05668990bef7749088ee5e72afac8e34e07edb55b26f2`  
		Last Modified: Tue, 02 Aug 2022 14:04:35 GMT  
		Size: 106.2 MB (106164552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292f52350cdcdfef6bb772303448c6d04258cef179310be8711a9b3f13cc4dad`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030d5567e60848fa47d516eccb165a83b9ba0e3ff50df104d90de5f4d8c1f540`  
		Last Modified: Tue, 02 Aug 2022 14:05:00 GMT  
		Size: 97.8 MB (97848680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123c6566c81129cd717b77b7656fdff7655520e8d6ca726554e3617f9926872a`  
		Last Modified: Tue, 02 Aug 2022 14:04:45 GMT  
		Size: 283.0 KB (283034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18091009f452ed85ae96624f6d932f8350ecafdedda1cc70e3d7ef55a044460`  
		Last Modified: Tue, 02 Aug 2022 14:04:46 GMT  
		Size: 2.2 KB (2249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388e81439f28e9eb3612a6c4f5d7c3f4538cb052e151c5017a4b507a1174d4ea`  
		Last Modified: Tue, 02 Aug 2022 14:04:50 GMT  
		Size: 23.0 MB (23006931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400e7013c241689097f8df1159db9317a7aaa68c6a2798340cad47ea5a69cc49`  
		Last Modified: Tue, 02 Aug 2022 14:07:11 GMT  
		Size: 823.8 MB (823814828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:76edca30f7e1ef03392a3f02356d1ebdedc6fea03edf5b1e350ab5fb49312d5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1034227178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7917f192cc7d1bb83f4d903e2ba00b8edd6a3bfd6807f9e0e22e804008f2d6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:27:39 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 15:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:28:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:28:31 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:29:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:29:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:29:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:29:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:32:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05fa5a00264cd775880db77d90a3ef55262e9fca2af5ce9b5829e8732057281`  
		Last Modified: Tue, 02 Aug 2022 15:49:30 GMT  
		Size: 103.9 MB (103889367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f851cc59237e6d46b391e74e170d98dfee8e2a0f1eeb69881e3ff47f20020f1e`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268f426f25631919b3a5f6d171d25f0b1c7eed19c2ff10805bfb5e2fd8acc246`  
		Last Modified: Tue, 02 Aug 2022 15:49:56 GMT  
		Size: 95.2 MB (95214628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c810faa1690af68f54ea46e1bdd750aac3e6e246a835ba0c70f85ce89614db`  
		Last Modified: Tue, 02 Aug 2022 15:49:43 GMT  
		Size: 283.0 KB (282977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5882ceb61cae13eccf9ebd03a7a30ce85f7bc53b71deb8705a7776522e6b03d6`  
		Last Modified: Tue, 02 Aug 2022 15:49:42 GMT  
		Size: 2.2 KB (2241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97be626b88d492edf0ca4cd8e116114811578dd05aea521639f25ccccdb848ad`  
		Last Modified: Tue, 02 Aug 2022 15:49:46 GMT  
		Size: 22.4 MB (22427651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa124ac25d3a1a83ea306f40bce0401e51ccb7cb7df5d46a4434747b1685c1d`  
		Last Modified: Tue, 02 Aug 2022 15:51:52 GMT  
		Size: 779.2 MB (779237300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:cf52e93f9bbee5864f83052672561fb0f6dc54f027bbd68c8aae2635de39ca49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:e3f310e9de945ad756d03d0f2609e5ed8415bca86c08f6e57e65d23da982795d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262753999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb33e15a008f880229bac48f5056f5dbb3d3764ef55c0801a7880138e76a9f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:35:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:57 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:35:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 13:37:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:37:39 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:37:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:37:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:38:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:38:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:38:48 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:39:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5bfc5848603bd668295b5a975d71c189291f87f6598cf6dc5205c57efdc41f`  
		Last Modified: Tue, 02 Aug 2022 14:04:13 GMT  
		Size: 1.2 MB (1192245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c425ff1dadf43c340925189568bc8f392e60eec7d53b401bb72a710aa66135c`  
		Last Modified: Tue, 02 Aug 2022 14:04:11 GMT  
		Size: 3.8 MB (3827758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eae6de5e53443906b64a12ebc086b149ea851be37c5c514c6a4b7d1446ac6e`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b619038cdfe7b8c10e6820e8ebbfc5b3ab2e7bff0008f9498e10f48a3948ca`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b149af5857de5b95b05668990bef7749088ee5e72afac8e34e07edb55b26f2`  
		Last Modified: Tue, 02 Aug 2022 14:04:35 GMT  
		Size: 106.2 MB (106164552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292f52350cdcdfef6bb772303448c6d04258cef179310be8711a9b3f13cc4dad`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030d5567e60848fa47d516eccb165a83b9ba0e3ff50df104d90de5f4d8c1f540`  
		Last Modified: Tue, 02 Aug 2022 14:05:00 GMT  
		Size: 97.8 MB (97848680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123c6566c81129cd717b77b7656fdff7655520e8d6ca726554e3617f9926872a`  
		Last Modified: Tue, 02 Aug 2022 14:04:45 GMT  
		Size: 283.0 KB (283034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18091009f452ed85ae96624f6d932f8350ecafdedda1cc70e3d7ef55a044460`  
		Last Modified: Tue, 02 Aug 2022 14:04:46 GMT  
		Size: 2.2 KB (2249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388e81439f28e9eb3612a6c4f5d7c3f4538cb052e151c5017a4b507a1174d4ea`  
		Last Modified: Tue, 02 Aug 2022 14:04:50 GMT  
		Size: 23.0 MB (23006931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:acdf5cdb5849df6e1eae707a9d59dea052812be1d5941cdc23b5773fdbcf6657
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254989878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2561d52df82b07ddd78498fcf61efa619edf34b086a4ab5b50afb4e72d0ea9ed`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:27:39 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 15:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:28:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:28:31 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:29:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:29:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:29:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:29:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05fa5a00264cd775880db77d90a3ef55262e9fca2af5ce9b5829e8732057281`  
		Last Modified: Tue, 02 Aug 2022 15:49:30 GMT  
		Size: 103.9 MB (103889367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f851cc59237e6d46b391e74e170d98dfee8e2a0f1eeb69881e3ff47f20020f1e`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268f426f25631919b3a5f6d171d25f0b1c7eed19c2ff10805bfb5e2fd8acc246`  
		Last Modified: Tue, 02 Aug 2022 15:49:56 GMT  
		Size: 95.2 MB (95214628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c810faa1690af68f54ea46e1bdd750aac3e6e246a835ba0c70f85ce89614db`  
		Last Modified: Tue, 02 Aug 2022 15:49:43 GMT  
		Size: 283.0 KB (282977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5882ceb61cae13eccf9ebd03a7a30ce85f7bc53b71deb8705a7776522e6b03d6`  
		Last Modified: Tue, 02 Aug 2022 15:49:42 GMT  
		Size: 2.2 KB (2241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97be626b88d492edf0ca4cd8e116114811578dd05aea521639f25ccccdb848ad`  
		Last Modified: Tue, 02 Aug 2022 15:49:46 GMT  
		Size: 22.4 MB (22427651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:cf52e93f9bbee5864f83052672561fb0f6dc54f027bbd68c8aae2635de39ca49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:e3f310e9de945ad756d03d0f2609e5ed8415bca86c08f6e57e65d23da982795d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262753999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb33e15a008f880229bac48f5056f5dbb3d3764ef55c0801a7880138e76a9f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:35:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:57 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:35:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 13:37:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:37:39 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:37:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:37:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:38:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:38:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:38:48 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:39:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5bfc5848603bd668295b5a975d71c189291f87f6598cf6dc5205c57efdc41f`  
		Last Modified: Tue, 02 Aug 2022 14:04:13 GMT  
		Size: 1.2 MB (1192245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c425ff1dadf43c340925189568bc8f392e60eec7d53b401bb72a710aa66135c`  
		Last Modified: Tue, 02 Aug 2022 14:04:11 GMT  
		Size: 3.8 MB (3827758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eae6de5e53443906b64a12ebc086b149ea851be37c5c514c6a4b7d1446ac6e`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b619038cdfe7b8c10e6820e8ebbfc5b3ab2e7bff0008f9498e10f48a3948ca`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b149af5857de5b95b05668990bef7749088ee5e72afac8e34e07edb55b26f2`  
		Last Modified: Tue, 02 Aug 2022 14:04:35 GMT  
		Size: 106.2 MB (106164552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292f52350cdcdfef6bb772303448c6d04258cef179310be8711a9b3f13cc4dad`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030d5567e60848fa47d516eccb165a83b9ba0e3ff50df104d90de5f4d8c1f540`  
		Last Modified: Tue, 02 Aug 2022 14:05:00 GMT  
		Size: 97.8 MB (97848680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123c6566c81129cd717b77b7656fdff7655520e8d6ca726554e3617f9926872a`  
		Last Modified: Tue, 02 Aug 2022 14:04:45 GMT  
		Size: 283.0 KB (283034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18091009f452ed85ae96624f6d932f8350ecafdedda1cc70e3d7ef55a044460`  
		Last Modified: Tue, 02 Aug 2022 14:04:46 GMT  
		Size: 2.2 KB (2249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388e81439f28e9eb3612a6c4f5d7c3f4538cb052e151c5017a4b507a1174d4ea`  
		Last Modified: Tue, 02 Aug 2022 14:04:50 GMT  
		Size: 23.0 MB (23006931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:acdf5cdb5849df6e1eae707a9d59dea052812be1d5941cdc23b5773fdbcf6657
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254989878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2561d52df82b07ddd78498fcf61efa619edf34b086a4ab5b50afb4e72d0ea9ed`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:27:39 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 15:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:28:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:28:31 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:29:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:29:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:29:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:29:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05fa5a00264cd775880db77d90a3ef55262e9fca2af5ce9b5829e8732057281`  
		Last Modified: Tue, 02 Aug 2022 15:49:30 GMT  
		Size: 103.9 MB (103889367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f851cc59237e6d46b391e74e170d98dfee8e2a0f1eeb69881e3ff47f20020f1e`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268f426f25631919b3a5f6d171d25f0b1c7eed19c2ff10805bfb5e2fd8acc246`  
		Last Modified: Tue, 02 Aug 2022 15:49:56 GMT  
		Size: 95.2 MB (95214628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c810faa1690af68f54ea46e1bdd750aac3e6e246a835ba0c70f85ce89614db`  
		Last Modified: Tue, 02 Aug 2022 15:49:43 GMT  
		Size: 283.0 KB (282977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5882ceb61cae13eccf9ebd03a7a30ce85f7bc53b71deb8705a7776522e6b03d6`  
		Last Modified: Tue, 02 Aug 2022 15:49:42 GMT  
		Size: 2.2 KB (2241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97be626b88d492edf0ca4cd8e116114811578dd05aea521639f25ccccdb848ad`  
		Last Modified: Tue, 02 Aug 2022 15:49:46 GMT  
		Size: 22.4 MB (22427651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:47cc5b39d0640626ed0fa4ee4988745d7330e0b46917f46d86c7a1defee5652d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:dccc7fca137da15eaca40717d4e6dd3c6309038e5d65516f472a88b5158122b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141613105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbceb707c80c255506109853fae5477fbf8f65dba1dc683325fe73d9ebfdb3d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:35:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:57 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:35:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 13:37:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:37:39 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:37:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:37:39 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5bfc5848603bd668295b5a975d71c189291f87f6598cf6dc5205c57efdc41f`  
		Last Modified: Tue, 02 Aug 2022 14:04:13 GMT  
		Size: 1.2 MB (1192245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c425ff1dadf43c340925189568bc8f392e60eec7d53b401bb72a710aa66135c`  
		Last Modified: Tue, 02 Aug 2022 14:04:11 GMT  
		Size: 3.8 MB (3827758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eae6de5e53443906b64a12ebc086b149ea851be37c5c514c6a4b7d1446ac6e`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b619038cdfe7b8c10e6820e8ebbfc5b3ab2e7bff0008f9498e10f48a3948ca`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b149af5857de5b95b05668990bef7749088ee5e72afac8e34e07edb55b26f2`  
		Last Modified: Tue, 02 Aug 2022 14:04:35 GMT  
		Size: 106.2 MB (106164552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292f52350cdcdfef6bb772303448c6d04258cef179310be8711a9b3f13cc4dad`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:13bf1b82f69a790ce0598ce60a1ab623d7d674831da3ae908b07b894293296e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137062381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a82769945152d9b284ed53731acfa50b3c4d02b968684c2b23e18ba2cde644`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:27:39 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 15:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:28:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:28:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05fa5a00264cd775880db77d90a3ef55262e9fca2af5ce9b5829e8732057281`  
		Last Modified: Tue, 02 Aug 2022 15:49:30 GMT  
		Size: 103.9 MB (103889367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f851cc59237e6d46b391e74e170d98dfee8e2a0f1eeb69881e3ff47f20020f1e`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:47cc5b39d0640626ed0fa4ee4988745d7330e0b46917f46d86c7a1defee5652d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:dccc7fca137da15eaca40717d4e6dd3c6309038e5d65516f472a88b5158122b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141613105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbceb707c80c255506109853fae5477fbf8f65dba1dc683325fe73d9ebfdb3d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:35:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:57 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:35:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 13:37:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:37:39 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:37:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:37:39 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5bfc5848603bd668295b5a975d71c189291f87f6598cf6dc5205c57efdc41f`  
		Last Modified: Tue, 02 Aug 2022 14:04:13 GMT  
		Size: 1.2 MB (1192245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c425ff1dadf43c340925189568bc8f392e60eec7d53b401bb72a710aa66135c`  
		Last Modified: Tue, 02 Aug 2022 14:04:11 GMT  
		Size: 3.8 MB (3827758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eae6de5e53443906b64a12ebc086b149ea851be37c5c514c6a4b7d1446ac6e`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b619038cdfe7b8c10e6820e8ebbfc5b3ab2e7bff0008f9498e10f48a3948ca`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b149af5857de5b95b05668990bef7749088ee5e72afac8e34e07edb55b26f2`  
		Last Modified: Tue, 02 Aug 2022 14:04:35 GMT  
		Size: 106.2 MB (106164552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292f52350cdcdfef6bb772303448c6d04258cef179310be8711a9b3f13cc4dad`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:13bf1b82f69a790ce0598ce60a1ab623d7d674831da3ae908b07b894293296e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137062381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a82769945152d9b284ed53731acfa50b3c4d02b968684c2b23e18ba2cde644`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:27:39 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 15:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:28:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:28:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05fa5a00264cd775880db77d90a3ef55262e9fca2af5ce9b5829e8732057281`  
		Last Modified: Tue, 02 Aug 2022 15:49:30 GMT  
		Size: 103.9 MB (103889367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f851cc59237e6d46b391e74e170d98dfee8e2a0f1eeb69881e3ff47f20020f1e`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:latest`

```console
$ docker pull ros@sha256:cf52e93f9bbee5864f83052672561fb0f6dc54f027bbd68c8aae2635de39ca49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:e3f310e9de945ad756d03d0f2609e5ed8415bca86c08f6e57e65d23da982795d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262753999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb33e15a008f880229bac48f5056f5dbb3d3764ef55c0801a7880138e76a9f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:35:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:57 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:35:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 13:37:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:37:39 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:37:39 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:37:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:38:38 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:38:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:38:48 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:39:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5bfc5848603bd668295b5a975d71c189291f87f6598cf6dc5205c57efdc41f`  
		Last Modified: Tue, 02 Aug 2022 14:04:13 GMT  
		Size: 1.2 MB (1192245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c425ff1dadf43c340925189568bc8f392e60eec7d53b401bb72a710aa66135c`  
		Last Modified: Tue, 02 Aug 2022 14:04:11 GMT  
		Size: 3.8 MB (3827758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eae6de5e53443906b64a12ebc086b149ea851be37c5c514c6a4b7d1446ac6e`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b619038cdfe7b8c10e6820e8ebbfc5b3ab2e7bff0008f9498e10f48a3948ca`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b149af5857de5b95b05668990bef7749088ee5e72afac8e34e07edb55b26f2`  
		Last Modified: Tue, 02 Aug 2022 14:04:35 GMT  
		Size: 106.2 MB (106164552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292f52350cdcdfef6bb772303448c6d04258cef179310be8711a9b3f13cc4dad`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030d5567e60848fa47d516eccb165a83b9ba0e3ff50df104d90de5f4d8c1f540`  
		Last Modified: Tue, 02 Aug 2022 14:05:00 GMT  
		Size: 97.8 MB (97848680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123c6566c81129cd717b77b7656fdff7655520e8d6ca726554e3617f9926872a`  
		Last Modified: Tue, 02 Aug 2022 14:04:45 GMT  
		Size: 283.0 KB (283034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18091009f452ed85ae96624f6d932f8350ecafdedda1cc70e3d7ef55a044460`  
		Last Modified: Tue, 02 Aug 2022 14:04:46 GMT  
		Size: 2.2 KB (2249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388e81439f28e9eb3612a6c4f5d7c3f4538cb052e151c5017a4b507a1174d4ea`  
		Last Modified: Tue, 02 Aug 2022 14:04:50 GMT  
		Size: 23.0 MB (23006931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:acdf5cdb5849df6e1eae707a9d59dea052812be1d5941cdc23b5773fdbcf6657
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254989878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2561d52df82b07ddd78498fcf61efa619edf34b086a4ab5b50afb4e72d0ea9ed`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:27:39 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 15:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:28:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:28:31 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:29:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:29:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:29:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:29:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05fa5a00264cd775880db77d90a3ef55262e9fca2af5ce9b5829e8732057281`  
		Last Modified: Tue, 02 Aug 2022 15:49:30 GMT  
		Size: 103.9 MB (103889367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f851cc59237e6d46b391e74e170d98dfee8e2a0f1eeb69881e3ff47f20020f1e`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268f426f25631919b3a5f6d171d25f0b1c7eed19c2ff10805bfb5e2fd8acc246`  
		Last Modified: Tue, 02 Aug 2022 15:49:56 GMT  
		Size: 95.2 MB (95214628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c810faa1690af68f54ea46e1bdd750aac3e6e246a835ba0c70f85ce89614db`  
		Last Modified: Tue, 02 Aug 2022 15:49:43 GMT  
		Size: 283.0 KB (282977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5882ceb61cae13eccf9ebd03a7a30ce85f7bc53b71deb8705a7776522e6b03d6`  
		Last Modified: Tue, 02 Aug 2022 15:49:42 GMT  
		Size: 2.2 KB (2241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97be626b88d492edf0ca4cd8e116114811578dd05aea521639f25ccccdb848ad`  
		Last Modified: Tue, 02 Aug 2022 15:49:46 GMT  
		Size: 22.4 MB (22427651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic`

```console
$ docker pull ros@sha256:33870f62e883c4205382ec9ff2c2f144f010d3e9101691be15a38ae456eb8ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic` - linux; amd64

```console
$ docker pull ros@sha256:17a8176d6e886bb868eb2fe93712548382781b762f62424ee98a64e194050ae2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 MB (437513102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2864ef7a388d5748aa5fd301591d1925922027f2e8d9189cf76018e5420737c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:57:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:57:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 12:57:48 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 12:57:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 12:57:48 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 12:57:48 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 13:01:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:01:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:01:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:01:53 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:02:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:02:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:04:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa6fbe30fbafa2fd890f1a634056fab84382d475fe85716949a1a44cc77f087`  
		Last Modified: Tue, 02 Aug 2022 13:52:33 GMT  
		Size: 839.1 KB (839126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7d6485ffdcfd34d9790c5e9f1e3deb6f1e01cd88b3ed1c2c4bfd798ce679c6`  
		Last Modified: Tue, 02 Aug 2022 13:52:31 GMT  
		Size: 4.9 MB (4873542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37d651da90ea517b4e41ab1754a0657cd17842014153817571fad7f62a21dd8`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8310f03235adb2a56f2ca99fcd6f4bf9c29d94663f625b160ef3534ffc2630bc`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f613727d0890c231f392123401bfc2194872d710cd8d8a8740db383fc8a599f4`  
		Last Modified: Tue, 02 Aug 2022 13:53:17 GMT  
		Size: 259.6 MB (259551224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ab03995e2e9bff9b259a370e6c30525ec9bc8cb87b98f29e3d3de46a99b36e`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0b7f91cbaa1e44e2ecae278c9b9bcec5d83eb8397cfd098ce9f394ca3642d2`  
		Last Modified: Tue, 02 Aug 2022 13:53:39 GMT  
		Size: 70.3 MB (70259542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e26ed31df7e549f55f79f7b17b78d0ba6d56d1cf0cd9a4f352729bc4be37f67`  
		Last Modified: Tue, 02 Aug 2022 13:53:27 GMT  
		Size: 283.1 KB (283134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99508511f69fc265efef3003c1bd53483ecc3d71f1bf6cdb319a64a2946042b0`  
		Last Modified: Tue, 02 Aug 2022 13:53:43 GMT  
		Size: 75.0 MB (74994419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm variant v7

```console
$ docker pull ros@sha256:8e3ceed077fce82a58f61e42dcf7ffcdf1ac40b9cdd7aec02ab53741f70290b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.1 MB (386058530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69498dc4a9cdd7010aeadee61ff767774c6d805477a3a6d8e29f3f5118e3b251`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:28 GMT
ADD file:d6d276f8f40c095bc2411f4d370eb87f8042a092ebb5bb0076863b2b6182b34f in / 
# Tue, 07 Jun 2022 05:50:29 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:07:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:07:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:07:56 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 10:07:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 10:07:59 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 10:07:59 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 10:08:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 07 Jun 2022 10:11:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 22:58:15 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 22:58:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 22:58:16 GMT
CMD ["bash"]
# Mon, 11 Jul 2022 22:59:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 22:59:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 11 Jul 2022 23:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9242055bc3f039f3566a5154c8b1a602652bfe444e9b4291817caae906444e75`  
		Last Modified: Tue, 07 Jun 2022 05:54:37 GMT  
		Size: 22.3 MB (22306284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddc7f6bb12de3f6e55c81fc14d7ebc77e5e7612bd09a2770d4cf1feae55f3d6`  
		Last Modified: Tue, 07 Jun 2022 10:32:01 GMT  
		Size: 840.2 KB (840219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc3e315dd2fd37157023b5350340af87fe236f4bcd29db3284eb3e86c37c85`  
		Last Modified: Tue, 07 Jun 2022 10:32:00 GMT  
		Size: 4.1 MB (4089918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b851bde5be9d93cd5bf76737b14ccdf776ace9a4d8ed7b1e11b042c22452a1`  
		Last Modified: Tue, 07 Jun 2022 10:31:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883aed8a39d8c90c486aec03c1809aa36c891e812219cf617b59ece7f9165291`  
		Last Modified: Tue, 07 Jun 2022 10:31:58 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd559c545cdb93ee204c62144d4375db3f0450040d3ef61a8ac599ffb1f043a1`  
		Last Modified: Tue, 07 Jun 2022 10:34:31 GMT  
		Size: 238.9 MB (238943066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6affb1b3206339bc5b43342d1c9945b174998df8674effb3cfb95da2c03bd8f9`  
		Last Modified: Mon, 11 Jul 2022 23:15:06 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03108c0184ca678f48226bd3277b4d8468a25b0016664e2d80eb4c968264856f`  
		Last Modified: Mon, 11 Jul 2022 23:15:47 GMT  
		Size: 54.8 MB (54848442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67520f2af1ef3aca6f8a6fa40d040de75a19438828ea7962a63fb9846b807b4`  
		Last Modified: Mon, 11 Jul 2022 23:15:18 GMT  
		Size: 282.4 KB (282374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4114dbccc760d1e5c5ac46a04ddf9364e3769d0e596ad434cee93f0188f5ce`  
		Last Modified: Mon, 11 Jul 2022 23:16:02 GMT  
		Size: 64.7 MB (64746381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e19db181648b571c1a017e730f52145de920147e64052fa8662b7f611ac707db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 MB (411718282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56b623ecaac63fef2cd569acd1b109d44ce4a7318e7d3bda7b0c6d1e2ab1334`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:03:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:03:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:03:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:03:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:03:41 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 15:05:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:05:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:05:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:05:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:06:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c7d887e7b961ba6c9db72dd6419c5ac455dd43d49b194dbc43680f849a6ef`  
		Last Modified: Tue, 02 Aug 2022 15:38:49 GMT  
		Size: 839.8 KB (839769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51fe758bc1275edfa803da680fe43894a9e4bdb69d83153ccca2d60ba34bbee`  
		Last Modified: Tue, 02 Aug 2022 15:38:47 GMT  
		Size: 4.3 MB (4265854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646eaa84fc50bf88a2bca0599491e795cf8122e6fe16671e23fd8b87804e823`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ce991e1d0bf36ab7c0c7db9323c2cc620b0d96c88f26c619287aee7598666`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101d7b97c7577b747e3cc14cb64c408587e6489c4b2420aad7fa1dbbd8fe189`  
		Last Modified: Tue, 02 Aug 2022 15:39:22 GMT  
		Size: 252.5 MB (252503681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716f26c3c2a680d90778a974e99dc5d04bf9e4fbd9077cdb619b311ff4f0d24`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b66bed859b212ff9f65c306618bc607825b531e9a79843b4d75f5e870b3195`  
		Last Modified: Tue, 02 Aug 2022 15:39:42 GMT  
		Size: 63.1 MB (63088414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee909ec215bcdf8f5cd2e47e3aaf397ef01b2695fd292ea49920505e539f80c9`  
		Last Modified: Tue, 02 Aug 2022 15:39:34 GMT  
		Size: 283.1 KB (283086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884a1a0922cfe088904523812cfa7b3897bc3fc1b7eb0f266e99c75d92662a17`  
		Last Modified: Tue, 02 Aug 2022 15:39:44 GMT  
		Size: 67.0 MB (67000963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-perception`

```console
$ docker pull ros@sha256:6209755aeb4e6ecd3cc0c0beb2b8fe93a015cbd9d3045ef2c201ca8ed976d2c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-perception` - linux; amd64

```console
$ docker pull ros@sha256:1f3b5df15ca60854de07682acabeb1009d55f56e7c7c0c19a41c5de9414b998f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.9 MB (742862325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab661038b8793b0427db56fe85f40e9b8d3b7aabbc82acae7e564c4636d4bae4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:57:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:57:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 12:57:48 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 12:57:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 12:57:48 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 12:57:48 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 13:01:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:01:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:01:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:01:53 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:02:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:02:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:04:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:09:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa6fbe30fbafa2fd890f1a634056fab84382d475fe85716949a1a44cc77f087`  
		Last Modified: Tue, 02 Aug 2022 13:52:33 GMT  
		Size: 839.1 KB (839126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7d6485ffdcfd34d9790c5e9f1e3deb6f1e01cd88b3ed1c2c4bfd798ce679c6`  
		Last Modified: Tue, 02 Aug 2022 13:52:31 GMT  
		Size: 4.9 MB (4873542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37d651da90ea517b4e41ab1754a0657cd17842014153817571fad7f62a21dd8`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8310f03235adb2a56f2ca99fcd6f4bf9c29d94663f625b160ef3534ffc2630bc`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f613727d0890c231f392123401bfc2194872d710cd8d8a8740db383fc8a599f4`  
		Last Modified: Tue, 02 Aug 2022 13:53:17 GMT  
		Size: 259.6 MB (259551224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ab03995e2e9bff9b259a370e6c30525ec9bc8cb87b98f29e3d3de46a99b36e`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0b7f91cbaa1e44e2ecae278c9b9bcec5d83eb8397cfd098ce9f394ca3642d2`  
		Last Modified: Tue, 02 Aug 2022 13:53:39 GMT  
		Size: 70.3 MB (70259542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e26ed31df7e549f55f79f7b17b78d0ba6d56d1cf0cd9a4f352729bc4be37f67`  
		Last Modified: Tue, 02 Aug 2022 13:53:27 GMT  
		Size: 283.1 KB (283134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99508511f69fc265efef3003c1bd53483ecc3d71f1bf6cdb319a64a2946042b0`  
		Last Modified: Tue, 02 Aug 2022 13:53:43 GMT  
		Size: 75.0 MB (74994419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a211461bcd28ecb3940dd7933e121068c7354be96bdda5dcef0b8a696b94b4`  
		Last Modified: Tue, 02 Aug 2022 13:55:04 GMT  
		Size: 305.3 MB (305349223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:d2a42b42115bd5254ae8170cfffe5dc793ec369a01f1345386165297648619f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.1 MB (646104096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd38e8b455233463eb77566608108e092bbccefec5186f0e291dcef643cfe26`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:28 GMT
ADD file:d6d276f8f40c095bc2411f4d370eb87f8042a092ebb5bb0076863b2b6182b34f in / 
# Tue, 07 Jun 2022 05:50:29 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:07:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:07:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:07:56 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 10:07:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 10:07:59 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 10:07:59 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 10:08:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 07 Jun 2022 10:11:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 22:58:15 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 22:58:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 22:58:16 GMT
CMD ["bash"]
# Mon, 11 Jul 2022 22:59:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 22:59:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 11 Jul 2022 23:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:05:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9242055bc3f039f3566a5154c8b1a602652bfe444e9b4291817caae906444e75`  
		Last Modified: Tue, 07 Jun 2022 05:54:37 GMT  
		Size: 22.3 MB (22306284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddc7f6bb12de3f6e55c81fc14d7ebc77e5e7612bd09a2770d4cf1feae55f3d6`  
		Last Modified: Tue, 07 Jun 2022 10:32:01 GMT  
		Size: 840.2 KB (840219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc3e315dd2fd37157023b5350340af87fe236f4bcd29db3284eb3e86c37c85`  
		Last Modified: Tue, 07 Jun 2022 10:32:00 GMT  
		Size: 4.1 MB (4089918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b851bde5be9d93cd5bf76737b14ccdf776ace9a4d8ed7b1e11b042c22452a1`  
		Last Modified: Tue, 07 Jun 2022 10:31:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883aed8a39d8c90c486aec03c1809aa36c891e812219cf617b59ece7f9165291`  
		Last Modified: Tue, 07 Jun 2022 10:31:58 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd559c545cdb93ee204c62144d4375db3f0450040d3ef61a8ac599ffb1f043a1`  
		Last Modified: Tue, 07 Jun 2022 10:34:31 GMT  
		Size: 238.9 MB (238943066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6affb1b3206339bc5b43342d1c9945b174998df8674effb3cfb95da2c03bd8f9`  
		Last Modified: Mon, 11 Jul 2022 23:15:06 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03108c0184ca678f48226bd3277b4d8468a25b0016664e2d80eb4c968264856f`  
		Last Modified: Mon, 11 Jul 2022 23:15:47 GMT  
		Size: 54.8 MB (54848442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67520f2af1ef3aca6f8a6fa40d040de75a19438828ea7962a63fb9846b807b4`  
		Last Modified: Mon, 11 Jul 2022 23:15:18 GMT  
		Size: 282.4 KB (282374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4114dbccc760d1e5c5ac46a04ddf9364e3769d0e596ad434cee93f0188f5ce`  
		Last Modified: Mon, 11 Jul 2022 23:16:02 GMT  
		Size: 64.7 MB (64746381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af294dba60a105b5e75a524be1909771b82662e70c64c8a05ea3a2f65ded426`  
		Last Modified: Mon, 11 Jul 2022 23:19:25 GMT  
		Size: 260.0 MB (260045566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c6099c16f7786d73e0d0aadb844b9acd7a6f7c58596b39fb0400ff8fbc5b8c3b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.2 MB (703163757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d1e45dcbdd3a8a9eb584bf7ed194f49343542bf5c85661e5c986dc1c3565e5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:03:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:03:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:03:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:03:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:03:41 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 15:05:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:05:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:05:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:05:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:06:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:08:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c7d887e7b961ba6c9db72dd6419c5ac455dd43d49b194dbc43680f849a6ef`  
		Last Modified: Tue, 02 Aug 2022 15:38:49 GMT  
		Size: 839.8 KB (839769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51fe758bc1275edfa803da680fe43894a9e4bdb69d83153ccca2d60ba34bbee`  
		Last Modified: Tue, 02 Aug 2022 15:38:47 GMT  
		Size: 4.3 MB (4265854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646eaa84fc50bf88a2bca0599491e795cf8122e6fe16671e23fd8b87804e823`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ce991e1d0bf36ab7c0c7db9323c2cc620b0d96c88f26c619287aee7598666`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101d7b97c7577b747e3cc14cb64c408587e6489c4b2420aad7fa1dbbd8fe189`  
		Last Modified: Tue, 02 Aug 2022 15:39:22 GMT  
		Size: 252.5 MB (252503681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716f26c3c2a680d90778a974e99dc5d04bf9e4fbd9077cdb619b311ff4f0d24`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b66bed859b212ff9f65c306618bc607825b531e9a79843b4d75f5e870b3195`  
		Last Modified: Tue, 02 Aug 2022 15:39:42 GMT  
		Size: 63.1 MB (63088414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee909ec215bcdf8f5cd2e47e3aaf397ef01b2695fd292ea49920505e539f80c9`  
		Last Modified: Tue, 02 Aug 2022 15:39:34 GMT  
		Size: 283.1 KB (283086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884a1a0922cfe088904523812cfa7b3897bc3fc1b7eb0f266e99c75d92662a17`  
		Last Modified: Tue, 02 Aug 2022 15:39:44 GMT  
		Size: 67.0 MB (67000963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4a1da1cf397ef69011d59232aacc2b256057abfafa903e3beb919cff024a2b`  
		Last Modified: Tue, 02 Aug 2022 15:41:08 GMT  
		Size: 291.4 MB (291445475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-perception-bionic`

```console
$ docker pull ros@sha256:6209755aeb4e6ecd3cc0c0beb2b8fe93a015cbd9d3045ef2c201ca8ed976d2c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-perception-bionic` - linux; amd64

```console
$ docker pull ros@sha256:1f3b5df15ca60854de07682acabeb1009d55f56e7c7c0c19a41c5de9414b998f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.9 MB (742862325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab661038b8793b0427db56fe85f40e9b8d3b7aabbc82acae7e564c4636d4bae4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:57:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:57:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 12:57:48 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 12:57:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 12:57:48 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 12:57:48 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 13:01:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:01:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:01:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:01:53 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:02:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:02:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:04:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:09:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa6fbe30fbafa2fd890f1a634056fab84382d475fe85716949a1a44cc77f087`  
		Last Modified: Tue, 02 Aug 2022 13:52:33 GMT  
		Size: 839.1 KB (839126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7d6485ffdcfd34d9790c5e9f1e3deb6f1e01cd88b3ed1c2c4bfd798ce679c6`  
		Last Modified: Tue, 02 Aug 2022 13:52:31 GMT  
		Size: 4.9 MB (4873542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37d651da90ea517b4e41ab1754a0657cd17842014153817571fad7f62a21dd8`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8310f03235adb2a56f2ca99fcd6f4bf9c29d94663f625b160ef3534ffc2630bc`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f613727d0890c231f392123401bfc2194872d710cd8d8a8740db383fc8a599f4`  
		Last Modified: Tue, 02 Aug 2022 13:53:17 GMT  
		Size: 259.6 MB (259551224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ab03995e2e9bff9b259a370e6c30525ec9bc8cb87b98f29e3d3de46a99b36e`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0b7f91cbaa1e44e2ecae278c9b9bcec5d83eb8397cfd098ce9f394ca3642d2`  
		Last Modified: Tue, 02 Aug 2022 13:53:39 GMT  
		Size: 70.3 MB (70259542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e26ed31df7e549f55f79f7b17b78d0ba6d56d1cf0cd9a4f352729bc4be37f67`  
		Last Modified: Tue, 02 Aug 2022 13:53:27 GMT  
		Size: 283.1 KB (283134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99508511f69fc265efef3003c1bd53483ecc3d71f1bf6cdb319a64a2946042b0`  
		Last Modified: Tue, 02 Aug 2022 13:53:43 GMT  
		Size: 75.0 MB (74994419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a211461bcd28ecb3940dd7933e121068c7354be96bdda5dcef0b8a696b94b4`  
		Last Modified: Tue, 02 Aug 2022 13:55:04 GMT  
		Size: 305.3 MB (305349223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:d2a42b42115bd5254ae8170cfffe5dc793ec369a01f1345386165297648619f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.1 MB (646104096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd38e8b455233463eb77566608108e092bbccefec5186f0e291dcef643cfe26`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:28 GMT
ADD file:d6d276f8f40c095bc2411f4d370eb87f8042a092ebb5bb0076863b2b6182b34f in / 
# Tue, 07 Jun 2022 05:50:29 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:07:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:07:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:07:56 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 10:07:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 10:07:59 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 10:07:59 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 10:08:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 07 Jun 2022 10:11:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 22:58:15 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 22:58:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 22:58:16 GMT
CMD ["bash"]
# Mon, 11 Jul 2022 22:59:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 22:59:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 11 Jul 2022 23:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:05:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9242055bc3f039f3566a5154c8b1a602652bfe444e9b4291817caae906444e75`  
		Last Modified: Tue, 07 Jun 2022 05:54:37 GMT  
		Size: 22.3 MB (22306284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddc7f6bb12de3f6e55c81fc14d7ebc77e5e7612bd09a2770d4cf1feae55f3d6`  
		Last Modified: Tue, 07 Jun 2022 10:32:01 GMT  
		Size: 840.2 KB (840219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc3e315dd2fd37157023b5350340af87fe236f4bcd29db3284eb3e86c37c85`  
		Last Modified: Tue, 07 Jun 2022 10:32:00 GMT  
		Size: 4.1 MB (4089918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b851bde5be9d93cd5bf76737b14ccdf776ace9a4d8ed7b1e11b042c22452a1`  
		Last Modified: Tue, 07 Jun 2022 10:31:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883aed8a39d8c90c486aec03c1809aa36c891e812219cf617b59ece7f9165291`  
		Last Modified: Tue, 07 Jun 2022 10:31:58 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd559c545cdb93ee204c62144d4375db3f0450040d3ef61a8ac599ffb1f043a1`  
		Last Modified: Tue, 07 Jun 2022 10:34:31 GMT  
		Size: 238.9 MB (238943066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6affb1b3206339bc5b43342d1c9945b174998df8674effb3cfb95da2c03bd8f9`  
		Last Modified: Mon, 11 Jul 2022 23:15:06 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03108c0184ca678f48226bd3277b4d8468a25b0016664e2d80eb4c968264856f`  
		Last Modified: Mon, 11 Jul 2022 23:15:47 GMT  
		Size: 54.8 MB (54848442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67520f2af1ef3aca6f8a6fa40d040de75a19438828ea7962a63fb9846b807b4`  
		Last Modified: Mon, 11 Jul 2022 23:15:18 GMT  
		Size: 282.4 KB (282374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4114dbccc760d1e5c5ac46a04ddf9364e3769d0e596ad434cee93f0188f5ce`  
		Last Modified: Mon, 11 Jul 2022 23:16:02 GMT  
		Size: 64.7 MB (64746381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af294dba60a105b5e75a524be1909771b82662e70c64c8a05ea3a2f65ded426`  
		Last Modified: Mon, 11 Jul 2022 23:19:25 GMT  
		Size: 260.0 MB (260045566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c6099c16f7786d73e0d0aadb844b9acd7a6f7c58596b39fb0400ff8fbc5b8c3b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.2 MB (703163757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d1e45dcbdd3a8a9eb584bf7ed194f49343542bf5c85661e5c986dc1c3565e5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:03:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:03:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:03:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:03:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:03:41 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 15:05:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:05:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:05:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:05:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:06:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:08:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c7d887e7b961ba6c9db72dd6419c5ac455dd43d49b194dbc43680f849a6ef`  
		Last Modified: Tue, 02 Aug 2022 15:38:49 GMT  
		Size: 839.8 KB (839769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51fe758bc1275edfa803da680fe43894a9e4bdb69d83153ccca2d60ba34bbee`  
		Last Modified: Tue, 02 Aug 2022 15:38:47 GMT  
		Size: 4.3 MB (4265854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646eaa84fc50bf88a2bca0599491e795cf8122e6fe16671e23fd8b87804e823`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ce991e1d0bf36ab7c0c7db9323c2cc620b0d96c88f26c619287aee7598666`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101d7b97c7577b747e3cc14cb64c408587e6489c4b2420aad7fa1dbbd8fe189`  
		Last Modified: Tue, 02 Aug 2022 15:39:22 GMT  
		Size: 252.5 MB (252503681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716f26c3c2a680d90778a974e99dc5d04bf9e4fbd9077cdb619b311ff4f0d24`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b66bed859b212ff9f65c306618bc607825b531e9a79843b4d75f5e870b3195`  
		Last Modified: Tue, 02 Aug 2022 15:39:42 GMT  
		Size: 63.1 MB (63088414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee909ec215bcdf8f5cd2e47e3aaf397ef01b2695fd292ea49920505e539f80c9`  
		Last Modified: Tue, 02 Aug 2022 15:39:34 GMT  
		Size: 283.1 KB (283086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884a1a0922cfe088904523812cfa7b3897bc3fc1b7eb0f266e99c75d92662a17`  
		Last Modified: Tue, 02 Aug 2022 15:39:44 GMT  
		Size: 67.0 MB (67000963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4a1da1cf397ef69011d59232aacc2b256057abfafa903e3beb919cff024a2b`  
		Last Modified: Tue, 02 Aug 2022 15:41:08 GMT  
		Size: 291.4 MB (291445475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-robot`

```console
$ docker pull ros@sha256:61e3c0bf6a18828c4aef055f538c5de117ae9bd28ad16628ec56a2a10861e4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot` - linux; amd64

```console
$ docker pull ros@sha256:ad2b0f62192244a09c899d3eb2db7c3e9ee256af2a1b3eb1dd00802f60b2f343
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.6 MB (448598867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e419202b9af9cd0dca24ceebce291a6026b258cd5ff89c8df101d4b0b1bbf32`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:57:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:57:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 12:57:48 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 12:57:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 12:57:48 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 12:57:48 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 13:01:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:01:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:01:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:01:53 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:02:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:02:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:04:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:04:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa6fbe30fbafa2fd890f1a634056fab84382d475fe85716949a1a44cc77f087`  
		Last Modified: Tue, 02 Aug 2022 13:52:33 GMT  
		Size: 839.1 KB (839126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7d6485ffdcfd34d9790c5e9f1e3deb6f1e01cd88b3ed1c2c4bfd798ce679c6`  
		Last Modified: Tue, 02 Aug 2022 13:52:31 GMT  
		Size: 4.9 MB (4873542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37d651da90ea517b4e41ab1754a0657cd17842014153817571fad7f62a21dd8`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8310f03235adb2a56f2ca99fcd6f4bf9c29d94663f625b160ef3534ffc2630bc`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f613727d0890c231f392123401bfc2194872d710cd8d8a8740db383fc8a599f4`  
		Last Modified: Tue, 02 Aug 2022 13:53:17 GMT  
		Size: 259.6 MB (259551224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ab03995e2e9bff9b259a370e6c30525ec9bc8cb87b98f29e3d3de46a99b36e`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0b7f91cbaa1e44e2ecae278c9b9bcec5d83eb8397cfd098ce9f394ca3642d2`  
		Last Modified: Tue, 02 Aug 2022 13:53:39 GMT  
		Size: 70.3 MB (70259542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e26ed31df7e549f55f79f7b17b78d0ba6d56d1cf0cd9a4f352729bc4be37f67`  
		Last Modified: Tue, 02 Aug 2022 13:53:27 GMT  
		Size: 283.1 KB (283134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99508511f69fc265efef3003c1bd53483ecc3d71f1bf6cdb319a64a2946042b0`  
		Last Modified: Tue, 02 Aug 2022 13:53:43 GMT  
		Size: 75.0 MB (74994419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eed61fe44d161864b1f15921748fdd6a0e864e30298dfb574cdf474b54b7691`  
		Last Modified: Tue, 02 Aug 2022 13:53:58 GMT  
		Size: 11.1 MB (11085765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:0c18e6ee51d336bcd8ef9be1a54634d92b33e79b7f59288c8e5c2f0726d88918
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.2 MB (396183560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb5c3c34a7eed5670b47fc4fadbee79602dc4dc6df9fdb025a7704a880a6907`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:28 GMT
ADD file:d6d276f8f40c095bc2411f4d370eb87f8042a092ebb5bb0076863b2b6182b34f in / 
# Tue, 07 Jun 2022 05:50:29 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:07:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:07:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:07:56 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 10:07:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 10:07:59 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 10:07:59 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 10:08:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 07 Jun 2022 10:11:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 22:58:15 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 22:58:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 22:58:16 GMT
CMD ["bash"]
# Mon, 11 Jul 2022 22:59:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 22:59:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 11 Jul 2022 23:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:01:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9242055bc3f039f3566a5154c8b1a602652bfe444e9b4291817caae906444e75`  
		Last Modified: Tue, 07 Jun 2022 05:54:37 GMT  
		Size: 22.3 MB (22306284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddc7f6bb12de3f6e55c81fc14d7ebc77e5e7612bd09a2770d4cf1feae55f3d6`  
		Last Modified: Tue, 07 Jun 2022 10:32:01 GMT  
		Size: 840.2 KB (840219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc3e315dd2fd37157023b5350340af87fe236f4bcd29db3284eb3e86c37c85`  
		Last Modified: Tue, 07 Jun 2022 10:32:00 GMT  
		Size: 4.1 MB (4089918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b851bde5be9d93cd5bf76737b14ccdf776ace9a4d8ed7b1e11b042c22452a1`  
		Last Modified: Tue, 07 Jun 2022 10:31:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883aed8a39d8c90c486aec03c1809aa36c891e812219cf617b59ece7f9165291`  
		Last Modified: Tue, 07 Jun 2022 10:31:58 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd559c545cdb93ee204c62144d4375db3f0450040d3ef61a8ac599ffb1f043a1`  
		Last Modified: Tue, 07 Jun 2022 10:34:31 GMT  
		Size: 238.9 MB (238943066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6affb1b3206339bc5b43342d1c9945b174998df8674effb3cfb95da2c03bd8f9`  
		Last Modified: Mon, 11 Jul 2022 23:15:06 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03108c0184ca678f48226bd3277b4d8468a25b0016664e2d80eb4c968264856f`  
		Last Modified: Mon, 11 Jul 2022 23:15:47 GMT  
		Size: 54.8 MB (54848442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67520f2af1ef3aca6f8a6fa40d040de75a19438828ea7962a63fb9846b807b4`  
		Last Modified: Mon, 11 Jul 2022 23:15:18 GMT  
		Size: 282.4 KB (282374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4114dbccc760d1e5c5ac46a04ddf9364e3769d0e596ad434cee93f0188f5ce`  
		Last Modified: Mon, 11 Jul 2022 23:16:02 GMT  
		Size: 64.7 MB (64746381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f909fac08f8dd35ddb78c91e50923309c058ea81335298c302ffdcc3295b479`  
		Last Modified: Mon, 11 Jul 2022 23:16:26 GMT  
		Size: 10.1 MB (10125030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3e6c59936fec78be28a82061db3e9537d38de8be5cc48b3206ab80d6d2b88e57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.5 MB (422454040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e19c4cf364dd50aa1b03a9be7ab0b56d5590c1f90619f74a262d39596aede6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:03:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:03:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:03:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:03:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:03:41 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 15:05:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:05:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:05:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:05:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:06:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:06:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c7d887e7b961ba6c9db72dd6419c5ac455dd43d49b194dbc43680f849a6ef`  
		Last Modified: Tue, 02 Aug 2022 15:38:49 GMT  
		Size: 839.8 KB (839769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51fe758bc1275edfa803da680fe43894a9e4bdb69d83153ccca2d60ba34bbee`  
		Last Modified: Tue, 02 Aug 2022 15:38:47 GMT  
		Size: 4.3 MB (4265854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646eaa84fc50bf88a2bca0599491e795cf8122e6fe16671e23fd8b87804e823`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ce991e1d0bf36ab7c0c7db9323c2cc620b0d96c88f26c619287aee7598666`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101d7b97c7577b747e3cc14cb64c408587e6489c4b2420aad7fa1dbbd8fe189`  
		Last Modified: Tue, 02 Aug 2022 15:39:22 GMT  
		Size: 252.5 MB (252503681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716f26c3c2a680d90778a974e99dc5d04bf9e4fbd9077cdb619b311ff4f0d24`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b66bed859b212ff9f65c306618bc607825b531e9a79843b4d75f5e870b3195`  
		Last Modified: Tue, 02 Aug 2022 15:39:42 GMT  
		Size: 63.1 MB (63088414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee909ec215bcdf8f5cd2e47e3aaf397ef01b2695fd292ea49920505e539f80c9`  
		Last Modified: Tue, 02 Aug 2022 15:39:34 GMT  
		Size: 283.1 KB (283086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884a1a0922cfe088904523812cfa7b3897bc3fc1b7eb0f266e99c75d92662a17`  
		Last Modified: Tue, 02 Aug 2022 15:39:44 GMT  
		Size: 67.0 MB (67000963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1236989f1fcde790f9d9aeda9bfc9ae97a4c7f11b790b4fb3cbd2e6872f13861`  
		Last Modified: Tue, 02 Aug 2022 15:40:05 GMT  
		Size: 10.7 MB (10735758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-robot-bionic`

```console
$ docker pull ros@sha256:61e3c0bf6a18828c4aef055f538c5de117ae9bd28ad16628ec56a2a10861e4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot-bionic` - linux; amd64

```console
$ docker pull ros@sha256:ad2b0f62192244a09c899d3eb2db7c3e9ee256af2a1b3eb1dd00802f60b2f343
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.6 MB (448598867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e419202b9af9cd0dca24ceebce291a6026b258cd5ff89c8df101d4b0b1bbf32`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:57:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:57:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 12:57:48 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 12:57:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 12:57:48 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 12:57:48 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 13:01:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:01:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:01:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:01:53 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:02:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:02:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:04:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:04:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa6fbe30fbafa2fd890f1a634056fab84382d475fe85716949a1a44cc77f087`  
		Last Modified: Tue, 02 Aug 2022 13:52:33 GMT  
		Size: 839.1 KB (839126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7d6485ffdcfd34d9790c5e9f1e3deb6f1e01cd88b3ed1c2c4bfd798ce679c6`  
		Last Modified: Tue, 02 Aug 2022 13:52:31 GMT  
		Size: 4.9 MB (4873542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37d651da90ea517b4e41ab1754a0657cd17842014153817571fad7f62a21dd8`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8310f03235adb2a56f2ca99fcd6f4bf9c29d94663f625b160ef3534ffc2630bc`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f613727d0890c231f392123401bfc2194872d710cd8d8a8740db383fc8a599f4`  
		Last Modified: Tue, 02 Aug 2022 13:53:17 GMT  
		Size: 259.6 MB (259551224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ab03995e2e9bff9b259a370e6c30525ec9bc8cb87b98f29e3d3de46a99b36e`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0b7f91cbaa1e44e2ecae278c9b9bcec5d83eb8397cfd098ce9f394ca3642d2`  
		Last Modified: Tue, 02 Aug 2022 13:53:39 GMT  
		Size: 70.3 MB (70259542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e26ed31df7e549f55f79f7b17b78d0ba6d56d1cf0cd9a4f352729bc4be37f67`  
		Last Modified: Tue, 02 Aug 2022 13:53:27 GMT  
		Size: 283.1 KB (283134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99508511f69fc265efef3003c1bd53483ecc3d71f1bf6cdb319a64a2946042b0`  
		Last Modified: Tue, 02 Aug 2022 13:53:43 GMT  
		Size: 75.0 MB (74994419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eed61fe44d161864b1f15921748fdd6a0e864e30298dfb574cdf474b54b7691`  
		Last Modified: Tue, 02 Aug 2022 13:53:58 GMT  
		Size: 11.1 MB (11085765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:0c18e6ee51d336bcd8ef9be1a54634d92b33e79b7f59288c8e5c2f0726d88918
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.2 MB (396183560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb5c3c34a7eed5670b47fc4fadbee79602dc4dc6df9fdb025a7704a880a6907`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:28 GMT
ADD file:d6d276f8f40c095bc2411f4d370eb87f8042a092ebb5bb0076863b2b6182b34f in / 
# Tue, 07 Jun 2022 05:50:29 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:07:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:07:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:07:56 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 10:07:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 10:07:59 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 10:07:59 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 10:08:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 07 Jun 2022 10:11:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 22:58:15 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 22:58:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 22:58:16 GMT
CMD ["bash"]
# Mon, 11 Jul 2022 22:59:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 22:59:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 11 Jul 2022 23:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:01:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9242055bc3f039f3566a5154c8b1a602652bfe444e9b4291817caae906444e75`  
		Last Modified: Tue, 07 Jun 2022 05:54:37 GMT  
		Size: 22.3 MB (22306284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddc7f6bb12de3f6e55c81fc14d7ebc77e5e7612bd09a2770d4cf1feae55f3d6`  
		Last Modified: Tue, 07 Jun 2022 10:32:01 GMT  
		Size: 840.2 KB (840219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc3e315dd2fd37157023b5350340af87fe236f4bcd29db3284eb3e86c37c85`  
		Last Modified: Tue, 07 Jun 2022 10:32:00 GMT  
		Size: 4.1 MB (4089918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b851bde5be9d93cd5bf76737b14ccdf776ace9a4d8ed7b1e11b042c22452a1`  
		Last Modified: Tue, 07 Jun 2022 10:31:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883aed8a39d8c90c486aec03c1809aa36c891e812219cf617b59ece7f9165291`  
		Last Modified: Tue, 07 Jun 2022 10:31:58 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd559c545cdb93ee204c62144d4375db3f0450040d3ef61a8ac599ffb1f043a1`  
		Last Modified: Tue, 07 Jun 2022 10:34:31 GMT  
		Size: 238.9 MB (238943066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6affb1b3206339bc5b43342d1c9945b174998df8674effb3cfb95da2c03bd8f9`  
		Last Modified: Mon, 11 Jul 2022 23:15:06 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03108c0184ca678f48226bd3277b4d8468a25b0016664e2d80eb4c968264856f`  
		Last Modified: Mon, 11 Jul 2022 23:15:47 GMT  
		Size: 54.8 MB (54848442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67520f2af1ef3aca6f8a6fa40d040de75a19438828ea7962a63fb9846b807b4`  
		Last Modified: Mon, 11 Jul 2022 23:15:18 GMT  
		Size: 282.4 KB (282374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4114dbccc760d1e5c5ac46a04ddf9364e3769d0e596ad434cee93f0188f5ce`  
		Last Modified: Mon, 11 Jul 2022 23:16:02 GMT  
		Size: 64.7 MB (64746381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f909fac08f8dd35ddb78c91e50923309c058ea81335298c302ffdcc3295b479`  
		Last Modified: Mon, 11 Jul 2022 23:16:26 GMT  
		Size: 10.1 MB (10125030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3e6c59936fec78be28a82061db3e9537d38de8be5cc48b3206ab80d6d2b88e57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.5 MB (422454040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e19c4cf364dd50aa1b03a9be7ab0b56d5590c1f90619f74a262d39596aede6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:03:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:03:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:03:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:03:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:03:41 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 15:05:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:05:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:05:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:05:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:06:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:06:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c7d887e7b961ba6c9db72dd6419c5ac455dd43d49b194dbc43680f849a6ef`  
		Last Modified: Tue, 02 Aug 2022 15:38:49 GMT  
		Size: 839.8 KB (839769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51fe758bc1275edfa803da680fe43894a9e4bdb69d83153ccca2d60ba34bbee`  
		Last Modified: Tue, 02 Aug 2022 15:38:47 GMT  
		Size: 4.3 MB (4265854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646eaa84fc50bf88a2bca0599491e795cf8122e6fe16671e23fd8b87804e823`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ce991e1d0bf36ab7c0c7db9323c2cc620b0d96c88f26c619287aee7598666`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101d7b97c7577b747e3cc14cb64c408587e6489c4b2420aad7fa1dbbd8fe189`  
		Last Modified: Tue, 02 Aug 2022 15:39:22 GMT  
		Size: 252.5 MB (252503681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716f26c3c2a680d90778a974e99dc5d04bf9e4fbd9077cdb619b311ff4f0d24`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b66bed859b212ff9f65c306618bc607825b531e9a79843b4d75f5e870b3195`  
		Last Modified: Tue, 02 Aug 2022 15:39:42 GMT  
		Size: 63.1 MB (63088414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee909ec215bcdf8f5cd2e47e3aaf397ef01b2695fd292ea49920505e539f80c9`  
		Last Modified: Tue, 02 Aug 2022 15:39:34 GMT  
		Size: 283.1 KB (283086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884a1a0922cfe088904523812cfa7b3897bc3fc1b7eb0f266e99c75d92662a17`  
		Last Modified: Tue, 02 Aug 2022 15:39:44 GMT  
		Size: 67.0 MB (67000963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1236989f1fcde790f9d9aeda9bfc9ae97a4c7f11b790b4fb3cbd2e6872f13861`  
		Last Modified: Tue, 02 Aug 2022 15:40:05 GMT  
		Size: 10.7 MB (10735758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-base`

```console
$ docker pull ros@sha256:33870f62e883c4205382ec9ff2c2f144f010d3e9101691be15a38ae456eb8ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:17a8176d6e886bb868eb2fe93712548382781b762f62424ee98a64e194050ae2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 MB (437513102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2864ef7a388d5748aa5fd301591d1925922027f2e8d9189cf76018e5420737c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:57:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:57:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 12:57:48 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 12:57:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 12:57:48 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 12:57:48 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 13:01:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:01:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:01:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:01:53 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:02:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:02:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:04:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa6fbe30fbafa2fd890f1a634056fab84382d475fe85716949a1a44cc77f087`  
		Last Modified: Tue, 02 Aug 2022 13:52:33 GMT  
		Size: 839.1 KB (839126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7d6485ffdcfd34d9790c5e9f1e3deb6f1e01cd88b3ed1c2c4bfd798ce679c6`  
		Last Modified: Tue, 02 Aug 2022 13:52:31 GMT  
		Size: 4.9 MB (4873542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37d651da90ea517b4e41ab1754a0657cd17842014153817571fad7f62a21dd8`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8310f03235adb2a56f2ca99fcd6f4bf9c29d94663f625b160ef3534ffc2630bc`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f613727d0890c231f392123401bfc2194872d710cd8d8a8740db383fc8a599f4`  
		Last Modified: Tue, 02 Aug 2022 13:53:17 GMT  
		Size: 259.6 MB (259551224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ab03995e2e9bff9b259a370e6c30525ec9bc8cb87b98f29e3d3de46a99b36e`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0b7f91cbaa1e44e2ecae278c9b9bcec5d83eb8397cfd098ce9f394ca3642d2`  
		Last Modified: Tue, 02 Aug 2022 13:53:39 GMT  
		Size: 70.3 MB (70259542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e26ed31df7e549f55f79f7b17b78d0ba6d56d1cf0cd9a4f352729bc4be37f67`  
		Last Modified: Tue, 02 Aug 2022 13:53:27 GMT  
		Size: 283.1 KB (283134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99508511f69fc265efef3003c1bd53483ecc3d71f1bf6cdb319a64a2946042b0`  
		Last Modified: Tue, 02 Aug 2022 13:53:43 GMT  
		Size: 75.0 MB (74994419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:8e3ceed077fce82a58f61e42dcf7ffcdf1ac40b9cdd7aec02ab53741f70290b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.1 MB (386058530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69498dc4a9cdd7010aeadee61ff767774c6d805477a3a6d8e29f3f5118e3b251`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:28 GMT
ADD file:d6d276f8f40c095bc2411f4d370eb87f8042a092ebb5bb0076863b2b6182b34f in / 
# Tue, 07 Jun 2022 05:50:29 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:07:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:07:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:07:56 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 10:07:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 10:07:59 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 10:07:59 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 10:08:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 07 Jun 2022 10:11:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 22:58:15 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 22:58:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 22:58:16 GMT
CMD ["bash"]
# Mon, 11 Jul 2022 22:59:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 22:59:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 11 Jul 2022 23:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9242055bc3f039f3566a5154c8b1a602652bfe444e9b4291817caae906444e75`  
		Last Modified: Tue, 07 Jun 2022 05:54:37 GMT  
		Size: 22.3 MB (22306284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddc7f6bb12de3f6e55c81fc14d7ebc77e5e7612bd09a2770d4cf1feae55f3d6`  
		Last Modified: Tue, 07 Jun 2022 10:32:01 GMT  
		Size: 840.2 KB (840219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc3e315dd2fd37157023b5350340af87fe236f4bcd29db3284eb3e86c37c85`  
		Last Modified: Tue, 07 Jun 2022 10:32:00 GMT  
		Size: 4.1 MB (4089918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b851bde5be9d93cd5bf76737b14ccdf776ace9a4d8ed7b1e11b042c22452a1`  
		Last Modified: Tue, 07 Jun 2022 10:31:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883aed8a39d8c90c486aec03c1809aa36c891e812219cf617b59ece7f9165291`  
		Last Modified: Tue, 07 Jun 2022 10:31:58 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd559c545cdb93ee204c62144d4375db3f0450040d3ef61a8ac599ffb1f043a1`  
		Last Modified: Tue, 07 Jun 2022 10:34:31 GMT  
		Size: 238.9 MB (238943066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6affb1b3206339bc5b43342d1c9945b174998df8674effb3cfb95da2c03bd8f9`  
		Last Modified: Mon, 11 Jul 2022 23:15:06 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03108c0184ca678f48226bd3277b4d8468a25b0016664e2d80eb4c968264856f`  
		Last Modified: Mon, 11 Jul 2022 23:15:47 GMT  
		Size: 54.8 MB (54848442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67520f2af1ef3aca6f8a6fa40d040de75a19438828ea7962a63fb9846b807b4`  
		Last Modified: Mon, 11 Jul 2022 23:15:18 GMT  
		Size: 282.4 KB (282374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4114dbccc760d1e5c5ac46a04ddf9364e3769d0e596ad434cee93f0188f5ce`  
		Last Modified: Mon, 11 Jul 2022 23:16:02 GMT  
		Size: 64.7 MB (64746381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e19db181648b571c1a017e730f52145de920147e64052fa8662b7f611ac707db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 MB (411718282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56b623ecaac63fef2cd569acd1b109d44ce4a7318e7d3bda7b0c6d1e2ab1334`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:03:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:03:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:03:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:03:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:03:41 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 15:05:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:05:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:05:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:05:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:06:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c7d887e7b961ba6c9db72dd6419c5ac455dd43d49b194dbc43680f849a6ef`  
		Last Modified: Tue, 02 Aug 2022 15:38:49 GMT  
		Size: 839.8 KB (839769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51fe758bc1275edfa803da680fe43894a9e4bdb69d83153ccca2d60ba34bbee`  
		Last Modified: Tue, 02 Aug 2022 15:38:47 GMT  
		Size: 4.3 MB (4265854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646eaa84fc50bf88a2bca0599491e795cf8122e6fe16671e23fd8b87804e823`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ce991e1d0bf36ab7c0c7db9323c2cc620b0d96c88f26c619287aee7598666`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101d7b97c7577b747e3cc14cb64c408587e6489c4b2420aad7fa1dbbd8fe189`  
		Last Modified: Tue, 02 Aug 2022 15:39:22 GMT  
		Size: 252.5 MB (252503681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716f26c3c2a680d90778a974e99dc5d04bf9e4fbd9077cdb619b311ff4f0d24`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b66bed859b212ff9f65c306618bc607825b531e9a79843b4d75f5e870b3195`  
		Last Modified: Tue, 02 Aug 2022 15:39:42 GMT  
		Size: 63.1 MB (63088414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee909ec215bcdf8f5cd2e47e3aaf397ef01b2695fd292ea49920505e539f80c9`  
		Last Modified: Tue, 02 Aug 2022 15:39:34 GMT  
		Size: 283.1 KB (283086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884a1a0922cfe088904523812cfa7b3897bc3fc1b7eb0f266e99c75d92662a17`  
		Last Modified: Tue, 02 Aug 2022 15:39:44 GMT  
		Size: 67.0 MB (67000963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-base-bionic`

```console
$ docker pull ros@sha256:33870f62e883c4205382ec9ff2c2f144f010d3e9101691be15a38ae456eb8ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base-bionic` - linux; amd64

```console
$ docker pull ros@sha256:17a8176d6e886bb868eb2fe93712548382781b762f62424ee98a64e194050ae2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 MB (437513102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2864ef7a388d5748aa5fd301591d1925922027f2e8d9189cf76018e5420737c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:57:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:57:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 12:57:48 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 12:57:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 12:57:48 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 12:57:48 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 13:01:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:01:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:01:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:01:53 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:02:40 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:02:47 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:04:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa6fbe30fbafa2fd890f1a634056fab84382d475fe85716949a1a44cc77f087`  
		Last Modified: Tue, 02 Aug 2022 13:52:33 GMT  
		Size: 839.1 KB (839126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7d6485ffdcfd34d9790c5e9f1e3deb6f1e01cd88b3ed1c2c4bfd798ce679c6`  
		Last Modified: Tue, 02 Aug 2022 13:52:31 GMT  
		Size: 4.9 MB (4873542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37d651da90ea517b4e41ab1754a0657cd17842014153817571fad7f62a21dd8`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8310f03235adb2a56f2ca99fcd6f4bf9c29d94663f625b160ef3534ffc2630bc`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f613727d0890c231f392123401bfc2194872d710cd8d8a8740db383fc8a599f4`  
		Last Modified: Tue, 02 Aug 2022 13:53:17 GMT  
		Size: 259.6 MB (259551224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ab03995e2e9bff9b259a370e6c30525ec9bc8cb87b98f29e3d3de46a99b36e`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0b7f91cbaa1e44e2ecae278c9b9bcec5d83eb8397cfd098ce9f394ca3642d2`  
		Last Modified: Tue, 02 Aug 2022 13:53:39 GMT  
		Size: 70.3 MB (70259542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e26ed31df7e549f55f79f7b17b78d0ba6d56d1cf0cd9a4f352729bc4be37f67`  
		Last Modified: Tue, 02 Aug 2022 13:53:27 GMT  
		Size: 283.1 KB (283134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99508511f69fc265efef3003c1bd53483ecc3d71f1bf6cdb319a64a2946042b0`  
		Last Modified: Tue, 02 Aug 2022 13:53:43 GMT  
		Size: 75.0 MB (74994419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:8e3ceed077fce82a58f61e42dcf7ffcdf1ac40b9cdd7aec02ab53741f70290b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.1 MB (386058530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69498dc4a9cdd7010aeadee61ff767774c6d805477a3a6d8e29f3f5118e3b251`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:28 GMT
ADD file:d6d276f8f40c095bc2411f4d370eb87f8042a092ebb5bb0076863b2b6182b34f in / 
# Tue, 07 Jun 2022 05:50:29 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:07:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:07:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:07:56 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 10:07:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 10:07:59 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 10:07:59 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 10:08:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 07 Jun 2022 10:11:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 22:58:15 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 22:58:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 22:58:16 GMT
CMD ["bash"]
# Mon, 11 Jul 2022 22:59:08 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 22:59:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 11 Jul 2022 23:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9242055bc3f039f3566a5154c8b1a602652bfe444e9b4291817caae906444e75`  
		Last Modified: Tue, 07 Jun 2022 05:54:37 GMT  
		Size: 22.3 MB (22306284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddc7f6bb12de3f6e55c81fc14d7ebc77e5e7612bd09a2770d4cf1feae55f3d6`  
		Last Modified: Tue, 07 Jun 2022 10:32:01 GMT  
		Size: 840.2 KB (840219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc3e315dd2fd37157023b5350340af87fe236f4bcd29db3284eb3e86c37c85`  
		Last Modified: Tue, 07 Jun 2022 10:32:00 GMT  
		Size: 4.1 MB (4089918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b851bde5be9d93cd5bf76737b14ccdf776ace9a4d8ed7b1e11b042c22452a1`  
		Last Modified: Tue, 07 Jun 2022 10:31:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883aed8a39d8c90c486aec03c1809aa36c891e812219cf617b59ece7f9165291`  
		Last Modified: Tue, 07 Jun 2022 10:31:58 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd559c545cdb93ee204c62144d4375db3f0450040d3ef61a8ac599ffb1f043a1`  
		Last Modified: Tue, 07 Jun 2022 10:34:31 GMT  
		Size: 238.9 MB (238943066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6affb1b3206339bc5b43342d1c9945b174998df8674effb3cfb95da2c03bd8f9`  
		Last Modified: Mon, 11 Jul 2022 23:15:06 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03108c0184ca678f48226bd3277b4d8468a25b0016664e2d80eb4c968264856f`  
		Last Modified: Mon, 11 Jul 2022 23:15:47 GMT  
		Size: 54.8 MB (54848442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67520f2af1ef3aca6f8a6fa40d040de75a19438828ea7962a63fb9846b807b4`  
		Last Modified: Mon, 11 Jul 2022 23:15:18 GMT  
		Size: 282.4 KB (282374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4114dbccc760d1e5c5ac46a04ddf9364e3769d0e596ad434cee93f0188f5ce`  
		Last Modified: Mon, 11 Jul 2022 23:16:02 GMT  
		Size: 64.7 MB (64746381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e19db181648b571c1a017e730f52145de920147e64052fa8662b7f611ac707db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 MB (411718282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56b623ecaac63fef2cd569acd1b109d44ce4a7318e7d3bda7b0c6d1e2ab1334`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:03:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:03:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:03:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:03:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:03:41 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 15:05:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:05:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:05:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:05:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:06:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c7d887e7b961ba6c9db72dd6419c5ac455dd43d49b194dbc43680f849a6ef`  
		Last Modified: Tue, 02 Aug 2022 15:38:49 GMT  
		Size: 839.8 KB (839769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51fe758bc1275edfa803da680fe43894a9e4bdb69d83153ccca2d60ba34bbee`  
		Last Modified: Tue, 02 Aug 2022 15:38:47 GMT  
		Size: 4.3 MB (4265854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646eaa84fc50bf88a2bca0599491e795cf8122e6fe16671e23fd8b87804e823`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ce991e1d0bf36ab7c0c7db9323c2cc620b0d96c88f26c619287aee7598666`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101d7b97c7577b747e3cc14cb64c408587e6489c4b2420aad7fa1dbbd8fe189`  
		Last Modified: Tue, 02 Aug 2022 15:39:22 GMT  
		Size: 252.5 MB (252503681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716f26c3c2a680d90778a974e99dc5d04bf9e4fbd9077cdb619b311ff4f0d24`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b66bed859b212ff9f65c306618bc607825b531e9a79843b4d75f5e870b3195`  
		Last Modified: Tue, 02 Aug 2022 15:39:42 GMT  
		Size: 63.1 MB (63088414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee909ec215bcdf8f5cd2e47e3aaf397ef01b2695fd292ea49920505e539f80c9`  
		Last Modified: Tue, 02 Aug 2022 15:39:34 GMT  
		Size: 283.1 KB (283086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884a1a0922cfe088904523812cfa7b3897bc3fc1b7eb0f266e99c75d92662a17`  
		Last Modified: Tue, 02 Aug 2022 15:39:44 GMT  
		Size: 67.0 MB (67000963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-core`

```console
$ docker pull ros@sha256:f367c7349aaa0d7b344ffbcdc8fa5f0fbe3415279d192d09f051e9c1ef3edcee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:12474f93b72af1d2a90ffd3a83465c2d7fc062f71e1bbd8219a4fbfd9465445f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (291976007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79acfd9a4048a562c4c833120a1741045623180f05bccd1f022b9196a1f31802`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:57:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:57:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 12:57:48 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 12:57:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 12:57:48 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 12:57:48 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 13:01:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:01:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:01:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:01:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa6fbe30fbafa2fd890f1a634056fab84382d475fe85716949a1a44cc77f087`  
		Last Modified: Tue, 02 Aug 2022 13:52:33 GMT  
		Size: 839.1 KB (839126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7d6485ffdcfd34d9790c5e9f1e3deb6f1e01cd88b3ed1c2c4bfd798ce679c6`  
		Last Modified: Tue, 02 Aug 2022 13:52:31 GMT  
		Size: 4.9 MB (4873542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37d651da90ea517b4e41ab1754a0657cd17842014153817571fad7f62a21dd8`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8310f03235adb2a56f2ca99fcd6f4bf9c29d94663f625b160ef3534ffc2630bc`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f613727d0890c231f392123401bfc2194872d710cd8d8a8740db383fc8a599f4`  
		Last Modified: Tue, 02 Aug 2022 13:53:17 GMT  
		Size: 259.6 MB (259551224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ab03995e2e9bff9b259a370e6c30525ec9bc8cb87b98f29e3d3de46a99b36e`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:d4a0131748a7ffb924a003845b10921ddd3f5d963a6cf71d497c3851b7e94fc0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266181333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f444660baa7a35fb7cadcf6ccdcea8d9e4436dbba5c800cf8304c755244cd158`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:28 GMT
ADD file:d6d276f8f40c095bc2411f4d370eb87f8042a092ebb5bb0076863b2b6182b34f in / 
# Tue, 07 Jun 2022 05:50:29 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:07:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:07:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:07:56 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 10:07:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 10:07:59 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 10:07:59 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 10:08:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 07 Jun 2022 10:11:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 22:58:15 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 22:58:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 22:58:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9242055bc3f039f3566a5154c8b1a602652bfe444e9b4291817caae906444e75`  
		Last Modified: Tue, 07 Jun 2022 05:54:37 GMT  
		Size: 22.3 MB (22306284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddc7f6bb12de3f6e55c81fc14d7ebc77e5e7612bd09a2770d4cf1feae55f3d6`  
		Last Modified: Tue, 07 Jun 2022 10:32:01 GMT  
		Size: 840.2 KB (840219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc3e315dd2fd37157023b5350340af87fe236f4bcd29db3284eb3e86c37c85`  
		Last Modified: Tue, 07 Jun 2022 10:32:00 GMT  
		Size: 4.1 MB (4089918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b851bde5be9d93cd5bf76737b14ccdf776ace9a4d8ed7b1e11b042c22452a1`  
		Last Modified: Tue, 07 Jun 2022 10:31:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883aed8a39d8c90c486aec03c1809aa36c891e812219cf617b59ece7f9165291`  
		Last Modified: Tue, 07 Jun 2022 10:31:58 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd559c545cdb93ee204c62144d4375db3f0450040d3ef61a8ac599ffb1f043a1`  
		Last Modified: Tue, 07 Jun 2022 10:34:31 GMT  
		Size: 238.9 MB (238943066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6affb1b3206339bc5b43342d1c9945b174998df8674effb3cfb95da2c03bd8f9`  
		Last Modified: Mon, 11 Jul 2022 23:15:06 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a3c706160ea294c6d504493c8788aba76ccfc4301d5a8ac1a7d89fe87c5cdeea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281345819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd9332cdc364c841103f5a91024056914be62095a4f80226a0efda07ffc73da`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:03:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:03:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:03:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:03:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:03:41 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 15:05:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:05:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:05:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c7d887e7b961ba6c9db72dd6419c5ac455dd43d49b194dbc43680f849a6ef`  
		Last Modified: Tue, 02 Aug 2022 15:38:49 GMT  
		Size: 839.8 KB (839769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51fe758bc1275edfa803da680fe43894a9e4bdb69d83153ccca2d60ba34bbee`  
		Last Modified: Tue, 02 Aug 2022 15:38:47 GMT  
		Size: 4.3 MB (4265854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646eaa84fc50bf88a2bca0599491e795cf8122e6fe16671e23fd8b87804e823`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ce991e1d0bf36ab7c0c7db9323c2cc620b0d96c88f26c619287aee7598666`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101d7b97c7577b747e3cc14cb64c408587e6489c4b2420aad7fa1dbbd8fe189`  
		Last Modified: Tue, 02 Aug 2022 15:39:22 GMT  
		Size: 252.5 MB (252503681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716f26c3c2a680d90778a974e99dc5d04bf9e4fbd9077cdb619b311ff4f0d24`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-core-bionic`

```console
$ docker pull ros@sha256:f367c7349aaa0d7b344ffbcdc8fa5f0fbe3415279d192d09f051e9c1ef3edcee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:12474f93b72af1d2a90ffd3a83465c2d7fc062f71e1bbd8219a4fbfd9465445f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (291976007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79acfd9a4048a562c4c833120a1741045623180f05bccd1f022b9196a1f31802`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:57:32 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:57:46 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:57:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 12:57:48 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 12:57:48 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 12:57:48 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 12:57:48 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 13:01:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:01:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:01:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:01:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa6fbe30fbafa2fd890f1a634056fab84382d475fe85716949a1a44cc77f087`  
		Last Modified: Tue, 02 Aug 2022 13:52:33 GMT  
		Size: 839.1 KB (839126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7d6485ffdcfd34d9790c5e9f1e3deb6f1e01cd88b3ed1c2c4bfd798ce679c6`  
		Last Modified: Tue, 02 Aug 2022 13:52:31 GMT  
		Size: 4.9 MB (4873542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37d651da90ea517b4e41ab1754a0657cd17842014153817571fad7f62a21dd8`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8310f03235adb2a56f2ca99fcd6f4bf9c29d94663f625b160ef3534ffc2630bc`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f613727d0890c231f392123401bfc2194872d710cd8d8a8740db383fc8a599f4`  
		Last Modified: Tue, 02 Aug 2022 13:53:17 GMT  
		Size: 259.6 MB (259551224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ab03995e2e9bff9b259a370e6c30525ec9bc8cb87b98f29e3d3de46a99b36e`  
		Last Modified: Tue, 02 Aug 2022 13:52:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:d4a0131748a7ffb924a003845b10921ddd3f5d963a6cf71d497c3851b7e94fc0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266181333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f444660baa7a35fb7cadcf6ccdcea8d9e4436dbba5c800cf8304c755244cd158`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:28 GMT
ADD file:d6d276f8f40c095bc2411f4d370eb87f8042a092ebb5bb0076863b2b6182b34f in / 
# Tue, 07 Jun 2022 05:50:29 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:07:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:07:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:07:56 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 10:07:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 10:07:59 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 10:07:59 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 10:08:00 GMT
ENV ROS_DISTRO=melodic
# Tue, 07 Jun 2022 10:11:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 22:58:15 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 22:58:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 22:58:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9242055bc3f039f3566a5154c8b1a602652bfe444e9b4291817caae906444e75`  
		Last Modified: Tue, 07 Jun 2022 05:54:37 GMT  
		Size: 22.3 MB (22306284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddc7f6bb12de3f6e55c81fc14d7ebc77e5e7612bd09a2770d4cf1feae55f3d6`  
		Last Modified: Tue, 07 Jun 2022 10:32:01 GMT  
		Size: 840.2 KB (840219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bc3e315dd2fd37157023b5350340af87fe236f4bcd29db3284eb3e86c37c85`  
		Last Modified: Tue, 07 Jun 2022 10:32:00 GMT  
		Size: 4.1 MB (4089918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b851bde5be9d93cd5bf76737b14ccdf776ace9a4d8ed7b1e11b042c22452a1`  
		Last Modified: Tue, 07 Jun 2022 10:31:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883aed8a39d8c90c486aec03c1809aa36c891e812219cf617b59ece7f9165291`  
		Last Modified: Tue, 07 Jun 2022 10:31:58 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd559c545cdb93ee204c62144d4375db3f0450040d3ef61a8ac599ffb1f043a1`  
		Last Modified: Tue, 07 Jun 2022 10:34:31 GMT  
		Size: 238.9 MB (238943066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6affb1b3206339bc5b43342d1c9945b174998df8674effb3cfb95da2c03bd8f9`  
		Last Modified: Mon, 11 Jul 2022 23:15:06 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a3c706160ea294c6d504493c8788aba76ccfc4301d5a8ac1a7d89fe87c5cdeea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281345819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd9332cdc364c841103f5a91024056914be62095a4f80226a0efda07ffc73da`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:03:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:03:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:03:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:03:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:03:41 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 15:05:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:05:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:05:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c7d887e7b961ba6c9db72dd6419c5ac455dd43d49b194dbc43680f849a6ef`  
		Last Modified: Tue, 02 Aug 2022 15:38:49 GMT  
		Size: 839.8 KB (839769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51fe758bc1275edfa803da680fe43894a9e4bdb69d83153ccca2d60ba34bbee`  
		Last Modified: Tue, 02 Aug 2022 15:38:47 GMT  
		Size: 4.3 MB (4265854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646eaa84fc50bf88a2bca0599491e795cf8122e6fe16671e23fd8b87804e823`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ce991e1d0bf36ab7c0c7db9323c2cc620b0d96c88f26c619287aee7598666`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101d7b97c7577b747e3cc14cb64c408587e6489c4b2420aad7fa1dbbd8fe189`  
		Last Modified: Tue, 02 Aug 2022 15:39:22 GMT  
		Size: 252.5 MB (252503681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716f26c3c2a680d90778a974e99dc5d04bf9e4fbd9077cdb619b311ff4f0d24`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic`

```console
$ docker pull ros@sha256:0b1508eb22177b9a5d0999f1071a3a468fd6f192c7b3b0915ef0402efa8d5562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:8d5b98bb3e6cdc51c8fc846c701c121f937ede2bd2b6986b6a42f962ccf9cb0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343166945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4252b5fd978bbce4290a3ed3989114693e03ae35cbcfb5bd24693c5808956cdd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 13:10:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:10:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:10:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:10:38 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 13:13:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:13:13 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:13:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:13:13 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:13:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:13:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3519a1bb471cc6b2b4369f7cd39735754c6744b07b26c3124855dd894dcba45b`  
		Last Modified: Tue, 02 Aug 2022 13:55:14 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e2dfee34126a0fd475079e48bed7166ed0963c44262b6d1c8673a3cc31af08`  
		Last Modified: Tue, 02 Aug 2022 13:55:14 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825e59fe62383c77e16376834caef0bf40982defaf9019928a574c1e90132559`  
		Last Modified: Tue, 02 Aug 2022 13:55:54 GMT  
		Size: 177.0 MB (176996918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55778ffb7b3f4c8289907a297c07ad6b31e1c7ea5a410a5414c408630273346c`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7e3c098d974561c8914411584759f9ec5ac5489735340137cb61a5ed6dfdca`  
		Last Modified: Tue, 02 Aug 2022 13:56:14 GMT  
		Size: 50.9 MB (50940142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde62a097a809942e493ede6b058a2b1af7c20561149da37ef0116f7250f4eb2`  
		Last Modified: Tue, 02 Aug 2022 13:56:05 GMT  
		Size: 323.5 KB (323534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a3313522d23bc6b63456324802c67644e381b81c42eab2a0fd5fccf81b324f`  
		Last Modified: Tue, 02 Aug 2022 13:56:18 GMT  
		Size: 79.6 MB (79603159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:10c289835b4ac749b2d4211b9698472cb67b083ae60ccf55992469f7a9796985
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289316487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa56e91bb12af2d6dec2e4a46b6e8c32723fe510d3f042f08cdbb3850380181`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:50 GMT
ADD file:c95d34737ba1f11ac8b92be0125aad2baae46448f0d8ebd85ad69076006a3254 in / 
# Tue, 07 Jun 2022 05:50:51 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:19:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:19:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:19:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 10:19:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 10:19:37 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 10:19:37 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 10:19:37 GMT
ENV ROS_DISTRO=noetic
# Tue, 07 Jun 2022 10:22:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:05:37 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 23:05:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 23:05:38 GMT
CMD ["bash"]
# Mon, 11 Jul 2022 23:06:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:06:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 11 Jul 2022 23:07:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:36754881d0ec0d456ee49776d62f6f0df47d29956ac7b2231b797e05780c6744`  
		Last Modified: Tue, 07 Jun 2022 05:55:05 GMT  
		Size: 24.6 MB (24592639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e21254ce415ea7b490674f4a33c60349d312819e79bd953b7353e3dd7d14fea`  
		Last Modified: Tue, 07 Jun 2022 10:39:01 GMT  
		Size: 1.2 MB (1181840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48aa457454d70347a026cdb39a3d256e0969f6becf1cb485456cd0944fa7965e`  
		Last Modified: Tue, 07 Jun 2022 10:38:59 GMT  
		Size: 4.7 MB (4676394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e672a3b2d46c78712db3b52ed8e3c47a9685c026d512bbf4bf05589aebd337cd`  
		Last Modified: Tue, 07 Jun 2022 10:38:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cac3050647c36fd475eac545b3dc5080db7e9f45e0871805c82cfff88c11326`  
		Last Modified: Tue, 07 Jun 2022 10:38:57 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f262fcc054725c10b56cb064f0fde57d26e36876aa8d0e0f6380250a21a79d`  
		Last Modified: Tue, 07 Jun 2022 10:41:05 GMT  
		Size: 157.4 MB (157415772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b342bdf9b11d603945c520ba34d1eb05324adb5bdcdb8870cba8fa987a2ba9c1`  
		Last Modified: Mon, 11 Jul 2022 23:19:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c046fbf5a031a4fc8b112134fc86acbf0c93d8a6af6da05bcaaf255a7aecf39`  
		Last Modified: Mon, 11 Jul 2022 23:20:11 GMT  
		Size: 40.6 MB (40643256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7af22af4fa6b6b3bb6b3a8bbc9cf2d84563206385cc5fd4d464944fd11e16`  
		Last Modified: Mon, 11 Jul 2022 23:19:48 GMT  
		Size: 322.1 KB (322086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c959d6512be80be43cede75f20500c80a427f01f374fd31e7a7cc562466801`  
		Last Modified: Mon, 11 Jul 2022 23:20:29 GMT  
		Size: 60.5 MB (60482082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8d2c3160385c2f5a6449fff4905f7290543a28713ffc6e1550747d5e0dcdb0ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322192151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108358074c3289edba33e14e8130004770bde5dd9106d446db28dd2548498a48`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:09:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:09:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:09:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:09:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:06 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:10:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:10:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:10:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7d1bf2cea5d6a7f0ef5ba787e95aa344e3e67e349bbdcaedd088b0732e48e`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ac26fe78d80a057263cfc59c64582efef7caaa111eb4b639861056cf0df95`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f493394889994de604dd62e022d4827365c0de34ad6cac870ea6af5dca4bba40`  
		Last Modified: Tue, 02 Aug 2022 15:41:50 GMT  
		Size: 171.4 MB (171424725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c191fa5a5fa889fff525b13caa35fb805e0bac7c673aebce455ffc8876fce9`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9227bd4aa30a597598fbc456d5aa784c527937a1f88d2ad2787b48b0ad396d6`  
		Last Modified: Tue, 02 Aug 2022 15:42:10 GMT  
		Size: 45.0 MB (44988903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80df4890a016b37679e242280f4c5981f02725f7e081609daba03d47c99cb3ab`  
		Last Modified: Tue, 02 Aug 2022 15:42:03 GMT  
		Size: 323.5 KB (323472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9700876cb7bd2a4af8a21af304524eafef9645266e38f92be7594dbf40519b67`  
		Last Modified: Tue, 02 Aug 2022 15:42:13 GMT  
		Size: 71.8 MB (71754502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:e07c723d4bef5e382bd5dafc6bd8e93953cb8a0fa17e7226dba09d6bdeb6a6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:457af7c9a97b12ace89935dba24303c6e77d5c454eaebbfe029f41e7e515b0ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.1 MB (835138745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b22816876f9c718ecb4b11b361b0199aef666957dd676a6e0822138ba01e3d1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 13:10:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:10:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:10:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:10:38 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 13:13:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:13:13 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:13:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:13:13 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:13:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:13:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:22:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3519a1bb471cc6b2b4369f7cd39735754c6744b07b26c3124855dd894dcba45b`  
		Last Modified: Tue, 02 Aug 2022 13:55:14 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e2dfee34126a0fd475079e48bed7166ed0963c44262b6d1c8673a3cc31af08`  
		Last Modified: Tue, 02 Aug 2022 13:55:14 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825e59fe62383c77e16376834caef0bf40982defaf9019928a574c1e90132559`  
		Last Modified: Tue, 02 Aug 2022 13:55:54 GMT  
		Size: 177.0 MB (176996918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55778ffb7b3f4c8289907a297c07ad6b31e1c7ea5a410a5414c408630273346c`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7e3c098d974561c8914411584759f9ec5ac5489735340137cb61a5ed6dfdca`  
		Last Modified: Tue, 02 Aug 2022 13:56:14 GMT  
		Size: 50.9 MB (50940142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde62a097a809942e493ede6b058a2b1af7c20561149da37ef0116f7250f4eb2`  
		Last Modified: Tue, 02 Aug 2022 13:56:05 GMT  
		Size: 323.5 KB (323534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a3313522d23bc6b63456324802c67644e381b81c42eab2a0fd5fccf81b324f`  
		Last Modified: Tue, 02 Aug 2022 13:56:18 GMT  
		Size: 79.6 MB (79603159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5935c43df901b4416e80cde1e4691707df0aa3d7393e2ad287d556fda18b98`  
		Last Modified: Tue, 02 Aug 2022 13:58:11 GMT  
		Size: 492.0 MB (491971800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:5874087d8190b2efab7c91cc84c5c666cb0510437df4b7643b00781ff77cd43e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.2 MB (726206634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c252a3c40ccb92883e0c452bbf8d223cd059b4014acb765415f8fe99a034fc1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:50 GMT
ADD file:c95d34737ba1f11ac8b92be0125aad2baae46448f0d8ebd85ad69076006a3254 in / 
# Tue, 07 Jun 2022 05:50:51 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:19:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:19:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:19:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 10:19:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 10:19:37 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 10:19:37 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 10:19:37 GMT
ENV ROS_DISTRO=noetic
# Tue, 07 Jun 2022 10:22:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:05:37 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 23:05:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 23:05:38 GMT
CMD ["bash"]
# Mon, 11 Jul 2022 23:06:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:06:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 11 Jul 2022 23:07:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:13:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:36754881d0ec0d456ee49776d62f6f0df47d29956ac7b2231b797e05780c6744`  
		Last Modified: Tue, 07 Jun 2022 05:55:05 GMT  
		Size: 24.6 MB (24592639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e21254ce415ea7b490674f4a33c60349d312819e79bd953b7353e3dd7d14fea`  
		Last Modified: Tue, 07 Jun 2022 10:39:01 GMT  
		Size: 1.2 MB (1181840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48aa457454d70347a026cdb39a3d256e0969f6becf1cb485456cd0944fa7965e`  
		Last Modified: Tue, 07 Jun 2022 10:38:59 GMT  
		Size: 4.7 MB (4676394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e672a3b2d46c78712db3b52ed8e3c47a9685c026d512bbf4bf05589aebd337cd`  
		Last Modified: Tue, 07 Jun 2022 10:38:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cac3050647c36fd475eac545b3dc5080db7e9f45e0871805c82cfff88c11326`  
		Last Modified: Tue, 07 Jun 2022 10:38:57 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f262fcc054725c10b56cb064f0fde57d26e36876aa8d0e0f6380250a21a79d`  
		Last Modified: Tue, 07 Jun 2022 10:41:05 GMT  
		Size: 157.4 MB (157415772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b342bdf9b11d603945c520ba34d1eb05324adb5bdcdb8870cba8fa987a2ba9c1`  
		Last Modified: Mon, 11 Jul 2022 23:19:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c046fbf5a031a4fc8b112134fc86acbf0c93d8a6af6da05bcaaf255a7aecf39`  
		Last Modified: Mon, 11 Jul 2022 23:20:11 GMT  
		Size: 40.6 MB (40643256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7af22af4fa6b6b3bb6b3a8bbc9cf2d84563206385cc5fd4d464944fd11e16`  
		Last Modified: Mon, 11 Jul 2022 23:19:48 GMT  
		Size: 322.1 KB (322086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c959d6512be80be43cede75f20500c80a427f01f374fd31e7a7cc562466801`  
		Last Modified: Mon, 11 Jul 2022 23:20:29 GMT  
		Size: 60.5 MB (60482082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2cd7610b3d7672a94207d78176c2fb8c7d6653ea4a02e442a0e5ee24538588a`  
		Last Modified: Mon, 11 Jul 2022 23:25:42 GMT  
		Size: 436.9 MB (436890147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0a06825f28b50c090d1b79874eddcb235ab8977dc3f26205d86f96307e14fbaf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **784.7 MB (784729415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73229aac1c29ad65732bf715e6cefa795fbbe38f93ce6348d12ae7e77d182811`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:09:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:09:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:09:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:09:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:06 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:10:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:10:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:10:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:13:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7d1bf2cea5d6a7f0ef5ba787e95aa344e3e67e349bbdcaedd088b0732e48e`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ac26fe78d80a057263cfc59c64582efef7caaa111eb4b639861056cf0df95`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f493394889994de604dd62e022d4827365c0de34ad6cac870ea6af5dca4bba40`  
		Last Modified: Tue, 02 Aug 2022 15:41:50 GMT  
		Size: 171.4 MB (171424725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c191fa5a5fa889fff525b13caa35fb805e0bac7c673aebce455ffc8876fce9`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9227bd4aa30a597598fbc456d5aa784c527937a1f88d2ad2787b48b0ad396d6`  
		Last Modified: Tue, 02 Aug 2022 15:42:10 GMT  
		Size: 45.0 MB (44988903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80df4890a016b37679e242280f4c5981f02725f7e081609daba03d47c99cb3ab`  
		Last Modified: Tue, 02 Aug 2022 15:42:03 GMT  
		Size: 323.5 KB (323472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9700876cb7bd2a4af8a21af304524eafef9645266e38f92be7594dbf40519b67`  
		Last Modified: Tue, 02 Aug 2022 15:42:13 GMT  
		Size: 71.8 MB (71754502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3ba7b86422cfbb851f49e5b6c651bbc5d3d24e15ac8200fa9c8341a38b6ff3`  
		Last Modified: Tue, 02 Aug 2022 15:43:50 GMT  
		Size: 462.5 MB (462537264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-buster`

```console
$ docker pull ros@sha256:d629b6817921c199257f141f3556de36558de9148a04345540e21c7beda5364b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-perception-buster` - linux; amd64

```console
$ docker pull ros@sha256:261bbee43c8fd92629d856290c1da7cdbadd93d1c53f1ada35da619d6e8097c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **951.4 MB (951402354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359f68e189ef08d52bd84491269cd0d07683a112cb6e037af121e743fb6af517`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:14 GMT
ADD file:647206e0e9c1daa306e4ebbdc26c3ef1840dd316ba4ffea905d17b0858e58e34 in / 
# Tue, 02 Aug 2022 01:20:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:22:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:22:51 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 13:22:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:22:52 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:22:53 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:22:53 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 13:23:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:23:57 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:23:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:23:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:24:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:24:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:24:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:27:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7e6a53d1988fa8e19db6bcfc96ee6783afb079c38dbe047528e691815d19a9fa`  
		Last Modified: Tue, 02 Aug 2022 01:24:34 GMT  
		Size: 50.4 MB (50440980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5785ad494f16fd45414b77fd2e2429ebc6d521448ef6d033e1585a5ed6bcbcd1`  
		Last Modified: Tue, 02 Aug 2022 13:58:24 GMT  
		Size: 10.9 MB (10893408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a04cce4da471da7339c364869465ed016774874978f22acce2cc39bb9ead437`  
		Last Modified: Tue, 02 Aug 2022 13:58:22 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b65bdc45a558ffba287816e17e1126b9285c238098635aa3c00f6579301a3b2`  
		Last Modified: Tue, 02 Aug 2022 13:58:22 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c550336ebd94e7da67ecab9e9641d1125ae9892a6e53beb15510cdaeb177d7`  
		Last Modified: Tue, 02 Aug 2022 13:59:01 GMT  
		Size: 239.2 MB (239187767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d7f1bdf1bd7fd0f7d737e9250e43650de8b5e815bd77d8403f6834729f133c`  
		Last Modified: Tue, 02 Aug 2022 13:58:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf730b591358262d29294f063a2a095bb438b736d09b9867750da9a660388827`  
		Last Modified: Tue, 02 Aug 2022 13:59:22 GMT  
		Size: 86.6 MB (86568972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bafa8402824e8fc2746fac433d95ca63c18c25e7157347c220bb275e701214a`  
		Last Modified: Tue, 02 Aug 2022 13:59:09 GMT  
		Size: 317.8 KB (317845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c53a4a6a59b2d6fb99c5aa1d32fd18b873d7c25500236c513a2330680a399a`  
		Last Modified: Tue, 02 Aug 2022 13:59:20 GMT  
		Size: 76.0 MB (75976721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4267ad0b82b0dbb9bb01d15864d86c5bc4a7f029b88bd6ff476a422cf665dba5`  
		Last Modified: Tue, 02 Aug 2022 14:01:06 GMT  
		Size: 488.0 MB (488014247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:73a1fb135a5c50853fca23fcc7cf602a957390be2fc3c146014679ca2fcaf430
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 MB (867665789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f989420a2040976d2c62b27c5491d66c07c8b6b6ed97c7206a1eeb767294a471`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:49 GMT
ADD file:dfd7e3791fa0512f0f7c9cc8530233d6bc1b0a586a3656fd3950ea386754808a in / 
# Tue, 02 Aug 2022 00:40:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:14:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:14:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:14:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:14:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:14:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:14:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:15:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:15:34 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:15:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:15:37 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:16:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:16:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:17:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71209d5eb534b9e48223962276993c68559f68e230f73c8a0efc2a2998362bd9`  
		Last Modified: Tue, 02 Aug 2022 00:46:28 GMT  
		Size: 49.2 MB (49229053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e88751172e93002d9fab715ef025cd9a58382c4888b4934c054c6173397dad`  
		Last Modified: Tue, 02 Aug 2022 15:44:04 GMT  
		Size: 10.7 MB (10689284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f0efe68ed19a3b673e70c93625803a8fb308bf11f8888841e81b8d0d6a9744`  
		Last Modified: Tue, 02 Aug 2022 15:44:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4855fcd49a7c12011d55ed482968d218c494e066da8b0e9df0a3ead99e7002ce`  
		Last Modified: Tue, 02 Aug 2022 15:44:03 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bfd4e3998e04572199a3d7bb537f309bc7477561fe26c3ddfed63b62abf3e7`  
		Last Modified: Tue, 02 Aug 2022 15:44:33 GMT  
		Size: 184.4 MB (184372250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f36ec89e9e1541930fa7fcaa7a8f92fcb400ee8fb5a4abcade58343bed9c44`  
		Last Modified: Tue, 02 Aug 2022 15:44:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39030940ae9a93159cb08570c346fd2752db24ffb712e6f3dadb2e60725810de`  
		Last Modified: Tue, 02 Aug 2022 15:44:53 GMT  
		Size: 84.4 MB (84370573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d057e3372b0e330210969889e51a3c9995917b106b06b89795293f5b414ae645`  
		Last Modified: Tue, 02 Aug 2022 15:44:42 GMT  
		Size: 317.8 KB (317803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffbef9b0e37dd10c397077421ef3b79575b972c2dd339ac10d4d57ac18a7d06`  
		Last Modified: Tue, 02 Aug 2022 15:44:51 GMT  
		Size: 73.9 MB (73865318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30970ebf8cbc2a1a57fa00b9475413cc0c3ec5e0a3fbdc242964e7432eed0cd9`  
		Last Modified: Tue, 02 Aug 2022 15:46:20 GMT  
		Size: 464.8 MB (464819139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:e07c723d4bef5e382bd5dafc6bd8e93953cb8a0fa17e7226dba09d6bdeb6a6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:457af7c9a97b12ace89935dba24303c6e77d5c454eaebbfe029f41e7e515b0ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.1 MB (835138745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b22816876f9c718ecb4b11b361b0199aef666957dd676a6e0822138ba01e3d1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 13:10:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:10:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:10:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:10:38 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 13:13:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:13:13 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:13:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:13:13 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:13:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:13:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:22:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3519a1bb471cc6b2b4369f7cd39735754c6744b07b26c3124855dd894dcba45b`  
		Last Modified: Tue, 02 Aug 2022 13:55:14 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e2dfee34126a0fd475079e48bed7166ed0963c44262b6d1c8673a3cc31af08`  
		Last Modified: Tue, 02 Aug 2022 13:55:14 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825e59fe62383c77e16376834caef0bf40982defaf9019928a574c1e90132559`  
		Last Modified: Tue, 02 Aug 2022 13:55:54 GMT  
		Size: 177.0 MB (176996918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55778ffb7b3f4c8289907a297c07ad6b31e1c7ea5a410a5414c408630273346c`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7e3c098d974561c8914411584759f9ec5ac5489735340137cb61a5ed6dfdca`  
		Last Modified: Tue, 02 Aug 2022 13:56:14 GMT  
		Size: 50.9 MB (50940142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde62a097a809942e493ede6b058a2b1af7c20561149da37ef0116f7250f4eb2`  
		Last Modified: Tue, 02 Aug 2022 13:56:05 GMT  
		Size: 323.5 KB (323534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a3313522d23bc6b63456324802c67644e381b81c42eab2a0fd5fccf81b324f`  
		Last Modified: Tue, 02 Aug 2022 13:56:18 GMT  
		Size: 79.6 MB (79603159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5935c43df901b4416e80cde1e4691707df0aa3d7393e2ad287d556fda18b98`  
		Last Modified: Tue, 02 Aug 2022 13:58:11 GMT  
		Size: 492.0 MB (491971800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:5874087d8190b2efab7c91cc84c5c666cb0510437df4b7643b00781ff77cd43e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.2 MB (726206634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c252a3c40ccb92883e0c452bbf8d223cd059b4014acb765415f8fe99a034fc1`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:50 GMT
ADD file:c95d34737ba1f11ac8b92be0125aad2baae46448f0d8ebd85ad69076006a3254 in / 
# Tue, 07 Jun 2022 05:50:51 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:19:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:19:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:19:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 10:19:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 10:19:37 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 10:19:37 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 10:19:37 GMT
ENV ROS_DISTRO=noetic
# Tue, 07 Jun 2022 10:22:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:05:37 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 23:05:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 23:05:38 GMT
CMD ["bash"]
# Mon, 11 Jul 2022 23:06:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:06:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 11 Jul 2022 23:07:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:13:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:36754881d0ec0d456ee49776d62f6f0df47d29956ac7b2231b797e05780c6744`  
		Last Modified: Tue, 07 Jun 2022 05:55:05 GMT  
		Size: 24.6 MB (24592639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e21254ce415ea7b490674f4a33c60349d312819e79bd953b7353e3dd7d14fea`  
		Last Modified: Tue, 07 Jun 2022 10:39:01 GMT  
		Size: 1.2 MB (1181840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48aa457454d70347a026cdb39a3d256e0969f6becf1cb485456cd0944fa7965e`  
		Last Modified: Tue, 07 Jun 2022 10:38:59 GMT  
		Size: 4.7 MB (4676394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e672a3b2d46c78712db3b52ed8e3c47a9685c026d512bbf4bf05589aebd337cd`  
		Last Modified: Tue, 07 Jun 2022 10:38:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cac3050647c36fd475eac545b3dc5080db7e9f45e0871805c82cfff88c11326`  
		Last Modified: Tue, 07 Jun 2022 10:38:57 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f262fcc054725c10b56cb064f0fde57d26e36876aa8d0e0f6380250a21a79d`  
		Last Modified: Tue, 07 Jun 2022 10:41:05 GMT  
		Size: 157.4 MB (157415772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b342bdf9b11d603945c520ba34d1eb05324adb5bdcdb8870cba8fa987a2ba9c1`  
		Last Modified: Mon, 11 Jul 2022 23:19:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c046fbf5a031a4fc8b112134fc86acbf0c93d8a6af6da05bcaaf255a7aecf39`  
		Last Modified: Mon, 11 Jul 2022 23:20:11 GMT  
		Size: 40.6 MB (40643256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7af22af4fa6b6b3bb6b3a8bbc9cf2d84563206385cc5fd4d464944fd11e16`  
		Last Modified: Mon, 11 Jul 2022 23:19:48 GMT  
		Size: 322.1 KB (322086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c959d6512be80be43cede75f20500c80a427f01f374fd31e7a7cc562466801`  
		Last Modified: Mon, 11 Jul 2022 23:20:29 GMT  
		Size: 60.5 MB (60482082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2cd7610b3d7672a94207d78176c2fb8c7d6653ea4a02e442a0e5ee24538588a`  
		Last Modified: Mon, 11 Jul 2022 23:25:42 GMT  
		Size: 436.9 MB (436890147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0a06825f28b50c090d1b79874eddcb235ab8977dc3f26205d86f96307e14fbaf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **784.7 MB (784729415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73229aac1c29ad65732bf715e6cefa795fbbe38f93ce6348d12ae7e77d182811`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:09:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:09:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:09:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:09:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:06 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:10:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:10:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:10:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:13:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7d1bf2cea5d6a7f0ef5ba787e95aa344e3e67e349bbdcaedd088b0732e48e`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ac26fe78d80a057263cfc59c64582efef7caaa111eb4b639861056cf0df95`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f493394889994de604dd62e022d4827365c0de34ad6cac870ea6af5dca4bba40`  
		Last Modified: Tue, 02 Aug 2022 15:41:50 GMT  
		Size: 171.4 MB (171424725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c191fa5a5fa889fff525b13caa35fb805e0bac7c673aebce455ffc8876fce9`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9227bd4aa30a597598fbc456d5aa784c527937a1f88d2ad2787b48b0ad396d6`  
		Last Modified: Tue, 02 Aug 2022 15:42:10 GMT  
		Size: 45.0 MB (44988903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80df4890a016b37679e242280f4c5981f02725f7e081609daba03d47c99cb3ab`  
		Last Modified: Tue, 02 Aug 2022 15:42:03 GMT  
		Size: 323.5 KB (323472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9700876cb7bd2a4af8a21af304524eafef9645266e38f92be7594dbf40519b67`  
		Last Modified: Tue, 02 Aug 2022 15:42:13 GMT  
		Size: 71.8 MB (71754502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3ba7b86422cfbb851f49e5b6c651bbc5d3d24e15ac8200fa9c8341a38b6ff3`  
		Last Modified: Tue, 02 Aug 2022 15:43:50 GMT  
		Size: 462.5 MB (462537264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:9532f0e7e88172be185b151d832f211dd1f0caa15fa293f3a55c9d46ba4fd095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:db42b54ef7554d262ac6398dfdaf2ceb5d7eb59420f9ae4a23bf6029e921996f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359027107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b091aa21da0fbc744566faba05547001227262d90ab5c67291570aab854a8ae`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 13:10:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:10:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:10:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:10:38 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 13:13:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:13:13 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:13:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:13:13 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:13:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:13:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:16:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3519a1bb471cc6b2b4369f7cd39735754c6744b07b26c3124855dd894dcba45b`  
		Last Modified: Tue, 02 Aug 2022 13:55:14 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e2dfee34126a0fd475079e48bed7166ed0963c44262b6d1c8673a3cc31af08`  
		Last Modified: Tue, 02 Aug 2022 13:55:14 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825e59fe62383c77e16376834caef0bf40982defaf9019928a574c1e90132559`  
		Last Modified: Tue, 02 Aug 2022 13:55:54 GMT  
		Size: 177.0 MB (176996918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55778ffb7b3f4c8289907a297c07ad6b31e1c7ea5a410a5414c408630273346c`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7e3c098d974561c8914411584759f9ec5ac5489735340137cb61a5ed6dfdca`  
		Last Modified: Tue, 02 Aug 2022 13:56:14 GMT  
		Size: 50.9 MB (50940142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde62a097a809942e493ede6b058a2b1af7c20561149da37ef0116f7250f4eb2`  
		Last Modified: Tue, 02 Aug 2022 13:56:05 GMT  
		Size: 323.5 KB (323534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a3313522d23bc6b63456324802c67644e381b81c42eab2a0fd5fccf81b324f`  
		Last Modified: Tue, 02 Aug 2022 13:56:18 GMT  
		Size: 79.6 MB (79603159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e723cb9b102de21090742e561236e03f5e341ca0d0a088210da2a9f7ee0c37b`  
		Last Modified: Tue, 02 Aug 2022 13:56:35 GMT  
		Size: 15.9 MB (15860162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:bc0eeeb1ee5510804a8ab8133fd705d2b03cad8b652fa75b65e42a6091ceb0bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303381184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a152a8065c0a7d864e1c89ff62ee286f491b4bb34e10ca6e23c6e6507f0c78`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:50 GMT
ADD file:c95d34737ba1f11ac8b92be0125aad2baae46448f0d8ebd85ad69076006a3254 in / 
# Tue, 07 Jun 2022 05:50:51 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:19:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:19:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:19:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 10:19:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 10:19:37 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 10:19:37 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 10:19:37 GMT
ENV ROS_DISTRO=noetic
# Tue, 07 Jun 2022 10:22:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:05:37 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 23:05:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 23:05:38 GMT
CMD ["bash"]
# Mon, 11 Jul 2022 23:06:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:06:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 11 Jul 2022 23:07:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:08:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:36754881d0ec0d456ee49776d62f6f0df47d29956ac7b2231b797e05780c6744`  
		Last Modified: Tue, 07 Jun 2022 05:55:05 GMT  
		Size: 24.6 MB (24592639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e21254ce415ea7b490674f4a33c60349d312819e79bd953b7353e3dd7d14fea`  
		Last Modified: Tue, 07 Jun 2022 10:39:01 GMT  
		Size: 1.2 MB (1181840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48aa457454d70347a026cdb39a3d256e0969f6becf1cb485456cd0944fa7965e`  
		Last Modified: Tue, 07 Jun 2022 10:38:59 GMT  
		Size: 4.7 MB (4676394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e672a3b2d46c78712db3b52ed8e3c47a9685c026d512bbf4bf05589aebd337cd`  
		Last Modified: Tue, 07 Jun 2022 10:38:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cac3050647c36fd475eac545b3dc5080db7e9f45e0871805c82cfff88c11326`  
		Last Modified: Tue, 07 Jun 2022 10:38:57 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f262fcc054725c10b56cb064f0fde57d26e36876aa8d0e0f6380250a21a79d`  
		Last Modified: Tue, 07 Jun 2022 10:41:05 GMT  
		Size: 157.4 MB (157415772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b342bdf9b11d603945c520ba34d1eb05324adb5bdcdb8870cba8fa987a2ba9c1`  
		Last Modified: Mon, 11 Jul 2022 23:19:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c046fbf5a031a4fc8b112134fc86acbf0c93d8a6af6da05bcaaf255a7aecf39`  
		Last Modified: Mon, 11 Jul 2022 23:20:11 GMT  
		Size: 40.6 MB (40643256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7af22af4fa6b6b3bb6b3a8bbc9cf2d84563206385cc5fd4d464944fd11e16`  
		Last Modified: Mon, 11 Jul 2022 23:19:48 GMT  
		Size: 322.1 KB (322086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c959d6512be80be43cede75f20500c80a427f01f374fd31e7a7cc562466801`  
		Last Modified: Mon, 11 Jul 2022 23:20:29 GMT  
		Size: 60.5 MB (60482082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa289c2880f665c3c543268ddd1ad35cda3671b682b38f5824306b3756aae84e`  
		Last Modified: Mon, 11 Jul 2022 23:20:55 GMT  
		Size: 14.1 MB (14064697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2363394d63c9226e43f228d4f6b516a73c354406130b4eb794b53417f9e4fc4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.6 MB (337641286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff135b7f4c695d352453bda4841ae8e7de427860245023f07b02fb4e71368dba`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:09:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:09:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:09:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:09:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:06 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:10:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:10:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:10:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:11:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7d1bf2cea5d6a7f0ef5ba787e95aa344e3e67e349bbdcaedd088b0732e48e`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ac26fe78d80a057263cfc59c64582efef7caaa111eb4b639861056cf0df95`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f493394889994de604dd62e022d4827365c0de34ad6cac870ea6af5dca4bba40`  
		Last Modified: Tue, 02 Aug 2022 15:41:50 GMT  
		Size: 171.4 MB (171424725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c191fa5a5fa889fff525b13caa35fb805e0bac7c673aebce455ffc8876fce9`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9227bd4aa30a597598fbc456d5aa784c527937a1f88d2ad2787b48b0ad396d6`  
		Last Modified: Tue, 02 Aug 2022 15:42:10 GMT  
		Size: 45.0 MB (44988903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80df4890a016b37679e242280f4c5981f02725f7e081609daba03d47c99cb3ab`  
		Last Modified: Tue, 02 Aug 2022 15:42:03 GMT  
		Size: 323.5 KB (323472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9700876cb7bd2a4af8a21af304524eafef9645266e38f92be7594dbf40519b67`  
		Last Modified: Tue, 02 Aug 2022 15:42:13 GMT  
		Size: 71.8 MB (71754502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd26413b5f7234b4810d580a8d95d41b71e839575515cae1e1326b6750e1ec62`  
		Last Modified: Tue, 02 Aug 2022 15:42:31 GMT  
		Size: 15.4 MB (15449135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:14d5ec8fa842fd801565297722a674fe9e555e6f833e603054ca75f75faafa63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:e8f1b61cbec3194dc13f0faf022db3c2e07803bca28d4ec936fe2ff3b97bb7ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.8 MB (484836559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6cf2ca2ea29a007ce1ca2d93df94706bc35438815f94ba7e9bb888a33af622`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:14 GMT
ADD file:647206e0e9c1daa306e4ebbdc26c3ef1840dd316ba4ffea905d17b0858e58e34 in / 
# Tue, 02 Aug 2022 01:20:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:22:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:22:51 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 13:22:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:22:52 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:22:53 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:22:53 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 13:23:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:23:57 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:23:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:23:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:24:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:24:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:24:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:25:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7e6a53d1988fa8e19db6bcfc96ee6783afb079c38dbe047528e691815d19a9fa`  
		Last Modified: Tue, 02 Aug 2022 01:24:34 GMT  
		Size: 50.4 MB (50440980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5785ad494f16fd45414b77fd2e2429ebc6d521448ef6d033e1585a5ed6bcbcd1`  
		Last Modified: Tue, 02 Aug 2022 13:58:24 GMT  
		Size: 10.9 MB (10893408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a04cce4da471da7339c364869465ed016774874978f22acce2cc39bb9ead437`  
		Last Modified: Tue, 02 Aug 2022 13:58:22 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b65bdc45a558ffba287816e17e1126b9285c238098635aa3c00f6579301a3b2`  
		Last Modified: Tue, 02 Aug 2022 13:58:22 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c550336ebd94e7da67ecab9e9641d1125ae9892a6e53beb15510cdaeb177d7`  
		Last Modified: Tue, 02 Aug 2022 13:59:01 GMT  
		Size: 239.2 MB (239187767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d7f1bdf1bd7fd0f7d737e9250e43650de8b5e815bd77d8403f6834729f133c`  
		Last Modified: Tue, 02 Aug 2022 13:58:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf730b591358262d29294f063a2a095bb438b736d09b9867750da9a660388827`  
		Last Modified: Tue, 02 Aug 2022 13:59:22 GMT  
		Size: 86.6 MB (86568972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bafa8402824e8fc2746fac433d95ca63c18c25e7157347c220bb275e701214a`  
		Last Modified: Tue, 02 Aug 2022 13:59:09 GMT  
		Size: 317.8 KB (317845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c53a4a6a59b2d6fb99c5aa1d32fd18b873d7c25500236c513a2330680a399a`  
		Last Modified: Tue, 02 Aug 2022 13:59:20 GMT  
		Size: 76.0 MB (75976721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d796c337da0642343ea5e4fda0369b1ee79e95769d0411e42801752f45acac07`  
		Last Modified: Tue, 02 Aug 2022 13:59:33 GMT  
		Size: 21.4 MB (21448452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e54c84be04eef82ae58679a0a59003f583e4e41219a6ea0e425127db199e9936
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.0 MB (423953230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d11199d3c652d0831423c0c814099e2fe9286eb0a0265f63d56097c46f74e3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:49 GMT
ADD file:dfd7e3791fa0512f0f7c9cc8530233d6bc1b0a586a3656fd3950ea386754808a in / 
# Tue, 02 Aug 2022 00:40:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:14:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:14:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:14:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:14:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:14:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:14:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:15:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:15:34 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:15:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:15:37 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:16:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:16:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:17:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:17:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71209d5eb534b9e48223962276993c68559f68e230f73c8a0efc2a2998362bd9`  
		Last Modified: Tue, 02 Aug 2022 00:46:28 GMT  
		Size: 49.2 MB (49229053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e88751172e93002d9fab715ef025cd9a58382c4888b4934c054c6173397dad`  
		Last Modified: Tue, 02 Aug 2022 15:44:04 GMT  
		Size: 10.7 MB (10689284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f0efe68ed19a3b673e70c93625803a8fb308bf11f8888841e81b8d0d6a9744`  
		Last Modified: Tue, 02 Aug 2022 15:44:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4855fcd49a7c12011d55ed482968d218c494e066da8b0e9df0a3ead99e7002ce`  
		Last Modified: Tue, 02 Aug 2022 15:44:03 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bfd4e3998e04572199a3d7bb537f309bc7477561fe26c3ddfed63b62abf3e7`  
		Last Modified: Tue, 02 Aug 2022 15:44:33 GMT  
		Size: 184.4 MB (184372250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f36ec89e9e1541930fa7fcaa7a8f92fcb400ee8fb5a4abcade58343bed9c44`  
		Last Modified: Tue, 02 Aug 2022 15:44:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39030940ae9a93159cb08570c346fd2752db24ffb712e6f3dadb2e60725810de`  
		Last Modified: Tue, 02 Aug 2022 15:44:53 GMT  
		Size: 84.4 MB (84370573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d057e3372b0e330210969889e51a3c9995917b106b06b89795293f5b414ae645`  
		Last Modified: Tue, 02 Aug 2022 15:44:42 GMT  
		Size: 317.8 KB (317803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffbef9b0e37dd10c397077421ef3b79575b972c2dd339ac10d4d57ac18a7d06`  
		Last Modified: Tue, 02 Aug 2022 15:44:51 GMT  
		Size: 73.9 MB (73865318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a645da24b8e418565191ca4f2880cbe42b6bb36b785731e43ed36977b7b63ff`  
		Last Modified: Tue, 02 Aug 2022 15:45:05 GMT  
		Size: 21.1 MB (21106580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:9532f0e7e88172be185b151d832f211dd1f0caa15fa293f3a55c9d46ba4fd095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:db42b54ef7554d262ac6398dfdaf2ceb5d7eb59420f9ae4a23bf6029e921996f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359027107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b091aa21da0fbc744566faba05547001227262d90ab5c67291570aab854a8ae`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 13:10:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:10:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:10:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:10:38 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 13:13:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:13:13 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:13:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:13:13 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:13:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:13:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:16:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3519a1bb471cc6b2b4369f7cd39735754c6744b07b26c3124855dd894dcba45b`  
		Last Modified: Tue, 02 Aug 2022 13:55:14 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e2dfee34126a0fd475079e48bed7166ed0963c44262b6d1c8673a3cc31af08`  
		Last Modified: Tue, 02 Aug 2022 13:55:14 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825e59fe62383c77e16376834caef0bf40982defaf9019928a574c1e90132559`  
		Last Modified: Tue, 02 Aug 2022 13:55:54 GMT  
		Size: 177.0 MB (176996918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55778ffb7b3f4c8289907a297c07ad6b31e1c7ea5a410a5414c408630273346c`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7e3c098d974561c8914411584759f9ec5ac5489735340137cb61a5ed6dfdca`  
		Last Modified: Tue, 02 Aug 2022 13:56:14 GMT  
		Size: 50.9 MB (50940142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde62a097a809942e493ede6b058a2b1af7c20561149da37ef0116f7250f4eb2`  
		Last Modified: Tue, 02 Aug 2022 13:56:05 GMT  
		Size: 323.5 KB (323534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a3313522d23bc6b63456324802c67644e381b81c42eab2a0fd5fccf81b324f`  
		Last Modified: Tue, 02 Aug 2022 13:56:18 GMT  
		Size: 79.6 MB (79603159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e723cb9b102de21090742e561236e03f5e341ca0d0a088210da2a9f7ee0c37b`  
		Last Modified: Tue, 02 Aug 2022 13:56:35 GMT  
		Size: 15.9 MB (15860162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:bc0eeeb1ee5510804a8ab8133fd705d2b03cad8b652fa75b65e42a6091ceb0bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303381184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a152a8065c0a7d864e1c89ff62ee286f491b4bb34e10ca6e23c6e6507f0c78`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:50 GMT
ADD file:c95d34737ba1f11ac8b92be0125aad2baae46448f0d8ebd85ad69076006a3254 in / 
# Tue, 07 Jun 2022 05:50:51 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:19:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:19:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:19:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 10:19:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 10:19:37 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 10:19:37 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 10:19:37 GMT
ENV ROS_DISTRO=noetic
# Tue, 07 Jun 2022 10:22:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:05:37 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 23:05:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 23:05:38 GMT
CMD ["bash"]
# Mon, 11 Jul 2022 23:06:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:06:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 11 Jul 2022 23:07:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:08:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:36754881d0ec0d456ee49776d62f6f0df47d29956ac7b2231b797e05780c6744`  
		Last Modified: Tue, 07 Jun 2022 05:55:05 GMT  
		Size: 24.6 MB (24592639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e21254ce415ea7b490674f4a33c60349d312819e79bd953b7353e3dd7d14fea`  
		Last Modified: Tue, 07 Jun 2022 10:39:01 GMT  
		Size: 1.2 MB (1181840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48aa457454d70347a026cdb39a3d256e0969f6becf1cb485456cd0944fa7965e`  
		Last Modified: Tue, 07 Jun 2022 10:38:59 GMT  
		Size: 4.7 MB (4676394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e672a3b2d46c78712db3b52ed8e3c47a9685c026d512bbf4bf05589aebd337cd`  
		Last Modified: Tue, 07 Jun 2022 10:38:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cac3050647c36fd475eac545b3dc5080db7e9f45e0871805c82cfff88c11326`  
		Last Modified: Tue, 07 Jun 2022 10:38:57 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f262fcc054725c10b56cb064f0fde57d26e36876aa8d0e0f6380250a21a79d`  
		Last Modified: Tue, 07 Jun 2022 10:41:05 GMT  
		Size: 157.4 MB (157415772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b342bdf9b11d603945c520ba34d1eb05324adb5bdcdb8870cba8fa987a2ba9c1`  
		Last Modified: Mon, 11 Jul 2022 23:19:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c046fbf5a031a4fc8b112134fc86acbf0c93d8a6af6da05bcaaf255a7aecf39`  
		Last Modified: Mon, 11 Jul 2022 23:20:11 GMT  
		Size: 40.6 MB (40643256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7af22af4fa6b6b3bb6b3a8bbc9cf2d84563206385cc5fd4d464944fd11e16`  
		Last Modified: Mon, 11 Jul 2022 23:19:48 GMT  
		Size: 322.1 KB (322086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c959d6512be80be43cede75f20500c80a427f01f374fd31e7a7cc562466801`  
		Last Modified: Mon, 11 Jul 2022 23:20:29 GMT  
		Size: 60.5 MB (60482082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa289c2880f665c3c543268ddd1ad35cda3671b682b38f5824306b3756aae84e`  
		Last Modified: Mon, 11 Jul 2022 23:20:55 GMT  
		Size: 14.1 MB (14064697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2363394d63c9226e43f228d4f6b516a73c354406130b4eb794b53417f9e4fc4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.6 MB (337641286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff135b7f4c695d352453bda4841ae8e7de427860245023f07b02fb4e71368dba`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:09:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:09:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:09:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:09:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:06 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:10:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:10:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:10:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:11:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7d1bf2cea5d6a7f0ef5ba787e95aa344e3e67e349bbdcaedd088b0732e48e`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ac26fe78d80a057263cfc59c64582efef7caaa111eb4b639861056cf0df95`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f493394889994de604dd62e022d4827365c0de34ad6cac870ea6af5dca4bba40`  
		Last Modified: Tue, 02 Aug 2022 15:41:50 GMT  
		Size: 171.4 MB (171424725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c191fa5a5fa889fff525b13caa35fb805e0bac7c673aebce455ffc8876fce9`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9227bd4aa30a597598fbc456d5aa784c527937a1f88d2ad2787b48b0ad396d6`  
		Last Modified: Tue, 02 Aug 2022 15:42:10 GMT  
		Size: 45.0 MB (44988903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80df4890a016b37679e242280f4c5981f02725f7e081609daba03d47c99cb3ab`  
		Last Modified: Tue, 02 Aug 2022 15:42:03 GMT  
		Size: 323.5 KB (323472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9700876cb7bd2a4af8a21af304524eafef9645266e38f92be7594dbf40519b67`  
		Last Modified: Tue, 02 Aug 2022 15:42:13 GMT  
		Size: 71.8 MB (71754502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd26413b5f7234b4810d580a8d95d41b71e839575515cae1e1326b6750e1ec62`  
		Last Modified: Tue, 02 Aug 2022 15:42:31 GMT  
		Size: 15.4 MB (15449135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:0b1508eb22177b9a5d0999f1071a3a468fd6f192c7b3b0915ef0402efa8d5562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:8d5b98bb3e6cdc51c8fc846c701c121f937ede2bd2b6986b6a42f962ccf9cb0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343166945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4252b5fd978bbce4290a3ed3989114693e03ae35cbcfb5bd24693c5808956cdd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 13:10:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:10:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:10:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:10:38 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 13:13:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:13:13 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:13:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:13:13 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:13:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:13:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3519a1bb471cc6b2b4369f7cd39735754c6744b07b26c3124855dd894dcba45b`  
		Last Modified: Tue, 02 Aug 2022 13:55:14 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e2dfee34126a0fd475079e48bed7166ed0963c44262b6d1c8673a3cc31af08`  
		Last Modified: Tue, 02 Aug 2022 13:55:14 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825e59fe62383c77e16376834caef0bf40982defaf9019928a574c1e90132559`  
		Last Modified: Tue, 02 Aug 2022 13:55:54 GMT  
		Size: 177.0 MB (176996918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55778ffb7b3f4c8289907a297c07ad6b31e1c7ea5a410a5414c408630273346c`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7e3c098d974561c8914411584759f9ec5ac5489735340137cb61a5ed6dfdca`  
		Last Modified: Tue, 02 Aug 2022 13:56:14 GMT  
		Size: 50.9 MB (50940142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde62a097a809942e493ede6b058a2b1af7c20561149da37ef0116f7250f4eb2`  
		Last Modified: Tue, 02 Aug 2022 13:56:05 GMT  
		Size: 323.5 KB (323534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a3313522d23bc6b63456324802c67644e381b81c42eab2a0fd5fccf81b324f`  
		Last Modified: Tue, 02 Aug 2022 13:56:18 GMT  
		Size: 79.6 MB (79603159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:10c289835b4ac749b2d4211b9698472cb67b083ae60ccf55992469f7a9796985
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289316487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa56e91bb12af2d6dec2e4a46b6e8c32723fe510d3f042f08cdbb3850380181`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:50 GMT
ADD file:c95d34737ba1f11ac8b92be0125aad2baae46448f0d8ebd85ad69076006a3254 in / 
# Tue, 07 Jun 2022 05:50:51 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:19:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:19:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:19:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 10:19:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 10:19:37 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 10:19:37 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 10:19:37 GMT
ENV ROS_DISTRO=noetic
# Tue, 07 Jun 2022 10:22:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:05:37 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 23:05:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 23:05:38 GMT
CMD ["bash"]
# Mon, 11 Jul 2022 23:06:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:06:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 11 Jul 2022 23:07:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:36754881d0ec0d456ee49776d62f6f0df47d29956ac7b2231b797e05780c6744`  
		Last Modified: Tue, 07 Jun 2022 05:55:05 GMT  
		Size: 24.6 MB (24592639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e21254ce415ea7b490674f4a33c60349d312819e79bd953b7353e3dd7d14fea`  
		Last Modified: Tue, 07 Jun 2022 10:39:01 GMT  
		Size: 1.2 MB (1181840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48aa457454d70347a026cdb39a3d256e0969f6becf1cb485456cd0944fa7965e`  
		Last Modified: Tue, 07 Jun 2022 10:38:59 GMT  
		Size: 4.7 MB (4676394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e672a3b2d46c78712db3b52ed8e3c47a9685c026d512bbf4bf05589aebd337cd`  
		Last Modified: Tue, 07 Jun 2022 10:38:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cac3050647c36fd475eac545b3dc5080db7e9f45e0871805c82cfff88c11326`  
		Last Modified: Tue, 07 Jun 2022 10:38:57 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f262fcc054725c10b56cb064f0fde57d26e36876aa8d0e0f6380250a21a79d`  
		Last Modified: Tue, 07 Jun 2022 10:41:05 GMT  
		Size: 157.4 MB (157415772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b342bdf9b11d603945c520ba34d1eb05324adb5bdcdb8870cba8fa987a2ba9c1`  
		Last Modified: Mon, 11 Jul 2022 23:19:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c046fbf5a031a4fc8b112134fc86acbf0c93d8a6af6da05bcaaf255a7aecf39`  
		Last Modified: Mon, 11 Jul 2022 23:20:11 GMT  
		Size: 40.6 MB (40643256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7af22af4fa6b6b3bb6b3a8bbc9cf2d84563206385cc5fd4d464944fd11e16`  
		Last Modified: Mon, 11 Jul 2022 23:19:48 GMT  
		Size: 322.1 KB (322086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c959d6512be80be43cede75f20500c80a427f01f374fd31e7a7cc562466801`  
		Last Modified: Mon, 11 Jul 2022 23:20:29 GMT  
		Size: 60.5 MB (60482082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8d2c3160385c2f5a6449fff4905f7290543a28713ffc6e1550747d5e0dcdb0ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322192151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108358074c3289edba33e14e8130004770bde5dd9106d446db28dd2548498a48`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:09:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:09:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:09:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:09:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:06 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:10:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:10:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:10:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7d1bf2cea5d6a7f0ef5ba787e95aa344e3e67e349bbdcaedd088b0732e48e`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ac26fe78d80a057263cfc59c64582efef7caaa111eb4b639861056cf0df95`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f493394889994de604dd62e022d4827365c0de34ad6cac870ea6af5dca4bba40`  
		Last Modified: Tue, 02 Aug 2022 15:41:50 GMT  
		Size: 171.4 MB (171424725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c191fa5a5fa889fff525b13caa35fb805e0bac7c673aebce455ffc8876fce9`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9227bd4aa30a597598fbc456d5aa784c527937a1f88d2ad2787b48b0ad396d6`  
		Last Modified: Tue, 02 Aug 2022 15:42:10 GMT  
		Size: 45.0 MB (44988903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80df4890a016b37679e242280f4c5981f02725f7e081609daba03d47c99cb3ab`  
		Last Modified: Tue, 02 Aug 2022 15:42:03 GMT  
		Size: 323.5 KB (323472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9700876cb7bd2a4af8a21af304524eafef9645266e38f92be7594dbf40519b67`  
		Last Modified: Tue, 02 Aug 2022 15:42:13 GMT  
		Size: 71.8 MB (71754502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:3079c4ae9bcc96785297b478364d1819f4406ca648f6b2e6e115fd25cf1c38fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:32e776592bc2676b559eca78d2cf447adbcf153aba7909c290e078933a9560f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.4 MB (463388107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6305a3b060b8ef21af857817efc0baa81168a01e75c72530e57380b0f89605e3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:14 GMT
ADD file:647206e0e9c1daa306e4ebbdc26c3ef1840dd316ba4ffea905d17b0858e58e34 in / 
# Tue, 02 Aug 2022 01:20:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:22:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:22:51 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 13:22:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:22:52 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:22:53 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:22:53 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 13:23:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:23:57 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:23:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:23:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:24:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:24:30 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:24:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7e6a53d1988fa8e19db6bcfc96ee6783afb079c38dbe047528e691815d19a9fa`  
		Last Modified: Tue, 02 Aug 2022 01:24:34 GMT  
		Size: 50.4 MB (50440980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5785ad494f16fd45414b77fd2e2429ebc6d521448ef6d033e1585a5ed6bcbcd1`  
		Last Modified: Tue, 02 Aug 2022 13:58:24 GMT  
		Size: 10.9 MB (10893408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a04cce4da471da7339c364869465ed016774874978f22acce2cc39bb9ead437`  
		Last Modified: Tue, 02 Aug 2022 13:58:22 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b65bdc45a558ffba287816e17e1126b9285c238098635aa3c00f6579301a3b2`  
		Last Modified: Tue, 02 Aug 2022 13:58:22 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c550336ebd94e7da67ecab9e9641d1125ae9892a6e53beb15510cdaeb177d7`  
		Last Modified: Tue, 02 Aug 2022 13:59:01 GMT  
		Size: 239.2 MB (239187767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d7f1bdf1bd7fd0f7d737e9250e43650de8b5e815bd77d8403f6834729f133c`  
		Last Modified: Tue, 02 Aug 2022 13:58:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf730b591358262d29294f063a2a095bb438b736d09b9867750da9a660388827`  
		Last Modified: Tue, 02 Aug 2022 13:59:22 GMT  
		Size: 86.6 MB (86568972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bafa8402824e8fc2746fac433d95ca63c18c25e7157347c220bb275e701214a`  
		Last Modified: Tue, 02 Aug 2022 13:59:09 GMT  
		Size: 317.8 KB (317845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c53a4a6a59b2d6fb99c5aa1d32fd18b873d7c25500236c513a2330680a399a`  
		Last Modified: Tue, 02 Aug 2022 13:59:20 GMT  
		Size: 76.0 MB (75976721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a38107b726611e43727c1b2e7229b39feaf72241daca46d4a4c47ac8d41f18d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.8 MB (402846650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd65edd326af89df0190f60b846bb6d458749f8e84780a72e3c54c4c832bec8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:49 GMT
ADD file:dfd7e3791fa0512f0f7c9cc8530233d6bc1b0a586a3656fd3950ea386754808a in / 
# Tue, 02 Aug 2022 00:40:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:14:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:14:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:14:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:14:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:14:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:14:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:15:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:15:34 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:15:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:15:37 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:16:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:16:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:17:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71209d5eb534b9e48223962276993c68559f68e230f73c8a0efc2a2998362bd9`  
		Last Modified: Tue, 02 Aug 2022 00:46:28 GMT  
		Size: 49.2 MB (49229053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e88751172e93002d9fab715ef025cd9a58382c4888b4934c054c6173397dad`  
		Last Modified: Tue, 02 Aug 2022 15:44:04 GMT  
		Size: 10.7 MB (10689284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f0efe68ed19a3b673e70c93625803a8fb308bf11f8888841e81b8d0d6a9744`  
		Last Modified: Tue, 02 Aug 2022 15:44:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4855fcd49a7c12011d55ed482968d218c494e066da8b0e9df0a3ead99e7002ce`  
		Last Modified: Tue, 02 Aug 2022 15:44:03 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bfd4e3998e04572199a3d7bb537f309bc7477561fe26c3ddfed63b62abf3e7`  
		Last Modified: Tue, 02 Aug 2022 15:44:33 GMT  
		Size: 184.4 MB (184372250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f36ec89e9e1541930fa7fcaa7a8f92fcb400ee8fb5a4abcade58343bed9c44`  
		Last Modified: Tue, 02 Aug 2022 15:44:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39030940ae9a93159cb08570c346fd2752db24ffb712e6f3dadb2e60725810de`  
		Last Modified: Tue, 02 Aug 2022 15:44:53 GMT  
		Size: 84.4 MB (84370573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d057e3372b0e330210969889e51a3c9995917b106b06b89795293f5b414ae645`  
		Last Modified: Tue, 02 Aug 2022 15:44:42 GMT  
		Size: 317.8 KB (317803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffbef9b0e37dd10c397077421ef3b79575b972c2dd339ac10d4d57ac18a7d06`  
		Last Modified: Tue, 02 Aug 2022 15:44:51 GMT  
		Size: 73.9 MB (73865318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:0b1508eb22177b9a5d0999f1071a3a468fd6f192c7b3b0915ef0402efa8d5562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:8d5b98bb3e6cdc51c8fc846c701c121f937ede2bd2b6986b6a42f962ccf9cb0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343166945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4252b5fd978bbce4290a3ed3989114693e03ae35cbcfb5bd24693c5808956cdd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 13:10:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:10:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:10:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:10:38 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 13:13:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:13:13 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:13:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:13:13 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:13:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:13:58 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3519a1bb471cc6b2b4369f7cd39735754c6744b07b26c3124855dd894dcba45b`  
		Last Modified: Tue, 02 Aug 2022 13:55:14 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e2dfee34126a0fd475079e48bed7166ed0963c44262b6d1c8673a3cc31af08`  
		Last Modified: Tue, 02 Aug 2022 13:55:14 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825e59fe62383c77e16376834caef0bf40982defaf9019928a574c1e90132559`  
		Last Modified: Tue, 02 Aug 2022 13:55:54 GMT  
		Size: 177.0 MB (176996918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55778ffb7b3f4c8289907a297c07ad6b31e1c7ea5a410a5414c408630273346c`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7e3c098d974561c8914411584759f9ec5ac5489735340137cb61a5ed6dfdca`  
		Last Modified: Tue, 02 Aug 2022 13:56:14 GMT  
		Size: 50.9 MB (50940142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde62a097a809942e493ede6b058a2b1af7c20561149da37ef0116f7250f4eb2`  
		Last Modified: Tue, 02 Aug 2022 13:56:05 GMT  
		Size: 323.5 KB (323534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a3313522d23bc6b63456324802c67644e381b81c42eab2a0fd5fccf81b324f`  
		Last Modified: Tue, 02 Aug 2022 13:56:18 GMT  
		Size: 79.6 MB (79603159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:10c289835b4ac749b2d4211b9698472cb67b083ae60ccf55992469f7a9796985
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289316487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa56e91bb12af2d6dec2e4a46b6e8c32723fe510d3f042f08cdbb3850380181`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:50 GMT
ADD file:c95d34737ba1f11ac8b92be0125aad2baae46448f0d8ebd85ad69076006a3254 in / 
# Tue, 07 Jun 2022 05:50:51 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:19:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:19:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:19:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 10:19:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 10:19:37 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 10:19:37 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 10:19:37 GMT
ENV ROS_DISTRO=noetic
# Tue, 07 Jun 2022 10:22:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:05:37 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 23:05:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 23:05:38 GMT
CMD ["bash"]
# Mon, 11 Jul 2022 23:06:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:06:29 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Mon, 11 Jul 2022 23:07:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:36754881d0ec0d456ee49776d62f6f0df47d29956ac7b2231b797e05780c6744`  
		Last Modified: Tue, 07 Jun 2022 05:55:05 GMT  
		Size: 24.6 MB (24592639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e21254ce415ea7b490674f4a33c60349d312819e79bd953b7353e3dd7d14fea`  
		Last Modified: Tue, 07 Jun 2022 10:39:01 GMT  
		Size: 1.2 MB (1181840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48aa457454d70347a026cdb39a3d256e0969f6becf1cb485456cd0944fa7965e`  
		Last Modified: Tue, 07 Jun 2022 10:38:59 GMT  
		Size: 4.7 MB (4676394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e672a3b2d46c78712db3b52ed8e3c47a9685c026d512bbf4bf05589aebd337cd`  
		Last Modified: Tue, 07 Jun 2022 10:38:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cac3050647c36fd475eac545b3dc5080db7e9f45e0871805c82cfff88c11326`  
		Last Modified: Tue, 07 Jun 2022 10:38:57 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f262fcc054725c10b56cb064f0fde57d26e36876aa8d0e0f6380250a21a79d`  
		Last Modified: Tue, 07 Jun 2022 10:41:05 GMT  
		Size: 157.4 MB (157415772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b342bdf9b11d603945c520ba34d1eb05324adb5bdcdb8870cba8fa987a2ba9c1`  
		Last Modified: Mon, 11 Jul 2022 23:19:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c046fbf5a031a4fc8b112134fc86acbf0c93d8a6af6da05bcaaf255a7aecf39`  
		Last Modified: Mon, 11 Jul 2022 23:20:11 GMT  
		Size: 40.6 MB (40643256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7af22af4fa6b6b3bb6b3a8bbc9cf2d84563206385cc5fd4d464944fd11e16`  
		Last Modified: Mon, 11 Jul 2022 23:19:48 GMT  
		Size: 322.1 KB (322086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c959d6512be80be43cede75f20500c80a427f01f374fd31e7a7cc562466801`  
		Last Modified: Mon, 11 Jul 2022 23:20:29 GMT  
		Size: 60.5 MB (60482082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8d2c3160385c2f5a6449fff4905f7290543a28713ffc6e1550747d5e0dcdb0ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322192151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108358074c3289edba33e14e8130004770bde5dd9106d446db28dd2548498a48`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:09:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:09:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:09:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:09:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:06 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:10:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:10:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:10:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7d1bf2cea5d6a7f0ef5ba787e95aa344e3e67e349bbdcaedd088b0732e48e`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ac26fe78d80a057263cfc59c64582efef7caaa111eb4b639861056cf0df95`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f493394889994de604dd62e022d4827365c0de34ad6cac870ea6af5dca4bba40`  
		Last Modified: Tue, 02 Aug 2022 15:41:50 GMT  
		Size: 171.4 MB (171424725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c191fa5a5fa889fff525b13caa35fb805e0bac7c673aebce455ffc8876fce9`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9227bd4aa30a597598fbc456d5aa784c527937a1f88d2ad2787b48b0ad396d6`  
		Last Modified: Tue, 02 Aug 2022 15:42:10 GMT  
		Size: 45.0 MB (44988903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80df4890a016b37679e242280f4c5981f02725f7e081609daba03d47c99cb3ab`  
		Last Modified: Tue, 02 Aug 2022 15:42:03 GMT  
		Size: 323.5 KB (323472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9700876cb7bd2a4af8a21af304524eafef9645266e38f92be7594dbf40519b67`  
		Last Modified: Tue, 02 Aug 2022 15:42:13 GMT  
		Size: 71.8 MB (71754502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:c631f90aa2dcfd3783c8e5f1095f43389193f19e1de9b32060e0d7878bf04e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:f80841523cc91af7ef9077abfefc7fc19a747af308b8cb6212085143c1189857
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212300110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a999dffc35e8802f5fb8e6cd81393c4d886ffd5883dabb15dec8cd887cba6c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 13:10:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:10:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:10:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:10:38 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 13:13:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:13:13 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:13:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:13:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3519a1bb471cc6b2b4369f7cd39735754c6744b07b26c3124855dd894dcba45b`  
		Last Modified: Tue, 02 Aug 2022 13:55:14 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e2dfee34126a0fd475079e48bed7166ed0963c44262b6d1c8673a3cc31af08`  
		Last Modified: Tue, 02 Aug 2022 13:55:14 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825e59fe62383c77e16376834caef0bf40982defaf9019928a574c1e90132559`  
		Last Modified: Tue, 02 Aug 2022 13:55:54 GMT  
		Size: 177.0 MB (176996918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55778ffb7b3f4c8289907a297c07ad6b31e1c7ea5a410a5414c408630273346c`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:2dc3de859007570553d6bd5d715a48c60f88f9c47d938a861e2175019a657e0e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187869063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afed666955632165dca98a067f844d7786b139273224e4c9d1adc88d2cdd4496`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:50 GMT
ADD file:c95d34737ba1f11ac8b92be0125aad2baae46448f0d8ebd85ad69076006a3254 in / 
# Tue, 07 Jun 2022 05:50:51 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:19:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:19:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:19:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 10:19:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 10:19:37 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 10:19:37 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 10:19:37 GMT
ENV ROS_DISTRO=noetic
# Tue, 07 Jun 2022 10:22:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:05:37 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 23:05:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 23:05:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:36754881d0ec0d456ee49776d62f6f0df47d29956ac7b2231b797e05780c6744`  
		Last Modified: Tue, 07 Jun 2022 05:55:05 GMT  
		Size: 24.6 MB (24592639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e21254ce415ea7b490674f4a33c60349d312819e79bd953b7353e3dd7d14fea`  
		Last Modified: Tue, 07 Jun 2022 10:39:01 GMT  
		Size: 1.2 MB (1181840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48aa457454d70347a026cdb39a3d256e0969f6becf1cb485456cd0944fa7965e`  
		Last Modified: Tue, 07 Jun 2022 10:38:59 GMT  
		Size: 4.7 MB (4676394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e672a3b2d46c78712db3b52ed8e3c47a9685c026d512bbf4bf05589aebd337cd`  
		Last Modified: Tue, 07 Jun 2022 10:38:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cac3050647c36fd475eac545b3dc5080db7e9f45e0871805c82cfff88c11326`  
		Last Modified: Tue, 07 Jun 2022 10:38:57 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f262fcc054725c10b56cb064f0fde57d26e36876aa8d0e0f6380250a21a79d`  
		Last Modified: Tue, 07 Jun 2022 10:41:05 GMT  
		Size: 157.4 MB (157415772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b342bdf9b11d603945c520ba34d1eb05324adb5bdcdb8870cba8fa987a2ba9c1`  
		Last Modified: Mon, 11 Jul 2022 23:19:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2de7b235c0f81dd7f2400b18a72f2e37c2eaff057a552ff4018d27b6e9283537
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205125274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef973504c6d304f7f2ee2f0be2414109ac868cf40926997b3d262097d2c63aa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:09:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:09:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:09:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:09:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:06 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:10:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:10:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7d1bf2cea5d6a7f0ef5ba787e95aa344e3e67e349bbdcaedd088b0732e48e`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ac26fe78d80a057263cfc59c64582efef7caaa111eb4b639861056cf0df95`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f493394889994de604dd62e022d4827365c0de34ad6cac870ea6af5dca4bba40`  
		Last Modified: Tue, 02 Aug 2022 15:41:50 GMT  
		Size: 171.4 MB (171424725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c191fa5a5fa889fff525b13caa35fb805e0bac7c673aebce455ffc8876fce9`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:84693dbdf2847f740b584229ebd3bfbebf411ea7e450a61f5272ca468b260a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:670d0f8f29324f5d15fe53c99f4cb268133580585924b92428ead3dc0dfb429e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300524569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a45164c156c820452f2bc1aa5c01e542e53f15a8349fa258fd4ee1197c5e1b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:14 GMT
ADD file:647206e0e9c1daa306e4ebbdc26c3ef1840dd316ba4ffea905d17b0858e58e34 in / 
# Tue, 02 Aug 2022 01:20:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:22:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:22:51 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 13:22:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:22:52 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:22:53 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:22:53 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 13:23:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:23:57 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:23:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:23:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7e6a53d1988fa8e19db6bcfc96ee6783afb079c38dbe047528e691815d19a9fa`  
		Last Modified: Tue, 02 Aug 2022 01:24:34 GMT  
		Size: 50.4 MB (50440980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5785ad494f16fd45414b77fd2e2429ebc6d521448ef6d033e1585a5ed6bcbcd1`  
		Last Modified: Tue, 02 Aug 2022 13:58:24 GMT  
		Size: 10.9 MB (10893408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a04cce4da471da7339c364869465ed016774874978f22acce2cc39bb9ead437`  
		Last Modified: Tue, 02 Aug 2022 13:58:22 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b65bdc45a558ffba287816e17e1126b9285c238098635aa3c00f6579301a3b2`  
		Last Modified: Tue, 02 Aug 2022 13:58:22 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c550336ebd94e7da67ecab9e9641d1125ae9892a6e53beb15510cdaeb177d7`  
		Last Modified: Tue, 02 Aug 2022 13:59:01 GMT  
		Size: 239.2 MB (239187767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d7f1bdf1bd7fd0f7d737e9250e43650de8b5e815bd77d8403f6834729f133c`  
		Last Modified: Tue, 02 Aug 2022 13:58:22 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c8162efc3fd26d1b5852c27967ec46955932f12ef40b64f120342a1183162644
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244292956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4dc8001330440dfc00997bb6dad496313c61b61d3c1a7f3f098b5165e8ed28`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:49 GMT
ADD file:dfd7e3791fa0512f0f7c9cc8530233d6bc1b0a586a3656fd3950ea386754808a in / 
# Tue, 02 Aug 2022 00:40:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:14:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:14:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:14:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:14:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:14:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:14:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:15:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:15:34 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:15:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:15:37 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:71209d5eb534b9e48223962276993c68559f68e230f73c8a0efc2a2998362bd9`  
		Last Modified: Tue, 02 Aug 2022 00:46:28 GMT  
		Size: 49.2 MB (49229053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e88751172e93002d9fab715ef025cd9a58382c4888b4934c054c6173397dad`  
		Last Modified: Tue, 02 Aug 2022 15:44:04 GMT  
		Size: 10.7 MB (10689284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f0efe68ed19a3b673e70c93625803a8fb308bf11f8888841e81b8d0d6a9744`  
		Last Modified: Tue, 02 Aug 2022 15:44:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4855fcd49a7c12011d55ed482968d218c494e066da8b0e9df0a3ead99e7002ce`  
		Last Modified: Tue, 02 Aug 2022 15:44:03 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bfd4e3998e04572199a3d7bb537f309bc7477561fe26c3ddfed63b62abf3e7`  
		Last Modified: Tue, 02 Aug 2022 15:44:33 GMT  
		Size: 184.4 MB (184372250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f36ec89e9e1541930fa7fcaa7a8f92fcb400ee8fb5a4abcade58343bed9c44`  
		Last Modified: Tue, 02 Aug 2022 15:44:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:c631f90aa2dcfd3783c8e5f1095f43389193f19e1de9b32060e0d7878bf04e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:f80841523cc91af7ef9077abfefc7fc19a747af308b8cb6212085143c1189857
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212300110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a999dffc35e8802f5fb8e6cd81393c4d886ffd5883dabb15dec8cd887cba6c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:10:15 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:10:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 13:10:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:10:38 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:10:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:10:38 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 13:13:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:13:13 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 13:13:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:13:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f991215ddc16cd6d5839a01c05ba58b96914830f35c25d3d72e0495b053e7`  
		Last Modified: Tue, 02 Aug 2022 13:55:17 GMT  
		Size: 1.2 MB (1181319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aedc0c69710a5bf5069bd2509080fc6d8b47b7f817d02eb6b5c420be6abe69e`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 5.5 MB (5546864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3519a1bb471cc6b2b4369f7cd39735754c6744b07b26c3124855dd894dcba45b`  
		Last Modified: Tue, 02 Aug 2022 13:55:14 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e2dfee34126a0fd475079e48bed7166ed0963c44262b6d1c8673a3cc31af08`  
		Last Modified: Tue, 02 Aug 2022 13:55:14 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825e59fe62383c77e16376834caef0bf40982defaf9019928a574c1e90132559`  
		Last Modified: Tue, 02 Aug 2022 13:55:54 GMT  
		Size: 177.0 MB (176996918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55778ffb7b3f4c8289907a297c07ad6b31e1c7ea5a410a5414c408630273346c`  
		Last Modified: Tue, 02 Aug 2022 13:55:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:2dc3de859007570553d6bd5d715a48c60f88f9c47d938a861e2175019a657e0e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187869063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afed666955632165dca98a067f844d7786b139273224e4c9d1adc88d2cdd4496`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Jun 2022 05:50:50 GMT
ADD file:c95d34737ba1f11ac8b92be0125aad2baae46448f0d8ebd85ad69076006a3254 in / 
# Tue, 07 Jun 2022 05:50:51 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:19:14 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:19:32 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:19:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 07 Jun 2022 10:19:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jun 2022 10:19:37 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jun 2022 10:19:37 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jun 2022 10:19:37 GMT
ENV ROS_DISTRO=noetic
# Tue, 07 Jun 2022 10:22:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Mon, 11 Jul 2022 23:05:37 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Mon, 11 Jul 2022 23:05:37 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Mon, 11 Jul 2022 23:05:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:36754881d0ec0d456ee49776d62f6f0df47d29956ac7b2231b797e05780c6744`  
		Last Modified: Tue, 07 Jun 2022 05:55:05 GMT  
		Size: 24.6 MB (24592639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e21254ce415ea7b490674f4a33c60349d312819e79bd953b7353e3dd7d14fea`  
		Last Modified: Tue, 07 Jun 2022 10:39:01 GMT  
		Size: 1.2 MB (1181840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48aa457454d70347a026cdb39a3d256e0969f6becf1cb485456cd0944fa7965e`  
		Last Modified: Tue, 07 Jun 2022 10:38:59 GMT  
		Size: 4.7 MB (4676394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e672a3b2d46c78712db3b52ed8e3c47a9685c026d512bbf4bf05589aebd337cd`  
		Last Modified: Tue, 07 Jun 2022 10:38:57 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cac3050647c36fd475eac545b3dc5080db7e9f45e0871805c82cfff88c11326`  
		Last Modified: Tue, 07 Jun 2022 10:38:57 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f262fcc054725c10b56cb064f0fde57d26e36876aa8d0e0f6380250a21a79d`  
		Last Modified: Tue, 07 Jun 2022 10:41:05 GMT  
		Size: 157.4 MB (157415772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b342bdf9b11d603945c520ba34d1eb05324adb5bdcdb8870cba8fa987a2ba9c1`  
		Last Modified: Mon, 11 Jul 2022 23:19:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2de7b235c0f81dd7f2400b18a72f2e37c2eaff057a552ff4018d27b6e9283537
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205125274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef973504c6d304f7f2ee2f0be2414109ac868cf40926997b3d262097d2c63aa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:09:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:09:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:09:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:09:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:06 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:10:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:10:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7d1bf2cea5d6a7f0ef5ba787e95aa344e3e67e349bbdcaedd088b0732e48e`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ac26fe78d80a057263cfc59c64582efef7caaa111eb4b639861056cf0df95`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f493394889994de604dd62e022d4827365c0de34ad6cac870ea6af5dca4bba40`  
		Last Modified: Tue, 02 Aug 2022 15:41:50 GMT  
		Size: 171.4 MB (171424725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c191fa5a5fa889fff525b13caa35fb805e0bac7c673aebce455ffc8876fce9`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling`

```console
$ docker pull ros@sha256:7985aeeda183ce1c7007d64744dfd5c116775d299928ecacd434d07fb406c987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:1e42f8cff90e1fe6f91c315155558ac618950e5e4731d2a72e5dfbfc65f48cd2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262740229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6246126d845d013b52c92c6b65936c428b8be255234df72ebcfcf1c1f03e543c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:35:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:57 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:35:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:48:06 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 13:48:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:48:47 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:48:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:48:47 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:49:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:49:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:49:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:49:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5bfc5848603bd668295b5a975d71c189291f87f6598cf6dc5205c57efdc41f`  
		Last Modified: Tue, 02 Aug 2022 14:04:13 GMT  
		Size: 1.2 MB (1192245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c425ff1dadf43c340925189568bc8f392e60eec7d53b401bb72a710aa66135c`  
		Last Modified: Tue, 02 Aug 2022 14:04:11 GMT  
		Size: 3.8 MB (3827758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eae6de5e53443906b64a12ebc086b149ea851be37c5c514c6a4b7d1446ac6e`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b619038cdfe7b8c10e6820e8ebbfc5b3ab2e7bff0008f9498e10f48a3948ca`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98307263b57b763e56c78ed4978fa903e4c666a7325e21a7132d9c8b11af102`  
		Last Modified: Tue, 02 Aug 2022 14:07:41 GMT  
		Size: 106.1 MB (106129329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07757fc5de68a9df5480ba8f62ed87206a92fd8291df9bddf5af6845d93377`  
		Last Modified: Tue, 02 Aug 2022 14:07:23 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff0935d6a9511b200b27c5e9f331aee4eeaadbb48bc5ab7245a79bcdd3118d0`  
		Last Modified: Tue, 02 Aug 2022 14:08:04 GMT  
		Size: 97.8 MB (97848772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf60bc9e016c3e91c6eb945fbde5a87a0db5a195074bbb797f63d4a94984261`  
		Last Modified: Tue, 02 Aug 2022 14:07:51 GMT  
		Size: 278.5 KB (278534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc5652973b10726d1359e04fc71fb0b9fd788a5a58fa9b5b026eb18d51cce52`  
		Last Modified: Tue, 02 Aug 2022 14:07:51 GMT  
		Size: 2.2 KB (2249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca36f6a376ef84b96010be932950ac3aa2c71be3fe02aedef3635a449397bba`  
		Last Modified: Tue, 02 Aug 2022 14:07:54 GMT  
		Size: 23.0 MB (23032792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:566852956ea3fc90533a5cc44c021d66b0693c4b85ae92313ee24a1ef567c481
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254967875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd12507a1529223aa1d1c513771d5b2cacd63d1157d0fe6ee02c9b4c1bb00a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:32:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 15:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:12 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:33:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:33:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:33:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:33:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:34:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c096920dab8b763106ab108f7f67ffd78e3a0a5b90062661f6e79ba6e5531450`  
		Last Modified: Tue, 02 Aug 2022 15:52:21 GMT  
		Size: 103.9 MB (103851243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca559a4d1d3cf5ca59d168e6032d9f6eb60609afefe51b8d4c582817823f711b`  
		Last Modified: Tue, 02 Aug 2022 15:52:05 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b563ebf532fc1a5282df03ef5138b18f01216151873445a92258c9638e56a2`  
		Last Modified: Tue, 02 Aug 2022 15:52:47 GMT  
		Size: 95.2 MB (95214507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dae2ccab1eb80eed07380bc35d064a2158a70931c354fef8471c6211d2d1172`  
		Last Modified: Tue, 02 Aug 2022 15:52:33 GMT  
		Size: 278.5 KB (278490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b858516da0fdda5810073563cd5fc6d2cb426f0c32a930e5b0791d373993a1c`  
		Last Modified: Tue, 02 Aug 2022 15:52:33 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a02b086f89c57f355fd6f8e3324803ad1643c2f655acb78f836780b0bb2fbd`  
		Last Modified: Tue, 02 Aug 2022 15:52:37 GMT  
		Size: 22.4 MB (22448437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:4d2821a6ddba963fe9c46854154679381d54b694c2a06b32724910edd81c8c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:6a56255e96f69d9639fbfe34d069881642b8f8144f2ebcb19e06bfe50f65bd4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1086548120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab7b9ff4375e8773af970379956d0b95378e513c2fc96fc6475af4ba555610e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:35:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:57 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:35:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:48:06 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 13:48:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:48:47 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:48:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:48:47 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:49:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:49:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:49:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:49:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:51:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5bfc5848603bd668295b5a975d71c189291f87f6598cf6dc5205c57efdc41f`  
		Last Modified: Tue, 02 Aug 2022 14:04:13 GMT  
		Size: 1.2 MB (1192245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c425ff1dadf43c340925189568bc8f392e60eec7d53b401bb72a710aa66135c`  
		Last Modified: Tue, 02 Aug 2022 14:04:11 GMT  
		Size: 3.8 MB (3827758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eae6de5e53443906b64a12ebc086b149ea851be37c5c514c6a4b7d1446ac6e`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b619038cdfe7b8c10e6820e8ebbfc5b3ab2e7bff0008f9498e10f48a3948ca`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98307263b57b763e56c78ed4978fa903e4c666a7325e21a7132d9c8b11af102`  
		Last Modified: Tue, 02 Aug 2022 14:07:41 GMT  
		Size: 106.1 MB (106129329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07757fc5de68a9df5480ba8f62ed87206a92fd8291df9bddf5af6845d93377`  
		Last Modified: Tue, 02 Aug 2022 14:07:23 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff0935d6a9511b200b27c5e9f331aee4eeaadbb48bc5ab7245a79bcdd3118d0`  
		Last Modified: Tue, 02 Aug 2022 14:08:04 GMT  
		Size: 97.8 MB (97848772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf60bc9e016c3e91c6eb945fbde5a87a0db5a195074bbb797f63d4a94984261`  
		Last Modified: Tue, 02 Aug 2022 14:07:51 GMT  
		Size: 278.5 KB (278534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc5652973b10726d1359e04fc71fb0b9fd788a5a58fa9b5b026eb18d51cce52`  
		Last Modified: Tue, 02 Aug 2022 14:07:51 GMT  
		Size: 2.2 KB (2249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca36f6a376ef84b96010be932950ac3aa2c71be3fe02aedef3635a449397bba`  
		Last Modified: Tue, 02 Aug 2022 14:07:54 GMT  
		Size: 23.0 MB (23032792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a83cd107ec53cb56f17b296744789bdfef9eb6adb6698aa871a444d6ab4871`  
		Last Modified: Tue, 02 Aug 2022 14:09:57 GMT  
		Size: 823.8 MB (823807891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:071f3c85c0ea3b4c8e0cd48cbbc904d375dfe2afbc171873b764fa7fb58dbcaa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1034200608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75310d9ea6a87a4b0b7c8b72b22175139ee533f9d4daa46b6aa355ae8eb0d782`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:32:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 15:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:12 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:33:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:33:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:33:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:33:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:34:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:36:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c096920dab8b763106ab108f7f67ffd78e3a0a5b90062661f6e79ba6e5531450`  
		Last Modified: Tue, 02 Aug 2022 15:52:21 GMT  
		Size: 103.9 MB (103851243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca559a4d1d3cf5ca59d168e6032d9f6eb60609afefe51b8d4c582817823f711b`  
		Last Modified: Tue, 02 Aug 2022 15:52:05 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b563ebf532fc1a5282df03ef5138b18f01216151873445a92258c9638e56a2`  
		Last Modified: Tue, 02 Aug 2022 15:52:47 GMT  
		Size: 95.2 MB (95214507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dae2ccab1eb80eed07380bc35d064a2158a70931c354fef8471c6211d2d1172`  
		Last Modified: Tue, 02 Aug 2022 15:52:33 GMT  
		Size: 278.5 KB (278490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b858516da0fdda5810073563cd5fc6d2cb426f0c32a930e5b0791d373993a1c`  
		Last Modified: Tue, 02 Aug 2022 15:52:33 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a02b086f89c57f355fd6f8e3324803ad1643c2f655acb78f836780b0bb2fbd`  
		Last Modified: Tue, 02 Aug 2022 15:52:37 GMT  
		Size: 22.4 MB (22448437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad0bc827b724b94ce49ee200b6dc031d69314c093ee84831ebbc91fe0c13ac5`  
		Last Modified: Tue, 02 Aug 2022 15:54:38 GMT  
		Size: 779.2 MB (779232733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception-jammy`

```console
$ docker pull ros@sha256:4d2821a6ddba963fe9c46854154679381d54b694c2a06b32724910edd81c8c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:6a56255e96f69d9639fbfe34d069881642b8f8144f2ebcb19e06bfe50f65bd4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1086548120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab7b9ff4375e8773af970379956d0b95378e513c2fc96fc6475af4ba555610e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:35:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:57 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:35:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:48:06 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 13:48:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:48:47 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:48:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:48:47 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:49:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:49:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:49:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:49:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:51:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5bfc5848603bd668295b5a975d71c189291f87f6598cf6dc5205c57efdc41f`  
		Last Modified: Tue, 02 Aug 2022 14:04:13 GMT  
		Size: 1.2 MB (1192245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c425ff1dadf43c340925189568bc8f392e60eec7d53b401bb72a710aa66135c`  
		Last Modified: Tue, 02 Aug 2022 14:04:11 GMT  
		Size: 3.8 MB (3827758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eae6de5e53443906b64a12ebc086b149ea851be37c5c514c6a4b7d1446ac6e`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b619038cdfe7b8c10e6820e8ebbfc5b3ab2e7bff0008f9498e10f48a3948ca`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98307263b57b763e56c78ed4978fa903e4c666a7325e21a7132d9c8b11af102`  
		Last Modified: Tue, 02 Aug 2022 14:07:41 GMT  
		Size: 106.1 MB (106129329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07757fc5de68a9df5480ba8f62ed87206a92fd8291df9bddf5af6845d93377`  
		Last Modified: Tue, 02 Aug 2022 14:07:23 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff0935d6a9511b200b27c5e9f331aee4eeaadbb48bc5ab7245a79bcdd3118d0`  
		Last Modified: Tue, 02 Aug 2022 14:08:04 GMT  
		Size: 97.8 MB (97848772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf60bc9e016c3e91c6eb945fbde5a87a0db5a195074bbb797f63d4a94984261`  
		Last Modified: Tue, 02 Aug 2022 14:07:51 GMT  
		Size: 278.5 KB (278534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc5652973b10726d1359e04fc71fb0b9fd788a5a58fa9b5b026eb18d51cce52`  
		Last Modified: Tue, 02 Aug 2022 14:07:51 GMT  
		Size: 2.2 KB (2249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca36f6a376ef84b96010be932950ac3aa2c71be3fe02aedef3635a449397bba`  
		Last Modified: Tue, 02 Aug 2022 14:07:54 GMT  
		Size: 23.0 MB (23032792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a83cd107ec53cb56f17b296744789bdfef9eb6adb6698aa871a444d6ab4871`  
		Last Modified: Tue, 02 Aug 2022 14:09:57 GMT  
		Size: 823.8 MB (823807891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:071f3c85c0ea3b4c8e0cd48cbbc904d375dfe2afbc171873b764fa7fb58dbcaa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1034200608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75310d9ea6a87a4b0b7c8b72b22175139ee533f9d4daa46b6aa355ae8eb0d782`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:32:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 15:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:12 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:33:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:33:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:33:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:33:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:34:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:36:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c096920dab8b763106ab108f7f67ffd78e3a0a5b90062661f6e79ba6e5531450`  
		Last Modified: Tue, 02 Aug 2022 15:52:21 GMT  
		Size: 103.9 MB (103851243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca559a4d1d3cf5ca59d168e6032d9f6eb60609afefe51b8d4c582817823f711b`  
		Last Modified: Tue, 02 Aug 2022 15:52:05 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b563ebf532fc1a5282df03ef5138b18f01216151873445a92258c9638e56a2`  
		Last Modified: Tue, 02 Aug 2022 15:52:47 GMT  
		Size: 95.2 MB (95214507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dae2ccab1eb80eed07380bc35d064a2158a70931c354fef8471c6211d2d1172`  
		Last Modified: Tue, 02 Aug 2022 15:52:33 GMT  
		Size: 278.5 KB (278490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b858516da0fdda5810073563cd5fc6d2cb426f0c32a930e5b0791d373993a1c`  
		Last Modified: Tue, 02 Aug 2022 15:52:33 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a02b086f89c57f355fd6f8e3324803ad1643c2f655acb78f836780b0bb2fbd`  
		Last Modified: Tue, 02 Aug 2022 15:52:37 GMT  
		Size: 22.4 MB (22448437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad0bc827b724b94ce49ee200b6dc031d69314c093ee84831ebbc91fe0c13ac5`  
		Last Modified: Tue, 02 Aug 2022 15:54:38 GMT  
		Size: 779.2 MB (779232733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:7985aeeda183ce1c7007d64744dfd5c116775d299928ecacd434d07fb406c987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:1e42f8cff90e1fe6f91c315155558ac618950e5e4731d2a72e5dfbfc65f48cd2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262740229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6246126d845d013b52c92c6b65936c428b8be255234df72ebcfcf1c1f03e543c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:35:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:57 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:35:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:48:06 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 13:48:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:48:47 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:48:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:48:47 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:49:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:49:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:49:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:49:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5bfc5848603bd668295b5a975d71c189291f87f6598cf6dc5205c57efdc41f`  
		Last Modified: Tue, 02 Aug 2022 14:04:13 GMT  
		Size: 1.2 MB (1192245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c425ff1dadf43c340925189568bc8f392e60eec7d53b401bb72a710aa66135c`  
		Last Modified: Tue, 02 Aug 2022 14:04:11 GMT  
		Size: 3.8 MB (3827758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eae6de5e53443906b64a12ebc086b149ea851be37c5c514c6a4b7d1446ac6e`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b619038cdfe7b8c10e6820e8ebbfc5b3ab2e7bff0008f9498e10f48a3948ca`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98307263b57b763e56c78ed4978fa903e4c666a7325e21a7132d9c8b11af102`  
		Last Modified: Tue, 02 Aug 2022 14:07:41 GMT  
		Size: 106.1 MB (106129329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07757fc5de68a9df5480ba8f62ed87206a92fd8291df9bddf5af6845d93377`  
		Last Modified: Tue, 02 Aug 2022 14:07:23 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff0935d6a9511b200b27c5e9f331aee4eeaadbb48bc5ab7245a79bcdd3118d0`  
		Last Modified: Tue, 02 Aug 2022 14:08:04 GMT  
		Size: 97.8 MB (97848772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf60bc9e016c3e91c6eb945fbde5a87a0db5a195074bbb797f63d4a94984261`  
		Last Modified: Tue, 02 Aug 2022 14:07:51 GMT  
		Size: 278.5 KB (278534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc5652973b10726d1359e04fc71fb0b9fd788a5a58fa9b5b026eb18d51cce52`  
		Last Modified: Tue, 02 Aug 2022 14:07:51 GMT  
		Size: 2.2 KB (2249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca36f6a376ef84b96010be932950ac3aa2c71be3fe02aedef3635a449397bba`  
		Last Modified: Tue, 02 Aug 2022 14:07:54 GMT  
		Size: 23.0 MB (23032792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:566852956ea3fc90533a5cc44c021d66b0693c4b85ae92313ee24a1ef567c481
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254967875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd12507a1529223aa1d1c513771d5b2cacd63d1157d0fe6ee02c9b4c1bb00a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:32:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 15:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:12 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:33:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:33:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:33:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:33:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:34:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c096920dab8b763106ab108f7f67ffd78e3a0a5b90062661f6e79ba6e5531450`  
		Last Modified: Tue, 02 Aug 2022 15:52:21 GMT  
		Size: 103.9 MB (103851243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca559a4d1d3cf5ca59d168e6032d9f6eb60609afefe51b8d4c582817823f711b`  
		Last Modified: Tue, 02 Aug 2022 15:52:05 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b563ebf532fc1a5282df03ef5138b18f01216151873445a92258c9638e56a2`  
		Last Modified: Tue, 02 Aug 2022 15:52:47 GMT  
		Size: 95.2 MB (95214507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dae2ccab1eb80eed07380bc35d064a2158a70931c354fef8471c6211d2d1172`  
		Last Modified: Tue, 02 Aug 2022 15:52:33 GMT  
		Size: 278.5 KB (278490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b858516da0fdda5810073563cd5fc6d2cb426f0c32a930e5b0791d373993a1c`  
		Last Modified: Tue, 02 Aug 2022 15:52:33 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a02b086f89c57f355fd6f8e3324803ad1643c2f655acb78f836780b0bb2fbd`  
		Last Modified: Tue, 02 Aug 2022 15:52:37 GMT  
		Size: 22.4 MB (22448437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base-jammy`

```console
$ docker pull ros@sha256:7985aeeda183ce1c7007d64744dfd5c116775d299928ecacd434d07fb406c987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:1e42f8cff90e1fe6f91c315155558ac618950e5e4731d2a72e5dfbfc65f48cd2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262740229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6246126d845d013b52c92c6b65936c428b8be255234df72ebcfcf1c1f03e543c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:35:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:57 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:35:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:48:06 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 13:48:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:48:47 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:48:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:48:47 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:49:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:49:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 13:49:20 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 13:49:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5bfc5848603bd668295b5a975d71c189291f87f6598cf6dc5205c57efdc41f`  
		Last Modified: Tue, 02 Aug 2022 14:04:13 GMT  
		Size: 1.2 MB (1192245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c425ff1dadf43c340925189568bc8f392e60eec7d53b401bb72a710aa66135c`  
		Last Modified: Tue, 02 Aug 2022 14:04:11 GMT  
		Size: 3.8 MB (3827758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eae6de5e53443906b64a12ebc086b149ea851be37c5c514c6a4b7d1446ac6e`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b619038cdfe7b8c10e6820e8ebbfc5b3ab2e7bff0008f9498e10f48a3948ca`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98307263b57b763e56c78ed4978fa903e4c666a7325e21a7132d9c8b11af102`  
		Last Modified: Tue, 02 Aug 2022 14:07:41 GMT  
		Size: 106.1 MB (106129329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07757fc5de68a9df5480ba8f62ed87206a92fd8291df9bddf5af6845d93377`  
		Last Modified: Tue, 02 Aug 2022 14:07:23 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff0935d6a9511b200b27c5e9f331aee4eeaadbb48bc5ab7245a79bcdd3118d0`  
		Last Modified: Tue, 02 Aug 2022 14:08:04 GMT  
		Size: 97.8 MB (97848772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf60bc9e016c3e91c6eb945fbde5a87a0db5a195074bbb797f63d4a94984261`  
		Last Modified: Tue, 02 Aug 2022 14:07:51 GMT  
		Size: 278.5 KB (278534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc5652973b10726d1359e04fc71fb0b9fd788a5a58fa9b5b026eb18d51cce52`  
		Last Modified: Tue, 02 Aug 2022 14:07:51 GMT  
		Size: 2.2 KB (2249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca36f6a376ef84b96010be932950ac3aa2c71be3fe02aedef3635a449397bba`  
		Last Modified: Tue, 02 Aug 2022 14:07:54 GMT  
		Size: 23.0 MB (23032792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:566852956ea3fc90533a5cc44c021d66b0693c4b85ae92313ee24a1ef567c481
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254967875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd12507a1529223aa1d1c513771d5b2cacd63d1157d0fe6ee02c9b4c1bb00a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:32:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 15:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:12 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:33:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:33:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:33:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:33:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:34:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c096920dab8b763106ab108f7f67ffd78e3a0a5b90062661f6e79ba6e5531450`  
		Last Modified: Tue, 02 Aug 2022 15:52:21 GMT  
		Size: 103.9 MB (103851243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca559a4d1d3cf5ca59d168e6032d9f6eb60609afefe51b8d4c582817823f711b`  
		Last Modified: Tue, 02 Aug 2022 15:52:05 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b563ebf532fc1a5282df03ef5138b18f01216151873445a92258c9638e56a2`  
		Last Modified: Tue, 02 Aug 2022 15:52:47 GMT  
		Size: 95.2 MB (95214507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dae2ccab1eb80eed07380bc35d064a2158a70931c354fef8471c6211d2d1172`  
		Last Modified: Tue, 02 Aug 2022 15:52:33 GMT  
		Size: 278.5 KB (278490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b858516da0fdda5810073563cd5fc6d2cb426f0c32a930e5b0791d373993a1c`  
		Last Modified: Tue, 02 Aug 2022 15:52:33 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a02b086f89c57f355fd6f8e3324803ad1643c2f655acb78f836780b0bb2fbd`  
		Last Modified: Tue, 02 Aug 2022 15:52:37 GMT  
		Size: 22.4 MB (22448437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:b1dad3eb86a8c1385608de5a791278966a45a3eca2e2f3ff408642d90372d0fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:7c7876c05cd92bb9baf28e1c425857cffc25ba54f1f5529640fd8b59ebfe3b64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141577882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36187e5fb92eaad918881daa5cb0b8fcaf4e1b23d3bec4afd3f9d1d5b020024`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:35:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:57 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:35:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:48:06 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 13:48:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:48:47 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:48:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:48:47 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5bfc5848603bd668295b5a975d71c189291f87f6598cf6dc5205c57efdc41f`  
		Last Modified: Tue, 02 Aug 2022 14:04:13 GMT  
		Size: 1.2 MB (1192245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c425ff1dadf43c340925189568bc8f392e60eec7d53b401bb72a710aa66135c`  
		Last Modified: Tue, 02 Aug 2022 14:04:11 GMT  
		Size: 3.8 MB (3827758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eae6de5e53443906b64a12ebc086b149ea851be37c5c514c6a4b7d1446ac6e`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b619038cdfe7b8c10e6820e8ebbfc5b3ab2e7bff0008f9498e10f48a3948ca`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98307263b57b763e56c78ed4978fa903e4c666a7325e21a7132d9c8b11af102`  
		Last Modified: Tue, 02 Aug 2022 14:07:41 GMT  
		Size: 106.1 MB (106129329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07757fc5de68a9df5480ba8f62ed87206a92fd8291df9bddf5af6845d93377`  
		Last Modified: Tue, 02 Aug 2022 14:07:23 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:32b569f822e027e13aaa6a7defc9e5bc87dbc8543f7a090bd99582d533b28dc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137024258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f0bcc8e53596876721fb6d7cd1a4600b4346e0fe4b57fc6166399d665e0144`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:32:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 15:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:12 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:33:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:33:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c096920dab8b763106ab108f7f67ffd78e3a0a5b90062661f6e79ba6e5531450`  
		Last Modified: Tue, 02 Aug 2022 15:52:21 GMT  
		Size: 103.9 MB (103851243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca559a4d1d3cf5ca59d168e6032d9f6eb60609afefe51b8d4c582817823f711b`  
		Last Modified: Tue, 02 Aug 2022 15:52:05 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core-jammy`

```console
$ docker pull ros@sha256:b1dad3eb86a8c1385608de5a791278966a45a3eca2e2f3ff408642d90372d0fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:7c7876c05cd92bb9baf28e1c425857cffc25ba54f1f5529640fd8b59ebfe3b64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141577882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36187e5fb92eaad918881daa5cb0b8fcaf4e1b23d3bec4afd3f9d1d5b020024`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:35:41 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:35:57 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 13:35:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 13:35:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 13:48:06 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 13:48:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 13:48:47 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 13:48:47 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 13:48:47 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5bfc5848603bd668295b5a975d71c189291f87f6598cf6dc5205c57efdc41f`  
		Last Modified: Tue, 02 Aug 2022 14:04:13 GMT  
		Size: 1.2 MB (1192245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c425ff1dadf43c340925189568bc8f392e60eec7d53b401bb72a710aa66135c`  
		Last Modified: Tue, 02 Aug 2022 14:04:11 GMT  
		Size: 3.8 MB (3827758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43eae6de5e53443906b64a12ebc086b149ea851be37c5c514c6a4b7d1446ac6e`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b619038cdfe7b8c10e6820e8ebbfc5b3ab2e7bff0008f9498e10f48a3948ca`  
		Last Modified: Tue, 02 Aug 2022 14:04:10 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98307263b57b763e56c78ed4978fa903e4c666a7325e21a7132d9c8b11af102`  
		Last Modified: Tue, 02 Aug 2022 14:07:41 GMT  
		Size: 106.1 MB (106129329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07757fc5de68a9df5480ba8f62ed87206a92fd8291df9bddf5af6845d93377`  
		Last Modified: Tue, 02 Aug 2022 14:07:23 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:32b569f822e027e13aaa6a7defc9e5bc87dbc8543f7a090bd99582d533b28dc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137024258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f0bcc8e53596876721fb6d7cd1a4600b4346e0fe4b57fc6166399d665e0144`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:32:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 15:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:12 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:33:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:33:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c096920dab8b763106ab108f7f67ffd78e3a0a5b90062661f6e79ba6e5531450`  
		Last Modified: Tue, 02 Aug 2022 15:52:21 GMT  
		Size: 103.9 MB (103851243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca559a4d1d3cf5ca59d168e6032d9f6eb60609afefe51b8d4c582817823f711b`  
		Last Modified: Tue, 02 Aug 2022 15:52:05 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
